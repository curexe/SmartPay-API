# Modify Webhook

~~~
PATCH https://api.smartpay.curexe.com/2-0/webhooks/{{WEBHOOK_ID}}
~~~

## Description

Modifies a webhook.  This is a patch action and will only change the values submitted.

## Input Parameters

<table>
  <tr>
    <td><b>Parameter</b></td>
    <td><b>Example</b></td>
    <td><b>Mandatory</b></td>
    <td><b>Notes</b></td>
  </tr>
  <tr>
    <td>webhook_id</td>
    <td>aBc123</td>
    <td>Yes</td>
    <td></td>
  </tr>
  <tr>
    <td>url</td>
    <td>https://site.com/webhooks</td>
    <td>Yes</td>
    <td></td>
  </tr>
</table>

## Results

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
