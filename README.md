# 🎓 Activités+ | University Club Management System

A comprehensive Flask-based web application for managing extracurricular activities at university institutions, featuring advanced data mining, statistics, and AI-powered database querying.

---

## ✨ Key Features

### 🏛️ Administrative Management (CRUD)
- **Students**: Profile management, departments, and contact information
- **Clubs**: Club creation, membership tracking, and status management
- **Events**: Planning, venue management, and scheduling
- **Sponsors**: Financial contribution tracking and contract management
- **Club Activities**: Meeting/workshop management with Budget and Rating tracking

### 🔍 Search & Data Mining
- **Advanced Search**: Multi-criteria filters (Department, Club, Date)
- **Set Operations**:
  - **Intersection**: Students enrolled in both Club A AND Club B
  - **Union**: Global search across multiple tables
  - **Difference**: Students without clubs or Clubs without activities
- **Relational Audit**: 360° inspection of entity relationships (Spider-web view)

### 🤖 AI Smart Search (Powered by Gemini)
Conversational interface for natural language database queries with text-to-SQL translation.

**Example queries:**
- *"Which Computer Science students were born after 2002?"*
- *"Rank clubs by descending budget"*
- *"Which club has the best average rating?"*

### 📊 Statistics & Rankings
- Real-time KPI dashboard
- Activity ranking by Budget (Gold/Silver/Bronze badges)
- Popularity ranking (Star system ⭐)

---

## 🛠️ Technology Stack

- **Backend**: Python 3.x, Flask
- **Database**: SQLite (Development), SQLAlchemy (ORM)
- **Frontend**: HTML5, Jinja2, CSS3 (Custom + Variables), FontAwesome
- **AI**: Google Generative AI SDK (`google-generativeai`)
- **Design**: Glassmorphism, Gradients (Indigo/Pink/Purple), Responsive

---

## 🚀 Installation & Setup

### 1. Clone the Repository
```bash
git clone https://github.com/your-username/activites-plus.git
cd activites-plus
```

### 2. Create Virtual Environment
```bash
# Windows
python -m venv venv
venv\Scripts\activate

# Mac/Linux
python3 -m venv venv
source venv/bin/activate
```

### 3. Install Dependencies
```bash
pip install -r requirements.txt
```

### 4. Configure AI (Google Gemini)
1. Get a free API key from [Google AI Studio](https://makersuite.google.com/app/apikey)
2. Open `main.py` and modify:
```python
GENAI_API_KEY = "YOUR_API_KEY_HERE"
```

### 5. Initialize Database
The application will automatically create `site.db` (or `database.db`) on first run.

**For existing databases**: To add Budget and Rating columns, run:
```bash
python update_db.py
```

### 6. Launch Application
```bash
python main.py
```
Access via browser: **http://127.0.0.1:5000**

---

## 📂 Project Structure

```
activites-plus/
│
├── static/
│   └── css/
│       ├── admin.css       # Dashboard and table styles
│       ├── clubs.css       # Club-specific styles
│       └── homepage.css    # General styles
│
├── templates/
│   ├── admin_dashboard.html
│   ├── ai_search.html      # AI Smart Search interface
│   ├── recherche.html      # Advanced Search (Filters)
│   ├── classement_budget.html
│   ├── modifierAC.html
│   ├── listeAC.html
│   └── ... (other CRUD templates)
│
├── instance/
│   └── site.db             # SQLite database
│
├── main.py                 # Flask entry point & Routes
├── models.py               # SQLAlchemy models
├── update_db.py            # Migration script (Budget/Rating)
└── requirements.txt        # Dependencies
```

---

## 📦 Dependencies (requirements.txt)

```
Flask==3.0.0
Flask-SQLAlchemy==3.1.1
SQLAlchemy==2.0.23
google-generativeai==0.3.1
werkzeug==3.0.1
```

---

## 📸 Core Modules

### 1. AI Smart Search
Conversational interface that generates secure SQL and displays results dynamically in a modern table.

**Route**: `/admin/smart-search`

### 2. Budget Ranking
Visualization of activities sorted by budget with rank badges (1st, 2nd, 3rd) and intelligent color coding.

**Route**: `/admin/activites/budget`

### 3. Relational Search
Find complex intersections (e.g., Students in club X who are also in club Y) via dynamic forms.

**Route**: `/admin/search`

---

## 🤝 Contributing

Contributions are welcome!

1. Fork the project
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

---

## 📝 License

Distributed under the MIT License.

---

## 🎯 Quick Start Guide

1. **First Launch**: Run the application and navigate to the admin dashboard
2. **Add Data**: Start by creating clubs, then add students and events
3. **Try AI Search**: Visit `/admin/smart-search` to query your database naturally
4. **Explore Analytics**: Check budget rankings and activity statistics
5. **Advanced Features**: Use set operations to find complex relationships

---

## 🔒 Security Notes

- Keep your Gemini API key private and never commit it to version control
- Use environment variables for production deployments
- The AI search sanitizes SQL queries to prevent injection attacks

---

## 📞 Support

For issues or questions, please open an issue on GitHub or contact the development team.

---

**Developed for ENSA Khouribga - Extracurricular Activities Management**

**Built with ❤️ for university communities**