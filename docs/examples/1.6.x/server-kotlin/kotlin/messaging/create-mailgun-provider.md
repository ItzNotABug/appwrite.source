import io.appwrite.Client
import io.appwrite.coroutines.CoroutineCallback
import io.appwrite.services.Messaging

val client = Client()
    .setEndpoint("https://cloud.appwrite.io/v1") // Your API Endpoint
    .setProject("&lt;YOUR_PROJECT_ID&gt;") // Your project ID
    .setKey("&lt;YOUR_API_KEY&gt;") // Your secret API key

val messaging = Messaging(client)

val response = messaging.createMailgunProvider(
    providerId = "<PROVIDER_ID>",
    name = "<NAME>",
    apiKey = "<API_KEY>", // optional
    domain = "<DOMAIN>", // optional
    isEuRegion = false, // optional
    fromName = "<FROM_NAME>", // optional
    fromEmail = "email@example.com", // optional
    replyToName = "<REPLY_TO_NAME>", // optional
    replyToEmail = "email@example.com", // optional
    enabled = false // optional
)