# Get Webhooks

~~~
POST https://api.smartpay.curexe.com/1-2/get_webhooks
~~~

## Description

Retreives a list of webhooks.  Parameters can be used to filter the list.

Will return up to 100 results at a time.  Use <b>page</b> to retreive the next results in the set.

### The following topics are available to be subscribed to:
> invoice/created<br />
> invoice/paid<br />
> invoice/cancelled<br />
> order/created<br />
> order/cancelled

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
    <td>https://site.com/webhooks</td>
    <td>No</td>
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
  <tr>
    <td>topic</td>
    <td>invoice/created</td>
    <td></td>
  </tr>
  <tr>
    <td>url</td>
    <td>https://site.com/webhooks</td>
    <td></td>
  </tr>
</table>
