# Intro to Bitcoin Development

###### Prerequisites

1. Create a [Github](https://github.com) Account
   
    This will be used to hold any code you'd like to save for later in your own repository.
    All code shown today will be runnable in your Browser's devtools, so no additional tools will be required.


## What and Why of Money

What is Money?

Latin term "Fiat Lux" in English translates to "Let there be light". 

Therefore, "Fiat Money" means ...

### Inflation

Price changes and other calamities since the USD became imaginary (decoupled from Gold) 
[wtfhappenedin1971.com](https://wtfhappenedin1971.com)

inflation of money supply. devaluation of each $1
$1 -> $5 != 1 + 4
$1 -> $5 == 1 * 5

## Bitcoin

[Official Network Site](https://bitcoin.org)

[Bitcoin Core Developer Site](http://bitcoindevs.xyz/)

Bitcoin is monetary network (replaces banking system), policy(replaces federal reserve), asset (replaces gold)
bitcoin describes the tokens that many think about.

Software platform enabling ownership, privacy
Currency, Trade

## Exercises

1. Visualize the Timechain

[Block Explorer Mempool.space](https://mempool.space/)

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

Curriculum

[Learn Bitcoin from the Command Line](https://github.com/BlockchainCommons/Learning-Bitcoin-from-the-Command-Line)

Reccommended Technical Bitcoin Installation Process

1. [WSL for Windows Users](https://learn.microsoft.com/en-us/windows/wsl/install) - https://learn.microsoft.com/en-us/windows/wsl/install

2. [Compile Bitcoin on Your Computer]() - https://github.com/BlockchainCommons/Learning-Bitcoin-from-the-Command-Line/blob/master/A2_0_Compiling_Bitcoin_from_Source.md

Easier Download and Install Process

1. [Download Bitcoin Core](https://bitcoin.org/en/download)

TextBook

[Mastering Bitcoin v3](https://github.com/bitcoinbook/bitcoinbook)
