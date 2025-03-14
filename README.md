# Disaster Management System

A comprehensive web application for managing and tracking disasters, safe zones, and weather alerts. Built with Flask and Streamlit.

## Features

- 📝 Report and track disasters with location mapping
- 📊 View active disasters and disaster history
- 🏥 Find nearby safe zones (hospitals and shelters)
- 🌤️ Real-time weather alerts
- 🗺️ Interactive mapping with OpenStreetMap
- 🔄 Auto-refresh capabilities for real-time updates

## Prerequisites

1. **Python Installation**
   - Download Python 3.8 or higher from [python.org](https://www.python.org/downloads/)
   - During installation, make sure to check "Add Python to PATH"
   - Verify installation by opening a terminal/command prompt and running:
     ```bash
     python --version
     ```

2. **Git Installation** (Optional, for cloning the repository)
   - Download Git from [git-scm.com](https://git-scm.com/downloads)
   - Follow the installation wizard

## Project Setup

1. **Clone the Repository** (if using Git)
   ```bash
   git clone <repository-url>
   cd disaster-management-system
   ```

   OR

   **Download the Project**
   - Download the project files as a ZIP
   - Extract the ZIP file to your desired location
   - Open a terminal/command prompt in the project directory

2. **Create a Virtual Environment**
   ```bash
   # Windows
   python -m venv venv
   venv\Scripts\activate

   # Linux/Mac
   python3 -m venv venv
   source venv/bin/activate
   ```

3. **Install Dependencies**
   ```bash
   pip install -r requirements.txt
   ```

4. **Environment Variables**
   - Create a `.env` file in the project root directory
   - Add the following variables:
     ```
     SECRET_KEY=your_secret_key_here
     GOMAPS_API_KEY=your_gomaps_api_key_here
     ```

## Project Structure

```
disaster-management-system/
├── app/
│   ├── __init__.py
│   ├── config.py
│   ├── models/
│   │   ├── disaster.py
│   │   └── safe_place.py
│   ├── routes/
│   │   ├── disasters.py
│   │   ├── alerts.py
│   │   └── safe_places.py
│   └── services/
│       └── maps.py
├── data/
├── venv/
├── .env
├── .env.example
├── requirements.txt
├── run.py
└── frontend.py
```

## Running the Application

1. **Start the Backend Server**
   ```bash
   # Make sure your virtual environment is activated
   python run.py
   ```
   The backend server will start on `http://localhost:5000`

2. **Start the Frontend Application**
   ```bash
   # Open a new terminal/command prompt
   # Make sure your virtual environment is activated
   streamlit run frontend.py
   ```
   The frontend will open in your default web browser at `http://localhost:8501`

## Using the Application

1. **Report a Disaster**
   - Click "📝 Report Disaster" in the menu
   - Fill in the disaster details
   - Submit the form

2. **View Disasters**
   - Click "📊 View Disasters" to see active disasters
   - Click "📜 Disaster History" to see all disasters
   - Use filters in the sidebar to filter disasters

3. **Find Safe Zones**
   - Click "🏥 Safe Zones" in the menu
   - Enter your location
   - Adjust the search radius
   - Click "Find Safe Zones"

4. **Weather Alerts**
   - Click "🌤️ Weather Alerts" in the menu
   - Enter a location
   - Enable real-time updates if needed

## Troubleshooting

1. **Backend Connection Issues**
   - Ensure the backend server is running (`python run.py`)
   - Check if port 5000 is available
   - Verify your `.env` file is properly configured

2. **Frontend Issues**
   - Make sure Streamlit is installed (`pip install streamlit`)
   - Check if port 8501 is available
   - Try clearing your browser cache

3. **Database Issues**
   - Ensure the `data` directory exists
   - Check if you have write permissions in the project directory
   - Try deleting the database file and restarting the application

4. **Map Display Issues**
   - Check your internet connection
   - Ensure your browser allows JavaScript
   - Try using a different browser

## Contributing

1. Fork the repository
2. Create a feature branch
3. Commit your changes
4. Push to the branch
5. Create a Pull Request

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Support

For support, please open an issue in the repository or contact the maintainers.

## Acknowledgments

- OpenStreetMap for providing free mapping services
- Flask and Streamlit communities for their excellent frameworks
- All contributors who have helped improve this project 
