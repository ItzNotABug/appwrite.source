<?php

use Appwrite\Client;
use Appwrite\Services\Storage;

$client = (new Client())
    ->setEndpoint('https://cloud.appwrite.io/v1') // Your API Endpoint
    ->setProject('&lt;YOUR_PROJECT_ID&gt;') // Your project ID
    ->setKey('&lt;YOUR_API_KEY&gt;'); // Your secret API key

$storage = new Storage($client);

$result = $storage->getBucket(
    bucketId: '<BUCKET_ID>'
);