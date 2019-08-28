# Create Webhook

~~~
POST https://api.smartpay.curexe.com/1-2/create_webhook
~~~

## Description

Creates a new webhook.  If any mandatory parameters are omitted it will be rejected.

### The following topics are available to be subscribed to:
> invoice/created<br />
> invoice/paid<br />
> invoice/cancelled<br />
> order/created<br />
> order/cancelled

## Parameters

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
