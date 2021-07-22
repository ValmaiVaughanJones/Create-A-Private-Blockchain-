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

What is the process describe by the employer to be implemented in the application?
The application will create a Genesis Block when we run the application.
The user will request the application to send a message to be signed using a Wallet and in this way verify the ownership over the wallet address. The message format will be: <WALLET_ADRESS>:${new Date().getTime().toString().slice(0,-3)}:starRegistry;
Once the user have the message the user can use a Wallet to sign the message.
The user will try to submit the Star object for that it will submit: wallet address, message, signature and the star object with the star information. The Start information will be formed in this format:
    "star": {
        "dec": "68° 52' 56.9",
        "ra": "16h 29m 1.0s",
        "story": "Testing the story 4"
	}
The application will verify if the time elapsed from the request ownership (the time is contained in the message) and the time when you submit the star is less than 5 minutes.
If everything is okay the star information will be stored in the block and added to the chain
