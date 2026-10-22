# Event_for_Multimodel_RAG

Launcher for a multimodal Retrieval-Augmented Generation (RAG) Streamlit demo, packaged to run in Google Colab for event presentations.

## What is in this repository

| File | Purpose |
| --- | --- |
| `Streamlit.ipynb` | Colab notebook that sets up and launches the demo. It clones the [LLM-AI-INDIA/RAG](https://github.com/LLM-AI-INDIA/RAG) application, installs its dependencies, opens a public ngrok tunnel on port 8501, and starts the Streamlit app. |
| `hello.py` | Minimal Python script that prints a greeting. Useful as a quick sanity check that the environment can run Python. |

## Running the demo

1. Open `Streamlit.ipynb` in Google Colab using the badge at the top of the notebook.
2. Replace the placeholder values in the first cell before running it:
   - `API_KEY` and `OPENAI_API_KEY` with your model provider keys
   - `SQL_URI` with the connection string for the backing database
   - `ngrok.set_auth_token("YOUR_TOKEN")` with your ngrok auth token
3. Run the cell. It prints a public URL once the tunnel is up. Open that URL to use the Streamlit app.

The notebook keeps the tunnel open for 20 minutes by default. Adjust the final `time.sleep` call if you need a longer session.

## Running the hello script

```bash
python hello.py
```

Expected output:

```
Hello from FI$Cal
```

## Notes

- Do not commit real API keys, database URIs, or ngrok tokens to this repository. Keep the placeholders in the notebook and enter secrets at runtime.
- The application code itself lives in the upstream `LLM-AI-INDIA/RAG` repository. This repository only contains the launcher.
