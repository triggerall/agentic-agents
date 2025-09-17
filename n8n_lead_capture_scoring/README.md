## 🛠 How It Works
1. Typeform Trigger – Captures new lead data whenever someone submits your form.
2. Deduplication Check – Searches HubSpot CRM by email to avoid duplicates.
3. Conditional Flow
	a. If no match → Creates a new contact in HubSpot.
	b. If match found → Updates the existing contact with fresh data.
4. Lead Scoring (Function Node) – Runs JavaScript to assign a score based on defined rules (e.g. company email, visits, enrichment).
5. Lead Tier Assignment – Categorizes the lead as ❄️ Cold, 🌡 Warm, or 🔥 Hot.
6. Slack Notification – Sends a formatted message with lead details and tier to your sales channel.

## 🎯 Who Is This For?
- Sales teams that want real-time lead alerts.
- Marketing teams capturing inbound leads via Typeform.
- Companies using HubSpot CRM but want custom lead scoring and tiered notifications.

## 🔧 What Problem This Solves
- Avoids duplicate contacts in CRM.
- Automates lead creation & enrichment.
- Adds custom scoring logic not available in HubSpot out of the box.
- Notifies sales in Slack with lead priority instantly.

## 📊 What This Workflow Does
- Captures lead data from Typeform.
- Cleans & deduplicates before pushing to HubSpot.
- Scores the lead based on your own rules (editable).
- Categorizes into tiers (Cold, Warm, Hot) for quick prioritization.
- Alerts your sales team on Slack with all relevant details.

## ⚙️ Setup Process

### - Typeform Node (Trigger)
Connect your Typeform account.
Select the form you want to track submissions from.
### - HubSpot Node (Search Contact)
Search HubSpot by email.
Route outcome: Not found → Create Contact, Found → Update Contact.
### - HubSpot Node (Create/Update Contact)
Map fields from Typeform to HubSpot (first name, last name, email, phone, company, etc.).
### - Function Node (Lead Scoring)
Paste the scoring code (rules-based, assigns leadScore and leadTier).
### - Slack Node (Send Message)
Format the message to show:
🚀 *New Lead Alert!*  
👤 {{$json["firstname"]}} {{$json["lastname"]}}  
📧 {{$json["email"]}}  
🏢 {{$json["company"]}}  
📊 *Score:* {{$json["leadScore"]}} — {{$json["leadTier"]}}

Send to your desired Slack channel.