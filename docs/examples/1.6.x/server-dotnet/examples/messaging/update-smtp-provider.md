using Appwrite;
using Appwrite.Enums;
using Appwrite.Models;
using Appwrite.Services;

Client client = new Client()
    .SetEndPoint("https://cloud.appwrite.io/v1") // Your API Endpoint
    .SetProject("&lt;YOUR_PROJECT_ID&gt;") // Your project ID
    .SetKey("&lt;YOUR_API_KEY&gt;"); // Your secret API key

Messaging messaging = new Messaging(client);

Provider result = await messaging.UpdateSmtpProvider(
    providerId: "<PROVIDER_ID>",
    name: "<NAME>", // optional
    host: "<HOST>", // optional
    port: 1, // optional
    username: "<USERNAME>", // optional
    password: "<PASSWORD>", // optional
    encryption: SmtpEncryption.None, // optional
    autoTLS: false, // optional
    mailer: "<MAILER>", // optional
    fromName: "<FROM_NAME>", // optional
    fromEmail: "email@example.com", // optional
    replyToName: "<REPLY_TO_NAME>", // optional
    replyToEmail: "<REPLY_TO_EMAIL>", // optional
    enabled: false // optional
);