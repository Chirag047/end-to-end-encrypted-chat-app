# 🔐 E2E Encrypted Real-Time Chat App

A secure, real-time chat application built with **React**, **Node.js**, and **Socket.IO**, featuring **AES-based end-to-end encryption** for safeguarding message content.

---

## 📌 Project Highlights

- ✉️ Real-time messaging with **Socket.IO** and **Express**
- 🔒 **AES encryption** utilized in React client to encrypt messages before sending
- 📩 Backend relays only encrypted content—decryption occurs exclusively on client-side
- 💬 Clean and responsive web UI built with **React**

---

## ⚙️ Architecture Overview

### Frontend (React)

- Encrypts outgoing messages using **AES**
- Decrypts incoming messages prior to display
- Connects to server over WebSocket via **Socket.IO client**

### Backend (Node.js + Express)

- Receives encrypted messages from clients
- Broadcasts them to targeted recipients or rooms without touching plaintext
- No access to user message content at any time

---

## 📈 How This Works

By encrypting messages on the client and decrypting only on the recipient’s device, this architecture ensures no server-side leakage of chat content. The encryption keys remain securely managed on the client, and the backend only handles ciphertext.

---

## 🛠️ Tech Stack

| Layer        | Technologies               |
|--------------|----------------------------|
| Frontend     | React.js, Socket.IO Client |
| Backend      | Node.js, Express, Socket.IO|
| Encryption   | AES (client-side)          |

---

## 🚀 Running the Project

```bash
# Clone the repository
git clone https://github.com/yourusername/E2E-Encrypted-Real-Time-Chat-App.git
cd E2E-Encrypted-Real-Time-Chat-App

# Install dependencies for backend and frontend
cd backend && npm install
cd ../frontend && npm install

# Start the server and client
cd backend && npm run dev
cd ../frontend && npm start
