import Appwrite

let client = Client()
    .setEndpoint("https://cloud.appwrite.io/v1") // Your API Endpoint
    .setProject("&lt;YOUR_PROJECT_ID&gt;") // Your project ID
    .setKey("&lt;YOUR_API_KEY&gt;") // Your secret API key

let databases = Databases(client)

let indexList = try await databases.listIndexes(
    databaseId: "<DATABASE_ID>",
    collectionId: "<COLLECTION_ID>",
    queries: [] // optional
)
