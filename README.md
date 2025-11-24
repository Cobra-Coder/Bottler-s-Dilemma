# 🏭 Bottler's Dilemma: OEE Tycoon

A high-stakes, cyberpunk-themed manufacturing simulation game running entirely in a single HTML file.

# 🕹️ About The Game
Bottler's Dilemma is a realtime multiplayer simulation game designed to teach the concepts of OEE (Overall Equipment Effectiveness).
Players act as Plant Managers with a limited budget of $50,000. You have 3 minutes to upgrade a failing production line. Every decision impacts Availability, Performance, and Quality.
Compete against friends or colleagues in a live lobby to see who can achieve the highest ROI before the shift ends.

# ✨ Key Features
•	Zero-Build Architecture: The entire application (React, Tailwind, Logic, Styles) lives in a single index.html file. No npm install, no webpack, no hassle.
•	Hybrid Multiplayer: * Online Mode: Real-time lobby system powered by Firebase Firestore.
o	Offline Mode: Fully playable locally using localStorage simulation.
•	Cyberpunk Aesthetic: Custom SCADA-style UI with immersive sound effects.
•	Educational Logic: Real-world manufacturing calculations (Six Big Losses, Unit Margins, CapEx ROI).

# 🚀 How to Play
1.	Host a Room: Create a lobby and share the 4-letter Room Code.
2.	Join: Players enter their name and the code to join the waiting room.
3.	Strategize: You have 3 minutes.
o	Buy Servo Motors to fix breakdowns.
o	Install AI Vision to reduce scrap.
o	Upgrade Nozzles to increase speed.
4.	Win: The leaderboard ranks players by Profit and ROI.

# 🛠️ Deployment & Setup
Option 1: Play Immediately
Simply download the index.html file and open it in your browser. By default, it runs in Offline/Mock Mode.
Option 2: Host Your Own (Multiplayer)
To enable multiplayer, you need your own free Firebase project.
1.	Clone the Repo:
2.	git clone [https://github.com/yourusername/bottlers-dilemma.git](https://github.com/yourusername/bottlers-dilemma.git)
3.	Create a Firebase Project:
o	Go to Firebase Console.
o	Create a project (Free "Spark" plan).
4.	Enable Services:
o	Authentication: Enable "Anonymous" sign-in.
o	Firestore Database: Create a database in "Production Mode".
o	Firestore Rules: Update rules to allow authenticated reads/writes:
o	match /rooms/{roomId} {
o	  allow read, write: if request.auth != null;
o	}
5.	Add Keys:
o	Open index.html in a text editor.
o	Set const USE_FIREBASE = true;.
o	Paste your Firebase Config keys in the firebaseConfig object.
6.	Deploy:
o	Drag and drop the file into Netlify Drop or enable GitHub Pages.

# 💸 Cost to Run
$0.00 / month. This project uses the Firebase Spark Plan (Free Tier).
•	Hosting: Free (GitHub Pages/Netlify)
•	Database: Free (up to 50k reads/day)
•	Auth: Free

# 🤝 Contributing
Feel free to fork this project! Ideas for improvement:
•	Add a "Spectator Mode" for the host.
•	Create different difficulty scenarios (e.g., "Budget Cuts" mode).
•	Add a chat feature in the lobby.

# 📄 License
This project is licensed under the MIT License - see the LICENSE file for details.

Original Concept & Design by Madhusudan Chhangani

