# Cardano DAO Governance Dashboard: Voting & Treasury

This project is an open-source, decentralized dashboard for managing DAO governance on the Cardano blockchain. It provides a unified interface for token-based voting, protocol parameter updates, and treasury management, integrating directly with the MuesliSwap DAO Smart Contract framework. The DAO governance dashboard is developed with the MuesliSwap design in mind but can easily be adapted for other Cardano projects. 

---

## Overview

DAOs on Cardano often struggle with fragmented governance solutions. Our dashboard addresses this gap by offering a fully open-source and customizable platform that allows:
- **Seamless Wallet Integration:** Users can connect their Cardano wallet with automatic wallet discovery.
- **Proposal Management:** View and interact with open and closed proposals.
- **Voting Mechanisms:** Cast votes on proposals, with on-chain transaction creation and signing handled directly in the frontend.
- **Treasury Oversight:** Monitor current treasury assets, review past treasury transactions (pay-ins and pay-outs), and track treasury performance over time.

---

## Features

- **Wallet Connection:** Effortless integration with Cardano wallets using libraries such as `@cardano-foundation/cardano-connect-with-wallet`.
- **Proposal Dashboard:** Lists open proposals (for which voting is active) and closed proposals (where voting has concluded).
- **Detailed Proposal View:** Each proposal shows comprehensive details, current voting statistics, and potential outcomes. A vote must exceed a minimum threshold to be accepted, and “Reject” is always available as an option.
- **Proposal Creation:** Users can create proposals through the frontend and directly interact with the smart contracts. 
- **Treasury Management:** Provides insights into the DAO treasury including current asset balances, transaction history, and performance charts.
- **Open-Source & Customizable:** The project is fully open-sourced under the GNU GPL license, allowing any Cardano DAO to adapt it for their needs.

---

## Technical Setup & Architecture

### Frontend Stack

- **Framework & Language:**  
  - **React** for building the user interface.
  - **TypeScript** for static type checking and improved maintainability.
  
- **Build & Development Tools:**  
  - **Vite** is used as the development server and bundler for fast builds.
  - **ESLint** and **Prettier** ensure code quality and consistency.

- **UI Components:**  
  - **Chakra UI** provides a robust and accessible component library for rapid UI development.
  
- **State Management:**  
  - **Redux Toolkit** is employed for predictable state management across the dashboard.

### Blockchain Integration

- **Smart Contract Data:**  
  The frontend communicates with the MuesliSwap DAO Smart Contract framework to retrieve governance data, such as proposals, voting tallies, and treasury transactions. For more information please check the detailed GitHub repository including report here (MuesliSwap On-Chain Governance)[https://github.com/MuesliSwapTeam/muesliswap-onchain-governance]

- **Transaction Handling:**  
  All transactions (voting, staking, etc.) are built and signed directly in the frontend. This approach leverages backend-provided smart contract information and ensures that users can interact with on-chain data seamlessly.

- **Key Libraries:**  
  - `@blockfrost/blockfrost-js`
  - `@cardano-foundation/cardano-connect-with-wallet`
  - `@emurgo/cardano-serialization-lib-browser`

### Additional Tools & Libraries

- **Visualization:**  
  - **Chart.js** and **react-chartjs-2** are used to render charts for treasury performance.
  
- **Forms & Validation:**  
  - **Formik** and **Yup** help manage form state and validation for proposals and other user inputs.
  
- **Animations:**  
  - **Framer Motion** is used for smooth transitions and UI animations.

---

## Smart Contract & Transaction Integration

The dashboard leverages data from the MuesliSwap DAO Smart Contract framework to manage governance processes on-chain. Key aspects include:

- **On-Chain Data:**  
  The backend supplies essential smart contract information such as proposals, vote counts, and treasury transactions.

- **Frontend Transaction Building:**  
  All transactions (voting, staking, etc.) are constructed and signed in the frontend using the smart contract data provided. This ensures a seamless user experience where all interactions occur directly in the browser.

- **Libraries Used:**  
  - `@cardano-foundation/cardano-connect-with-wallet`
  - `@emurgo/cardano-serialization-lib-browser`

---

## License

This project is licensed under the GNU GPL license. See the [LICENSE](LICENSE) file for details.

---

## Community & Support

For questions, support, or to provide feedback, please join our community channels or open an issue in this repository.

