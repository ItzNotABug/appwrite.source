POST /v1/account/tokens/email HTTP/1.1
Host: cloud.appwrite.io
Content-Type: application/json
X-Appwrite-Response-Format: 1.5.0
X-Appwrite-Project: &lt;YOUR_PROJECT_ID&gt;

{
  "userId": "<USER_ID>",
  "email": "email@example.com",
  "phrase": false
}