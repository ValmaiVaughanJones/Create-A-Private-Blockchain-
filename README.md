# Create-A-Private-Blockchain-

Run the application with the following command from the root directory:

node app.js
Be sure you run npm install before trying to run the application.

Notes
The route submitstar was renamed to submitStar for consistency.

The existing routes for getting a block by height/hash were functionally identical (GET /block/:height vs GET /block/:hash). This resulted in the first defined route overriding the second, meaning that the code for GET /block/:hash was never reached.

To resolve this, I renamed the route to get blocks by hash to be /block/hash/:hash.
