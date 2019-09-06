# API 2.0 Overview

# Endpoints

## Authentication

- Authenticate (get bearer token)
	* [GET /authenticate](authenticate/authenticate.md)

## Consumers

- List Consumers 
	* [GET /consumers](consumers/get_consumers.md)
- Create Consumer 
	* [POST /consumers](consumers/create_consumer.md)
- Modify Consumer 
	* [PATCH /consumers/ID](consumers/modify_consumer.md)
- Delete Consumer 
	* [DELETE /consumers/ID](consumers/delete_consumer.md)

## Orders

Orders are a grouping of invoices.  Each orders has at least 1 invoice initially (a single amount to be collected from the consumer).  Future implementations of recurring billing will include multiple invoices per order.

- List Orders
	* [GET /orders](orders/get_orders.md)

## Invoices

Invoices represent the amount to be collected from the consumer, when it was received, and if there was any problems with processing the payment.

- List Invoices
	* [GET /invoices](invoices/get_invoices.md)

## Webhooks

Webhooks allow you to subscribe to have status updates sent to a url when certain actions occur within SmartPay.

[For additional information please see our webhooks implementation document.](webhooks/README.md)

- List Webhooks
	* [GET /webhooks](webhooks/get_webhooks.md)
- Create Webhook
	* [POST /webhooks](webhooks/create_webhook.md)
- Modify Webhook
	* [PATCH /webhooks/ID](webhooks/modify_webhook.md)
- Delete Webhook
	* [DELETE /webhooks/ID](webhooks/delete_webhook.md)
- Test Webhook
	* [PUT /webhooks/ID/actions/test](webhooks/test_webhook.md)