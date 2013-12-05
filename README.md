Nemesis-Project
===============

A cryptographic ledger that amasses valuable information.  Reuse code from other crypto currencies when possible

Bitcoin source code:
http://github.com/bitcoin/bitcoin

Namecoin source code:
http://github.com/namecoin/namecoin

Anoncoin source code:
https://github.com/Anoncoin/anoncoin

Type A maximum shares outstanding: 100,000

Type B maximum shares outstanding: 100

    Type B shares availabe through proof of storage mining (regulated by equation/algorithm): 50
    Type B shares availabe through data submission (become available at same rate as mined coins): 50
    
Proof of storage network stores each encrypted submission
Server stores topic and key of each submission (retrieves from storage network and decrypts for end user)

Shares availability

    Mining retarget time: X
    Max shares available via mining: 50
    Max shares available for submitting content: 50
    Shares become available when blocks are found for storing information
    for (t >= 0) {
        
        Type A shares outstanding approximates the curve: [100000 - 100000e^(-b2*t1)] //where t1 is the time of the timeline of                                                                                 //claims
        Type B shares outstanding approximates the curve: [100 - 100e^(-b1*t2)] // where t2 is the time since content                                                                                     //submission
        }
        
        
Wallets to make advertising payments to

  
  Sub Projects
  
  
    * Proof of Work single computational mining network
      - perform the function of finding blocks and storing sections of the storage array with the same function
      - rather than 2 mining networks have a single network based on producing a random string that satisfies the checksum
        of the hashed network status (balance of payments), encrypted claim with key, and padding
      - combined network of proof of storage and proof of work
  
    * IP masking for users (both viewers and submitters of content)
      - needs to have enough speed to stream movies real time
      - needs to provide enough anonymity to protect sources of information
    
    * Encryption protocol for encrypting submitted information for each block
      - use public key so key length that has to be stored can be shorter than information
      
      
    **websites for viewing information** (this will be done by a third party)
      - user interface
      - protocol for retrieving and streaming information
    
    * Advertising bid system // make advertising bids to designated wallets
      - the bid transaction
      - length of advertising slots: stays at one block
      - two advertising slots on web page: on home page, and with specific content
        - home page advertising paid in type A stock
        - submission specific advertising paid in type B stock of submission specific currency
      - submit advertisements as a claim/submission and make a bid to the bid receiving wallet
      - tally bids for a new block, highest bid wins
      - length of advertising rights correlates with projected length of time to find a new block for proof of storage
    
    **question system for categorizing submissions** (done by a third party website)
      - MP3+
        - music
        - music videos
        - movies
      - hardware
      - software
      - text
      - images
      - leaked confidential
      
    **search function** (performed by website)
      - search on unencrypted topics of submissions or topic encrypted using property preserving encryption: 
        http://outsourcedbits.org/2013/10/06/how-to-search-on-encrypted-data-part-1/
        (how to search on encrypted data)
      - allow user control to filter results by: categories and strength of storage network


    * format for submissions
      - topic (encrypted with PPE or left unencrypted)
      - file of certain length to be encrypted
  
    * PPE encryption protocol for encrypting topics of submited claims


    * 2D array: "timeline of claims submissions" and corresponding advertisements
      - the first row is an array of data submissions with x1y1 submitted before x2y1 submitted before x3y1
      - row y2 could be random bit padding
      - row y3 through yn are advertisements submitted for the claims
      - advertisements are ordered with row y3 containing the claim submission number of the advertisement with the               highest bid and being stored with a data submission
      - new blocks from proof of work add storage slots to the array
      - prevent buffer overflow by adding elements to the array (or creating a new array) each time a new block is found          for proof of work
