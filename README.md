🤖 AI Beauty FAQ Chatbot (n8n + Google Sheets)

This project is a Beauty FAQ AI Agent built with n8n that acts like a virtual skincare consultant.

✨ Features

Collects client details (Name, Email, Phone)

Greets returning users by name (using Google Sheets lookup)

Explains skincare issues in simple terms

Recommends 3 realistic skincare products dynamically

Highlights the best product with a friendly explanation

Saves client data into Google Sheets automatically

🛠️ How It Works

Email Check

The agent first asks for an email.

If the email exists in Google Sheets → fetches the name and greets the user personally.

If not → collects name + phone number.

Skincare Flow

Asks about the problem

Explains reasons

Suggests 3 fake but realistic products

Highlights 1 best recommendation

Asks for client’s choice

Data Saving

Internally generates structured JSON (not shown to the user).

Appends data to Google Sheets.

For existing users, phone is saved as "already have".

📂 Data Format (hidden from user)
{
  "name": "Client Name",
  "email": "client@email.com",
  "phone": "1234567890" or "already have",
  "problem": "Client's skincare problem",
  "chosen_product": {
    "name": "Best Product Name",
    "price": "$XX"
  }
}

🚀 Setup

Import workflow into n8n

Connect Google Sheets (Lookup Row + Append Row)

Add AI Agent (Gemini / OpenAI) with the system message provided

Deploy webhook → ready to chat!
