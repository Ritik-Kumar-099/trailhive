<div align="center">

<img src="https://readme-typing-svg.herokuapp.com?font=Cormorant+Garamond&size=40&duration=3000&pause=1000&color=2E8B57&center=true&vCenter=true&width=600&lines=%E2%9B%B0%EF%B8%8F+TrailHive;Adventure+Travel+Platform" alt="TrailHive" />

<p><em>Discover destinations. Register your interest. Travel together.</em></p>

<p>
  <img src="https://img.shields.io/badge/Node.js-v18+-339933?style=for-the-badge&logo=node.js&logoColor=white" />
  <img src="https://img.shields.io/badge/MongoDB-Atlas-47A248?style=for-the-badge&logo=mongodb&logoColor=white" />
  <img src="https://img.shields.io/badge/Express.js-000000?style=for-the-badge&logo=express&logoColor=white" />
  <img src="https://img.shields.io/badge/Razorpay-02042B?style=for-the-badge&logo=razorpay&logoColor=white" />
</p>

<br/>

> **TrailHive** is a full-stack group travel booking platform — explore destinations, register for trips, and travel once enough adventurers join in.

<br/>

</div>

---

## 🌍 How It Works

<table>
  <tr>
    <td align="center" width="200">
      <h3>🔍 Explore</h3>
      <p>Browse curated destinations and trip details on the landing page</p>
    </td>
    <td align="center" width="200">
      <h3>📝 Register</h3>
      <p>Fill in your details and pay securely via Razorpay to lock your spot</p>
    </td>
    <td align="center" width="200">
      <h3>👥 Wait for Crew</h3>
      <p>Trip is confirmed once enough travelers have registered</p>
    </td>
    <td align="center" width="200">
      <h3>✈️ Adventure!</h3>
      <p>Pack your bags — your group journey is confirmed and ready</p>
    </td>
  </tr>
</table>

---

## 🛠️ Tech Stack

<table>
  <tr>
    <th>Layer</th>
    <th>Technology</th>
  </tr>
  <tr>
    <td>🖥️ Frontend</td>
    <td>HTML5, CSS3, Vanilla JavaScript</td>
  </tr>
  <tr>
    <td>⚙️ Backend</td>
    <td>Node.js + Express.js</td>
  </tr>
  <tr>
    <td>🗄️ Database</td>
    <td>MongoDB + Mongoose ODM</td>
  </tr>
  <tr>
    <td>💳 Payments</td>
    <td>Razorpay (UPI / Card / Netbanking / Wallet)</td>
  </tr>
  <tr>
    <td>🔤 Fonts</td>
    <td>Cormorant Garamond + DM Sans (Google Fonts)</td>
  </tr>
  <tr>
    <td>🎨 Icons</td>
    <td>Font Awesome 6</td>
  </tr>
</table>

---

## 📁 Project Structure

```
trailhive/
├── public/                  # Frontend
│   ├── index.html           # Main landing page
│   ├── register.html        # Registration + Payment page
│   ├── admin.html           # Admin dashboard
│   ├── css/
│   │   └── style.css        # Main stylesheet
│   └── js/
│       └── main.js          # Navbar, counters, effects
├── server/
│   └── index.js             # Node.js + Express backend
├── .env.example             # Copy to .env and configure
├── package.json
└── README.md
```

---

## 🚀 Quick Setup

### Step 1 — Clone & Install Dependencies

```bash
git clone https://github.com/your-username/trailhive.git
cd trailhive
npm install
```

---

### Step 2 — Configure Environment

```bash
cp .env.example .env
```

Open `.env` and set your MongoDB URI:

```env
# Local MongoDB
MONGO_URI=mongodb://localhost:27017/trailhive

# MongoDB Atlas (recommended — free cloud)
MONGO_URI=mongodb+srv://youruser:yourpassword@cluster0.abcde.mongodb.net/trailhive
```

---

### Step 3 — Start the Server

```bash
# Production
npm start

# Development (auto-restart on file changes)
npm run dev
```

---

### Step 4 — Open in Browser

<table>
  <tr>
    <th>URL</th>
    <th>Page</th>
  </tr>
  <tr>
    <td><code>http://localhost:3000</code></td>
    <td>🏠 Landing Page</td>
  </tr>
  <tr>
    <td><code>http://localhost:3000/register</code></td>
    <td>📝 Registration & Payment</td>
  </tr>
  <tr>
    <td><code>http://localhost:3000/admin</code></td>
    <td>📊 Admin Dashboard</td>
  </tr>
</table>

---

## ☁️ MongoDB Atlas Setup <sub>(Free Cloud DB)</sub>

<ol>
  <li>Go to <a href="https://cloud.mongodb.com">cloud.mongodb.com</a> and create a free account</li>
  <li>Create a <strong>free cluster</strong> (M0 tier)</li>
  <li>Under <strong>Database Access</strong> → add a new database user</li>
  <li>Under <strong>Network Access</strong> → Add IP → enter <code>0.0.0.0/0</code> (allow all)</li>
  <li>Click <strong>Connect</strong> → <strong>Connect your application</strong> → copy the connection string</li>
  <li>Paste it in your <code>.env</code> file as <code>MONGO_URI</code></li>
</ol>

---

## 💳 Razorpay Integration

<table>
  <tr>
    <td>🧪 <strong>Test Mode</strong></td>
    <td>Pre-configured — no setup needed. Just run and test payments instantly.</td>
  </tr>
  <tr>
    <td>🚀 <strong>Go Live</strong></td>
    <td>
      <ol>
        <li>Login to <a href="https://dashboard.razorpay.com">Razorpay Dashboard</a></li>
        <li>Go to <strong>Settings → API Keys → Generate Live Key</strong></li>
        <li>Replace <code>rzp_test_...</code> with <code>rzp_live_...</code> in <code>public/register.html</code></li>
      </ol>
    </td>
  </tr>
</table>

---

## 🌐 API Reference

<table>
  <tr>
    <th>Method</th>
    <th>Endpoint</th>
    <th>Description</th>
  </tr>
  <tr>
    <td><img src="https://img.shields.io/badge/POST-49cc90?style=flat-square" /></td>
    <td><code>/api/register</code></td>
    <td>Save a new booking after payment</td>
  </tr>
  <tr>
    <td><img src="https://img.shields.io/badge/GET-61affe?style=flat-square" /></td>
    <td><code>/api/bookings</code></td>
    <td>Get all bookings (admin)</td>
  </tr>
  <tr>
    <td><img src="https://img.shields.io/badge/GET-61affe?style=flat-square" /></td>
    <td><code>/api/bookings/:id</code></td>
    <td>Get a single booking by ID</td>
  </tr>
  <tr>
    <td><img src="https://img.shields.io/badge/GET-61affe?style=flat-square" /></td>
    <td><code>/api/stats</code></td>
    <td>Revenue & booking statistics</td>
  </tr>
</table>

---

## 🗺️ User Flow

```
🏠 Landing Page
        │
        ▼  Click "Book Now" on a trip card
📝 Registration Form  ──▶  Fill personal details + select trip
        │
        ▼
🔍 Review Summary  ──▶  Confirm booking details
        │
        ▼
💳 Razorpay Checkout  ──▶  Pay via UPI / Card / Netbanking / Wallet
        │
        ▼
📡 POST /api/register  ──▶  Booking saved to MongoDB
        │
        ▼
✅ Confirmation Screen  ──▶  Booking ID + full details shown
```

---

## 📞 Contact & Support

<div align="center">

<p>Built with ❤️ by <strong>Rohit</strong></p>

<p>
  <a href="mailto:rohit99782@gmail.com">
    <img src="https://img.shields.io/badge/Email-rohit99782@gmail.com-D14836?style=for-the-badge&logo=gmail&logoColor=white" />
  </a>
</p>

<br/>

<sub>⛰️ <em>TrailHive — Where adventures begin together</em></sub>

</div>
