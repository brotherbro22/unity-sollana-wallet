Unity-Solana Wallet
The First Open-Source Unity-Solana Wallet with NFT support
![solana](https://github.com/brotherbro22/unity-sollana-wallet/assets/167093182/5de0e667-1eb7-4e66-81f5-57fcc307b9ed)

The Unity-Solana Wallet is an essential bridge connecting game developers and the Solana blockchain. With Solana’s quick and low-cost transactions, games can start using blockchain technology like never before - in real-time. Thousands of developers will bring millions of players into the Solana ecosystem. This will, in turn, make the Solana projects benefit from an increased number of participants, and cross-protocol interoperability in games will take us beyond the current understanding of DeFi.

Unity-Solana Wallet uses Solnet's implementation .NET SDK, but we had to modify the library to make it Unity compatible with .NET Standard 2.0 and .NET 4.x. Solnet is Solana's .NET SDK to integrate with the .NET ecosystem. Solnet.


https://github.com/brotherbro22/unity-sollana-wallet/assets/167093182/133c6816-099f-45ef-8a23-64e48ac0ea1d


Features
Create/Backup wallet with mnemonic phrase
Account handling
Transaction building
SOL balance
SPL-token balances
SPL-token transfers
Basic UI examples
WebSocket subscription
Save and load mnemonics from local txt file
Save private key in txt file
Dependencies
Newtonsoft.Json
Chaos.NaCl.Standard
Portable.BouncyCastle
Zxing
External packages
Native File Picker
Standalone File Browser
Roadmap
Multiple wallet accounts
Camera support with QR code scanning for token transfers
Improved UI for in-game easy integration
Metaplex NFT / NFT-PRO support with GameObjects
Token swaps
NFT swaps
One-click in-game currency creator
Themed UI support
Metaplex auctions for in-game store items
Installation
Clone this repository outside of the main Unity project
Go to Package Manager in your project
Click on the plus in the top left corner and select "Add package from disk"
Select package.json file from a cloned dir
Once the package is installed, in the Package Manager inspector you will have Samples. Click on Import
Step-by-step instructions
If you have an older version of Unity that doesn't have imported Newtonsoft.Json just import it.
After importing the wallet Unity will throw unity-plastic error. Just restart Unity.
Create a new scene.
![Phantom-SOL](https://github.com/brotherbro22/unity-sollana-wallet/assets/167093182/e5a8a8ca-3560-4af0-bfc2-728f5042be57)

Import WalletController prefab into your scene.
Set Client Source (Mainnet/Testnet/Devnet/Custom uri) and Storage Method (Json/Simple txt) on SimpleWallet script in WalletController prefab.
If you use custom URI be careful to use WS/WSS instead of HTTP/HTTPS because WebSocket does not work with HTTP / HTTPS.
To save mnemonics in JSON format, select the JSON storage method, and if you want to save it as a regular string, select Simple Txt.
If you want to use mnemonics saved in JSON format, you must deserialize it first. You have an example in ReGenerateAccountScreen.cs in the ResolveMnemonicsByType method.
Create new Canvas
Import WalletHolder prefab into the Canvas or if you want your design just import wallet prefab and customize the scene like we did with WalletHolder.
