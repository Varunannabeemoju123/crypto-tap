# 💸 CrypTap Offramp Backend

Welcome to the **CrypTap Offramp API** – a Node.js and Express-based backend that facilitates crypto-to-INR transactions using services like **Transak** or **Onmeta**. This API accepts payment info, initiates an offramp transaction, and triggers INR settlements to UPI IDs.

---

## 🚀 Features

- 🔐 Secure Express server setup
- 🔄 POST endpoint to initiate crypto-to-INR offramp
- 🧾 Integration with **Transak** Offramp API (Onmeta supported too)
- ✅ Environment-based configuration using `.env`
- 📡 Ready to connect with MetaMask & frontend (React/Next.js)

---

## 🛠️ Tech Stack

- Node.js
- Express.js
- Axios
- dotenv

---

## 📂 Project Structure

server/
│
├── index.js # Main entry point
├── routes/
│ └── offramp.js # Offramp POST endpoint
├── .env # API keys and secrets
└── package.json

yaml
Copy
Edit

---

## ⚙️ Setup Instructions

1. **Clone the repo**
   ```bash
   git clone https://github.com/your-username/crytap-offramp-backend.git
   cd crytap-offramp-backend
Install dependencies

bash
Copy
Edit
npm install
Configure .env
Create a .env file and add the following:

env
Copy
Edit
TRANSAK_API_KEY=your_transak_key
TRANSAK_SECRET=your_transak_secret
BASE_URL=https://api.transak.com
PORT=8000
Start the server

bash
Copy
Edit
npx nodemon index.js
🧪 How to Test with Postman
Method: POST

URL: http://localhost:8000/api/offramp

Body (JSON):

json
Copy
Edit
{
  "amount": 1000,
  "upiId": "example@upi",
  "walletAddress": "0x1234567890abcdef1234567890abcdef12345678"
}
Response: JSON with success or error info.

🛡️ Security Notes
Keep your API keys safe using .env

Do not commit .env to version control

Validate and sanitize all inputs before forwarding to Transak or Onmeta

📞 Contact
For questions or support:

🔗 Project Maintainer: Varun Annabeemoju