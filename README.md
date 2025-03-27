# neural-style-transfer
**Streamlit App with Ngrok**

**Overview**

This project sets up a Streamlit web application and makes it accessible over the internet using Ngrok. The script runs the Streamlit app in the background and establishes an Ngrok tunnel to expose it to a public URL.

**Requirements**

Before running the script, ensure you have the following installed:

Python 3.8+

Streamlit

Pyngrok

You can install the required packages using:

pip install streamlit pyngrok

**How to Run**

Clone this repository or copy the script.

Ensure app.py contains your Streamlit application.

**Run the script:**

python script.py

The script will:

Start Streamlit in the background.

Wait for it to launch.

Establish an Ngrok tunnel.

Print the public URL to access the app.

Open the provided Ngrok URL in your browser to access the Streamlit app.

**Troubleshooting**

If Ngrok does not start, try stopping existing Ngrok processes:

!kill -9 $(pgrep ngrok)

Ensure Streamlit is properly installed by running:

streamlit --version

If you encounter Thread 'MainThread': missing ScriptRunContext!, ensure Streamlit is started correctly with os.system("streamlit run app.py &").

**Notes**

The script includes a delay (time.sleep(10)) to allow Streamlit to start before creating the Ngrok tunnel.

Running Streamlit with & ensures it does not block execution.

Ngrok provides a temporary URL that resets upon restarting the script.

**Author**
Jaideep Dabral
