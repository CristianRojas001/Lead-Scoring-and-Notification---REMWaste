# Lead-Scoring-and-Notification---REMWaste
A production-grade n8n workflow to validate, score, store, and notify on incoming sales leads.

Data Ingestion

Receive real submissions via /lead-submit or auto-generate test leads on a Cron schedule.

Processing

Validate required fields (full_name, email, budget, interest_level) with clear error messaging.

Apply a 0–100 point scoring model (budget, interest, company size, email domain, phone bonus).

Categorize leads as Cold, Warm, or Hot based on thresholds.

Persistence

Archive every raw payload to Airtable for audit and recovery.

Upsert scored leads into Airtable “Leads” table (avoids duplicates, typecasts data).

Notifications

Instantly DM reps when a Hot lead arrives, including a deep-link to its record.

Send a timed follow-up (2 minutes later) to reinforce outreach.

Error Handling & Resilience

Route validation/runtime errors into an Airtable “ErrorLogging” table.

Push formatted error alerts to Slack so ops can intervene quickly.

Business Impact

Automates lead triage to surface high-value prospects within seconds.

Ensures 100% capture and follow-up, reducing manual drop-offs and boosting conversion rates.
