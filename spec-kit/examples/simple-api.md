# Example: Simple API Feature

## Feature

Add a health-check endpoint to an API service.

## Problem

Operators need a predictable endpoint to verify that the service is running.

## Requirements

- The API shall expose `GET /health`.
- A healthy service shall return HTTP 200.
- The response shall identify the service as healthy.
- The endpoint shall not require authentication.

## Acceptance Criteria

- [ ] `GET /health` returns HTTP 200 when the service is healthy.
- [ ] The response is valid JSON.
- [ ] The response contains a clear health status.
- [ ] Automated tests cover the endpoint.

## Implementation Notes

Implementation details belong in the plan and tasks. The specification intentionally focuses on observable behavior and acceptance criteria.
