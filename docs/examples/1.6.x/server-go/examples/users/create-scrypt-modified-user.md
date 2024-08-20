package main

import (
    "fmt"
    "github.com/appwrite/sdk-for-go/client"
    "github.com/appwrite/sdk-for-go/users"
)

func main() {
    client := client.NewClient()

    client.SetEndpoint("https://cloud.appwrite.io/v1") // Your API Endpoint
    client.SetProject("") // Your project ID
    client.SetKey("") // Your secret API key

    service := users.NewUsers(client)
    response, error := service.CreateScryptModifiedUser(
        "<USER_ID>",
        "email@example.com",
        "password",
        "<PASSWORD_SALT>",
        "<PASSWORD_SALT_SEPARATOR>",
        "<PASSWORD_SIGNER_KEY>",
        users.WithCreateScryptModifiedUserName("<NAME>"),
    )

    if error != nil {
        panic(error)
    }

    fmt.Println(response)
}