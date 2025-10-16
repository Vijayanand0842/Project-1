import React from "react";
import { BrowserRouter as Router, Routes, Route, Link } from "react-router-dom";
import Home from "./Home";
import Courses from "./Courses";
import Contact from "./Contact";

function App() {
  return (
    <Router>
      <div>
        {/* Navigation Bar */}
        <nav style={{ background: "#333", padding: "10px" }}>
          <Link to="/" style={{ color: "#fff", marginRight: "15px" }}>Home</Link>
          <Link to="/courses" style={{ color: "#fff", marginRight: "15px" }}>Courses</Link>
          <Link to="/contact" style={{ color: "#fff" }}>Contact</Link>
        </nav>

        {/* Routes */}
        <Routes>
          <Route path="/" element={<Home />} />
          <Route path="/courses" element={<Courses />} />
          <Route path="/contact" element={<Contact />} />
        </Routes>
      </div>
    </Router>
  );
}

export default App;
