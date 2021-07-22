# Create-A-Private-Blockchain-

Run the application with the following command from the root directory:

node app.js
Be sure you run npm install before trying to run the application.

Notes
The route submitstar was renamed to submitStar for consistency.

The existing routes for getting a block by height/hash were functionally identical (GET /block/:height vs GET /block/:hash). This resulted in the first defined route overriding the second, meaning that the code for GET /block/:hash was never reached.

To resolve this, I renamed the route to get blocks by hash to be /block/hash/:hash.
Private Blockchain Application
You are starting your journey as a Blockchain Developer, this project allows you to demonstrate that you are familiarized with the fundamentals concepts of a Blockchain platform. Concepts like: - Block - Blockchain - Wallet - Blockchain Identity - Proof of Existance

Are some of the most important components in the Blockchain Framework that you will need to describe and also why not? Implement too.

In this project you will have a boilerplate code with a REST Api already setup to expose some of the functionalities you will implement in your private blockchain.

What problem will you solve implementing this private Blockchain application?
Your employer is trying to make a test of concept on how a Blockchain application can be implemented in his company. He is an astronomy fans and he spend most of his free time on searching stars in the sky, that's why he would like to create a test application that will allows him to register stars, and also some others of his friends can register stars too but making sure the application know who owned each star.

