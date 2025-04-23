# Agrotech
-> Prompt Summary: Smart Farming Advisor
The Problem:
Farmers often struggle to optimize crop yield due to:
Changing weather
Inefficient use of water & fertilizer
Late pest detection
The Solution Goal:
Create a smart farming assistant that:
Uses sensor or manual input (soil, temperature, etc.)
Applies basic AI/logic to recommend actions
Runs on low-power hardware or offline
Is easy for farmers to use in real-world rural settings
-> What's in the Code
-> Purpose:
Simulates a decision-making tool for farmers using:
Soil moisture
Temperature
Soil type
It analyzes this input and gives actionable advice:
Should I water?
Should I fertilize?
Are pests likely?
-> Code Explanation (Line by Line)
-> Header and Function Declarations
#include <stdio.h>
#include <stdlib.h>
#include <string.h>
Standard libraries: input/output, string handling.

-> Main Logic Function: analyze_data_and_recommend(...)
void analyze_data_and_recommend(float moisture, float temp, char soil_type[20]) {
Takes 3 parameters: moisture, temperature, soil type.
-> Watering Logic:
if (moisture < 30 && temp > 32)
If soil is dry AND it's hot → recommend watering.
-> Fertilizer Logic:
if (strcmp(soil_type, "sandy") == 0 && moisture > 25 && moisture < 40)
Soil-specific fertilizer tips: Sandy needs more frequent, clay retains better.
-> Pest Logic:
if (temp > 35)
If temp is very high → warn about pest risk (simulated).
-> Main Function: int main()
float soil_moisture, temperature;
char soil_type[20];
Declares variables to take user input.
scanf("%f", &soil_moisture);
scanf("%f", &temperature);
scanf("%s", soil_type);
Reads user input from console.
analyze_data_and_recommend(soil_moisture, temperature, soil_type);
Calls the logic function with user input.

**Example Use Case (For Judges or Demo)
A farmer enters:
Soil Moisture: 25%
Temperature: 37°C
Soil Type: sandy

* The system replies:
“Water your crops now.”
“Apply 60% NPK fertilizer.”
“High pest risk, watch for insects.”
-> This is simple, fast, useful advice — exactly what farmers need.
