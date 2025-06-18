import React from "react";
import { BrowserRouter, Routes, Route } from "react-router-dom";
import Dashboard from "./pages/Dashboard";
import Login from "./pages/Login";

function App() {
  return (
    <BrowserRouter>
      <Routes>
        <Route path="/" element={<Login />} />
        <Route path="/dashboard" element={<Dashboard />} />
      </Routes>
    </BrowserRouter>
  );
}

export default App;


import React, { useState } from "react";
import { useNavigate } from "react-router-dom";

export default function Login() {
  const [username, setUser] = useState("");
  const [password, setPass] = useState("");
  const navigate = useNavigate();

  const handleLogin = () => {
    if (username === "admin" && password === "masterkey123") {
      navigate("/dashboard");
    } else {
      alert("Invalid credentials");
    }
  };

  return (
    <div className="flex flex-col items-center justify-center h-screen bg-gray-900 text-white">
      <h1 className="text-3xl mb-4">Login to AI Toolbox</h1>
      <input type="text" placeholder="Username" onChange={e => setUser(e.target.value)} className="mb-2 p-2 rounded" />
      <input type="password" placeholder="Password" onChange={e => setPass(e.target.value)} className="mb-4 p-2 rounded" />
      <button onClick={handleLogin} className="bg-blue-500 px-4 py-2 rounded">Login</button>
    </div>
  );
import React, { useState } from "react";
import { useNavigate } from "react-router-dom";

export default function Login() {
  const [username, setUser] = useState("");
  const [password, setPass] = useState("");
  const navigate = useNavigate();

  const handleLogin = () => {
    if (username === "admin" && password === "masterkey123") {
      navigate("/dashboard");
    } else {
      alert("Invalid credentials");
    }
  };

  return (
    <div className="flex flex-col items-center justify-center h-screen bg-gray-900 text-white">
      <h1 className="text-3xl mb-4">Login to AI Toolbox</h1>
      <input type="text" placeholder="Username" onChange={e => setUser(e.target.value)} className="mb-2 p-2 rounded" />
      <input type="password" placeholder="Password" onChange={e => setPass(e.target.value)} className="mb-4 p-2 rounded" />
      <button onClick={handleLogin} className="bg-blue-500 px-4 py-2 rounded">Login</button>
    </div>
  );



