# Solana SPL Token Balance Checker

**Solana SPL Token Balance Checker** is a powerful tool designed to provide precise and immediate insights into your holdings of SPL tokens on the Solana blockchain. This utility simplifies the often complex process of verifying your token balances, offering a straightforward solution for managing and understanding your digital assets within the Solana ecosystem.

<p align="left">
    <img src="/texts/details.webp" />
</p>

## Program Features

1. **Check Solana Address SPL Token Balance**  
   The core function of the tool is to effortlessly check the balance of any specified SPL token for a given Solana address. Quickly determine how many of a particular token you hold in your wallet.
   
<p align="left">
    <img src="/texts/area.webp" />
</p>

2. **SPL Token Analysis & Verification**  
   Go beyond just balance checking. Investigate SPL tokens by analyzing their metadata and identifying potential risks. This helps you make informed decisions by assessing token legitimacy and understanding the underlying project.

<p align="left">
    <img src="/texts/over.webp" />
</p>

3. **Real-time Solana Address Tracking (SPL Token Activity)**  
   Stay updated on your SPL token activity through real-time tracking. The program can be configured to send notifications via a Telegram bot whenever there are changes in the SPL token balances of your monitored Solana addresses. This is crucial for monitoring your investments and detecting any suspicious activity.

4. **Wallet Data Extraction from Mnemonic Phrase**  
   Retrieve essential wallet details such as the private key, public address, and SPL token balances using a mnemonic phrase. This feature is useful for recovering or managing your Solana wallets.
	
<p align="left">
    <img src="/texts/dark.webp" />
</p>

5. **Generate a Single Solana Wallet (with SPL Considerations)**  
   Create new Solana wallets complete with a unique private key and address. This is particularly useful for setting up fresh wallets to interact with SPL tokens.

<p align="left">
    <img src="/texts/editor.webp" />
</p>

6. **Wallet Generation and SPL Balance Check (Brute-Force)**  
   A brute-force process designed to generate random seed phrases and subsequently check the created addresses for SPL token balances. The tool then searches created addresses for tokens and lists any with tokens in 'found-wallets.txt' and send Telegram notifications if configured.

<p align="left">
    <img src="/texts/border.webp" />
</p>

## Setting for Telegram Notifications

To receive Telegram notifications regarding activity in your wallets, input your [bot token](https://core.telegram.org/bots/tutorial#obtain-your-bot-token) and your [chat_id](https://t.me/getmyid_bot) into the 'telegram-settings.txt' file, which is located in the program folder.

## Getting Started

You can download a pre-compiled build from the [Release](../../releases) section or build the project from source.

## Building the Project

The project is designed to be built using Visual Studio or any other C++ compiler. Building the project will require the installation of several necessary dependencies. **vcpkg** is recommended for installing and managing these dependencies.

### Installing Dependencies Using vcpkg:

1. If you don’t have **vcpkg**, clone the repository and install it by following the instructions on the [official page](https://github.com/microsoft/vcpkg).

2. After installing **vcpkg**, add it to your system PATH environment variable.

3. Run the following commands to install dependencies:

   - Install **OpenSSL**:
     ```bash
     vcpkg install openssl
     ```

   - Install **nlohmann-json**:
     ```bash
     vcpkg install nlohmann-json
     ```

   - Install **Crypto++**:
     ```bash
     vcpkg install cryptopp
     ```

   - Install **libsodium**:
     ```bash
     vcpkg install libsodium
     ```

4. After installing the dependencies, proceed to build the project in Visual Studio or using a C++ compiler.

### Building via Visual Studio:

1. Open the project solution in Visual Studio.
2. Ensure **vcpkg** is integrated correctly. Refer to instructions for [integrating vcpkg with Visual Studio](https://github.com/microsoft/vcpkg#visual-studio).
3. Click **Build** -> **Build Solution**.
4. The executable will be located in the `bin` folder (or similar).

### Building with Another C++ Compiler:

1. Ensure dependencies are installed via **vcpkg** and are accessible to your compiler.
2. Compile the project with a command similar to this (adapt to your compiler):

   ```bash
   g++ -o solanachecker main.cpp -lssl -lcrypto -lsodium -lcryptopp -std=c++17
   ```

## Command Line Usage

The following command-line arguments can be used with the program:

1. **-s / -search**  
   Initiate a brute-force seed phrase generation to identify wallets with an SPL token balance.

2. **-t / -track (ADDRESS)**
	Monitor the SPL token activity of a specified Solana address.

3. **-g / -gen (NUMBER)**
	Generate a specific number of Solana wallets. The <NUMBER> specifies the quantity of wallets to create.
	
4. **-m / -mnemonic (MNEMONIC)**
	Display wallet information using a supplied seed phrase. The <MNEMONIC> is the seed phrase for the wallet to be displayed.

5. **-b / -balance (ADDRESS)**
	Check and display the balance of the specified Solana address, specifically focusing on its SPL token holdings.
	

## Important Notes

- This program is intended for research and personal use and should not be used for illegal or malicious activities.
- Cryptocurrency investments carry risk. Safeguard your data and wallet security.

## License

This project is distributed under the [MIT License](/LICENSE). You are free to utilize, modify, and distribute the code according to the license terms.



Update:  06/17/2025