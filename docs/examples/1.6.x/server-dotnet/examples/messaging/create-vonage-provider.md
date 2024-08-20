using Appwrite;
using Appwrite.Models;
using Appwrite.Services;

Client client = new Client()
    .SetEndPoint("https://cloud.appwrite.io/v1") // Your API Endpoint
    .SetProject("&lt;YOUR_PROJECT_ID&gt;") // Your project ID
    .SetKey("&lt;YOUR_API_KEY&gt;"); // Your secret API key

Messaging messaging = new Messaging(client);

Provider result = await messaging.CreateVonageProvider(
    providerId: "<PROVIDER_ID>",
    name: "<NAME>",
    from: "+12065550100", // optional
    apiKey: "<API_KEY>", // optional
    apiSecret: "<API_SECRET>", // optional
    enabled: false // optional
);