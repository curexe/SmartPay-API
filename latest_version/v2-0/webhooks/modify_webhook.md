# Modify Webhook

~~~
PATCH https://api.smartpay.curexe.com/2-0/webhooks/{{WEBHOOK_ID}}
~~~
* replace {{WEBHOOK_ID}} with the actual webhook_id

## Description

Modifies a webhook.  This is a patch action and will only change the values submitted.

- When a webhook is modified a notification of the topic webhook/created will be sent to the webhook URL as a test.
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

## Body Params (JSON application/json or x-www-form-urlencoded)

<table>
  <tr>
    <td><b>Parameter</b></td>
    <td><b>Example</b></td>
    <td><b>Mandatory</b></td>
    <td><b>Notes</b></td>
  </tr>
  <tr>
    <td>url</td>
    <td>https://site.com/webhooks</td>
    <td>Yes</td>
    <td></td>
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

- List Webhooks
  * [GET /webhooks](get_webhooks.md)
- Create Webhook
  * [POST /webhooks](create_webhook.md)
- Delete Webhook
  * [DELETE /webhooks/ID](delete_webhook.md)
- Test Webhook
  * [PUT /webhooks/ID/actions/test](test_webhook.md)

[For additional information please see our webhooks implementation document.](implementation.md)