# Express.js JSON Body Parsing Issue

This repository demonstrates a common error in Express.js applications where JSON request bodies are not parsed correctly. The issue arises from incorrect placement of the `express.json()` middleware.

## Bug Description

The provided `bug.js` file contains an Express.js app that attempts to parse a JSON request body using the `express.json()` middleware. However, due to the middleware's placement, the request body remains unparsed. This leads to unexpected behavior and potential errors.

## Solution

The `bugSolution.js` file shows the corrected implementation where `express.json()` is placed before the route handler that expects JSON data. This ensures the middleware correctly parses the request body before it is accessed.

## Setup

1. Clone this repository.
2. Run `npm install` to install Express.js.
3. Run `node bug.js` to reproduce the bug. Note: Send a POST request to `/user` with a JSON payload (e.g., using Postman or curl).
4. Run `node bugSolution.js` to see the fixed version.