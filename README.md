# code-challenge-1-phase2
# 🌿 Plantsy Admin Dashboard

Welcome to **Plantsy**, the admin dashboard for a plant store! You've been tasked with building out functionality that enables users to manage plant listings via a React frontend and a JSON Server backend. The UI components and styles are already built — your job is to wire up state and data persistence via API calls.

---

## 🚀 Setup Instructions

1. **Install dependencies**
   ```bash
   npm install
Start the backend

bash
Copy
Edit
npm run server
This will launch the backend on http://localhost:6001

Start the React frontend

bash
Copy
Edit
npm start
Verify backend connectivity
Visit: http://localhost:6001/plants in your browser. You should see the plant data in JSON format.

📋 User Stories
✅ Core Deliverables
As a user:

✅ I can see all plants when the app loads.

✅ I can add a new plant using the form.

✅ I can mark a plant as "sold out".

✅ I can search for plants by name and see a filtered list.

🌟 Advanced Deliverables (Optional)
As a user:

✅ I can update the price of a plant and see it after refreshing.

✅ I can delete a plant and it stays deleted after refresh.

🌐 API Reference
📌 Base URL
arduino
Copy
Edit
http://localhost:6001
🔍 GET /plants
Fetch all plants.

Example Response:

json
Copy
Edit
[
  {
    "id": 1,
    "name": "Aloe",
    "image": "./images/aloe.jpg",
    "price": 15.99
  },
  {
    "id": 2,
    "name": "ZZ Plant",
    "image": "./images/zz-plant.jpg",
    "price": 25.98
  }
]
➕ POST /plants
Add a new plant.

Headers:

json
Copy
Edit
{
  "Content-Type": "application/json"
}
Request Body:

json
Copy
Edit
{
  "name": "string",
  "image": "string",
  "price": number
}
Example Response:

json
Copy
Edit
{
  "id": 3,
  "name": "Snake Plant",
  "image": "./images/snake.jpg",
  "price": 19.99
}
✏️ PATCH /plants/:id
Update a plant's price or sold-out status.

Headers:

json
Copy
Edit
{
  "Content-Type": "application/json"
}
Request Body Example:

json
Copy
Edit
{
  "price": 17.99
}
Example Response:

json
Copy
Edit
{
  "id": 1,
  "name": "Aloe",
  "image": "./images/aloe.jpg",
  "price": 17.99
}
❌ DELETE /plants/:id
Delete a plant by ID.

Example Response:

json
Copy
Edit
{}
🧱 Project Structure
bash
Copy
Edit
src/
├── components/
│   ├── NewPlantForm.js       # Form to add new plant
│   ├── PlantList.js          # List of plant cards
│   ├── PlantCard.js          # Individual plant component
│   └── Search.js             # Search input component
├── PlantPage.js              # Main logic container
├── App.js                    # Root component
└── index.js                  # Entry point
🛠 Technologies Used
React (Frontend)

json-server (Mock Backend)

JavaScript / JSX

HTML & CSS

💡 Development Tips
Use the browser DevTools → Network tab to monitor fetch calls.

Use .catch() in fetch calls to gracefully handle network failures.

Use parseFloat() to convert input values (like price) to numbers before sending to the backend.

Always verify your backend is running and accessible before testing the app.

🧑‍💻 Author
Made with ❤️ for learning and practicing full-stack JavaScript.

markdown
Copy
Edit

Let me know if you'd like:
- Markdown with **badges** (React, JSON Server, etc.)
- Deployment tips (e.g., for Netlify + hosted JSON Server)
- Or a printable PDF version of this `README`.
