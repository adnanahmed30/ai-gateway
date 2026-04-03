# Contributing to AI Gateway

Thank you for your interest in contributing.
This project welcomes contributions of all kinds.

## Ways to contribute

- Report bugs via GitHub Issues
- Suggest features via GitHub Issues
- Submit pull requests for fixes or improvements
- Improve documentation
- Add new LLM provider adapters

## Getting started

1. Fork the repository
2. Clone your fork locally
3. Install dependencies: `npm install`
4. Copy `.env.example` to `.env` and configure
5. Create a feature branch: `git checkout -b feature/your-feature`
6. Make your changes
7. Run tests: `npm test`
8. Submit a pull request

## Good first issues

These are great starting points for new contributors:

- Add a new provider adapter (OpenAI, Anthropic, Together.ai)
- Improve confidence checker with score-based evaluation
- Implement semantic caching using existing embeddings
- Add more intent classification examples
- Improve documentation or examples

## Provider adapter pattern

New providers follow the pattern in `src/providers/groq.js`.

Every adapter must:
- Accept `(prompt, model)` as parameters
- Return `{ ok, output, model, cost, latency, usage }`
- Handle errors by throwing — not returning error objects
- Never import application logic — only config and axios

## Code style

- One responsibility per file
- Defensive input handling on all external data
- Record metrics on every execution path
- Follow existing naming conventions

## Questions

Open a GitHub Discussion if you have questions
about the architecture or want to discuss ideas
before submitting a pull request.
