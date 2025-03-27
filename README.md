# Intro to Bitcoin Development

###### Prerequisites

1. Create a [Github](https://github.com) Account
    This will be used to hold any code you'd like to save for later in your own repository.
    All code shown today will be runnable in your Browser's devtools, so no additional tools will be required.

# Notes for Discussion

## What and Why of Money
What is Money?
Latin term "Fiat Lux" in English translates to "Let there be light". Therefore, "Fiat Money" means ...

Money communicates the value that we use to interact with each other. 

### Properties of Money

1. Fungibility: Money must be interchangeable and of equal value.
1. Durability: Money should withstand wear and tear.
1. Divisibility: Money can be divided into smaller units for transactions.
1. Portability: Money should be easy to carry.
1. Acceptability: Money must be widely accepted.
1. Limited supply: Money supply should be controlled.
1. Uniformity: All units of money should be the same.

### Functions of Money

1. Store of Value - Any asset where it's value persists (or increases) overtime and redeemable now or later.
1. Medium of Exchange - The money is able to be exchanged for other goods/services/valuables.
1. Unit of Account - The standard numerical monetary unit. 

### Inflation
Inflation - The increase of the money in a system. The causes the devaluation of each unit of money and price increases in the markets that are effected. 
When the rich get richer, the assets they buy/own/trade tend to increase in price (vehicles, houses, stock market, land). When everyone gets an economic boost, day to day items like eggs will increase in price (Post 2020 stimulus grocery prices).

This is also not a spot increase. Inflation increasing or slowing down is akin to velocity. It is a rate of change of a value.
Velocity is the rate at which your speed or direction is changing.
Inflation is the rate at which the money is losing value.

It is also not additive, but a multiplier. It's often spoken of in terms of percentages, the Federal Reserve targets 2% inflation per year. That means price would increase X * 1.02 each year.

#### Quick Math 

Items going from $1 to $5 is not an increase of $4, this price of the item has increased 5X.

$1 -> $5 != 1 + 4
$1 -> $5 == 1 * 5

#### The Last 50 Years of Fiat

Price changes and other calamities since the USD became imaginary (decoupled from Gold) 
[wtfhappenedin1971.com](https://wtfhappenedin1971.com)

### Broken System

Going on about 40 years of a Fiat USD and nearing 100 years of the Federal Reserve Bank holding and profiting from the money of the US Government, and after cycles of regular recession every decade or so, the first recession of the 2000s came in 2008 with the Housing Crisis.

In 2009, several forms of Hope were making progress towards "fixing" the system. That January saw both the inauguration of our First Black President on January 20, 2009 and Bitcoin software first started running on January 3, 2009.

## Bitcoin

[The Bitcoin Whitepaper](https://bitcoin.org/bitcoin.pdf)

[Official Network Site](https://bitcoin.org)

[Bitcoin Core Developer Site](http://bitcoindevs.xyz/)

Bitcoin (capital B) is usually mentioning the entire Bitcoin network. It is it's own monetary network that replaces banking system, has it's own public monetary policy that replaces the secret plans of federal reserve and the government (the federal reserve is not actually a federal entity). Lastly, the asset itself, commonly written as bitcoin (lowercase b) is the finite token that acts as digital gold.

One of the layer 2 networks of Bitcoin, Lightning has been developed over the last 10 years as a faster way to transact and perfect Bitcoin as a Medium of Exchange.

### No one, not even Satoshi Nakamoto, Controls Bitcoin

National currencies are distrubuted, controlled, and owned by the nation that makes it.
No one controls the Bitcoin network. Updates are handled by the entire userbase. Anyone can build and run a Bitcoin node to verify transactions and interact with the network. Anyone can build and run mining computers to process transactions. Anyone can propose changes, anyone can agree to opt into or ignore the changes. This is public consensus a

### Peer to Peer

The only peer to peer money you may have access to today is cash. Once it is in the bank, or if it is credit, the money is just a number in a database somewhere. It requires to interaction of your bank to the bank of someone else, along with potentially other intermediaries and systems, to send or receive money.

### Open Source Software

Open Software is Free to View, Run, Update, and use as your wish.
[https://github.com/bitcoin/bitcoin](https://github.com/bitcoin/bitcoin)

### Cryptography

#### Seed Phrases
12 words -> encrypted to form a random 255 byte number -> private key

#### Public/Private Keys
Public Keys are derived from Private Keys. Non-reversible

#### Wallets

Hold Private Keys and sign transactions. Only the Private Key can verify/unlock a transaction.

### The Monetary Ledger

Blockchain - a block of transactions forms every 10 minutes. This ledger tells the state of all the Bitcoin on the network, which keys own which amount of satoshis.
Similar to your own account in a bank, and a bank's accounting of all their clientele, the blockchain tracks all transactions of coins.

Bitcoin is always in the network, just changing ownership of who has what. This is similar to [public stone ownership](https://www.timesnownews.com/travel/destinations/this-remote-island-uses-giant-rocks-as-moneyand-it-actually-works-article-119473338) where a large rock would be an asset that changes ownership when used for transactions.

Timechain - Another name given to the chain due to the impervious nature of the decentralized network, someone somewhere is continuously running a node. Someone somewhere is going to be mining. Blocks continue to be added every 10 minutes, given no odd disruptions of miners. Tick Tock, Next Block.


### Mining

Proof of Work - Work earns rewards
Game of energy production, efficiency
Electrifying the world and creating and improving power grids

## Exercises

1. [Block Explorer Mempool.space](https://mempool.space/)

2. Derive Private Key

Alphanumeric -> Binary -> Hexadecimal -> Hash

[Learn Me A Bitcoin - Tools Page](https://learnmeabitcoin.com/tools/)


3. [Hash Functions](https://learnmeabitcoin.com/technical/cryptography/hash-function/)

    async function sha256(message) {
        // Encode the message as a Uint8Array (utf-8 bytes)
        const msgBuffer = new TextEncoder().encode(message);

        // Hash the message
        const hashBuffer = await crypto.subtle.digest('SHA-256', msgBuffer);

        // Convert the hash to a byte array
        const hashArray = Array.from(new Uint8Array(hashBuffer));

        // Convert bytes to hex string
        const hashHex = hashArray.map(b => b.toString(16).padStart(2, '0')).join('');
        return hashHex;
    }

    // Example usage:
    sha256("Hello, world!").then(hash => console.log(hash));


4. [SavingSatoshi.com](https://SavingSatoshi.com)

Learn and Play through 10 Chapter Story centered around a young computer scientist 100 years from now when the Bitcoin mining subsidy will drop to 0 and no more new Bitcoin will ever be created again.



We'll go through as much of the first 3 Challenges together..
1. enter text to hash and hit nonce
2. write a hash function
3. visualize hashing


# Homework

## Curriculum

[Learn Bitcoin from the Command Line](https://github.com/BlockchainCommons/Learning-Bitcoin-from-the-Command-Line)


## Install Bitcoin Core

### Reccommended Technical Bitcoin Installation Process

1. [WSL for Windows Users](https://learn.microsoft.com/en-us/windows/wsl/install) - https://learn.microsoft.com/en-us/windows/wsl/install

2. [Compile Bitcoin on Your Computer]() - https://github.com/BlockchainCommons/Learning-Bitcoin-from-the-Command-Line/blob/master/A2_0_Compiling_Bitcoin_from_Source.md

### Easier Download and Install Process

1. [Download Bitcoin Core](https://bitcoin.org/en/download)

## TextBook

[Mastering Bitcoin v3](https://github.com/bitcoinbook/bitcoinbook)
