# Backend (app/backend)

This directory contains the backend code for the RAG chat app, built with Python and Quart. It provides API endpoints, authentication, and the core Retrieval Augmented Generation (RAG) logic for chat and Q&A over your data using Azure OpenAI and Azure AI Search.

## Structure

- `app.py`, `main.py`: Main entry points for the backend server, route definitions, and app configuration.
- `approaches/`: Contains RAG approaches and logic for chat and ask tabs, including prompt management.
- `prepdocs.py`, `prepdocslib/`: Utilities for document ingestion, embedding, and search setup.
- `core/`, `chat_history/`: Authentication, session, and chat history management (including Cosmos DB support).
- `requirements.txt`: Python dependencies for the backend.
- `Dockerfile`, `gunicorn.conf.py`: Containerization and server configuration for deployment.

## Running Locally

After deploying once with `azd up`, you can run the backend locally:

```powershell
# From the repo root
./app/start.ps1
```

The backend will start on port 50505 by default.

## Development

- Hot reloading is enabled by default when using the start scripts.
- For debugging and advanced usage, see [docs/localdev.md](../../docs/localdev.md).

## Customization

- To customize RAG logic, edit or add classes in `approaches/`.
- For authentication or API changes, modify `app.py` and related modules.

## Logging

Logging is configured in `app.py`. You can adjust log levels using the `APP_LOG_LEVEL` environment variable.

## Related Documentation

- [Local development guide](../../docs/localdev.md)
- [Customizing the backend](../../docs/customization.md)
- [Productionizing the app](../../docs/productionizing.md)
