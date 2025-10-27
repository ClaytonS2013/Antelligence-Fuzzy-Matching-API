# Public API for Antelligence Fuzzy Matching

This directory contains the documentation and code for the **public API** of the Antelligence fuzzy matching data pipeline. The public API exposes endpoints that allow clients to fetch cleaned and deduplicated practice records without exposing sensitive internal details.

## Available Endpoints

- **GET `/api/public/practice_records`**
  - Returns a list of canonical practice records produced by the fuzzy matching pipeline.
- **GET `/api/public/practice_records/{id}`**
  - Returns detailed information for a single canonical practice record.

## Purpose

These endpoints allow external services or applications to query the cleaned data set while preserving privacy and security. For private/internal API endpoints and administrative operations, please see the `private` directory.
