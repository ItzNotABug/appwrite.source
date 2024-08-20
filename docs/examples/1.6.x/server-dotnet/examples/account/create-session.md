using Appwrite;
using Appwrite.Models;
using Appwrite.Services;

Client client = new Client()
    .SetEndPoint("https://cloud.appwrite.io/v1") // Your API Endpoint
    .SetProject("&lt;YOUR_PROJECT_ID&gt;"); // Your project ID

Account account = new Account(client);

Session result = await account.CreateSession(
    userId: "<USER_ID>",
    secret: "<SECRET>"
);