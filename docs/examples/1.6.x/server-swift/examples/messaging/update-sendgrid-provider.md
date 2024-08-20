import Appwrite

let client = Client()
    .setEndpoint("https://cloud.appwrite.io/v1") // Your API Endpoint
    .setProject("&lt;YOUR_PROJECT_ID&gt;") // Your project ID
    .setKey("&lt;YOUR_API_KEY&gt;") // Your secret API key

let messaging = Messaging(client)

let provider = try await messaging.updateSendgridProvider(
    providerId: "<PROVIDER_ID>",
    name: "<NAME>", // optional
    enabled: false, // optional
    apiKey: "<API_KEY>", // optional
    fromName: "<FROM_NAME>", // optional
    fromEmail: "email@example.com", // optional
    replyToName: "<REPLY_TO_NAME>", // optional
    replyToEmail: "<REPLY_TO_EMAIL>" // optional
)
