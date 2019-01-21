# Cancel Order

~~~
https://api.smartpay.curexe.com/1-2/cancel_order
~~~

## Description

The /cancel_order endpoint allows retailers to terminate a currently active order. When an order is cancelled, no further invoices will be created, although existing invoices will not be impacted by cancellation.

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
    <td>order_id</td>
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
