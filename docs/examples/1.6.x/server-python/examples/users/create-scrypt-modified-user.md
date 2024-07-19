from appwrite.client import Client

client = Client()
client.set_endpoint('https://cloud.appwrite.io/v1') # Your API Endpoint
client.set_project('&lt;YOUR_PROJECT_ID&gt;') # Your project ID
client.set_key('&lt;YOUR_API_KEY&gt;') # Your secret API key

users = Users(client)

result = users.create_scrypt_modified_user(
    user_id = '<USER_ID>',
    email = 'email@example.com',
    password = 'password',
    password_salt = '<PASSWORD_SALT>',
    password_salt_separator = '<PASSWORD_SALT_SEPARATOR>',
    password_signer_key = '<PASSWORD_SIGNER_KEY>',
    name = '<NAME>' # optional
)