# 🃏 Guess The Suit — Algorand dApp
## 📘 Project Description

**Guess The Suit** is a fun and beginner-friendly decentralized application (dApp) built on the **Algorand blockchain**. It allows users to guess a card suit (hearts, clubs, spades, or diamonds), and the smart contract will determine if the guess is correct using a deterministic algorithm tied to the current blockchain round.

This project is designed to demonstrate how simple and powerful smart contracts can be using TypeScript-like syntax on Algorand.

---

## 🚀 What It Does

- Accepts a user’s guess for a card suit.
- Uses the current blockchain **round number** to determine the "correct" suit.
- Compares the guess with the computed suit.
- Returns `"correct"` or `"wrong"` instantly.

---

## ✨ Features

- 🔁 **Round-based randomness** — fully on-chain, using `Global.round`.
- 💡 **Minimal logic** — easy to understand for beginners learning smart contracts.
- ⚡ **Fast responses** — the contract returns results immediately.
- 🧠 **Deterministic** — no oracle or external randomness required.
- 🌐 **Deployable on Algorand TestNet or MainNet.**

---

## 🔗 Deployed Smart Contract

**Deployed Address**: `Guess The Suit`  
> _Replace `XXX` with your actual contract address once deployed._

---

## 💻 Smart Contract Code

```ts
//import { Contract, Global } from '@algorandfoundation/algorand-typescript'

export class GuessSuit extends Contract {
  pick(suit: string): string {
    const suits = ["hearts", "clubs", "spades", "diamonds"]
    return suit === suits[Number(Global.round % 4)] ? "correct" : "wrong"
  }
}
