# NFT Hunt
NFT Hunt is a gamified marketplace in which users can track down NFTs anywhere in the world.
Whether it's a new song, an animated renaissance style painting or a unique piece of armor for that indie game you're playing; access a new layer of
interaction between artists and collectors at the touch of your fingertips.

This project was part the Chainlink Hackathon Spring 2021.

# Inspiration
Our esteemed teammate Dani originally came up with the idea while we were brainstorming back in march. Our first thought was that it could revolutionize part of the tourism industry. People traveling to popular destinations can now buy location specific NFT’s to prove that they went there. Since people love to show off their travels, this would be a logical next step in the way of social interaction through a gamified NFT search.

Eventually we realized that we could gamify the NFT space and add a layer of interaction between creators/retailers and their fans/customers.

# What it does
Our proposed functionality is different than our actual functionality. 
Proposed: Users can travel around the world and open our app to view NFT’s that are around their current location. They can buy these NFT’s only if they are at the specified location. 
Actual: You can query an IPFS file where location data is stored. You can check to see if that location is within the predetermined location square of that given NFT. You can record your GPS location to a Firebase database.

# How we built it
We built it using Solidity, Remix, and Android Studios. We started with Android Studios in an attempt to establish the connection between phone GPS data and Firebase. Once this connection was established, we moved onto creating a connection with Chainlink oracles. This proved harder than originally anticipated, so we downloaded the .json file with the GPS data and uploaded that to IPFS. Once it was on IPFS we could use the Chainlink oracle GET request more easily. Next, we wrote a smart contract in Solidity to use the Chainlink oracle, and another smart contract to check the coordinates of the GPS data.

# Challenges we ran into
This was a learning curve for all of us, at different levels. We spent a LOT of time learning about Chainlink oracles, blockchain structure, Remix and Hardhat. One of the main challenges that stuck out was connecting the Chainlink oracle to Firebase. The Firebase API was unclear and we could just not figure out the connection. Another challenge was using the Kovan testnet in Hardhat. For some reason it refused to work and so the Chainlink oracle smart contract has to be executed in Remix at the time of writing this.

# Accomplishments that we're proud of
Connecting the Chainlink oracle to IPFS, learning Solidity, Javascript, Remix hardhat, navigating the cryptic command line and getting a landing page up and running in time for demo day.

# What we learned
Shoot high. Although we did not complete the project, we still learned quite a lot. Between Solidity, Hardhat, JS, Bootstrap our brains were ready to bust. Teamwork. We worked well together and communicated like at team. I think we can all agree we had a good time 😉

# What's next for NFT-Hunt
Tie together the backend: Finish the Android GPS app, connect the Chainlink oracle to Firebase, put up an NFT to buy, connect that NFT to the GPS_check_locations smart contract. 
Frontend: a create a frontend using React.js


