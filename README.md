# 🤖 AI Kurs-Assistent

Ein intelligenter ChatBot für den AI Development Kurs, der Fragen zu Kursinhalten beantwortet.

## 🚀 Features

- **Dual-API Support**: OpenAI (ChatGPT) und Anthropic (Claude)
- **Kurs-spezifisches Wissen**: Optimiert für AI Development Kurs-Inhalte
- **Streamlit Web-Interface**: Benutzerfreundliche Chat-Oberfläche
- **Responsive Design**: Funktioniert auf Desktop und Mobile

## 📋 Voraussetzungen

- Python 3.13+
- OpenAI API-Schlüssel ODER Anthropic API-Schlüssel

## ⚙️ Setup

### 1. Repository klonen
```bash
git clone <repository-url>
cd ai-course-assistant
```

### 2. Dependencies installieren
```bash
# Mit uv (empfohlen)
uv sync

# Oder mit pip
pip install -r requirements.txt
```

### 3. API-Schlüssel konfigurieren

#### Option A: .env Datei (für lokale Entwicklung)
```bash
# Beispiel-Datei kopieren
cp .env.example .env

# .env bearbeiten und echte API-Schlüssel einfügen
nano .env
```

#### Option B: Streamlit Secrets (für Deployment)
```bash
# Beispiel-Datei kopieren
cp .streamlit/secrets.toml.example .streamlit/secrets.toml

# secrets.toml bearbeiten und echte API-Schlüssel einfügen
nano .streamlit/secrets.toml
```

### 4. App starten
```bash
streamlit run app.py
```

Die App ist dann verfügbar unter: http://localhost:8501

## 🔑 API-Schlüssel erhalten

### OpenAI API-Schlüssel
1. Gehen Sie zu https://platform.openai.com/api-keys
2. Erstellen Sie einen neuen API-Schlüssel
3. Kopieren Sie den Schlüssel (beginnt mit `sk-`)

### Anthropic API-Schlüssel
1. Gehen Sie zu https://console.anthropic.com/
2. Erstellen Sie einen neuen API-Schlüssel
3. Kopieren Sie den Schlüssel (beginnt mit `sk-ant-api03-`)

## 🌐 Deployment auf Streamlit Cloud

1. Pushen Sie Ihr Repository zu GitHub
2. Gehen Sie zu https://share.streamlit.io/
3. Verbinden Sie Ihr GitHub Repository
4. Fügen Sie API-Schlüssel in den App-Einstellungen hinzu:
   - `OPENAI_API_KEY`: Ihr OpenAI Schlüssel
   - `ANTHROPIC_API_KEY`: Ihr Anthropic Schlüssel

## 📁 Projektstruktur

```
ai-course-assistant/
├── app.py                          # Hauptanwendung
├── course_knowledge.py             # Kurs-Wissensbasis
├── .env.example                    # Beispiel Environment Variables
├── .streamlit/
│   └── secrets.toml.example        # Beispiel Streamlit Secrets
├── pyproject.toml                  # Python Dependencies
└── README.md                       # Diese Datei
```

## 🛠️ Entwicklung

### Lokale Entwicklung
```bash
# App mit Auto-Reload starten
streamlit run app.py

# Auf anderem Port
streamlit run app.py --server.port 8502
```

### Code-Struktur
- `app.py`: Streamlit UI und API-Integration
- `course_knowledge.py`: Kurs-spezifische Wissensbasis und System-Prompts

## 🔒 Sicherheit

- **Niemals echte API-Schlüssel in Git committen!**
- `.env` und `.streamlit/secrets.toml` sind in `.gitignore`
- Nur `.example` Dateien werden versioniert

## 📚 Verwendung

1. Starten Sie die App
2. Wählen Sie ein Thema in der Sidebar
3. Stellen Sie Ihre Frage im Chat
4. Der AI-Assistent antwortet basierend auf Kursinhalten

## 🤝 Beitragen

1. Fork das Repository
2. Erstellen Sie einen Feature-Branch
3. Committen Sie Ihre Änderungen
4. Erstellen Sie einen Pull Request

## 📄 Lizenz

Dieses Projekt ist für Bildungszwecke im Rahmen des AI Development Kurses erstellt.