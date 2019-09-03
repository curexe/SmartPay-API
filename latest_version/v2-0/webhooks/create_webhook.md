# Create Webhook

~~~
POST https://api.smartpay.curexe.com/2-0/webhooks
~~~

## Description

Creates a new webhook.  If any mandatory parameters are omitted it will be rejected.

Note: If a webhook url is unreachable 10 times the webhook will be disabled.

[For additional information please see our webhooks implementation document.](implementation.md)

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
