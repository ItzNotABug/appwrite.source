require 'appwrite'

include Appwrite

client = Client.new
    .set_endpoint('https://cloud.appwrite.io/v1') # Your API Endpoint
    .set_project('&lt;YOUR_PROJECT_ID&gt;') # Your project ID
    .set_key('&lt;YOUR_API_KEY&gt;') # Your secret API key

messaging = Messaging.new(client)

result = messaging.create_msg91_provider(
    provider_id: '<PROVIDER_ID>',
    name: '<NAME>',
    template_id: '<TEMPLATE_ID>', # optional
    sender_id: '<SENDER_ID>', # optional
    auth_key: '<AUTH_KEY>', # optional
    enabled: false # optional
)