<?php

use Appwrite\Client;
use Appwrite\Services\Users;
use Appwrite\Enums\MessagingProviderType;

$client = (new Client())
    ->setEndpoint('https://cloud.appwrite.io/v1') // Your API Endpoint
    ->setProject('&lt;YOUR_PROJECT_ID&gt;') // Your project ID
    ->setKey('&lt;YOUR_API_KEY&gt;'); // Your secret API key

$users = new Users($client);

$result = $users->createTarget(
    userId: '<USER_ID>',
    targetId: '<TARGET_ID>',
    providerType: MessagingProviderType::EMAIL(),
    identifier: '<IDENTIFIER>',
    providerId: '<PROVIDER_ID>', // optional
    name: '<NAME>' // optional
);