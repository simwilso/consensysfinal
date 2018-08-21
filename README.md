##########Consensys Final Project - By Simon Wilson##########

##What does your project do?

This dApp is for something we are calling SOLidarity Token'.
The SOLidarity Token allows a 'solar' customer who is produces more power than they consume to donate that 'surplus' as a token to a SOLShare mini-grid recipient who needs power in Bangladesh.

This is a demo of a concept that was described by SOLShare at the Free Electrons Accelerator in SanFrancisco. The scenario described involved a 'Solar' customer in Germany logging onto their power company webpage and donating surplus energy 'credits' to a SOLShare 'mini-grid' recipient in Bangladesh.

##How does it work?

The dApp in this case is for demonstration purposes.
It's built modular so that depending on the customer both the 'donating' energy company and the 'recipients' can be specified.

There are 2 main 'actors' in the system these are:

  1 - The USER
  The user is the energy customer who is producing the 'surplus energy' and making the donations.
  i.e. In our example above this is the Solar system prosumer from Germany).

  2 - The RECIPIENT
  The recipient is the 'user' who needs power in Bangladesh.  This may be a school, a hospital, a shop or some other entity.

The dApp is built so that the specifics of both of these actors shown can be customised.
For example the demonstrator may wish to tailor the demonstration to show a hospital, shop, school and a football ground as the possible recipients.
The dApp also allows logos and pictures to be uploaded (to IPFS) for both the recipients and donor.

##Features
The dApp offers several features.  These are:

  1 - I can register as a user
  This allows me to enter the credentials of the USER (or donor energy company) which are displayed in the UI.
  When a user is registered they are automatically given a balance of 1,000,000 SOLidarity Tokens to spend.
  Energy company Logo is also uploaded to IPFS in registration.

  2 - I can register Recipients
  This allows me to enter the credentials of the RECIPIENT which are also displayed in the UI.
  This includes how much SOL the recipient currently has and how your balance could provide them.
  Again the uploading of a Recipient Avatar through IPFS integration is also available.
  There are a maximum of 4 recipients that can be added to this demo.

  3 - I can manually change the regional exchange rates or 'vote' for a region to reduce the SOL/kWH price.
  Different regions in country have different price per kWH.  These sections allow the admin to manually update that regional price (which is shown in the SOL/kWH exchange table).
  There are four regions.
  Additionally users may 'vote' for a region to increase the SOL/kWH ratio for users in that region.
  This is useful to show government and foundations to demonstrate that the token value can be adjusted based on current needs per region.


##How to set it up?

  Pre-requisites:
    -have IPFS installed
    -have Truffle installed
    -have Metamask installed
    -have NPM Lite web server installed
    -have the Solidarity folder copied

  Run:
    open terminal (term window1).
      $ipfs daemon
    open another terminal (term window2) and browse to 'solidarity' folder.
      $truffle compile
    open another terminal(term window3) window
      $ganache-cli
    copy 'seed phrase to clipboard' open browser and connect to metamask 'private network 8545'.
    go back to 'term window2'
      $truffle test
    verify that all tests succeed    
      $truffle migrate
      $npm run dev
    open browser (ensure Metamask is added)
    open Metamask dialog and select 'private network 8545' then hit 'import using account seed phrase'
    paste seed phrase from Ganache-cli
    browse to 'localhost' with the url and port shown in 'term window2' (i.e. localhost:8081)

##How to use it?

  Register yourself as a user:
    Once you see the WebUI scroll down to 'register user'.
    Enter some credentials and submit
    Metamask will prompt you to approve the transaction
    Approve it..
    when the page refreshes the User credentials will also update.
  Register recipients (you can do this from the same ethereum account or a new one):
    same as above scroll to the 'register recipient' section
    enter credentials and submit
    Metamask will prompt you to approve the transaction
    Approve it..
    when the page refreshes the Recipient credentials will also update.

  Once your added recipients you can vote and/or change exchange rates for regions and donate SOL Tokens to recipients.

  Have fun and be gentle grading me!!!







