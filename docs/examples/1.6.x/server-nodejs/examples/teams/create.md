const sdk = require('node-appwrite');

const client = new sdk.Client()
    .setEndpoint('https://cloud.appwrite.io/v1') // Your API Endpoint
    .setProject('&lt;YOUR_PROJECT_ID&gt;') // Your project ID
    .setSession(''); // The user session to authenticate with

const teams = new sdk.Teams(client);

const result = await teams.create(
    '<TEAM_ID>', // teamId
    '<NAME>', // name
    [] // roles (optional)
);