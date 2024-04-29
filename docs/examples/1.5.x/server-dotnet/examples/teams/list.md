using Appwrite;
using Appwrite.Models;
using Appwrite.Services;

Client client = new Client()
    .SetEndPoint("https://cloud.appwrite.io/v1") // Your API Endpoint
    .SetProject("5df5acd0d48c2") // Your project ID
    .SetSession(""); // The user session to authenticate with

Teams teams = new Teams(client);

TeamList result = await teams.List(
    queries: new List<string>(), // optional
    search: "<SEARCH>" // optional
);