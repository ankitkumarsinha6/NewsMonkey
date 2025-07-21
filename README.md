NewsMonkey: Your Daily Dose of News!
📝 Description
NewsMonkey is a dynamic web application built with React.js (Class-Based Components) that provides users with a quick and easy way to browse daily news headlines across various categories. Leveraging the News API, it fetches and displays up-to-date articles, offering a smooth user experience with features like:

Categorized News: Explore headlines across Business, Entertainment, General, Health, Science, Sports, and Technology.

Infinite Scrolling: Efficiently load more news articles as you scroll down, providing a seamless Browse experience.

Top Loading Bar: A visual indicator (using react-top-loading-bar) to show data fetching progress, enhancing user feedback.

Responsive Design: Built with Bootstrap 5 for a mobile-first, responsive layout that looks great on any device.

This project was developed as an exercise to deepen understanding of React's class-based components, lifecycle methods, state management, props, and routing.

📸 Screenshot
![NewsMonkey App Screenshot](public/screenshots/firsthomepage.png)

🚀 Technologies Used
React.js (Class-Based Components): Core JavaScript library for building the user interface.

React Router DOM: For handling client-side routing and navigation between news categories.

News API: The external REST API used to fetch news articles.

Bootstrap 5: CSS framework for styling and responsive layout.

react-top-loading-bar: A React component for displaying a progress bar at the top of the page.

react-infinite-scroll-component: A component for easily implementing infinite scrolling.

prop-types: For runtime type checking of props (development only).

🛠️ Installation and Setup
To get a local copy up and running, follow these simple steps.

Prerequisites:

Node.js (LTS version recommended)

npm (comes with Node.js) or Yarn

1. Clone the repository:

Bash

git clone [(https://github.com/ankitkumarsinha6/NewsMonkey.git)]
cd NewsMonkey
2. Install dependencies:

Bash

npm install
# OR
yarn install
3. Obtain a News API Key:

Go to https://newsapi.org/register and sign up for a free API key.

Important: For security and flexibility, it's recommended to use environment variables for your API key.

Create a file named .env.local in the root of your project (same level as package.json).

Add your API key to this file:

REACT_APP_NEWS_API_KEY=YOUR_ACTUAL_NEWS_API_KEY_HERE
(Replace YOUR_ACTUAL_NEWS_API_KEY_HERE with the key you obtained).

Then, in your src/components/News.js file, replace your hardcoded API key (6252ed4b02e84bebbfd10c72467cf520) with:

JavaScript

const url = `https://newsapi.org/v2/top-headlines?country=${this.props.country}&category=${this.props.category}&apiKey=${process.env.REACT_APP_NEWS_API_KEY}&page=${this.state.page}&pageSize=${this.props.pageSize}`;
(Do this for both updateNews and fetchMoreData methods).

4. Run the development server:

Bash

npm start
# OR
yarn start
This will open the application in your browser at http://localhost:3000.

📦 Project Structure
NewsMonkey/
├── public/                 # Public assets (index.html, favicon, etc.)
│   └── assets/             # Recommended folder for images/screenshots within public
│       └── screenshot.png  # Your project screenshot
├── src/
│   ├── components/
│   │   ├── NavBar.js       # Navigation bar component
│   │   ├── News.js         # Main component for fetching and displaying news
│   │   ├── NewsItem.js     # Individual news card component
│   │   ├── Spinner.js      # Loading spinner component
│   │   └── loading.gif     # Loading animation GIF
│   ├── App.css             # Styling for the App component
│   ├── App.js              # Main application component (routing, loading bar)
│   ├── index.css           # Global styling
│   ├── index.js            # React app entry point
│   └── reportWebVitals.js  # Web Vitals reporting (optional)
├── .env.local              # Environment variables (e.g., REACT_APP_NEWS_API_KEY)
├── .gitignore              # Specifies intentionally untracked files to ignore
├── package.json            # Project dependencies and scripts
└── README.md               # This file
🤝 Contributing
Contributions are what make the open-source community such an amazing place to learn, inspire, and create. Any contributions you make are greatly appreciated.

If you have a suggestion that would make this better, please fork the repo and create a pull request. Don't forget to give the project a star!

Fork the Project

Create your Feature Branch (git checkout -b feature/AmazingFeature)

Commit your Changes (git commit -m 'Add some AmazingFeature')

Push to the Branch (git push origin feature/AmazingFeature)

Open a Pull Request

📄 License
Distributed under the MIT License. See LICENSE for more information. (You might want to create a LICENSE file in your root directory if you don't have one).

📧 Contact
Ankit Kumar Sinha - ankitkumarsinha6@gmail.com
Project Link: (https://github.com/ankitkumarsinha6/NewsMonkey.git)

