const sdk = require('node-appwrite');

const client = new sdk.Client()
    .setEndpoint('https://cloud.appwrite.io/v1') // Your API Endpoint
    .setProject('&lt;YOUR_PROJECT_ID&gt;') // Your project ID
    .setKey('&lt;YOUR_API_KEY&gt;'); // Your secret API key

const messaging = new sdk.Messaging(client);

const result = await messaging.updatePush(
    '<MESSAGE_ID>', // messageId
    [], // topics (optional)
    [], // users (optional)
    [], // targets (optional)
    '<TITLE>', // title (optional)
    '<BODY>', // body (optional)
    {}, // data (optional)
    '<ACTION>', // action (optional)
    '[ID1:ID2]', // image (optional)
    '<ICON>', // icon (optional)
    '<SOUND>', // sound (optional)
    '<COLOR>', // color (optional)
    '<TAG>', // tag (optional)
    null, // badge (optional)
    false, // draft (optional)
    '' // scheduledAt (optional)
);