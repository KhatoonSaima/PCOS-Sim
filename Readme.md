PCOS Treatment Simulation Project
================================

A Streamlit-based simulation modeling treatment effects on PCOS patients.

Featured in University Demo Day: [View Article](https://www.uwindsor.ca/dailynews/2025-04-25/)


1. PREREQUISITES
----------------
- Python 3.8 or later
- Firebase account
- Required data files:
  * Cleaned-Data.csv (PCOS training dataset)
  * pcos-service-key.json (Firebase credentials)

2. INSTALLATION STEPS
---------------------
2.1 Download the main.py file

2.2 Create and activate virtual environment:
    # Linux/Mac:
    python -m venv venv
    source venv/bin/activate
    
    # Windows:
    python -m venv venv
    .\venv\Scripts\activate

2.3 Install required packages:main.py
    pip install streamlit mesa pandas scikit-learn matplotlib firebase-admin

3. FIREBASE SETUP 
----------------------------
3.1 Create Firebase project:
    - Go to https://console.firebase.google.com/
    - Click "Add Project" and follow prompts

3.2 Get service account key:
    - Project Settings > Service Accounts > Generate new private key
    - Save as pcos-service-key.json in project root

3.3 Enable Firestore:
    - In Firebase Console, go to Firestore Database
    - Click "Create database" (start in test mode)

4. DATA FILES
-------------
Place these files in the same location where main.py file is present:
- Cleaned-Data-new.csv (PCOS training data)
- pcos-service-key.json (Firebase credentials)

5. RUNNING THE APPLICATION
-------------------------
5.1 Start Streamlit server:
    streamlit run main.py

5.2 Access the app:
    Open http://localhost:8501 in your browser

6. USING THE APPLICATION
-----------------------
6.1 Fill out patient information form
6.2 Click "Submit & Simulate"
6.3 View results:
    - PCOS risk percentage
    - Interactive treatment comparison graphs
    - Final health metrics table

7. TROUBLESHOOTING
------------------
7.1 File not found errors:
    - Verify Cleaned-Data-new.csv exists in root directory
    - Check pcos-service-key.json path in main.py

7.2 Firebase authentication issues:
    - Ensure service account key has proper permissions
    - Check Firebase project ID matches credentials

7.3 Port conflicts:
    streamlit run main.py --server.port 8502

8. CUSTOMIZATION
----------------
To modify treatment effects, edit in main.py:
- Update weight change logic in PatientAgent.update_weight()
- Adjust insulin resistance in update_insulin_resistance()
- Modify hirsutism updates in update_hirsutism()

