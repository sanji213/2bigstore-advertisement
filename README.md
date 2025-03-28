// src/components/Header.js
import React from 'react';
import { Link } from 'react-router-dom';

const Header = () => {
  return (
    <nav className="bg-blue-600 p-4 text-white">
      <ul className="flex space-x-6">
        <li><Link to="/">Home</Link></li>
        <li><Link to="/about">About</Link></li>
      </ul>
    </nav>
  );
};

export default Header;

// src/components/Home.js
import React from 'react';

const Home = () => {
  return (
    <div className="p-8">
      <h1 className="text-4xl font-bold">Welcome to 2BIG Store!</h1>
      <img src="/banner.jpg" alt="2BIG Store Banner" className="mt-4" />
      <p className="mt-4">Providing clean, refreshing water with a commitment to sustainability and quality.</p>
    </div>
  );
};

export default Home;

// src/components/About.js
import React from 'react';

const About = () => {
  return (
    <div className="p-8">
      <h1 className="text-4xl font-bold">About 2BIG Store</h1>
      <img src="/tta1.png" alt="About 2BIG Store" className="mt-4" />
      <p className="mt-4">2BIG Store offers premium purified water with an eco-friendly mission. Our water goes through multiple stages of filtration to ensure the highest quality for our community.</p>
    </div>
  );
};

export default About;

// src/App.js
import React from 'react';
import { BrowserRouter as Router, Routes, Route } from 'react-router-dom';
import Header from './components/Header';
import Home from './components/Home';
import About from './components/About';

const App = () => {
  return (
    <Router>
      <Header />
      <Routes>
        <Route path="/" element={<Home />} />
        <Route path="/about" element={<About />} />
      </Routes>
    </Router>
  );
};

export default App;
