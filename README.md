# Joepegs Collections List
This repo contains logos, banners, and collection info for the Joepegs marketplace. May be deprecated in future. 

## Add new collections
Add collection info to the `joepegs.collections.json` like the below example. 

1. **Contract addresses should be checksummed.**
- If it is all lower-case it is likely not correct. 
- Enter it into snowtrace, and then copy the address from the UI. 

2. `symbol` can be found from snowtrace. 

3. `desc` can be the length of tweet, but no hard limits. 

```
{
    "address": "0x880Fe52C6bc4FFFfb92D6C03858C97807a900691",
    "name": "Party Animals",
    "desc": "Avalanche Party Animals is a collection of 10,000 unique, NFTs, who are breaking the dance floor on the Avalanche Blockchain and can’t wait to finally enter the Party Animals Mansion. APA are based on the unofficial Avalanche mascot, Wolfie. We hope to bring it to its rightful place as the official mascot and by doing so, also bring recognition to the platform. Each Party Animal is hand-drawn by our talented artist anxd is randomly generated from numerous of assets. All of them are unique, but some are simply legendary.", 
    "symbol": "APA",
    "verified": 1,
    "royalties": 0.05, 
    "fees": 0.02,
    "twitter": "https://twitter.com/apa_nft",
    "discord": "https://t.co/BkdreWVBMTt",
    "website": "https://partyanimalsxyz.com//",
    "logoURI": "https://raw.githubusercontent.com/traderjoe-xyz/collections-list/main/images/0x880Fe52C6bc4FFFfb92D6C03858C97807a900691/logo.png",
    "bannerURI": "https://raw.githubusercontent.com/traderjoe-xyz/collections-list/main/images/0x880Fe52C6bc4FFFfb92D6C03858C97807a900691/banner.png"
}

```

4. Add `banner.png` into the location like `images/<address>/banner.png`. 
- Should be `1440x700px` size
- **must** be renamed `banner.png`

5. Add `logo.png` into the location like `images/<address>/logo.png`. 
- Should be `200x200px` size
- **must** be renamed `logo.png`

6. The `verified` field can be `0, 1, 2` to denote number of ticks. Obviously if they are `0` ticks, murloc will come ask you what you're doing. 

7. `JSON` files are lists; make sure you add a `,` to the previous entry like so: 
```
    collections: [
        { 
            some collection ...  
        }, // add this comma here
        { 
            your new collection...    
        } // don't add comma here
    ]
```

## Updating
You can in fact add files and change JSON file directly in github on browser. 
- When saving changes always select Pull Request (PR). 
- Name the branch after the collection you are adding or fixing, e.g. `add-APA` or `fix-APA`. 
- Don't worry about versioning. 