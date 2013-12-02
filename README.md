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
    Share availabiltiy approximates the curve: y = ?
    
Wallets to make advertising payments to

  
  Sub Projects
  
  
    * IP masking for users (both viewers and submitters of content)
      - needs to have enough speed to stream movies real time
      - needs to provide enough anonymity to protect sources of information
    
    * Encryption protocol for encrypting submitted information
      - use public key so key length that has to be stored on server is shorter than information
      - 
      
      
    **websites for viewing information** (this will be done by a third party)
      - user interface
      - protocol for retrieving and streaming information
    
    * Advertising bid system // make advertising bids to designated wallets
      - length of advertising slots: starts at 24 hours and decreases to 2 hours over time
      - two advertising slots on web page: on home page, and with specific content
        - home page advertising paid in type A stock
        - submission specific advertising paid in type B stock of submission specific currency
      - submit advertisements as a claim
      - tally bids for a given time slot, highest bid wins
      - advertisements will likely be broadcast embedded in the files being stored by the proof of storage scheme
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
      - topic (remains unencrypted in server)
      - file of certain length


    * thoughts on a 2D array, "timeline of claims/submissions" and corresponding advertisements
      - the first row is an array of data submissions with x1y1 submitted before x2y1 submitted before x3y1
      - row y2 is random bit padding
      - row y3 through yn are advertisements submitted for the claims
      - advertisements are ordered with row y2 containing the advertisement with the highest bid and being stored with
        a data submission
      - new blocks from proof of work add storage slots to the array
      - prevent buffer overflow by adding elements to the array (or creating a new array) each time a new block is found for     proof of work
      - 
        

