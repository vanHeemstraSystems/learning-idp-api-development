# References - API Development for IDP

This document contains curated resources for learning API development with Python to build Internal Development Platforms (IDP).

## 📚 Table of Contents

- [Official Documentation](#official-documentation)
- [Books](#books)
- [Articles & Blog Posts](#articles--blog-posts)
- [Video Tutorials](#video-tutorials)
- [Online Courses](#online-courses)
- [Tools & Libraries](#tools--libraries)
- [GitHub Repositories](#github-repositories)
- [Related Learning Repositories](#related-learning-repositories)
- [Community Resources](#community-resources)

-----

## 📖 Official Documentation

### FastAPI

#### Core Documentation

- [FastAPI Documentation](https://fastapi.tiangolo.com/) - Complete FastAPI guide
- [Tutorial](https://fastapi.tiangolo.com/tutorial/) - Step-by-step tutorial
- [Advanced User Guide](https://fastapi.tiangolo.com/advanced/) - Advanced topics
- [Deployment](https://fastapi.tiangolo.com/deployment/) - Production deployment
- [Best Practices](https://fastapi.tiangolo.com/async/) - Async best practices

#### Key Features

- [Path Parameters](https://fastapi.tiangolo.com/tutorial/path-params/) - URL parameters
- [Query Parameters](https://fastapi.tiangolo.com/tutorial/query-params/) - Query strings
- [Request Body](https://fastapi.tiangolo.com/tutorial/body/) - Request payloads
- [Response Model](https://fastapi.tiangolo.com/tutorial/response-model/) - Response schemas
- [Dependencies](https://fastapi.tiangolo.com/tutorial/dependencies/) - Dependency injection

#### Security

- [Security](https://fastapi.tiangolo.com/tutorial/security/) - Security overview
- [OAuth2](https://fastapi.tiangolo.com/tutorial/security/oauth2-jwt/) - OAuth2 with JWT
- [API Keys](https://fastapi.tiangolo.com/tutorial/security/api-keys/) - API key auth

### Pydantic

- [Pydantic Documentation](https://docs.pydantic.dev/) - Data validation
- [Models](https://docs.pydantic.dev/latest/concepts/models/) - Model definition
- [Validators](https://docs.pydantic.dev/latest/concepts/validators/) - Custom validation
- [Settings](https://docs.pydantic.dev/latest/concepts/pydantic_settings/) - Configuration management

### Flask

#### Core Documentation

- [Flask Documentation](https://flask.palletsprojects.com/) - Flask guide
- [Quickstart](https://flask.palletsprojects.com/en/latest/quickstart/) - Getting started
- [Tutorial](https://flask.palletsprojects.com/en/latest/tutorial/) - Complete tutorial
- [Patterns](https://flask.palletsprojects.com/en/latest/patterns/) - Design patterns

#### Extensions

- [Flask-RESTful](https://flask-restful.readthedocs.io/) - REST API extension
- [Flask-SMOREST](https://flask-smorest.readthedocs.io/) - OpenAPI integration
- [Flask-JWT-Extended](https://flask-jwt-extended.readthedocs.io/) - JWT authentication
- [Flask-SQLAlchemy](https://flask-sqlalchemy.palletsprojects.com/) - Database integration

### GraphQL

#### Strawberry GraphQL

- [Strawberry Documentation](https://strawberry.rocks/) - Modern GraphQL
- [FastAPI Integration](https://strawberry.rocks/docs/integrations/fastapi) - FastAPI plugin
- [Subscriptions](https://strawberry.rocks/docs/general/subscriptions) - Real-time updates

#### Graphene

- [Graphene Documentation](https://docs.graphene-python.org/) - GraphQL for Python
- [SQLAlchemy](https://docs.graphene-python.org/projects/sqlalchemy/en/latest/) - Database integration

### API Standards

#### REST

- [REST API Guidelines](https://restfulapi.net/) - REST principles
- [HTTP Status Codes](https://developer.mozilla.org/en-US/docs/Web/HTTP/Status) - Status reference
- [Richardson Maturity Model](https://martinfowler.com/articles/richardsonMaturityModel.html) - REST levels

#### OpenAPI

- [OpenAPI Specification](https://swagger.io/specification/) - API documentation standard
- [Swagger UI](https://swagger.io/tools/swagger-ui/) - API documentation UI
- [ReDoc](https://redocly.com/docs/redoc/) - Alternative documentation

-----

## 📚 Books

### FastAPI & Modern Python

1. **“Building Data-Driven Applications with FastAPI”** by Giunter Richter
- FastAPI fundamentals
- Production deployment
- [Packt Publishing](https://www.packtpub.com/)
1. **“FastAPI Modern Python Web Development”** by Bill Lubanovic
- Complete FastAPI guide
- Real-world applications
- [O’Reilly](https://www.oreilly.com/)

### API Design

1. **“REST API Design Rulebook”** by Mark Massé
- REST design principles
- Best practices
- [O’Reilly](https://www.oreilly.com/library/view/rest-api-design/9781449317904/)
1. **“Web API Design”** by Brian Mulloy (Free)
- API design patterns
- Practical examples
- [Apigee](https://pages.apigee.com/rs/apigee/images/api-design-ebook-2012-03.pdf)
1. **“Designing Web APIs”** by Brenda Jin, Saurabh Sahni, Amir Shevat
- API architecture
- Best practices
- [O’Reilly](https://www.oreilly.com/library/view/designing-web-apis/9781492026914/)

### GraphQL

1. **“Learning GraphQL”** by Eve Porcello and Alex Banks
- GraphQL fundamentals
- Query language
- [O’Reilly](https://www.oreilly.com/library/view/learning-graphql/9781492030706/)
1. **“Production Ready GraphQL”** by Marc-André Giroux
- Production patterns
- Schema design
- [Self-published](https://productionreadygraphql.com/)

### Python Web Development

1. **“Flask Web Development”** by Miguel Grinberg (3rd Edition)
- Flask fundamentals
- Database integration
- [O’Reilly](https://www.oreilly.com/library/view/flask-web-development/9781491991725/)
1. **“Two Scoops of Django”** by Daniel Roy Greenfeld and Audrey Roy Greenfeld
- Django best practices
- Applicable patterns
- [Two Scoops Press](https://www.feldroy.com/books/two-scoops-of-django-3-x)

-----

## 📝 Articles & Blog Posts

### FastAPI

#### Getting Started

- [FastAPI Best Practices](https://fastapi.tiangolo.com/tutorial/best-practices/) - Official guide
- [FastAPI Tips and Tricks](https://medium.com/@estretyakov/the-ultimate-fastapi-tutorial-part-1-basic-api-endpoints-c77b2de2f0ff) - Tutorial series
- [Production FastAPI](https://testdriven.io/blog/fastapi-best-practices/) - Production tips

#### Advanced Topics

- [Background Tasks in FastAPI](https://fastapi.tiangolo.com/tutorial/background-tasks/) - Async tasks
- [WebSocket with FastAPI](https://fastapi.tiangolo.com/advanced/websockets/) - Real-time communication
- [Testing FastAPI](https://fastapi.tiangolo.com/tutorial/testing/) - Testing guide

### API Design

#### Design Principles

- [REST API Best Practices](https://stackoverflow.blog/2020/03/02/best-practices-for-rest-api-design/) - Stack Overflow
- [API Design Patterns](https://cloud.google.com/apis/design) - Google Cloud
- [Microsoft REST API Guidelines](https://github.com/microsoft/api-guidelines/blob/vNext/Guidelines.md) - Microsoft

#### Versioning

- [API Versioning](https://www.freecodecamp.org/news/rest-api-design-best-practices-build-a-rest-api/) - Best practices
- [Semantic Versioning](https://semver.org/) - Version numbering

### Authentication & Security

#### OAuth2

- [OAuth 2.0 Simplified](https://aaronparecki.com/oauth-2-simplified/) - OAuth guide
- [JWT Introduction](https://jwt.io/introduction) - JWT explained
- [API Security Best Practices](https://github.com/OWASP/API-Security/blob/master/2019/en/dist/owasp-api-security-top-10.pdf) - OWASP

### GraphQL

- [GraphQL Best Practices](https://graphql.org/learn/best-practices/) - Official guide
- [GraphQL Schema Design](https://blog.apollographql.com/graphql-schema-design-building-evolvable-schemas-1501f3c59ed5) - Apollo
- [Batching and Caching](https://github.com/graphql/dataloader) - DataLoader pattern

-----

## 🎥 Video Tutorials

### FastAPI

#### Fundamentals

- [FastAPI Tutorial for Beginners](https://www.youtube.com/watch?v=7t2alSnE2-I) - FreeCodeCamp (3 hours)
- [FastAPI Course](https://www.youtube.com/watch?v=0sOvCWFmrtA) - Full course (6 hours)
- [Building APIs with FastAPI](https://www.youtube.com/watch?v=SORiTsvnU28) - Real Python (1 hour)

#### Advanced Topics

- [FastAPI Advanced Features](https://www.youtube.com/watch?v=GN6ICac3OXY) - Advanced tutorial (2 hours)
- [FastAPI + Docker](https://www.youtube.com/watch?v=0H2miBK_gAk) - Deployment (45 min)

### Flask

- [Flask Tutorial](https://www.youtube.com/watch?v=Z1RJmh_OqeA) - FreeCodeCamp (6 hours)
- [Flask REST API](https://www.youtube.com/watch?v=GMppyAPbLYk) - Tech With Tim (1 hour)

### GraphQL

- [GraphQL Tutorial](https://www.youtube.com/watch?v=ed8SzALpx1Q) - FreeCodeCamp (4 hours)
- [GraphQL with Python](https://www.youtube.com/watch?v=FQSJjPLLa_Q) - Tutorial (1 hour)

### API Design

- [API Design Best Practices](https://www.youtube.com/watch?v=_gQaygjm_hg) - Microsoft (30 min)
- [RESTful API Design](https://www.youtube.com/watch?v=_YlYuNMTCc8) - Tutorial (45 min)

-----

## 🎓 Online Courses

### Microsoft Learn (Free)

#### API Development

- [Build Web APIs with FastAPI](https://learn.microsoft.com/en-us/training/modules/build-web-api-minimal-api/) - Module
- [Create REST APIs](https://learn.microsoft.com/en-us/training/paths/create-rest-api/) - Learning path

### Paid Platforms

#### Pluralsight

- [Python REST APIs with Flask](https://www.pluralsight.com/courses/python-rest-apis-flask) - Flask course
- [FastAPI Fundamentals](https://www.pluralsight.com/courses/fastapi-fundamentals) - FastAPI
- [GraphQL: The Big Picture](https://www.pluralsight.com/courses/graphql-big-picture) - GraphQL

#### Udemy

- [REST APIs with Flask and Python](https://www.udemy.com/course/rest-api-flask-and-python/) - Jose Salvatierra
- [FastAPI - The Complete Course](https://www.udemy.com/course/fastapi-the-complete-course/) - Complete guide
- [GraphQL with Python](https://www.udemy.com/course/graphql-with-python/) - GraphQL course

#### Real Python

- [Python REST APIs With FastAPI](https://realpython.com/fastapi-python-web-apis/) - Tutorial
- [Flask by Example](https://realpython.com/learning-paths/flask-by-example/) - Learning path
- [Token-Based Authentication](https://realpython.com/token-based-authentication-with-flask/) - Auth tutorial

-----

## 🛠️ Tools & Libraries

### API Frameworks

#### FastAPI Stack

- **[fastapi](https://pypi.org/project/fastapi/)** - Modern API framework
- **[uvicorn](https://pypi.org/project/uvicorn/)** - ASGI server
- **[starlette](https://pypi.org/project/starlette/)** - ASGI toolkit
- **[pydantic](https://pypi.org/project/pydantic/)** - Data validation

#### Flask Stack

- **[flask](https://pypi.org/project/Flask/)** - Micro framework
- **[flask-restful](https://pypi.org/project/Flask-RESTful/)** - REST extension
- **[flask-smorest](https://pypi.org/project/flask-smorest/)** - OpenAPI integration
- **[marshmallow](https://pypi.org/project/marshmallow/)** - Serialization

### Database & ORM

- **[sqlalchemy](https://pypi.org/project/SQLAlchemy/)** - SQL toolkit
- **[alembic](https://pypi.org/project/alembic/)** - Database migrations
- **[databases](https://pypi.org/project/databases/)** - Async database
- **[tortoise-orm](https://pypi.org/project/tortoise-orm/)** - Async ORM

### Authentication

- **[python-jose](https://pypi.org/project/python-jose/)** - JWT implementation
- **[passlib](https://pypi.org/project/passlib/)** - Password hashing
- **[authlib](https://pypi.org/project/Authlib/)** - OAuth library
- **[python-oauth2](https://pypi.org/project/python-oauth2/)** - OAuth2 provider

### GraphQL

- **[strawberry-graphql](https://pypi.org/project/strawberry-graphql/)** - Modern GraphQL
- **[graphene](https://pypi.org/project/graphene/)** - GraphQL framework
- **[ariadne](https://pypi.org/project/ariadne/)** - Schema-first GraphQL

### API Documentation

- **[swagger-ui-py](https://pypi.org/project/swagger-ui-py/)** - Swagger UI
- **[flasgger](https://pypi.org/project/flasgger/)** - Flask Swagger
- **[openapi-spec-validator](https://pypi.org/project/openapi-spec-validator/)** - OpenAPI validator

### Testing

- **[httpx](https://pypi.org/project/httpx/)** - HTTP client
- **[pytest](https://pypi.org/project/pytest/)** - Testing framework
- **[pytest-asyncio](https://pypi.org/project/pytest-asyncio/)** - Async testing
- **[faker](https://pypi.org/project/Faker/)** - Test data generation

### API Clients

- **[requests](https://pypi.org/project/requests/)** - HTTP library
- **[aiohttp](https://pypi.org/project/aiohttp/)** - Async HTTP
- **[httpx](https://pypi.org/project/httpx/)** - Modern HTTP client

### Rate Limiting

- **[slowapi](https://pypi.org/project/slowapi/)** - Rate limiting for FastAPI
- **[flask-limiter](https://pypi.org/project/Flask-Limiter/)** - Flask rate limiting

### Monitoring

- **[prometheus-client](https://pypi.org/project/prometheus-client/)** - Metrics
- **[opentelemetry-api](https://pypi.org/project/opentelemetry-api/)** - Observability

-----

## 💻 GitHub Repositories

### Official Repositories

#### FastAPI

- [FastAPI](https://github.com/tiangolo/fastapi) - FastAPI source
- [Full Stack FastAPI](https://github.com/tiangolo/full-stack-fastapi-template) - Project template
- [FastAPI Users](https://github.com/fastapi-users/fastapi-users) - User management

#### Flask

- [Flask](https://github.com/pallets/flask) - Flask source
- [Flask-RESTful](https://github.com/flask-restful/flask-restful) - REST extension
- [Flask Mega-Tutorial](https://github.com/miguelgrinberg/microblog) - Complete example

### Learning Resources

- [Awesome FastAPI](https://github.com/mjhea0/awesome-fastapi) - Curated resources
- [Awesome Flask](https://github.com/mjhea0/awesome-flask) - Flask resources
- [API Design Guide](https://github.com/microsoft/api-guidelines) - Microsoft guidelines
- [REST API Tutorial](https://github.com/tfredrich/RestApiTutorial.com) - REST guide

### Example Projects

- [FastAPI Best Practices](https://github.com/zhanymkanov/fastapi-best-practices) - Best practices
- [FastAPI Boilerplate](https://github.com/teamhide/fastapi-boilerplate) - Production template
- [Real World FastAPI](https://github.com/nsidnev/fastapi-realworld-example-app) - Real-world example

-----

## 🔗 Related Learning Repositories

### From learning-internal-development-platform Series

1. **[learning-internal-development-platform](https://github.com/vanHeemstraSystems/learning-internal-development-platform)**
- Main overview
- Complete roadmap
1. **[learning-idp-python-azure-sdk](https://github.com/vanHeemstraSystems/learning-idp-python-azure-sdk)**
- Azure SDK fundamentals
- API integration
1. **[learning-idp-test-driven-development](https://github.com/vanHeemstraSystems/learning-idp-test-driven-development)**
- API testing
- Test patterns
1. **[learning-idp-containerization](https://github.com/vanHeemstraSystems/learning-idp-containerization)**
- API containerization
- Deployment
1. **[learning-idp-observability](https://github.com/vanHeemstraSystems/learning-idp-observability)**
- API monitoring
- Logging
1. **[learning-idp-azure-security](https://github.com/vanHeemstraSystems/learning-idp-azure-security)**
- API security
- Authentication

-----

## 👥 Community Resources

### Forums & Discussion

#### Official Communities

- [FastAPI Discussions](https://github.com/tiangolo/fastapi/discussions) - FastAPI community
- [Flask Discord](https://discord.com/invite/pallets) - Flask chat
- [GraphQL Slack](https://graphql.slack.com/) - GraphQL community

#### Stack Overflow

- [fastapi](https://stackoverflow.com/questions/tagged/fastapi) - FastAPI questions
- [flask](https://stackoverflow.com/questions/tagged/flask) - Flask questions
- [graphql](https://stackoverflow.com/questions/tagged/graphql) - GraphQL questions

### Social Media

#### Reddit

- [r/FastAPI](https://www.reddit.com/r/FastAPI/) - FastAPI community
- [r/flask](https://www.reddit.com/r/flask/) - Flask discussions
- [r/graphql](https://www.reddit.com/r/graphql/) - GraphQL topics

### Blogs & Newsletters

- [FastAPI Blog](https://fastapi.tiangolo.com/blog/) - Official blog
- [Real Python](https://realpython.com/) - Python tutorials
- [Python Weekly](https://www.pythonweekly.com/) - Python newsletter
- [API Evangelist](https://apievangelist.com/) - API news

-----

## 📊 Cheat Sheets & Quick References

### FastAPI

- [FastAPI Cheat Sheet](https://github.com/euri10/fastapi_cheatsheet) - Quick reference
- [HTTP Status Codes](https://httpstatuses.com/) - Status reference

### REST

- [REST API Quick Tips](https://restfulapi.net/rest-api-quick-tips/) - Best practices
- [HTTP Methods](https://developer.mozilla.org/en-US/docs/Web/HTTP/Methods) - Method reference

### GraphQL

- [GraphQL Cheat Sheet](https://devhints.io/graphql) - Syntax guide

-----

## 🎯 Next Steps

After mastering API Development, continue with:

1. **[learning-idp-cicd-pipelines](https://github.com/vanHeemstraSystems/learning-idp-cicd-pipelines)** - API deployment
1. **[learning-idp-platform-engineering](https://github.com/vanHeemstraSystems/learning-idp-platform-engineering)** - Platform APIs
1. **[learning-idp-infrastructure-as-code](https://github.com/vanHeemstraSystems/learning-idp-infrastructure-as-code)** - Infrastructure APIs

-----

*Last updated: December 18, 2025*
*Part of the learning-internal-development-platform series*
