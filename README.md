Web Clock Application
🕒 Project Overview

Web Clock is a modern, real-time digital clock application built with JavaScript that displays both current time and date. The application features a clean, responsive design and updates in real-time every second.
✨ Features

    🕐 Real-time clock - Updates every second automatically

    📅 Date display - Shows current date in readable format

    🌍 Localized format - Uses Indonesian locale for date/time formatting

    🎨 Responsive design - Clean, modern interface with flexbox layout

    ⚡ Live development - Hot reload with webpack-dev-server

🛠️ Technology Stack
Frontend

    HTML5 - Semantic markup

    CSS3 with Flexbox - Modern styling and layout

    JavaScript ES6+ - Application logic

    jQuery - DOM manipulation

    Moment.js - Advanced date/time handling

Build Tools

    Webpack 4 - Module bundler and build tool

    Babel - JavaScript transpilation (ES6+ → ES5)

    Webpack Dev Server - Development environment

    CSS Loader & Style Loader - CSS module handling

    HTML Webpack Plugin - HTML template processing

📁 Project Structure
--

WEBCLOCK/

├── dist/   
                 # Production build files
│   ├── bundle.js           # Bundled JavaScript

│   └── index.html          # Generated HTML file

├── node_modules/           # Dependencies (excluded from Git)

├── src/                    # Source code

│   ├── css style/         # CSS styles (note: folder has space)

│   │   └── style.css      # Main stylesheet

│   ├── index.js           # Main application entry point

│   └── template.html      # HTML template

├── package.json            # Project dependencies and scripts

├── package-lock.json       # Exact dependency versions

├── README.md               # Documentation (this file)

├── webpack.common.js       # Shared webpack configuration

├── webpack.dev.js          # Development configuration

└── webpack.prod.js         # Production configuration

🚀 Getting Started
Prerequisites

    Node.js (version 12 or higher)

    npm (Node Package Manager)

Installation

    Clone the repository
    bash

    git clone https://github.com/yourusername/web-clock.git
    cd web-clock

    Install dependencies
    bash

    npm install

Development Mode

Run the development server with hot reload:
bash

npm run start-dev

The application will open automatically at http://localhost:8080
Production Build

Create an optimized production build:
bash

npm run build

The built files will be available in the dist/ directory.
📦 Dependencies
Production Dependencies

    jquery (^3.4.1) - DOM manipulation library

    moment (^2.24.0) - Date and time formatting library

Development Dependencies

    @babel/core & @babel/preset-env - JavaScript transpilation

    babel-loader - Webpack loader for Babel

    css-loader & style-loader - CSS module handling

    html-webpack-plugin - HTML template processing

    webpack & webpack-cli - Build tool and CLI

    webpack-dev-server - Development server

    webpack-merge - Webpack configuration merging

🔧 Webpack Configuration

The project uses three webpack configuration files:
webpack.common.js

    Entry point: ./src/index.js

    Output: dist/bundle.js

    CSS loader configuration

    HTML template processing

webpack.dev.js

    Development mode configuration

    Merged with common configuration

webpack.prod.js

    Production mode configuration

    Babel loader for ES6+ transpilation

    Optimized builds

🎨 Styling

The application uses a clean, minimal design:

    Main clock container: Blue background with white text

    Time display: Large 64px font size

    Date display: Smaller 24px font size

    Flexbox layout: Centered content with column direction

    Responsive design: Fixed width container (400px)

📝 Code Explanation
Main Application Logic (src/index.js)
javascript

import './style/style.css';   // Import CSS
import $ from 'jquery';       // Import jQuery
import moment from 'moment';  // Import Moment.js

const displayTime = () => {
  moment.locale('id');  // Set to Indonesian locale
  $('.time').text(moment().format('LTS'));  // Format: HH:mm:ss
  $('.date').text(moment().format('LL'));   // Format: Full date
};

const updateTime = () => {
  displayTime();
  setTimeout(updateTime, 1000);  // Update every second
};

updateTime();  // Start the clock

Styles (src/css style/style.css)

    Uses flexbox for vertical centering

    Blue color scheme (#0000FF)

    Sans-serif font family

    Responsive padding and margins

🤝 Contributing

    Fork the repository

    Create a feature branch (git checkout -b feature/AmazingFeature)

    Commit your changes (git commit -m 'Add some AmazingFeature')

    Push to the branch (git push origin feature/AmazingFeature)

    Open a Pull Request

📄 License

This project is licensed under the ISC License.
🙏 Acknowledgments

    Moment.js for comprehensive date/time manipulation

    jQuery for simplified DOM operations

    Webpack for powerful module bundling

    Babel for JavaScript compatibility

🔍 Troubleshooting
Common Issues:

    Port 8080 already in use
    bash

    # Kill process on port 8080
    sudo lsof -ti:8080 | xargs kill -9

    Node modules not installing
    bash

    # Clear npm cache and reinstall
    npm cache clean --force
    rm -rf node_modules package-lock.json
    npm install

    Webpack build errors
    bash

    # Update webpack and related packages
    npm update webpack webpack-cli webpack-dev-server

Browser Compatibility:

    Chrome 50+

    Firefox 45+

    Safari 10+

    Edge 15+

📈 Future Enhancements

Potential features for future development:

    Multiple timezone support

    Theme switching (light/dark mode)

    Alarm functionality

    Stopwatch and timer features

    Analog clock display option

    Weather integration