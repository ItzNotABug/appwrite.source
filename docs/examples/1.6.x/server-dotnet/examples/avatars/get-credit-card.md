using Appwrite;
using Appwrite.Enums;
using Appwrite.Models;
using Appwrite.Services;

Client client = new Client()
    .SetEndPoint("https://cloud.appwrite.io/v1") // Your API Endpoint
    .SetProject("&lt;YOUR_PROJECT_ID&gt;") // Your project ID
    .SetSession(""); // The user session to authenticate with

Avatars avatars = new Avatars(client);

byte[] result = await avatars.GetCreditCard(
    code: CreditCard.AmericanExpress,
    width: 0, // optional
    height: 0, // optional
    quality: 0 // optional
);