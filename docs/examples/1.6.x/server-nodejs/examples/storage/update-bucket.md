const sdk = require('node-appwrite');

const client = new sdk.Client()
    .setEndpoint('https://cloud.appwrite.io/v1') // Your API Endpoint
    .setProject('&lt;YOUR_PROJECT_ID&gt;') // Your project ID
    .setKey('&lt;YOUR_API_KEY&gt;'); // Your secret API key

const storage = new sdk.Storage(client);

const result = await storage.updateBucket(
    '<BUCKET_ID>', // bucketId
    '<NAME>', // name
    ["read("any")"], // permissions (optional)
    false, // fileSecurity (optional)
    false, // enabled (optional)
    1, // maximumFileSize (optional)
    [], // allowedFileExtensions (optional)
    sdk..None, // compression (optional)
    false, // encryption (optional)
    false // antivirus (optional)
);