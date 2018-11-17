# Cancel Invoice

~~~
https://api.smartpay.curexe.com/1-0/cancel_invoice
~~~

## Description

The /cancel_invoice endpoint allows retailers to cancel any invoice in the system. If the invoice has not yet been paid, no payment will be solicited from the consumer. If the invoice has been paid, SmartPay will attempt to initiate a refund.

> ***Warning**: This is a write query. Any data sent through this endpoint will be written to the SmartPay database in real-time. There is no undo. Please use with caution.*

## Input Parameters

<table>
  <tr>
    <td><b>Parameter</b></td>
    <td><b>Example</b></td>
    <td><b>Mandatory</b></td>
    <td><b>Notes</b></td>
  </tr>
  <tr>
    <td>token</td>
    <td>ABC123</td>
    <td>Yes</td>
    <td></td>
  </tr>
  <tr>
    <td>format</td>
    <td>json</td>
    <td>No</td>
    <td>At this time only JSON format is available</td>
  </tr>
  <tr>
    <td>invoice_id</td>
    <td>aBc123</td>
    <td>Yes</td>
    <td></td>
  </tr>
</table>

## Resultset

<table>
  <tr>
    <td><b>Field</b></td>
    <td><b>Value</b></td>
    <td><b><b>Notes</b></b></td>
  </tr>
  <tr>
    <td>status</td>
    <td>success</td>
    <td>"success" or "failure"</td>
  </tr>
</table>
