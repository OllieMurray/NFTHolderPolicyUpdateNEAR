# NFTHolderPolicyUpdateNEAR
# 🏛️ Purpose:

MVP for updating DAO with a 'Holders' Policy.
1. Pull all NFT holders from [Paras]
2. Propose holders policy to sputnikv2 DAO
3. Vote on proposal in [AstroDao], but recommended testing in [AstroDaoTestNet] first!

# 📘 Procedure:
## 1. Pull all NFT holders from [Paras]:
### Install prerequisites:
 Install [NPM] and [Node.js] by running the following in cmd:
 
    npm install -g npm
    
 Check successfull installation:

    node -v
    npm -v

Install [axios] (verify installation and version similar to above commands):

    npm install axios

### Query holders of NFT from [Paras]:
1. navigate to the [Paras] landing page and find the name of your nft project through the search bar
2. select the name of the collection author, for example:

![CollAuthor]

3. Modify the API string in GetCollectionID.js so that it references your collections author. It looks like this:

![APIStringColl]

   The query will return a string like this, this is the collection Id and should be used in step 4.
 
4. Use the result from the previous step to modify the API string in GetHolders.js, so that it references your collection ID. It looks like this:

![APIStringHolders]

   The query will return a list of all of the nft holders formatted such that they can be dropped right into our policy proposal.  Keep this for later.

## 2. Propose holders policy to sputnikv2 DAO
### Install prerequisites:
1. Install NEAR CLI, a detailed walk through can be found [Here]:
 
[Paras]: https://paras.id/
[AstroDao]: https://astrodao.com/
[AstroDaoTestNet]: https://testnet.app.astrodao.com/my/feed
[NPM]: https://docs.npmjs.com/downloading-and-installing-node-js-and-npm
[Node.js]: https://nodejs.dev/download/package-manager/
[axios]: https://www.npmjs.com/package/axios
[CollAuthor]: https://github.com/OllieMurray/NFTHolderPolicyUpdateNEAR/blob/main/MonkeyGodImage.png "Collection Author"
[APIStringColl]: https://github.com/OllieMurray/NFTHolderPolicyUpdateNEAR/blob/main/APIString.png "API String"
[APIStringHolders]: https://github.com/OllieMurray/NFTHolderPolicyUpdateNEAR/blob/main/APIString.png "API String"
