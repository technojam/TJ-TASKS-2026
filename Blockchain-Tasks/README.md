# Blockchain Tasks

Welcome to the Web 3.0 / Blockchain

This year's tasks are designed to take you beyond basic wallet interaction and introduce you to real blockchain development. You will work with cryptographic signatures, Solana programs, Rust, wallets, transactions, and decentralized applications.

No prior blockchain experience is required, but you are expected to research, experiment, debug, and understand the code you write.

**Important:** Use testnets/devnets only. Do not use real funds.

---

> **Resources:** For reference materials, tools, and helpful links for Web 3 , check out `resources.md`.

---

## Easy Task: Sign Your First On-Chain Identity

### Objective

Understand how blockchain wallets use cryptographic signatures to prove that a user controls a wallet address without revealing their private key.

### Task

Build a small webpage that connects to a browser wallet such as MetaMask.

Your application should:

1. Provide a **Connect Wallet** button.
2. Display the connected wallet address.
3. Display the current blockchain/network.
4. Provide a **Sign Message** button.
5. Ask the user to sign a custom message such as:

```text
I am participating in the Web3 Auditions 2026.
```

6. Display the generated signature.
7. Recover the wallet address from the signature.
8. Display whether the recovered address matches the connected wallet.

### Conceptual Questions

Along with your code, answer the following:

- What is a digital signature?
- Why doesn't the website need your private key?
- What is the difference between a wallet address and a private key?
- Why should users be careful about what messages they sign?
- How can a signature be used to prove ownership of an address?

### Bonus

Add a **Verify Signature** section where someone can enter:

- Message
- Signature
- Wallet address

Your application should determine whether the signature is valid.

### Resources

**Documentation**

- [MetaMask Developer Documentation](https://docs.metamask.io/)
- [Ethereum Wallets](https://ethereum.org/en/wallets/)
- [ethers.js Documentation](https://docs.ethers.org/)

**Video Resources**

- Search for beginner tutorials on Ethereum wallet signatures and message signing.

### What We're Testing

- Wallet fundamentals
- Cryptography concepts
- JavaScript
- Web3 interaction
- Debugging
- Understanding of digital signatures

---

## Medium Task: Build Your First Solana Program

### Objective

Get familiar with the **Solana blockchain**, its account model, programs, transactions, and wallet interaction by building a small on-chain application.

You will create a **Decentralized Student Registry** where users can store and retrieve a small piece of information on Solana.

Use **Solana Devnet** for this task. No real SOL is required.

### The Scenario

Imagine a university wants to maintain a decentralized student registry.

A student should be able to connect their Solana wallet and create a profile containing:

- Student Name
- Student ID
- Course
- Graduation Year

The information should be stored on-chain and associated with the student's Solana wallet.

### Part 1: Understand Solana

Before coding, briefly explain the following:

- What is Solana?
- What is a Solana wallet address?
- What is a Solana account?
- What is a Solana Program?
- How is a Solana Program different from an Ethereum smart contract?
- What is SOL used for?
- What is Solana Devnet?

Also explain the following flow:

```text
Wallet
   |
   v
Account
   |
   v
Program
   |
   v
Transaction
   |
   v
Solana Blockchain
```

### Part 2: Build the Solana Program

Create a basic Solana program using **Rust**.

You may use the **Anchor framework** to simplify development.

Your program should support at least the following operations:

```text
createProfile()
updateProfile()
getProfile()
```

A profile should contain data similar to:

```json
{
  "studentName": "Ansh",
  "studentId": "CSE2026",
  "course": "Computer Science",
  "graduationYear": 2029
}
```

The profile must be associated with the user's Solana wallet.

### Part 3: Add Validation

Your program should perform basic validation.

At minimum:

- Student name cannot be empty.
- Student ID cannot be empty.
- Graduation year must be reasonable.
- A user must not be able to modify another user's profile.
- A profile should not be initialized twice for the same user.

Explain **where these checks are performed and why they should be enforced on-chain rather than only in the frontend.**

### Part 4: Build a Frontend

Create a simple webpage that allows a user to:

1. Connect a Solana wallet such as Phantom.
2. Display their wallet address.
3. Create their student profile.
4. View their existing profile.
5. Update their profile.
6. Display transaction status.

The interface should show states such as:

```text
Wallet Connected
Creating profile...
Transaction submitted
Transaction confirmed
Profile successfully stored on Solana
```

The UI does not need to be highly polished. Focus on functionality and understanding.

### Part 5: Deploy to Solana Devnet

Deploy your program to **Solana Devnet**.

Your submission must include:

- GitHub repository
- Program ID
- Solana Explorer link
- Frontend
- Screenshots or demo video
- Setup instructions

**Do not deploy to Mainnet or use real funds.**

### Part 6: Think Like a Blockchain Developer

Answer the following questions in your README.

**1. Account Model**
Why does Solana use accounts to store program state?

**2. Programs**
Why are Solana programs generally considered stateless?

**3. Transactions**
What happens when your frontend calls `createProfile()`?

**4. Fees**
Who pays the transaction fee?

**5. Ownership**
How does your program ensure that one student cannot modify another student's profile?

**6. Ethereum vs Solana**

Compare Ethereum and Solana using the following table:

| Feature                           | Ethereum | Solana |
| --------------------------------- | -------- | ------ |
| Smart contract / program language |          |        |
| State model                       |          |        |
| Transaction model                 |          |        |
| Wallet                            |          |        |
| Native token                      |          |        |
| Development framework             |          |        |

### Bonus Challenge

Implement **Profile Ownership Transfer**.

Allow a student to transfer their profile to another Solana wallet.

For example:

```text
Student A
    |
    v
Transfer Profile
    |
    v
Student B
```

Your program should ensure that:

- Only the current owner can initiate the transfer.
- The new owner must provide a valid Solana address.
- The previous owner can no longer modify the profile.
- The new owner becomes the profile authority.

### Resources

**Documentation**

- [Solana Developer Documentation](https://solana.com/docs)
- [Solana Cookbook](https://solanacookbook.com/)
- [Solana Playground](https://beta.solpg.io/)
- [Anchor Documentation](https://www.anchor-lang.com/)
- [Solana Web3.js Documentation](https://solana-foundation.github.io/solana-web3.js/)
- [Phantom Developer Documentation](https://docs.phantom.com/)

**Video Resources**

- [Solana Development Tutorials](https://www.youtube.com/results?search_query=solana+development+anchor+rust)
- [Solana Accounts and Programs](https://www.youtube.com/results?search_query=solana+accounts+programs+tutorial)
- [Anchor Framework Tutorials](https://www.youtube.com/results?search_query=solana+anchor+framework+tutorial)

### What We're Testing

This task evaluates:

- Understanding of Solana's architecture
- Basic Rust knowledge
- Solana accounts and programs
- Anchor fundamentals
- Wallet integration
- Frontend and blockchain interaction
- Transaction handling
- On-chain validation
- Ability to read documentation
- Ability to debug unfamiliar technology

The most important part is not the visual design of your application. We care about whether you understand what your code is doing and can explain how data moves through the Solana network.

---

## Hard Task: Build a Mini Decentralized Marketplace

### Objective

Build a small decentralized application where users can list and purchase digital items using a smart contract.

This task combines:

- Solidity
- Smart contracts
- Wallets
- Transactions
- Events
- Frontend development
- Blockchain state
- Basic smart-contract security

You may use Ethereum Sepolia or another supported EVM testnet.

### The Scenario

Create a decentralized marketplace for digital items.

A user should be able to:

1. Connect their wallet.
2. Create a listing.
3. Set a price.
4. View active listings.
5. Purchase another user's listing.
6. See the current owner of an item.
7. View the item's transaction/history information.

You do not need to build a complete NFT marketplace like OpenSea.

A simple marketplace for unique digital items represented by IDs is sufficient.

### Part 1: Smart Contract

Create a Solidity smart contract that maintains information similar to:

```text
Item ID
Seller
Current Owner
Price
Is Listed
```

Implement functions similar to:

```text
createItem()
listItem()
buyItem()
cancelListing()
getItem()
```

### Part 2: Purchase Logic

The `buyItem()` function should:

1. Check that the item exists.
2. Check that the item is currently listed.
3. Check that the buyer has sent enough ETH.
4. Transfer ownership.
5. Transfer payment to the seller.
6. Remove the item from the marketplace.
7. Emit an event describing the purchase.

### Part 3: Events

Your contract must emit events for important actions.

For example:

```text
ItemCreated
ItemListed
ItemPurchased
ListingCancelled
```

Your frontend should listen for these events and update the UI accordingly.

### Part 4: Frontend

Build a simple interface containing the following sections.

**Wallet**

- Connect wallet
- Display wallet address
- Display network

**Marketplace**

- Display available items
- Display seller
- Display price
- Display owner
- Buy button

**Seller Dashboard**

Allow users to:

- Create an item
- List an item
- Cancel their listing
- View their items

**Transaction State**

Your UI should clearly show states such as:

```text
Waiting for wallet confirmation
Transaction submitted
Transaction confirmed
Transaction failed
```

### Part 5: Security Challenge

After completing the marketplace, identify at least **three potential security problems** in your implementation.

For each vulnerability:

1. Explain the problem.
2. Explain how an attacker could exploit it.
3. Explain how you would fix it.
4. Explain why your proposed fix works.

At least one of your findings should involve smart-contract security.

You may investigate concepts such as:

- Reentrancy
- Access control
- Integer/amount handling
- Incorrect ownership checks
- Replay attacks
- Front-running
- Unsafe external calls
- Transaction ordering

Do not blindly copy security fixes from tutorials. Explain the reasoning behind your solution.

### Bonus Challenges

Choose **one** of the following.

**Option A: NFT Upgrade**
Convert your marketplace into an actual **ERC-721 NFT marketplace**.

**Option B: Marketplace Analytics**

Build a page displaying:

- Total items created
- Total items sold
- Total marketplace volume
- Number of active listings
- User purchase history

Use blockchain events to derive this information.

### Submission Requirements

Submit a GitHub repository containing a structure similar to:

```text
project/
├── README.md
├── contracts/
├── frontend/
└── tests/
```

Your README must contain:

- Project description
- Architecture diagram
- Tech stack
- Setup instructions
- Smart-contract address
- Testnet used
- Block explorer link
- Screenshots
- Known limitations
- Security vulnerabilities discovered
- Security fixes
- What you learned

Also submit a **2–5 minute demo video** showing:

1. Connecting the wallet.
2. Creating an item.
3. Listing the item.
4. Purchasing the item.
5. Confirming the transaction.
6. Showing the ownership change.
7. Demonstrating at least one security consideration.

### Resources

**Smart Contracts**

- [Solidity Documentation](https://docs.soliditylang.org/)
- [OpenZeppelin Contracts](https://docs.openzeppelin.com/contracts/)
- [Ethereum Developer Documentation](https://ethereum.org/en/developers/)

**Development**

- [Remix IDE](https://remix.ethereum.org/)
- [Hardhat](https://hardhat.org/)
- [Foundry](https://book.getfoundry.sh/)

**Security**

- [OpenZeppelin Security](https://docs.openzeppelin.com/contracts/5.x/api/utils)
- [Solidity Security Considerations](https://docs.soliditylang.org/en/latest/security-considerations.html)

### What We're Testing

The hard task evaluates:

- Solidity fundamentals
- Smart-contract architecture
- Wallet integration
- Blockchain transactions
- Event handling
- Frontend integration
- Smart-contract security
- Debugging
- Understanding of decentralized applications
- Ability to research independently

The goal is not to create a production ready marketplace.

The goal is to demonstrate that you understand how a decentralized application works from the **frontend to the wallet, from the wallet to the smart contract, and from the smart contract to the blockchain**.

---

## Note

You are encouraged to use documentation, tutorials, AI tools, forums, and other resources while working on the tasks.

However, **you must understand the code you submit**.

During the audition, you may be asked to explain your implementation, modify your code, or solve a small problem based on your project.

All the best guys !!!!!!!!

**Made with ❤️ by Team TechnoJam**
