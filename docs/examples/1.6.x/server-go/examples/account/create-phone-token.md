package main

import (
    "fmt"
    "github.com/appwrite/sdk-for-go/client"
    "github.com/appwrite/sdk-for-go/account"
)

func main() {
    client := client.NewClient()

    client.SetEndpoint("https://cloud.appwrite.io/v1") // Your API Endpoint
    client.SetProject("") // Your project ID

    service := account.NewAccount(client)
    response, error := service.CreatePhoneToken(
        "<USER_ID>",
        "+12065550100",
    )

    if error != nil {
        panic(error)
    }

    fmt.Println(response)
}