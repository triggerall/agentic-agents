## How it works
This workflow listens for new Shopify orders, formats the order details, and then:
1. Sends the customer an order confirmation email via Gmail
2. Notifies your team in Slack with the same order details

This is a cost-saving alternative to WhatsApp Business notifications. It leverages tools SMBs already use (Gmail + Slack) and avoids per-message fees.

## Who is this for?

- SMBs in India (and globally) looking for low-cost ways to notify customers.
- Shopify merchants who want both customer emails and internal Slack alerts.
- Ops/Sales teams that want real-time visibility on orders without logging into Shopify.

## What problem this solves

- Shopify default email templates are limited.
- WhatsApp Business API is costly and not SMB-friendly.
- Staff often need instant alerts for high-value orders.

## 👉 With this template you get:

- Automated customer email with formatted order details.
- Slack alerts for your sales/support team.
- Zero WhatsApp costs.

##Setup Process:
### - Shopify Setup
	- Connect Shopify credentials in n8n.
	- Add the Shopify Trigger node → select “Order Created”.
### - Gmail Setup
	- Connect Gmail OAuth2 credentials in n8n.
	- In the Gmail node, set Send Email → To = {{$json["email"]}}.
### - Slack Setup
	- Connect Slack credentials.
	- Choose target channel (e.g., #sales-alerts).
