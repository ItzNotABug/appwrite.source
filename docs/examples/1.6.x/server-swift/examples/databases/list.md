import Appwrite

let client = Client()
    .setEndpoint("https://cloud.appwrite.io/v1") // Your API Endpoint
    .setProject("&lt;YOUR_PROJECT_ID&gt;") // Your project ID
    .setKey("&lt;YOUR_API_KEY&gt;") // Your secret API key

let databases = Databases(client)

let databaseList = try await databases.list(
    queries: [], // optional
    search: "<SEARCH>" // optional
)
