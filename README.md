# OCI Worker (Public)

This public repository hosts the GitHub Actions workflow for the OCI Manager Worker.
It is designed to run in a public repository to benefit from standard GitHub Actions quotas.

## Setup

1.  **Secrets**: Go to **Settings -> Secrets and variables -> Actions** and add the following secrets:
    *   **`OCI_SERVER_URL`**: The URL of your OCI Manager Worker API (e.g., `https://api-worker.example.com`).
    *   **`OCI_WORKER_TOKEN`**: The authentication token for the worker.
    *   **`GH_PAT`**: A **Personal Access Token (Classic)** with `repo` scope (read-only is sufficient if possible, but private repo access requires `repo` scope) to allow downloading the worker binary from the private repository `suwei8/OCI-Manager-Go`.

2.  **Usage**: The workflow runs automatically on schedule (every 5 mins) or can be triggered manually via the "Actions" tab.
