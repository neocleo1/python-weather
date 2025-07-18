# Weather App

A simple Flask web application that displays current weather conditions for any city using the OpenWeatherMap API.

## Features

- Get current weather conditions for any city
- Displays temperature, "feels like" temperature, and weather description
- Clean, responsive web interface
- Error handling for invalid city names
- Defaults to Kansas City if no city is provided

## Technologies Used

- **Python 3.x**
- **Flask** - Web framework
- **Waitress** - WSGI server for production
- **OpenWeatherMap API** - Weather data source
- **HTML/CSS** - Frontend styling

## Setup and Installation

### Prerequisites

- Python 3.x installed
- OpenWeatherMap API key (free at [openweathermap.org](https://openweathermap.org/api))

### Installation Steps

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd weather-app
   ```

2. **Create a virtual environment**
   ```bash
   python -m venv .venv
   ```

3. **Activate the virtual environment**
   - On Windows:
     ```bash
     .venv\Scripts\activate
     ```
   - On macOS/Linux:
     ```bash
     source .venv/bin/activate
     ```

4. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

5. **Set up environment variables**
   - Create a `.env` file in the root directory
   - Add your OpenWeatherMap API key:
     ```
     API_KEY=your_openweathermap_api_key_here
     ```

## Usage

### Running the Application

1. **Start the server**
   ```bash
   python server.py
   ```

2. **Access the application**
   - Open your web browser
   - Navigate to `http://localhost:8000`

3. **Get weather information**
   - Enter a city name in the input field
   - Click "Submit" to view current weather conditions

### Testing the Weather Module

You can also test the weather functionality directly:

```bash
python weather.py
```

This will prompt you to enter a city name and display the raw weather data.

## Project Structure

```
weather-app/
├── .env                    # Environment variables (not tracked)
├── .gitignore             # Git ignore file
├── requirements.txt       # Python dependencies
├── server.py             # Main Flask application
├── weather.py            # Weather API functionality
├── static/
│   └── styles/
│       └── style.css     # CSS styling
└── templates/
    ├── index.html        # Home page
    ├── weather.html      # Weather results page
    └── city-not-found.html # Error page
```

## API Information

This application uses the OpenWeatherMap Current Weather Data API:
- **Endpoint**: `http://api.openweathermap.org/data/2.5/weather`
- **Units**: Imperial (Fahrenheit)
- **Rate Limit**: 60 calls/minute, 1,000,000 calls/month (free tier)

## Error Handling

- Invalid or non-existent cities display a "City Not Found" page
- Empty input defaults to Kansas City
- Network errors are handled gracefully

## Troubleshooting

**Common Issues:**

- **"City Not Found" error**: Ensure the city name is spelled correctly and exists in the OpenWeatherMap database
- **API errors**: Check that your API key is valid and not expired
- **Connection errors**: Verify your internet connection and API endpoint availability

**Getting Help:**

If you encounter issues, please check:
1. Your API key is correctly set in the `.env` file
2. All dependencies are installed
3. The virtual environment is activated
4. Your internet connection is stable
