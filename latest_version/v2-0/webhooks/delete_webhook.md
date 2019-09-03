# Delete Webhook

~~~
DELETE https://api.smartpay.curexe.com/2-0/webhooks/{{WEBHOOK_ID}}
~~~
* replace {{WEBHOOK_ID}} with the actual webhook_id

## Description

Deletes a webhook.

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
    <td colspan="4">- none -</td>
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
    <td>status</td>
    <td>success</td>
    <td></td>
  </tr>
</table>

## See Also:

- List Webhooks
  * [GET /webhooks](get_webhooks.md)
- Create Webhook
  * [POST /webhooks](create_webhook.md)
- Modify Webhook
  * [PATCH /webhooks/ID](modify_webhook.md)
- Test Webhook
  * [PUT /webhooks/ID/actions/test](test_webhook.md)

[For additional information please see our webhooks implementation document.](implementation.md)