import { Client, Users, AuthenticatorType } from "https://deno.land/x/appwrite/mod.ts";

const client = new Client()
    .setEndpoint('https://cloud.appwrite.io/v1') // Your API Endpoint
    .setProject('&lt;YOUR_PROJECT_ID&gt;') // Your project ID
    .setKey('&lt;YOUR_API_KEY&gt;'); // Your secret API key

const users = new Users(client);

const response = await users.deleteMfaAuthenticator(
    '<USER_ID>', // userId
    AuthenticatorType.Totp // type
);