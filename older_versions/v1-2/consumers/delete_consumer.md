# Delete Consumer

~~~
POST https://api.smartpay.curexe.com/1-2/delete_consumer
~~~

## Description

Deletes a consumer.  Will be rejected if the consumer has any invoices.

## Parameters

<table>
  <tr>
    <td><b>Parameter</b></td>
    <td><b>Example</b></td>
    <td><b>Mandatory</b></td>
    <td><b>Notes</b></td>
  </tr>
  <tr>
    <td>consumer_id</td>
    <td>aBc123</td>
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
    <td>status</td>
    <td>success</td>
    <td></td>
  </tr>
</table>
