# Phase 2 — Practical Engineering (3–9 months)

Goal: Build real applications, learn tooling, testing, and deployment.

## Topics

- Web basics (HTTP, REST)
  - Definition: Web basics cover the protocols and concepts used to communicate over the internet, primarily HTTP/HTTPS and RESTful API design.
  - Discussion: Start by learning how requests and responses work, common status codes, and how to design simple REST endpoints. Practice with tools like curl or Postman and implement a small API to observe headers, query parameters, and body payloads.

- Databases (SQL basics), ORMs
  - Definition: Databases store persistent data. SQL is the language for relational databases; ORMs (Object-Relational Mappers) provide a language-native way to work with DBs.
  - Discussion: Learn how to design simple schemas, run basic queries (SELECT/INSERT/UPDATE/DELETE), and understand transactions. Try using an ORM to map classes to tables but also learn raw SQL to debug and optimize queries.

- Unit testing and test-driven development basics
  - Definition: Unit testing verifies small units of code (functions, classes). TDD is a workflow where tests are written before implementing functionality.
  - Discussion: Write tests for edge cases and common paths. Start with unit tests, then add integration tests. Try the red-green-refactor TDD cycle on a small feature to experience the discipline it enforces.

- Debugging, logging, and observability
  - Definition: Debugging is finding and fixing bugs; logging records runtime information; observability is the practice of making systems understandable through metrics, logs, and traces.
  - Discussion: Learn to use debuggers, structured logging, and basic metrics. Add meaningful logs to your projects and practice tracing a request through your app to find failures or performance problems.

- Git workflows: branching, pull requests, code reviews
  - Definition: Git workflows describe how teams use branches, commits, and pull requests to collaborate. Code reviews are the practice of reviewing changes before merging.
  - Discussion: Practice feature branches, opening PRs, and responding to review comments. Learn to write clear PR descriptions and break changes into small, reviewable commits.

- Deploying simple apps to Heroku/Vercel or cloud free tiers
  - Definition: Deployment is the process of packaging and running your application on a remote environment where users can access it.
  - Discussion: Start with simple, managed platforms like Heroku or Vercel to understand buildpacks, environment variables, and deployment pipelines. Deploy a small app, observe logs in production, and iterate on configuration and scaling basics.

## Exercises

- Build a CRUD REST API with a database backend.
- Write unit and integration tests for your services.
- Set up a basic CI pipeline that runs tests on push.

## Projects

- Personal blog with DB-backed posts
- Todo app with user authentication
- Simple web scraper and data storage
