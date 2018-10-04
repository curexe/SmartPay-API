# Modify Order

~~~
[POST] https://smartpay.curexe.com/api/1.0/modify_order
~~~

## Description

The /modify_order endpoint allows retailers to modify an existing order in SmartPay. Modifying an order will impact all future invoices, but not prior invoices.

> ***Warning**: This is a write query. Any data sent through this endpoint will be written to the SmartPay database in real-time. There is no undo. Please use with caution.*

## Input Parameters

<table>
  <tr>
    <td><b>Parameter</b></td>
    <td><b>Example</b></td>
    <td><b><b>Notes</b></b></td>
  </tr>
  <tr>
    <td>token</td>
    <td>ABC123</td>
    <td>Mandatory</td>
  </tr>
  <tr>
    <td>format</td>
    <td>json</td>
    <td>At this time only JSON format is available</td>
  </tr>
  <tr>
    <td>order_id</td>
    <td>aBc123</td>
    <td></td>
  </tr>
  <tr>
    <td>recurring_amount</td>
    <td>10.00</td>
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
    <td>order_id</td>
    <td>aBc123</td>
    <td></td>
  </tr>
  <tr>
    <td>success</td>
    <td>true</td>
    <td>"true" if update successful, "false" otherwise</td>
  </tr>
</table>
