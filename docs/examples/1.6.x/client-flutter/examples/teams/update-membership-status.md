import 'package:appwrite/appwrite.dart';

Client client = Client()
    .setEndpoint('https://cloud.appwrite.io/v1') // Your API Endpoint
    .setProject('&lt;YOUR_PROJECT_ID&gt;'); // Your project ID

Teams teams = Teams(client);

Membership result = await teams.updateMembershipStatus(
    teamId: '<TEAM_ID>',
    membershipId: '<MEMBERSHIP_ID>',
    userId: '<USER_ID>',
    secret: '<SECRET>',
);