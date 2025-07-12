Temporal Pattern Recognition (TPR) Recommendation System
What is this project?
The TPR Recommendation System is a smart tool designed to suggest personalized products to customers based on their shopping habits over time. It uses advanced artificial intelligence to understand when and what people buy, grouping customers into similar segments and predicting what they might want next. This makes shopping experiences more relevant and engaging, perfect for online stores, retail, or subscription services.
Key Features

Personalized Suggestions: Recommends products based on past purchases and trends.
Customer Grouping: Organizes customers into segments for tailored recommendations.
Real-Time Delivery: Provides instant recommendations through a simple web interface.
Smart Updates: Adapts to changing customer behavior and monitors performance.

How to Get Started
Follow these steps to set up and run the project on your computer.
1. Prerequisites

Python 3.8+: Make sure Python is installed. You can download it from python.org.
A computer with internet access to install required tools.

2. Setup

Clone or Download: Download the project folder to your computer.
Install Tools: Open a terminal in the project folder and run:pip install -r requirements.txt

This installs all the necessary software libraries.
Prepare Folders: Create models/segmentation/ and models/recommendation/ folders inside the project directory to store AI models.

3. Running the System

Start the System: In the terminal, run:python main.py

This processes the data, trains the AI models, and starts a web server.
Get Recommendations: Open a web browser or use a tool like curl to request recommendations for a customer. For example:curl http://localhost:8000/recommend/C0001

You’ll see a response like:{
  "client_id": "C1",
  "segment": 1,
  "recommendations": [
    {"article": "RG-RAP1200(P)", "categorie": "Network", "score": 2.8},
    {"article": "SWITCH-N200", "categorie": "Network", "score": 1.5}
  ]
}

This shows the customer’s group (segment) and suggested products.

4. Checking Performance
To monitor if the system is working correctly with new data, run:
python src/monitoring.py

This checks for any changes in customer behavior that might affect recommendations.
Project Structure

data/: Contains customer purchase data (e.g., sample_data.csv).
src/: Code for processing data, grouping customers, making recommendations, and running the web server.
config/: Settings for the system (e.g., config.yaml).
models/: Stores trained AI models.
requirements.txt: List of required software libraries.
main.py: Main script to run everything.

Example Data
The project includes a sample dataset (data/sample_data.csv) with customer purchases, like:

Customer ID, product, category, quantity, and purchase date.You can replace it with your own data in the same format.

Tips

Add Your Data: Update data/sample_data.csv with your customer purchase records.
Customize Settings: Edit config/config.yaml to tweak how the system works.
Extend the System: Add more customer data or product details for better recommendations.

Need Help?
If you run into issues or want to add new features (like handling new customers or visualizing results), contact the project team or check the code comments for guidance.
Why Use TPR?
This system helps businesses:

Boost customer engagement with relevant product suggestions.
Increase sales by predicting what customers want.
Manage inventory better by understanding purchase trends.

Happy recommending!
