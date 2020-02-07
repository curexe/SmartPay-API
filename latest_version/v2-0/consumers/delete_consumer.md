# Delete Consumer

~~~
DELETE https://api.smartpay.curexe.com/2-0/consumers/{{CONSUMER_ID}}
~~~
* replace {{CONSUMER_ID}} with the actual consumer_id

## Description

Deletes a consumer.  Will be rejected if the consumer has any invoices.

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
