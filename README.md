### 🌍 Global Currency Converter (HTML + Tailwind CSS + JavaScript)
---
A modern, responsive Global Currency Converter web application that converts currencies in real time using live exchange rates from a public API.
Built using HTML, Tailwind CSS, and JavaScript, with a clean glass-morphism UI and smooth user experience.

---
### 🚀 Features<br>
🌐 Real-time currency conversion<br>
💱 Supports multiple global currencies (INR, USD, EUR, GBP, JPY, AUD, CAD, CNY)<br>
🎨 Modern glass-morphism UI using Tailwind CSS<br>
⏳ Loading spinner while fetching live exchange rates<br>
❌ Error handling for invalid inputs and network issues<br>
📱 Fully responsive design<br>

---
### 🚀 Project Overview<br>
This project allows users to:<br>
 1. Enter an amount<br>
 2. Select source and target currencies<br>
 3. Fetch live exchange rates<br>
 4. Instantly view the converted value with a clean UI<br>
<br>
The application uses a glassmorphism UI design, smooth animations, and asynchronous API calls for real-time conversion.<br>

---
### 🛠️ Tech Stack<br>

HTML5 – Structure<br>
Tailwind CSS – Styling & responsive layout<br>
JavaScript (ES6) – Logic & API integration<br>
ExchangeRate API – Live currency data<br>

---
### 📁 Project Structure<br>

```
📦 Global-Currency-Converter
 ┣ 📄 index.html
 ┗ 📄 README.md
```
---
### 🔄 How the Application Works (Step-by-Step)<br>
### Step 1: Page Load 
<br>
The webpage loads with a default amount (1)<br>
Default currencies are set (INR → USD)<br>
The convertCurrency() function automatically runs on page load<br>

```
window.onload = convertCurrency;
```

---
### Step 2: User Input
<br>

####  The user:<br>
Enters the amount<br>
Selects From Currency<br>
Selects To Currency<br>
Clicks Convert Now<br>

---
### Step 3: Input Validation
<br>

#### Before conversion:<br>
Checks if the entered amount is valid (> 0)<br>
Shows an error message if invalid<br>

```
if (!amount || amount <= 0) {
    showError("Please enter a valid amount");
    return;
}
```

---
### Step 4: API Call for Live Rates
<br>

####  Fetches real-time exchange rates using:<br>

```
https://open.er-api.com/v6/latest/{FROM_CURRENCY}
```

#### Example:<br>

```
const response = await fetch(`${API_URL}${from}`);
```

---
### Step 5: Currency Conversion
<br>
Extracts the exchange rate<br>
Multiplies amount × exchange rate<br>
Rounds the result to 2 decimal places<br>

```
const rate = data.rates[to];
const convertedValue = (amount * rate).toFixed(2);
```

---
### Step 6: Display Result
<br>
Displays converted amount<br>
Shows exchange rate info<br>

```
finalAmount.innerText = `${convertedValue} ${to}`;
rateInfo.innerText = `1 ${from} = ${rate.toFixed(4)} ${to}`;
```

---
### Step 7: Loading & Error Handling
<br>
Shows a loading spinner while fetching data<br>
Displays user-friendly error messages if API fails or network issues occur<br>

---
### 🎨 UI Features
<br>
Glassmorphism card layout<br>
Gradient background<br>
Animated loading spinner<br>
Responsive for mobile & desktop<br>
Smooth hover and focus effects<br>

---
### 🌐 Supported Currencies
<br>
INR – Indian Rupee 🇮🇳<br>
USD – US Dollar 🇺🇸<br>
EUR – Euro 🇪🇺<br>
GBP – British Pound 🇬🇧<br>
JPY – Japanese Yen 🇯🇵<br>
AUD – Australian Dollar 🇦🇺<br>
CAD – Canadian Dollar 🇨🇦<br>
CNY – Chinese Yuan 🇨🇳<br>

---
### 🔐 API Used
<br>
ExchangeRate-API (Free Tier)<br>
No API key required<br>
Live currency exchange rates<br>

---
### 📌 Key Highlights
<br>
Built a responsive currency converter using HTML, Tailwind CSS, and JavaScript<br>
Integrated real-time exchange rate API using asynchronous JavaScript (fetch)<br>
Implemented input validation, loading states, and error handling<br>
Designed a modern glassmorphism UI with smooth animations<br>
Ensured cross-device compatibility and clean user experience<br>

---
### 📷 Demo Preview

<img width="1918" height="866" alt="image" src="https://github.com/user-attachments/assets/c04ecd02-d5a2-4a1d-ac45-1dd298d56760" />
<br>

---

