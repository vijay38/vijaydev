---
title: Meta WhatsApp Business Setup
tags:
  - meta
  - whatsapp
  - api
  - tutorial
---

# Meta WhatsApp Business API Setup

Learn how to set up WhatsApp messaging for church services.

## 📋 Prerequisites
- Meta Business Account
- WhatsApp Business Account
- Developer Portal Access

## 🚀 Step-by-Step Setup

### 1. Create Meta Developer Account
1. Go to [developers.facebook.com](https://developers.facebook.com)
2. Click "My Apps" → "Create App"
3. Select "Other" → "Business"
4. Fill in app details

### 2. Setup WhatsApp Product
1. In your app dashboard
2. Add "WhatsApp" product
3. Get Phone Number ID
4. Get WhatsApp Business Account ID

### 3. Get Access Token
1. Settings → WhatsApp → Configuration
2. Generate temporary access token
3. Note the token expiry time

### 4. Setup Webhook
1. Configure webhook URL
2. Verify webhook secret
3. Subscribe to events:
   - messages
   - message_sent
   - message_delivered

## 📱 Sending Messages

### Using cURL
```bash
curl -X POST 'https://graph.facebook.com/v21.0/PHONE_NUMBER_ID/messages' \
  -H 'Authorization: Bearer ACCESS_TOKEN' \
  -H 'Content-Type: application/json' \
  -d '{
    "messaging_product": "whatsapp",
    "to": "RECIPIENT_PHONE",
    "type": "text",
    "text": {"body": "Hello!"}
  }'
```

### Using Node.js
```javascript
const axios = require('axios');

async function sendMessage(phoneNumberId, to, message) {
  await axios.post(
    `https://graph.facebook.com/v21.0/${phoneNumberId}/messages`,
    {
      messaging_product: "whatsapp",
      to: to,
      type: "text",
      text: { body: message }
    },
    {
      headers: {
        Authorization: `Bearer ${accessToken}`,
        "Content-Type": "application/json"
      }
    }
  );
}
```

## 📝 Message Templates

Templates must be approved by Meta:
- Use meaningful variables: {{1}}, {{2}}
- Keep under character limits
- Include opt-out option for marketing

## 🔐 Security Best Practices
1. Store tokens in environment variables
2. Use webhooks for verification
3. Validate incoming messages
4. Rate limiting

## 🐛 Common Issues

| Error | Solution |
|-------|----------|
| Token expired | Regenerate in dashboard |
| Phone not verified | Complete business verification |
| Rate limit | Implement backoff |

## 📚 Resources
- [Meta WhatsApp Docs](https://developers.facebook.com/docs/whatsapp)
- [API Reference](https://developers.facebook.com/docs/whatsapp-api/reference)

---
*Built WhatsApp service for Emmanuel Ministries!*