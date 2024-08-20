package main

import (
    "fmt"
    "github.com/appwrite/sdk-for-go/client"
    "github.com/appwrite/sdk-for-go/messaging"
)

func main() {
    client := client.NewClient()

    client.SetEndpoint("https://cloud.appwrite.io/v1") // Your API Endpoint
    client.SetProject("") // Your project ID
    client.SetKey("") // Your secret API key

    service := messaging.NewMessaging(client)
    response, error := service.CreateMailgunProvider(
        "<PROVIDER_ID>",
        "<NAME>",
        messaging.WithCreateMailgunProviderApiKey("<API_KEY>"),
        messaging.WithCreateMailgunProviderDomain("<DOMAIN>"),
        messaging.WithCreateMailgunProviderIsEuRegion(false),
        messaging.WithCreateMailgunProviderFromName("<FROM_NAME>"),
        messaging.WithCreateMailgunProviderFromEmail("email@example.com"),
        messaging.WithCreateMailgunProviderReplyToName("<REPLY_TO_NAME>"),
        messaging.WithCreateMailgunProviderReplyToEmail("email@example.com"),
        messaging.WithCreateMailgunProviderEnabled(false),
    )

    if error != nil {
        panic(error)
    }

    fmt.Println(response)
}