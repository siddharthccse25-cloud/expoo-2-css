# expoo-2-css
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: 'Segoe UI', sans-serif;
}

body {
    background: #0f172a;
    color: #fff;
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
}

.container {
    width: 90%;
    max-width: 900px;
    background: #1e293b;
    border-radius: 12px;
    padding: 20px;
    box-shadow: 0 0 20px rgba(0,0,0,0.5);
}

h2 {
    margin-bottom: 15px;
}

/* Tabs */
.tabs {
    display: flex;
    border-bottom: 2px solid #334155;
}

.tab {
    padding: 10px 20px;
    cursor: pointer;
    transition: 0.3s;
}

.tab.active {
    border-bottom: 3px solid #38bdf8;
    color: #38bdf8;
}

/* Content */
.tab-content {
    display: none;
    margin-top: 20px;
    animation: fade 0.3s ease-in-out;
}

.tab-content.active {
    display: block;
}

@keyframes fade {
    from { opacity: 0; transform: translateY(10px); }
    to { opacity: 1; transform: translateY(0); }
}

/* Form */
.form-group {
    margin-bottom: 15px;
}

label {
    display: block;
    margin-bottom: 5px;
}

input, select {
    width: 100%;
    padding: 10px;
    border-radius: 6px;
    border: none;
    background: #334155;
    color: white;
}

/* Toggle */
.toggle {
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin-bottom: 10px;
}

.switch {
    position: relative;
    width: 50px;
    height: 25px;
}

.switch input {
    display: none;
}

.slider {
    position: absolute;
    background: #555;
    border-radius: 25px;
    width: 100%;
    height: 100%;
    cursor: pointer;
}

.slider::before {
    content: "";
    position: absolute;
    width: 20px;
    height: 20px;
    background: white;
    border-radius: 50%;
    top: 2.5px;
    left: 3px;
    transition: 0.3s;
}

input:checked + .slider {
    background: #38bdf8;
}

input:checked + .slider::before {
    transform: translateX(24px);
}

/* Button */
button {
    margin-top: 10px;
    padding: 10px 20px;
    background: #38bdf8;
    border: none;
    border-radius: 6px;
    cursor: pointer;
    color: #659bec;
    font-weight: bold;
}

button:hover {
    background: #0ea5e9;
}
