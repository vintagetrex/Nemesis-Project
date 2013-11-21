Nemesis-Project
===============

A cryptographic ledger that amasses valuable information.  Reuse code from other crypto currencies when possible

Bitcoin source code:
http://github.com/bitcoin/bitcoin

Namecoin source code:
http://github.com/namecoin/namecoin

Type A maximum shares outstanding: 100,000

Type B maximum shares outstanding per submission: 100

    Type B shares availabe through proof of storage mining (regulated by equation/algorithm): 50
    Type B shares availabe through data submission (become available at same rate as mined coins): 50
    
Proof of storage network stores each encrypted submission
Server stores topic and key of each submission (retrieves from storage network and decrypts for end user)

  Sub Projects
  
  
    * IP masking for users (both viewers and submitters of content)
      - needs to have enough speed to stream movies real time
      - needs to provide enough anonymity to protect sources of information
    
    * Encryption protocol for encrypting submitted information
      - use public key so key length that has to be stored on server is shorter than information
      - 
      
    * Deepweb site for viewing information
      - user interface
      - protocol for retrieving and streaming information
    
    * Advertising bid system
      - length of advertising slots: starts at 24 hours and decreases to 2 hours over time
      - two advertising slots on web page: on home page, and with specific content
        - home page advertising paid in type A stock
        - submission specific advertising paid in type B stock of submission specific currency
      - submit advertisements as a claim
      - tally bids for a given time slot, highest bid wins
    
    * question system for categorizing submissions
      - MP3+
        - music
        - music videos
        - movies
        - porn
      - hardware
      - software
      - text
      - images
      - leaked confidential
      
    * search function
      - search on unencrypted topics of submissions
      - allow user control to filter results by: categories and strength of storage network


    * format for submissions
      - topic (remains unencrpted in server)
      - file of certain length
