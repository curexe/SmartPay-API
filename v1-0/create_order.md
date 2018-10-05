# Create Order

~~~
https://api.smartpay.curexe.com/1-0/create_order
~~~

## Description

The /create_order endpoint allows retailers to create a new order in SmartPay. Note that you can only create an order for an existing consumer, so you may need to use the /create_consumer endpoint beforehand.

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
    <td>consumer_id</td>
    <td>aBc123</td>
    <td>Mandatory</td>
  </tr>
  <tr>
    <td>single_amount</td>
    <td>150.00</td>
    <td></td>
  </tr>
  <tr>
    <td>currency</td>
    <td>CAD</td>
    <td>Defaults to CAD</td>
  </tr>
  <tr>
    <td>recurring_amount</td>
    <td>10.00</td>
    <td></td>
  </tr>
  <tr>
    <td>recurring_frequency</td>
    <td>m</td>
    <td>At this time, only "m" (monthly) is available</td>
  </tr>
  <tr>
    <td>recurring_start</td>
    <td>2018-01-01</td>
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
</table>
