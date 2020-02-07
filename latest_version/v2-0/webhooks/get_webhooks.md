
# List Webhooks

~~~
GET https://api.smartpay.curexe.com/2-0/webhooks
~~~

## Description

Retreives a list of webhooks.  Parameters can be used to filter the list.

Will return up to 100 results at a time.  Use <b>page</b> to retreive the next results in the set.

[For additional information see: Webhooks Implementation.](README.md)

## Headers

<table>
  <tr>
    <td><b>Header</b></td>
    <td><b>Mandatory</b></td>
    <td><b>Notes</b></td>
  </tr>
  <tr>
    <td>Authorization: Bearer ACCESS_TOKEN</td>
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

## Query Params (URL Encoded)

<table>
  <tr>
    <td><b>Parameter</b></td>
    <td><b>Example</b></td>
    <td><b>Mandatory</b></td>
    <td><b>Notes</b></td>
  </tr>
  <tr>
    <td>page</td>
    <td>1</td>
    <td>No</td>
    <td>Defaults to 1 if not specified</td>
  </tr>
  <tr>
    <td>webhook_id</td>
    <td>aBc123</td>
    <td>No</td>
    <td></td>
  </tr>
  <tr>
    <td>topic</td>
    <td>invoice/created</td>
    <td>No</td>
    <td></td>
  </tr>
  <tr>
    <td>url</td>
    <td>https://site.com/webhooks</td>
    <td>No</td>
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
  <tr>
    <td>topic</td>
    <td>invoice/created</td>
    <td></td>
  </tr>
  <tr>
    <td>url</td>
    <td>https://site.com/webhooks</td>
    <td></td>
  </tr>
</table>

## See Also:

- Create Webhook
  * [POST /webhooks](create_webhook.md)
- Modify Webhook
  * [PATCH /webhooks/ID](modify_webhook.md)
- Delete Webhook
  * [DELETE /webhooks/ID](delete_webhook.md)
- Test Webhook
  * [PUT /webhooks/ID/actions/test](test_webhook.md)

[For additional information see: Webhooks Implementation.](README.md)