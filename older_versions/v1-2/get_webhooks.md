# Get Orders

~~~
https://api.smartpay.curexe.com/1-2/get_orders
~~~

## Description

Retreives a list of the current webhooks.

## Input Parameters

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
    <td>https://www.my-site.com/webhooks</td>
    <td>No</td>
    <td></td>
  </tr>
</table>

## Results

<table>
  <tr>
    <td><b>Field</b></td>
    <td><b>Value</b></td>
    <td><b><b>Notes</b></b></td>
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
    <td>https://www.my-site.com/webhooks</td>
    <td></td>
  </tr>
</table>
