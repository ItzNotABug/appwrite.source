const sdk = require('node-appwrite');

const client = new sdk.Client()
    .setEndpoint('https://cloud.appwrite.io/v1') // Your API Endpoint
    .setProject('&lt;YOUR_PROJECT_ID&gt;') // Your project ID
    .setKey('&lt;YOUR_API_KEY&gt;'); // Your secret API key

const messaging = new sdk.Messaging(client);

const result = await messaging.createSms(
    '<MESSAGE_ID>', // messageId
    '<CONTENT>', // content
    [], // topics (optional)
    [], // users (optional)
    [], // targets (optional)
    false, // draft (optional)
    '' // scheduledAt (optional)
);