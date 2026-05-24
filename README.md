1. Install Python

Download Python from:

Python Official Website

While installing:

CHECK → Add Python to PATH
Use Python 3.11 or 3.10

Do NOT use random outdated versions.

2. Open Project Folder in VS Code

Example project:

insurance-prediction/

Open terminal inside VS Code:

Ctrl + `
3. Create Virtual Environment

Run:

python -m venv .venv

This creates:

.venv/
4. Activate Virtual Environment
Windows
.venv\Scripts\activate
Mac/Linux
source .venv/bin/activate

If activated correctly, terminal shows:

(.venv)
5. Install Required Libraries

For a typical ML project:

pip install pandas numpy scikit-learn matplotlib seaborn streamlit joblib

If using XGBoost:

pip install xgboost

If using TensorFlow:

pip install tensorflow

If using PyTorch:

pip install torch torchvision

Do NOT install everything blindly.
Install only what your project uses.

6. Save Dependencies

After installation:

pip freeze > requirements.txt

This creates:

requirements.txt

Example:

numpy==2.3.1
pandas==2.3.0
scikit-learn==1.7.0
streamlit==1.45.0
joblib==1.5.1
7. Install Dependencies Later

If someone clones your project:

pip install -r requirements.txt

That installs everything automatically.

This is mandatory for deployment.

8. Verify Installation

Run:

pip list

or:

python

Then:

import pandas
import sklearn
import streamlit

If no errors appear, installation worked.

Exit Python:

exit()
9. Common Errors
Error: python is not recognized

Fix:

reinstall Python
CHECK Add Python to PATH
Error: pip not recognized

Run:

python -m pip install --upgrade pip
Error: Streamlit not found

Wrong:

streamlit run app.py

Correct:

python -m streamlit run app.py

This avoids PATH problems.

10. Recommended Setup for Your ML Projects

For your insurance prediction project:

Install:

pip install pandas numpy scikit-learn streamlit matplotlib joblib

Then:

pip freeze > requirements.txt

Then test:

python -m streamlit run app.py

If the app runs locally first, deployment becomes much easier.
