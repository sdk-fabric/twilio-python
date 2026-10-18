
# twilio-python

This [SDK](https://github.com/sdk-fabric/twilio-python) is managed by the [SDK Fabric](https://sdk-fabric.org/) project, a global infrastructure to
automatically generate SDKs for every API.

You can find more information about this SDK at [TypeHub](https://typehub.cloud/):
https://app.typehub.cloud/d/sdkfabric/twilio

## Usage

```python
from sdk.client import Client

client = Client.build("[access_token]")

# Delete the Media resource.
response = client.media().delete("account_sid", "message_sid", "sid")

# Fetch a single Media resource associated with a specific Message resource.
response = client.media().get("account_sid", "message_sid", "sid")

# Read a list of Media resources associated with a specific Message resource.
response = client.media().getAll("date_created", 1, 1, "page_token", "account_sid", "message_sid")

# Send a message (SMS, MMS, WhatsApp or other channel).
response = client.messages().create("account_sid", Any())

# Deletes a Message resource from your account.
response = client.messages().delete("account_sid", "sid")

# Fetch a specific Message.
response = client.messages().get("account_sid", "sid")

# Retrieve a list of Message resources associated with a Twilio Account.
response = client.messages().getAll("date_sent", "from", 1, 1, "page_token", "to", "account_sid")

# Update a Message resource (used to redact Message `body` text and to cancel not-yet-sent messages).
response = client.messages().update("account_sid", "sid", Any())
```
