# Copilot Instructions

## API Integration Testing

Any new API endpoint added to `custom_components/myengie/api.py` **must** be tested using `debug_auth.py` before being considered complete.

### Steps
1. Add the method to `MyEngieAPI` in `api.py`
2. Add a corresponding test block in `debug_auth.py` following the existing numbered pattern (e.g. `# 13. get_new_endpoint`)
3. Run the script: `/Users/andreisarbu/Code/ha-myEngie/.venv/bin/python debug_auth.py`
4. Confirm the endpoint returns `✅` and inspect the response structure
5. Use the real response structure to implement sensor parsing in `sensor.py`

### Credentials
Stored in `.env` (git-ignored). The script loads them automatically via `python-dotenv`.
