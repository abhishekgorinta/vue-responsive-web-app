# vue-Api callings and responsive 

A modern, responsive website built with Vue 3 and Vite. This project showcases a professional web application with a navigation bar, image carousel, user directory, and contact form.

## 📋 Table of Contents

- [Features](#features)
- [Tech Stack](#tech-stack)
- [Project Structure](#project-structure)
- [Installation](#installation)
- [Running the Project](#running-the-project)
- [Available Scripts](#available-scripts)
- [Components](#components)
- [Browser Support](#browser-support)

## ✨ Features

### 1. **Responsive Navigation Bar**
   - Fixed header with logo and navigation links
   - Smooth scroll navigation with anchor links
   - Mobile hamburger menu for responsive design
   - Animated transitions and hover effects

### 2. **Image Carousel**
   - Auto-playing image carousel powered by Bootstrap
   - Navigation controls (Previous/Next buttons)
   - Responsive image display with responsive padding

### 3. **User Directory**
   - Fetches 10 random users from the [RandomUser API](https://randomuser.me/)
   - Displays users in a responsive card grid layout
   - Shows user avatar, name, and email
   - Hover effects with smooth animations

### 4. **Contact Form**
   - Custom contact form with validation
   - Real-time form validation with error highlighting
   - Bootstrap Toast notification on successful submission
   - Responsive form design
   - Fields: Name, Email, Message

### 5. **Footer**
   - Dark professional footer
   - Copyright information
   - Social media links (Facebook, Twitter, LinkedIn, Instagram)
   - Responsive design with proper spacing

## 🛠 Tech Stack

- **Frontend Framework:** [Vue 3](https://vuejs.org/) - Progressive JavaScript framework
- **Build Tool:** [Vite](https://vitejs.dev/) - Next generation frontend tooling
- **CSS Framework:** [Bootstrap 5](https://getbootstrap.com/) - CSS utility framework
- **Icons:** [Font Awesome 6](https://fontawesome.com/) - Icon library
- **HTTP Client:** [Axios](https://axios-http.com/) - Promise-based HTTP client
- **Language:** JavaScript (ES6+)
- **Styling:** CSS3 with responsive design

## 📁 Project Structure

```
week-9/
├── index.html              # Main HTML entry point
├── package.json            # Project dependencies and scripts
├── vite.config.js          # Vite configuration
├── README.md               # This file
├── public/                 # Static assets
├── src/
│   ├── main.js            # Vue app entry point
│   ├── App.vue            # Root component
│   ├── style.css          # Global styles
│   ├── assets/            # Images and other assets
│   │   ├── img1.jpg
│   │   ├── img2.jpg
│   │   ├── img3.jpg
│   │   └── logo.png
│   └── components/        # Vue components
│       ├── navbar.vue     # Navigation bar component
│       ├── carousel.vue   # Image carousel component
│       ├── users.vue      # User directory component
│       ├── form.vue       # Contact form component
│       └── footer.vue     # Footer component
```

## 🚀 Installation

### Prerequisites
- [Node.js](https://nodejs.org/) (v14 or higher)
- npm or yarn package manager

### Steps

1. **Clone the repository** (or navigate to the project directory)
   ```bash
   cd week-9
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

## 🎯 Running the Project

### Development Server
Start the development server with hot module replacement:

```bash
npm run dev
```

The application will be available at `http://localhost:5173` (or the next available port).


## 🧩 Components

### navbar.vue
- **Purpose:** Responsive navigation header
- **Features:** 
  - Fixed positioning
  - Mobile hamburger menu
  - Smooth navigation links with anchor scrolling
  - Logo display
- **Dependencies:** Vue Composition API, Font Awesome

### carousel.vue
- **Purpose:** Display rotating images
- **Features:**
  - Bootstrap carousel implementation
  - Auto-play functionality
  - Previous/Next navigation buttons
  - Responsive image sizing
- **Dependencies:** Bootstrap 5

### users.vue
- **Purpose:** Display random user profiles
- **Features:**
  - Fetches data from RandomUser API on component mount
  - Displays 10 users in a responsive grid
  - User cards with avatar, name, and email
  - Responsive grid layout (auto-fit columns)
- **Dependencies:** Vue Composition API, Fetch API

### form.vue
- **Purpose:** Contact form for user inquiries
- **Features:**
  - Form validation for all fields
  - Error state highlighting
  - Toast notification on successful submission
  - Form reset after submission
  - Bootstrap integration
- **Dependencies:** Vue Composition API, Bootstrap 5

### footer.vue
- **Purpose:** Application footer
- **Features:**
  - Copyright information
  - Social media links
  - Dark theme design
  - Responsive layout
- **Dependencies:** Font Awesome

## 🌐 Browser Support

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)

## 👨‍💻 Author:
Developed by Abhishek Gorinta

## 📝 License

This project is free to use and modify for learning purposes.

⭐ If you like this project, don't forget to give it a star on GitHub!




