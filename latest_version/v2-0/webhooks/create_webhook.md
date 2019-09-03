# Create Webhook

~~~
POST https://api.smartpay.curexe.com/2-0/webhooks
~~~

## Description

Creates a new webhook.  If any mandatory parameters are omitted it will be rejected.

- You may subscribe to each available topic one time each. You cannot subscribe to a topic twice for separate URLs.
- When a webhook is created (or modified) a notification of the topic webhook/created will be sent to the webhook URL as a test.
- The API will reject a webhook for a URL that cannot be reached or does not respond with 200 OK in response to the test.

*When processing notifications, if a webhook notification is undeliverable 20 times the webhook will be disabled (and all associated queued webhook notifications for that webhook URL).*

[For additional information on webhooks see our implementation document.](implementation.md)

## Headers

<table>
  <tr>
    <td><b>Header</b></td>
    <td><b>Mandatory</b></td>
    <td><b>Notes</b></td>
  </tr>
  <tr>
    <td>Authentication: Bearer ACCESS_TOKEN</td>
    <td>yes</td>
    <td>the bearer token issued by <a href="..\authenticate\authenticate.md">authenticate</a></td>
  </tr>
</table>

### The following topics are available to be subscribed to:
> invoice/created<br />
> invoice/paid<br />
> invoice/cancelled<br />
> order/created<br />
> order/cancelled

## Body Params (JSON application/json or x-www-form-urlencoded)

<table>
  <tr>
    <td><b>Parameter</b></td>
    <td><b>Example</b></td>
    <td><b>Mandatory</b></td>
    <td><b>Notes</b></td>
  </tr>
  <tr>
    <td>topic</td>
    <td>invoice/created</td>
    <td>Yes</td>
    <td>Must be a valid topic</td>
  </tr>
  <tr>
    <td>url</td>
    <td>https://site.com/webhooks</td>
    <td>Yes</td>
    <td>Must be a valid URL, must respond <b>200 OK</b> to requests</td>
  </tr>
</table>

## Result

<table>
  <tr>
    <td><b>Field</b></td>
    <td><b>Value</b></td>
    <td><b>Notes</b></td>
  </tr>
  <tr>
    <td>webhook_id</td>
    <td>aBc123</td>
    <td></td>
  </tr>
</table>

## See Also:

[For additional information please see our webhooks implementation document.](implementation.md)

- List Webhooks
  * [GET /webhooks](get_webhooks.md)
- Modify Webhook
  * [PATCH /webhooks/ID](modify_webhook.md)
- Delete Webhook
  * [DELETE /webhooks/ID](delete_webhook.md)
- Test Webhook
  * [PUT /webhooks/ID/actions/test](test_webhook.md)