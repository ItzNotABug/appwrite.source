import Appwrite

let client = Client()
    .setEndpoint("https://cloud.appwrite.io/v1") // Your API Endpoint
    .setProject("&lt;YOUR_PROJECT_ID&gt;") // Your project ID
    .setSession("") // The user session to authenticate with

let storage = Storage(client)

let fileList = try await storage.listFiles(
    bucketId: "<BUCKET_ID>",
    queries: [], // optional
    search: "<SEARCH>" // optional
)
