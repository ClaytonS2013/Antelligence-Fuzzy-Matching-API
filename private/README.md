# Private API for Antelligence Fuzzy Matching

This directory contains documentation and code for the **private API** of the Antelligence fuzzy matching data pipeline. It includes endpoints for internal operations such as loading raw practice records, triggering deduplication runs, retrieving full dedupe logs, and managing pipeline configuration.

## Available Endpoints

- **POST `/api/private/practice_records`**
  - Ingest new practice records into the pipeline. Authentication required.
- **GET `/api/private/dedupe_results`**
  - Retrieve detailed dedupe results including cluster identifiers, similarity scores and canonical record IDs. Authorization required.
- **POST `/api/private/trigger_dedupe`**
  - Trigger a deduplication run on demand. Use with caution.

## Purpose

The private API is intended for internal service-to-service communication and is not exposed to external clients. It allows administrators and trusted services to manage the dedupe pipeline, adjust thresholds, and view detailed logs. External consumers should use the endpoints defined in the `public` directory.
