# Webhooks Implementation

## How they work:

1.	When any action occurs that is related to a webhook topic, if that topic is subscribed to then a notification will be added to the webhook notification queue for processing.
2.	The webhook will be sent as JSON POST data to the URL.  The receiving server must respond **200 OK** in response to webhook or it is assumed the server has an error or is unresponsive. 
3.	If a webhook notification is undeliverable **20 times** the webhook will be disabled (and all associated queued webhook notifications for that webhook URL).

## Subscribing:

1.	Webhooks can be created, updated, and deleted through the API.  They cannot be managed within the dashboard at this time.
2.	Each retailer may subscribe to each available topic one time each.  *You cannot subscribe to a topic twice for separate URLs.*
3.	When a webhook is created (or modified) a notification of the topic *webhook/created* will be sent to the webhook URL as a test.
4.	The API will reject a webhook for a URL that cannot be reached or does not respond with *200 OK* in response to the test.

## Topics:

The following topics are available to be subscribed to:

- invoice/created
- invoice/paid
- invoice/cancelled
- order/created
- order/cancelled

## Receiving Webhooks

Webhooks are submitted to the URL with HTTP headers and a JSON payload.

The following HTTP headers are provided:

- X-SmartPay-Topic
- X-SmartPay-Hmac-Sha256

**X-SmartPay-Topic**

Contains the topic of the webhooks. 

*Example: invoice/paid*

**X-SmartPay-Hmac-Sha256**

Each webhook request includes a base64-encoded X-SmartPay-Hmac-SHA256 header, which is generated using the api key along with the data sent in the request.  This header can be used to verify this is an authentic webhook from SmartPay.

*Example: +XWmrwMey6OsLMeiZKwP4FppHH3cmAiiJJAweH5Jo4bM=*

### Validation Example (PHP)

> $data = file_get_contents('php://input');
>
> $hmac = base64_encode(hash_hmac('sha256', $data, API_KEY, true));
>
> if ($hmac  ==  getallheaders()[‘X-SmartPay-Hmac-Sha256’]) {
>
> 	echo ‘is valid!’;
>
> }