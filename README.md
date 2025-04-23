Problem Statement:
Farmers face challenges like:
- Unpredictable environmental conditions
- Inefficient water/fertilizer use
- Crop losses due to pests
Goal:
Create a smart, offline-capable system using IoT sensors, satellite imagery, and machine learning to give farmers real-time recommendations on:
- Water usage
- Fertilizer application
- Pest control
  
✅ Your Project Breakdown
💡 What You've Built:
You've created a web-based tool with:
- A Flask backend (Python)
- A Frontend UI (HTML + JS)
- Offline capability (runs on local server, no internet needed)
  
📦 Flask Backend Code Explanation:
Purpose:
- Handles POST requests from the frontend, analyzes data, and returns recommendations.
- Input Data (from user or sensors):
  moisture (soil moisture %)
- temperature (air/soil temperature °C)
- soilType (like sandy, clay, loamy)
Backend Logic:
Irrigation:
- If moisture < 30 and temperature > 32 → prompt to water crops.
Fertilizer:
- Customized recommendation based on soil type and moisture level.
Pest Warning:
- If temperature > 35 → warn about increased pest risk.
Output:
Returns a JSON object with:
- "irrigation" message
- "fertilizer" suggestion
- "pestWarning" (if any)
  
🖥️ HTML + JavaScript Frontend:
Purpose:
Provides an easy-to-use interface for farmers to input conditions and view smart advice.
Features:
Input fields: Soil moisture, temperature, soil type
Button: Triggers logic to show recommendations
Output section: Displays advice in text format
Offline Capability:
Everything runs locally (you can deploy with Flask on a laptop or Raspberry Pi)
No internet required — great for rural/farm areas

🚀 How This Solves the Prompt
Feature	Addressed?	How
📡 Use of sensors/data              	✅	Manual input simulates sensor data (can be automated later)
🤖 Machine learning (basic logic)   	✅	Rule-based logic now, can evolve into ML models (train on sensor data)
💧 Water usage optimization	          ✅	Advises watering based on temperature & moisture
🌿 Fertilizer optimization	          ✅	Tailored by soil type and condition
🐛 Pest control alerts	              ✅	Warns based on high temperature conditions
🛠️ Offline support	                  ✅	Works 100% offline (local Flask server + frontend)
⚡ Low-power device optimization	    ✅	Lightweight UI + Python backend can run on a Pi or low-end laptop
