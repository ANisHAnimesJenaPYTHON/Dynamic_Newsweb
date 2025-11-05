# News Website

A modern, responsive news website that fetches and displays news articles from various categories using the NewsAPI. Built with vanilla HTML, CSS, and JavaScript.

## Features

- 📰 Real-time news articles from NewsAPI
- 🔍 Search functionality for custom news queries
- 📱 Responsive design for all devices
- 🎨 Modern and clean UI/UX
- 🏷️ Category filtering (Cricket, India, Technology, Politics)
- 🖼️ Image-rich article cards
- 🔗 Direct links to full articles

## Project Structure

```
NewsWebsite/
├── images/
│   ├── logo.png
│   └── NewsWebsite.png
├── index.html          # Main HTML structure
├── styles.css          # Styling and responsive design
├── script.js           # JavaScript functionality and API integration
├── Dockerfile          # Docker configuration
├── .dockerignore       # Docker ignore file
└── README.md           # Project documentation
```

## Technologies Used

- **HTML5** - Structure and semantic markup
- **CSS3** - Styling with modern CSS features (Flexbox, CSS Variables)
- **JavaScript (ES6+)** - Fetch API, async/await, DOM manipulation
- **NewsAPI** - News data source
- **Nginx** - Web server (Docker container)

## Prerequisites

- Docker and Docker Engine installed
- Git (for version control)
- NewsAPI key (optional - one is already included in the code)

## Docker Setup & Usage

### Build the Docker Image

```bash
docker build -t news-website .
```

### Run the Container

```bash
docker run -d -p 8080:80 --name news-app news-website
```

The website will be accessible at: `http://localhost:8080`

### View Running Container

```bash
docker ps
```

### Stop the Container

```bash
docker stop news-app
```

### Remove the Container

```bash
docker rm news-app
```

### View Container Logs

```bash
docker logs news-app
```

## Local Development (Without Docker)

1. Clone the repository:
```bash
git clone <repository-url>
cd NewsWebsite
```

2. Open `index.html` in your web browser or use a local server:

```bash
# Using Python
python -m http.server 8000

# Using Node.js (http-server)
npx http-server -p 8000
```

3. Access the website at `http://localhost:8000`

## API Configuration

The project uses NewsAPI to fetch news articles. The API key is currently hardcoded in `script.js`. 

**Important:** For production use, consider:
- Moving the API key to environment variables
- Using a backend proxy to hide the API key
- Implementing rate limiting

### Update API Key

Edit `script.js` and replace the `API_KEY` constant:

```javascript
const API_KEY = "your-api-key-here";
```

Get your free API key from: [NewsAPI.org](https://newsapi.org/)

## Features Breakdown

### Navigation
- Fixed navigation bar with logo
- Category buttons (Cricket, India, Technology, Politics)
- Search bar for custom queries

### News Cards
- Responsive card layout
- Article images
- Title, description, and source information
- Click to open full article in new tab
- Hover effects for better UX

### Search Functionality
- Real-time news search
- Custom query support
- Clears active category selection

## Browser Support

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)

## Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## License

This project is open source and available under the MIT License.

## Author

News Website Project

## Acknowledgments

- [NewsAPI](https://newsapi.org/) for providing the news data
- [Poppins Font](https://fonts.google.com/specimen/Poppins) for typography

