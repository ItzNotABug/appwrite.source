package main

import (
    "fmt"
    "github.com/appwrite/sdk-for-go/client"
    "github.com/appwrite/sdk-for-go/databases"
)

func main() {
    client := client.NewClient()

    client.SetEndpoint("https://cloud.appwrite.io/v1") // Your API Endpoint
    client.SetProject("") // Your project ID
    client.SetSession("") // The user session to authenticate with

    service := databases.NewDatabases(client)
    response, error := service.ListDocuments(
        "<DATABASE_ID>",
        "<COLLECTION_ID>",
        databases.WithListDocumentsQueries([]interface{}{}),
    )

    if error != nil {
        panic(error)
    }

    fmt.Println(response)
}