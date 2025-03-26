AI Supplier Search Agent
=======================

Overview
--------
This project is an AI-powered supplier search agent designed to scrape, classify, and rank industrial suppliers across multiple industries (e.g., automotive, lighting, machinery) and manufacturing processes (e.g., casting, forging, machining). It fulfills a business goal of identifying manufacturers and a technical goal of real-time web scraping and data processing. The project is built with Python and is intended to be scalable, sustainable, and open-source.

Features
--------
- Real-time web scraping from B2B marketplaces like Alibaba and IndiaMART
- AI-based classification of suppliers into industries and processes
- Data cleaning and enrichment (deduplication, standardization)
- Searchable supplier database via a Flask API
- Bonus: Periodic scraping for real-time updates using APScheduler

Requirements
------------
- Python 3.8+
- Libraries: requests, beautifulsoup4, pandas, spacy, flask, apscheduler
- Optional: spaCy English model (en_core_web_sm) for NLP classification

Installation
------------
1. Clone the repository:
   git clone https://github.com/yourusername/AI-Supplier-Search-Agent.git
2. Navigate to the project directory:
   cd AI-Supplier-Search-Agent
3. Install dependencies:
   pip install -r requirements.txt
4. (Optional) Download spaCy model:
   python -m spacy download en_core_web_sm

Usage
-----
1. Run the main script to start scraping:
   python main.py
2. Access the API (after running the Flask app):
   http://localhost:5000/suppliers?industry=automotive
3. Check the 'data/' folder for scraped and cleaned supplier data in JSON format.

Project Structure
-----------------
- scraper/          : Web scraping logic and site configurations
- classifier/       : AI-based industry and process classification
- data/             : Output supplier data and sample datasets
- api/              : Flask API for querying suppliers
- utils/            : Data cleaning and ranking utilities
- main.py           : Entry point for the application
- requirements.txt  : List of dependencies
- README.txt        : This file

Scalability & Sustainability
----------------------------
- Modular design allows easy addition of new scraping sources
- APScheduler enables periodic updates (e.g., daily rescraping)
- Lightweight Flask API can be deployed to cloud platforms like Heroku or AWS

Contributing
------------
1. Fork the repository
2. Create a feature branch: git checkout -b my-feature
3. Commit changes: git commit -m "Add my feature"
4. Push to the branch: git push origin my-feature
5. Submit a pull request

License
-------
This project is licensed under the MIT License. See LICENSE file for details (to be added).

Contact
-------
For questions or suggestions, reach out via GitHub Issues or email: your.email@example.com

Acknowledgements
----------------
Built as part of a challenge to create an AI-powered supplier search tool. Inspired by B2B marketplaces like Alibaba, IndiaMART, and ThomasNet.
