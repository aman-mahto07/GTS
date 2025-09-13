

# 🃏 GuessSuit dApp

A decentralized game built on **Algorand** where users try to guess the correct suit. Are you feeling lucky?
<img width="1600" height="773" alt="image" src="https://github.com/user-attachments/assets/74764e4c-173a-4868-8f8e-983a8f67bf73" />
https://lora.algokit.io/testnet/application/745511299
---

## 📜 Project Description

**GuessSuit** is a simple, smart contract-powered game built on the Algorand blockchain. It allows users to pick a card suit — **hearts**, **clubs**, **spades**, or **diamonds** — and see if their guess matches the winning suit.

This project demonstrates how blockchain and smart contracts can power lightweight, trustless games with verifiable outcomes.

---

## 🚀 What It Does

1. A user selects a suit (e.g., `"hearts"`).
2. The smart contract compares the user's guess against a preset correct value.
3. Returns `"correct"` if the guess matches the winning suit, or `"wrong"` otherwise.

> ✅ Simple logic, fully decentralized execution.

---

## ✨ Features

* 🔗 **Smart Contract on Algorand**: All logic runs on-chain using the Algorand blockchain.
* 🎮 **Interactive Game Logic**: A quick and fun "guess the suit" game.
* 📦 **Lightweight**: Minimal dependencies and efficient contract.
* 🔐 **Verifiable Results**: Anyone can verify the contract's behavior on-chain.
* 💡 **Educational**: Great example for beginners learning smart contracts on Algorand.

---

## 🛠️ Tech Stack

* [Algorand](https://www.algorand.com/)
* [algorand-typescript](https://github.com/algorandfoundation/algorand-typescript)

---

## 📁 Code Snippet

```ts
import { Contract } from "@algorandfoundation/algorand-typescript"

export class GuessSuit extends Contract {
  pick(suit: string): string {
    const suits = ["hearts", "clubs", "spades", "diamonds"]
    return suit === suits[0] ? "correct" : "wrong"
  }
}
```

---

## 📌 Next Steps

* [ ] Add randomness to the winning suit
* [ ] Integrate frontend UI
* [ ] Deploy on TestNet/MainNet
* [ ] Add wallet support (AlgoSigner, Pera, etc.)

---
