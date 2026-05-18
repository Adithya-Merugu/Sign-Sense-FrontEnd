# SignSense Frontend

Static responsive frontend for the SignSense backend.

## Run

Start the backend first:

```bash
cd "/Users/adithya.merugu/Desktop/LifeScience/SignSense Backend"
export GOOGLE_API_KEY="your_google_ai_studio_key"
export GEMMA_MODEL="your_gemma_4_model_name"
../.venv/bin/python -m uvicorn main:app --reload --port 8000
```

Then serve this folder:

```bash
cd "/Users/adithya.merugu/Desktop/LifeScience/SignSense Frontend"
python3 -m http.server 5173
```

Open:

```text
http://127.0.0.1:5173
```

The frontend calls:

```text
http://127.0.0.1:8000/api/analyze
http://127.0.0.1:8000/api/follow-up
```

You can change the backend URL in the browser console:

```js
localStorage.setItem("signsense_api_base", "http://127.0.0.1:8000")
```
