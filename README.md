# Simple Postman Base for Salesforce

There are quite a number of documents and blog articles on how to get started with Postman and Salesforce.  This repo is a collection of a few practices in files that can be imported directly into Postman and used quickly.

## How to use
1. Import `Org.postman_environment.json` as an environment in Postman
2. Import `Salesforce-Base.postman_collection.json` as a collection in Postman
3. Edit the new org environment in postman - add user, password, token details
4. Run the `Salesforce-Base` collection using the collection runner.  Be sure to set the correct environment for the run.
5. If you wish to run the collection via a CLI, use this command to run newman: `newman run Salesforce-Base.postman_collection.json -e Org.postman_environment.json`.  Be sure to edit the environment json file or export your environment config from Postman.  [Additional docs on the Postman site](https://learning.getpostman.com/docs/postman/collection_runs/command_line_integration_with_newman).

*Note: The `! Salesforce Auth - Login` requst must be the first request run in any execution.  It gets the session ID and endpoint URLs used for all other requests.*

## Contributing
PRs gladly accepted!