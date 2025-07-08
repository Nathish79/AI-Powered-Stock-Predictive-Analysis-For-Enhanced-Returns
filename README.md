# AI-Powered-Stock-Predictive-Analysis-For-Enhanced-Returns
Rocket Money: AI-driven platform for intelligent stock analysis &amp; portfolio management. Empowers investors with a ranking algorithm, real-time news, AI insights, comprehensive backtesting, and automated PDF reports. Built with React, Node.js, and Supabase. Transforms data into confident investment decisions.
# Market Pulse

**Quickstart:**
1. Run the backend (see Backend Service section below, default port: 5000).
2. Run the frontend with `npm run dev` in the main folder (default port: 5173).

**Note:** This project now includes both a frontend (React) and a backend (Node.js/Express) for full functionality. Please run both parts as described below.

A modern web application built with React and TypeScript for tracking and analyzing market trends.

## Prerequisites

Before you begin, ensure you have the following installed:
- Node.js (v14 or higher)
- npm (comes with Node.js)

## Installation

Follow these steps to get the project running:

```sh
# Step 1: Clone the repository
git clone https://github.com/yourusername/market-pulse.git

# Step 2: Navigate to the project directory
cd market-pulse

# Step 3: Install the necessary dependencies
npm i

# Step 4: Start the development server with auto-reloading and an instant preview
npm run dev
```

The application will be available at `http://localhost:5173` by default.

## Technologies Used

This project is built with:

- [Vite](https://vitejs.dev/) - Next Generation Frontend Tooling
- [TypeScript](https://www.typescriptlang.org/) - JavaScript with syntax for types
- [React](https://reactjs.org/) - A JavaScript library for building user interfaces
- [shadcn-ui](https://ui.shadcn.com/) - Re-usable components built with Radix UI and Tailwind CSS
- [Tailwind CSS](https://tailwindcss.com/) - A utility-first CSS framework

## Project Structure

```
market-pulse/
├── src/              # Source files
├── public/           # Static files
├── components/       # React components
├── styles/          # CSS and styling files
└── ...
```

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Backend Service (NewsAPI & Sentiment Analysis)

A simple Node.js/Express backend is used to fetch stock-related news from NewsAPI and perform sentiment analysis. (Uses Express and a basic sentiment analysis for demonstration.)

### Setup

1. Navigate to the backend folder:
   ```sh
   cd backend
   ```
2. Install dependencies:
   ```sh
   npm install
   ```
3. Create a `.env` file with your NewsAPI key:
   ```env
   NEWS_API_KEY=your_newsapi_key_here
   # Replace 'your_newsapi_key_here' with your actual NewsAPI key
   ```
4. Start the backend server:
   ```sh
   node index.js
   ```

The backend will run on `http://localhost:5000` by default.

You can use the provided NewsAPI key for testing, but use your own for production.

## Market Sentiment Page

A new page (`/market-sentiment`) displays live market sentiment using news data and sentiment analysis from the backend. It features:
- Sentiment summary (positive/neutral/negative)
- List of recent news articles
- Visual sentiment chart

This page fetches data from the backend service for live updates.

Navigate to this page from the main menu to view real-time market sentiment analysis.

## Future Improvements
- Advanced sentiment analysis using AI/ML models
- Integration with GroqAPI for detailed market reports
- Email report feature using MailJS API

## Troubleshooting
- If the backend cannot access NewsAPI, check your API key in the .env file.
- If the frontend cannot fetch data, ensure the backend is running on the correct port (default: 5000).
- For CORS issues, make sure the backend allows requests from the frontend's origin.

## Backend API Endpoints
- `GET /api/market-sentiment`: Fetches latest stock-related news and sentiment analysis.

_More endpoints will be added for GroqAPI and MailJS integration in the future._
