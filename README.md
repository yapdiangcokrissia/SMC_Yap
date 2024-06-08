# My Personal Savings DApp

## Overview

This project is a decentralized application (DApp) that simulates a simple personal savings ATM on the Ethereum blockchain. Users can connect their MetaMask wallet, deposit funds, and withdraw funds from their personal savings account.

## Prerequisites

- Node.js and npm installed
- MetaMask extension installed in your browser
- Basic knowledge of React and Solidity

## Getting Started

### Installation

1. **Clone the repository:**

   ```bash
   git clone https://github.com/yourusername/my-personal-savings.git
   cd my-personal-savings
   ```

2. **Install dependencies:**

   ```bash
   npm install
   ```

3. **Compile the smart contract:**

   Ensure you have Hardhat installed:

   ```bash
   npm install --save-dev hardhat
   ```

   Compile the contract:

   ```bash
   npx hardhat compile
   ```

4. **Deploy the smart contract:**

   Deploy the contract to your local Ethereum network:

   ```bash
   npx hardhat node
   npx hardhat run scripts/deploy.js --network localhost
   ```

5. **Run the application:**

   Start the React development server:

   ```bash
   npm run dev
   ```

   Open your browser and navigate to `http://localhost:3000`.

## File Structure

- **index.js**: Main React component that handles user interaction and communicates with the smart contract.
- **Assessment.sol**: Solidity smart contract that manages the personal savings account.
- **artifacts/**: Contains the compiled contract JSON files.

## Smart Contract (Assessment.sol)

The smart contract allows for the following functionalities:

- **getBalance**: Retrieve the current balance of the savings account.
- **deposit**: Deposit a specified amount into the savings account. Only the owner can deposit funds.
- **withdraw**: Withdraw a specified amount from the savings account. Only the owner can withdraw funds.

## React Component (index.js)

The React component interacts with the smart contract through the ethers.js library. It allows users to:

- Connect their MetaMask wallet
- Display the connected account and wallet balance
- Deposit and withdraw funds

### Key Functions

- **getWallet**: Checks for MetaMask and retrieves the user's account.
- **connectAccount**: Prompts the user to connect their MetaMask wallet.
- **getATMContract**: Creates an instance of the smart contract.
- **getBalance**: Fetches the current balance from the smart contract.
- **deposit**: Deposits the entered amount into the smart contract.
- **withdraw**: Withdraws the entered amount from the smart contract.

### UI Elements

- **Account Information**: Displays the connected account address and wallet balance.
- **Input Field**: Allows the user to enter the amount to deposit or withdraw.
- **Buttons**: Trigger deposit and withdrawal actions.

## Usage

1. **Connect MetaMask Wallet**: Click the button to connect your MetaMask wallet.
2. **Deposit Funds**: Enter the amount to deposit and click the "Deposit" button.
3. **Withdraw Funds**: Enter the amount to withdraw and click the "Withdraw" button.

## Styles

The application uses simple CSS for styling, located within the JSX of the React component.

```css
.container {
  padding-top: 5px;
  padding-bottom: 5px;
  text-align: center;
  background-color: #c6e6c6; /* Pastel green */
  font-family: 'Poppins', sans-serif;
}
```

## License

This project is licensed under the MIT License.

## Acknowledgements

- [Ethers.js](https://docs.ethers.io/v5/)
- [Hardhat](https://hardhat.org/)
- [MetaMask](https://metamask.io/)

## Troubleshooting

If you encounter issues:

- Ensure MetaMask is installed and configured correctly.
- Make sure you are connected to the correct Ethereum network.
- Check the console for any error messages and troubleshoot accordingly.

Feel free to open an issue on GitHub if you need further assistance.
