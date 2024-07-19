require 'appwrite'

include Appwrite

client = Client.new
    .set_endpoint('https://cloud.appwrite.io/v1') # Your API Endpoint
    .set_project('&lt;YOUR_PROJECT_ID&gt;') # Your project ID
    .set_session('') # The user session to authenticate with

teams = Teams.new(client)

result = teams.update_name(
    team_id: '<TEAM_ID>',
    name: '<NAME>'
)