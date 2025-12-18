# Learning IDP: API Development

This repository focuses on mastering API development using Python frameworks to build, manage, and automate RESTful APIs for Internal Development Platform (IDP) development.

## 🎯 Learning Objectives

By working through this repository, you will:

1. Master FastAPI and Flask for API development
1. Implement RESTful API best practices
1. Work with API authentication and authorization
1. Build GraphQL APIs with Python
1. Implement API documentation with OpenAPI/Swagger
1. Configure API gateways and rate limiting
1. Deploy APIs to production environments

## 📚 Prerequisites

- Python 3.11 or higher
- Basic understanding of HTTP and REST principles
- Completed [learning-idp-python-azure-sdk](https://github.com/vanHeemstraSystems/learning-idp-python-azure-sdk)
- Completed [learning-idp-test-driven-development](https://github.com/vanHeemstraSystems/learning-idp-test-driven-development)
- Git and GitHub account

## 🗂️ Directory Structure

```
learning-idp-api-development/
├── README.md                          # This file
├── REFERENCES.md                      # Links to resources and related repos
├── pyproject.toml                     # Python project configuration
├── requirements.txt                   # Python dependencies
├── requirements-dev.txt               # Development dependencies
├── .python-version                    # Python version for pyenv
├── .gitignore                         # Git ignore patterns
├── .env.example                       # Environment variables template
│
├── docs/
│   ├── concepts/
│   │   ├── 01-api-overview.md
│   │   ├── 02-rest-principles.md
│   │   ├── 03-api-design.md
│   │   ├── 04-authentication.md
│   │   ├── 05-api-versioning.md
│   │   └── 06-api-security.md
│   ├── guides/
│   │   ├── getting-started.md
│   │   ├── fastapi-setup.md
│   │   ├── authentication-oauth2.md
│   │   ├── api-documentation.md
│   │   └── deployment.md
│   └── examples/
│       ├── simple-rest-api.md
│       ├── crud-operations.md
│       ├── authentication-flow.md
│       ├── graphql-api.md
│       └── microservices-api.md
│
├── src/
│   ├── __init__.py
│   │
│   ├── core/
│   │   ├── __init__.py
│   │   ├── config.py                  # Configuration management
│   │   ├── exceptions.py              # Custom exceptions
│   │   ├── logging_config.py          # Logging setup
│   │   └── dependencies.py            # FastAPI dependencies
│   │
│   ├── api/
│   │   ├── __init__.py
│   │   ├── main.py                    # FastAPI application
│   │   ├── routes/
│   │   │   ├── __init__.py
│   │   │   ├── health.py              # Health check endpoint
│   │   │   ├── users.py               # User endpoints
│   │   │   ├── auth.py                # Authentication endpoints
│   │   │   └── items.py               # Resource endpoints
│   │   └── middleware/
│   │       ├── __init__.py
│   │       ├── cors.py                # CORS middleware
│   │       ├── auth.py                # Auth middleware
│   │       ├── rate_limit.py          # Rate limiting
│   │       └── logging.py             # Request logging
│   │
│   ├── models/
│   │   ├── __init__.py
│   │   ├── user.py                    # User model
│   │   ├── item.py                    # Item model
│   │   ├── auth.py                    # Auth models
│   │   └── base.py                    # Base model
│   │
│   ├── schemas/
│   │   ├── __init__.py
│   │   ├── user.py                    # User schemas (Pydantic)
│   │   ├── item.py                    # Item schemas
│   │   ├── auth.py                    # Auth schemas
│   │   └── common.py                  # Common schemas
│   │
│   ├── services/
│   │   ├── __init__.py
│   │   ├── user_service.py            # User business logic
│   │   ├── auth_service.py            # Authentication logic
│   │   ├── item_service.py            # Item business logic
│   │   └── cache_service.py           # Caching service
│   │
│   ├── repositories/
│   │   ├── __init__.py
│   │   ├── user_repository.py         # User data access
│   │   ├── item_repository.py         # Item data access
│   │   └── base_repository.py         # Base repository
│   │
│   ├── auth/
│   │   ├── __init__.py
│   │   ├── jwt.py                     # JWT token handling
│   │   ├── oauth2.py                  # OAuth2 implementation
│   │   ├── password.py                # Password hashing
│   │   └── permissions.py             # Permission system
│   │
│   ├── database/
│   │   ├── __init__.py
│   │   ├── session.py                 # Database session
│   │   ├── base.py                    # Base database class
│   │   └── migrations/                # Alembic migrations
│   │       └── versions/
│   │
│   ├── graphql/
│   │   ├── __init__.py
│   │   ├── schema.py                  # GraphQL schema
│   │   ├── queries.py                 # GraphQL queries
│   │   ├── mutations.py               # GraphQL mutations
│   │   └── resolvers.py               # Field resolvers
│   │
│   └── utils/
│       ├── __init__.py
│       ├── validators.py              # Input validators
│       ├── serializers.py             # Data serializers
│       ├── pagination.py              # Pagination helpers
│       └── rate_limiter.py            # Rate limiting utilities
│
├── examples/
│   ├── 01_fastapi_basics/
│   │   ├── 01_hello_world.py
│   │   ├── 02_path_parameters.py
│   │   ├── 03_query_parameters.py
│   │   ├── 04_request_body.py
│   │   └── 05_response_model.py
│   │
│   ├── 02_crud_operations/
│   │   ├── 01_create_user.py
│   │   ├── 02_read_user.py
│   │   ├── 03_update_user.py
│   │   ├── 04_delete_user.py
│   │   └── 05_list_users.py
│   │
│   ├── 03_authentication/
│   │   ├── 01_basic_auth.py
│   │   ├── 02_jwt_auth.py
│   │   ├── 03_oauth2_flow.py
│   │   ├── 04_refresh_tokens.py
│   │   └── 05_permissions.py
│   │
│   ├── 04_database_integration/
│   │   ├── 01_sqlalchemy_setup.py
│   │   ├── 02_models.py
│   │   ├── 03_relationships.py
│   │   ├── 04_queries.py
│   │   └── 05_migrations.py
│   │
│   ├── 05_advanced_features/
│   │   ├── 01_file_upload.py
│   │   ├── 02_background_tasks.py
│   │   ├── 03_websockets.py
│   │   ├── 04_streaming.py
│   │   └── 05_caching.py
│   │
│   ├── 06_graphql/
│   │   ├── 01_basic_schema.py
│   │   ├── 02_queries.py
│   │   ├── 03_mutations.py
│   │   ├── 04_subscriptions.py
│   │   └── 05_dataloader.py
│   │
│   ├── 07_testing/
│   │   ├── 01_test_endpoints.py
│   │   ├── 02_test_auth.py
│   │   ├── 03_test_database.py
│   │   ├── 04_test_integration.py
│   │   └── 05_test_performance.py
│   │
│   └── 08_deployment/
│       ├── 01_docker_deployment/
│       │   ├── Dockerfile
│       │   └── docker-compose.yml
│       ├── 02_kubernetes_deployment/
│       │   ├── deployment.yaml
│       │   └── service.yaml
│       └── 03_azure_deployment/
│           └── deploy_to_azure.py
│
├── templates/
│   ├── api/
│   │   ├── basic_rest_api.py
│   │   ├── crud_api.py
│   │   └── microservice_api.py
│   ├── schemas/
│   │   ├── user_schema.py
│   │   ├── auth_schema.py
│   │   └── error_schema.py
│   └── middleware/
│       ├── auth_middleware.py
│       ├── cors_middleware.py
│       └── rate_limit_middleware.py
│
├── notebooks/
│   ├── 01_api_basics.ipynb
│   ├── 02_authentication.ipynb
│   ├── 03_database_integration.ipynb
│   ├── 04_graphql_api.ipynb
│   └── 05_api_testing.ipynb
│
├── scripts/
│   ├── create_api_project.sh          # Project setup script
│   ├── run_dev_server.sh              # Development server
│   ├── generate_openapi.py            # Generate OpenAPI spec
│   └── migrate_database.sh            # Run migrations
│
├── tests/
│   ├── __init__.py
│   ├── conftest.py
│   ├── unit/
│   │   ├── test_models.py
│   │   ├── test_schemas.py
│   │   ├── test_services.py
│   │   └── test_auth.py
│   ├── integration/
│   │   ├── test_api_endpoints.py
│   │   ├── test_authentication.py
│   │   ├── test_database.py
│   │   └── test_webhooks.py
│   └── e2e/
│       ├── test_user_flow.py
│       └── test_api_flow.py
│
└── .github/
    └── workflows/
        ├── api-test.yml               # API testing
        ├── api-deploy.yml             # Deployment
        └── api-docs.yml               # Documentation generation
```

## 🚀 Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/vanHeemstraSystems/learning-idp-api-development.git
cd learning-idp-api-development
```

### 2. Set Up Python Environment

```bash
# Create virtual environment
python3 -m venv venv

# Activate virtual environment
# On Linux/MacOS:
source venv/bin/activate
# On Windows:
# venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt
pip install -r requirements-dev.txt
```

### 3. Run Your First API

```bash
# Run the basic FastAPI example
cd examples/01_fastapi_basics
uvicorn 01_hello_world:app --reload

# Test it
curl http://localhost:8000
curl http://localhost:8000/docs  # Swagger UI
```

### 4. Create a Full CRUD API

```bash
# Run the CRUD example
python examples/02_crud_operations/01_create_user.py

# Access the API
curl -X POST http://localhost:8000/users \
  -H "Content-Type: application/json" \
  -d '{"name": "John Doe", "email": "john@example.com"}'
```

## 📖 Learning Path

Follow this recommended sequence:

### Week 1: FastAPI Fundamentals

**Day 1-2: FastAPI Basics**

1. Read `docs/concepts/01-api-overview.md`
1. Complete examples in `examples/01_fastapi_basics/`
1. Practice path and query parameters

**Day 3-4: CRUD Operations**

1. Study `docs/concepts/02-rest-principles.md`
1. Work through `examples/02_crud_operations/`
1. Implement full CRUD API

**Day 5-7: Database Integration**

1. Complete examples in `examples/04_database_integration/`
1. Implement SQLAlchemy models
1. Practice database migrations

### Week 2: Authentication & Security

**Day 1-3: Authentication**

1. Read `docs/concepts/04-authentication.md`
1. Complete examples in `examples/03_authentication/`
1. Implement JWT authentication

**Day 4-7: API Security**

1. Study `docs/concepts/06-api-security.md`
1. Implement OAuth2 flows
1. Configure CORS and rate limiting

### Week 3: Advanced Features

**Day 1-3: Advanced API Features**

1. Work through `examples/05_advanced_features/`
1. Implement file uploads
1. Configure background tasks

**Day 4-7: GraphQL API**

1. Complete examples in `examples/06_graphql/`
1. Build GraphQL schema
1. Implement queries and mutations

### Week 4: Testing & Deployment

**Day 1-3: API Testing**

1. Study testing best practices
1. Work through `examples/07_testing/`
1. Implement integration tests

**Day 4-7: Deployment**

1. Complete examples in `examples/08_deployment/`
1. Deploy to containers
1. Deploy to Azure

## 🔑 Key Python Packages

### API Frameworks

```python
# FastAPI Stack
fastapi>=0.109.0            # Modern API framework
uvicorn[standard]>=0.27.0   # ASGI server
pydantic>=2.5.0             # Data validation
python-multipart>=0.0.6     # Form data support

# Flask Alternative
flask>=3.0.0                # Flask framework
flask-restful>=0.3.10       # REST extensions
flask-smorest>=0.44.0       # OpenAPI integration

# GraphQL
strawberry-graphql>=0.219.0 # GraphQL library
graphene>=3.3              # GraphQL framework
```

### Database & ORM

```python
sqlalchemy>=2.0.0           # SQL toolkit and ORM
alembic>=1.13.0             # Database migrations
asyncpg>=0.29.0             # Async PostgreSQL
databases>=0.8.0            # Async database support
```

### Authentication

```python
python-jose[cryptography]>=3.3.0  # JWT tokens
passlib[bcrypt]>=1.7.4      # Password hashing
python-oauth2>=1.1.1        # OAuth2 implementation
```

## 💡 Common Operations Examples

### Basic FastAPI Application

```python
from fastapi import FastAPI, HTTPException
from pydantic import BaseModel, EmailStr
from typing import List

app = FastAPI(
    title="My API",
    description="API for learning",
    version="1.0.0"
)

# Pydantic models
class User(BaseModel):
    id: int | None = None
    name: str
    email: EmailStr
    is_active: bool = True

# In-memory storage
users_db: List[User] = []

@app.get("/")
async def root():
    return {"message": "Welcome to my API"}

@app.post("/users", response_model=User, status_code=201)
async def create_user(user: User):
    user.id = len(users_db) + 1
    users_db.append(user)
    return user

@app.get("/users", response_model=List[User])
async def list_users():
    return users_db

@app.get("/users/{user_id}", response_model=User)
async def get_user(user_id: int):
    for user in users_db:
        if user.id == user_id:
            return user
    raise HTTPException(status_code=404, detail="User not found")

@app.put("/users/{user_id}", response_model=User)
async def update_user(user_id: int, updated_user: User):
    for idx, user in enumerate(users_db):
        if user.id == user_id:
            updated_user.id = user_id
            users_db[idx] = updated_user
            return updated_user
    raise HTTPException(status_code=404, detail="User not found")

@app.delete("/users/{user_id}", status_code=204)
async def delete_user(user_id: int):
    for idx, user in enumerate(users_db):
        if user.id == user_id:
            users_db.pop(idx)
            return
    raise HTTPException(status_code=404, detail="User not found")
```

### JWT Authentication

```python
from datetime import datetime, timedelta
from jose import JWTError, jwt
from passlib.context import CryptContext
from fastapi import Depends, HTTPException, status
from fastapi.security import OAuth2PasswordBearer, OAuth2PasswordRequestForm

# Configuration
SECRET_KEY = "your-secret-key-here"
ALGORITHM = "HS256"
ACCESS_TOKEN_EXPIRE_MINUTES = 30

pwd_context = CryptContext(schemes=["bcrypt"], deprecated="auto")
oauth2_scheme = OAuth2PasswordBearer(tokenUrl="token")

# Password utilities
def verify_password(plain_password: str, hashed_password: str) -> bool:
    return pwd_context.verify(plain_password, hashed_password)

def get_password_hash(password: str) -> str:
    return pwd_context.hash(password)

# Token utilities
def create_access_token(data: dict, expires_delta: timedelta | None = None):
    to_encode = data.copy()
    if expires_delta:
        expire = datetime.utcnow() + expires_delta
    else:
        expire = datetime.utcnow() + timedelta(minutes=15)
    
    to_encode.update({"exp": expire})
    encoded_jwt = jwt.encode(to_encode, SECRET_KEY, algorithm=ALGORITHM)
    return encoded_jwt

async def get_current_user(token: str = Depends(oauth2_scheme)):
    credentials_exception = HTTPException(
        status_code=status.HTTP_401_UNAUTHORIZED,
        detail="Could not validate credentials",
        headers={"WWW-Authenticate": "Bearer"},
    )
    
    try:
        payload = jwt.decode(token, SECRET_KEY, algorithms=[ALGORITHM])
        username: str = payload.get("sub")
        if username is None:
            raise credentials_exception
    except JWTError:
        raise credentials_exception
    
    # Get user from database
    user = get_user_from_db(username)
    if user is None:
        raise credentials_exception
    
    return user

@app.post("/token")
async def login(form_data: OAuth2PasswordRequestForm = Depends()):
    user = authenticate_user(form_data.username, form_data.password)
    if not user:
        raise HTTPException(
            status_code=status.HTTP_401_UNAUTHORIZED,
            detail="Incorrect username or password",
            headers={"WWW-Authenticate": "Bearer"},
        )
    
    access_token_expires = timedelta(minutes=ACCESS_TOKEN_EXPIRE_MINUTES)
    access_token = create_access_token(
        data={"sub": user.username},
        expires_delta=access_token_expires
    )
    
    return {"access_token": access_token, "token_type": "bearer"}

@app.get("/users/me")
async def read_users_me(current_user: User = Depends(get_current_user)):
    return current_user
```

### Database Integration with SQLAlchemy

```python
from sqlalchemy import create_engine, Column, Integer, String, Boolean
from sqlalchemy.ext.declarative import declarative_base
from sqlalchemy.orm import sessionmaker, Session
from fastapi import Depends

# Database setup
DATABASE_URL = "postgresql://user:password@localhost/dbname"

engine = create_engine(DATABASE_URL)
SessionLocal = sessionmaker(autocommit=False, autoflush=False, bind=engine)
Base = declarative_base()

# Database models
class UserDB(Base):
    __tablename__ = "users"
    
    id = Column(Integer, primary_key=True, index=True)
    name = Column(String, index=True)
    email = Column(String, unique=True, index=True)
    hashed_password = Column(String)
    is_active = Column(Boolean, default=True)

# Create tables
Base.metadata.create_all(bind=engine)

# Dependency
def get_db():
    db = SessionLocal()
    try:
        yield db
    finally:
        db.close()

# API endpoints with database
@app.post("/users", response_model=User)
async def create_user_db(user: UserCreate, db: Session = Depends(get_db)):
    db_user = UserDB(
        name=user.name,
        email=user.email,
        hashed_password=get_password_hash(user.password)
    )
    db.add(db_user)
    db.commit()
    db.refresh(db_user)
    return db_user

@app.get("/users/{user_id}", response_model=User)
async def get_user_db(user_id: int, db: Session = Depends(get_db)):
    db_user = db.query(UserDB).filter(UserDB.id == user_id).first()
    if db_user is None:
        raise HTTPException(status_code=404, detail="User not found")
    return db_user
```

### GraphQL API with Strawberry

```python
import strawberry
from typing import List
from fastapi import FastAPI
from strawberry.fastapi import GraphQLRouter

@strawberry.type
class User:
    id: int
    name: str
    email: str
    is_active: bool

@strawberry.type
class Query:
    @strawberry.field
    def user(self, id: int) -> User | None:
        # Get user from database
        return get_user_from_db(id)
    
    @strawberry.field
    def users(self) -> List[User]:
        # Get all users from database
        return get_all_users_from_db()

@strawberry.type
class Mutation:
    @strawberry.mutation
    def create_user(self, name: str, email: str) -> User:
        # Create user in database
        return create_user_in_db(name, email)
    
    @strawberry.mutation
    def update_user(self, id: int, name: str | None = None, 
                    email: str | None = None) -> User:
        # Update user in database
        return update_user_in_db(id, name, email)

schema = strawberry.Schema(query=Query, mutation=Mutation)

# Add to FastAPI
graphql_app = GraphQLRouter(schema)
app.include_router(graphql_app, prefix="/graphql")
```

### Rate Limiting

```python
from slowapi import Limiter, _rate_limit_exceeded_handler
from slowapi.util import get_remote_address
from slowapi.errors import RateLimitExceeded

limiter = Limiter(key_func=get_remote_address)
app.state.limiter = limiter
app.add_exception_handler(RateLimitExceeded, _rate_limit_exceeded_handler)

@app.get("/limited")
@limiter.limit("5/minute")
async def limited_endpoint(request: Request):
    return {"message": "This endpoint is rate limited"}
```

## 🎯 Best Practices

### 1. API Versioning

```python
from fastapi import APIRouter

# Version 1
router_v1 = APIRouter(prefix="/api/v1")

@router_v1.get("/users")
async def get_users_v1():
    return {"version": "1.0", "users": []}

# Version 2
router_v2 = APIRouter(prefix="/api/v2")

@router_v2.get("/users")
async def get_users_v2():
    return {"version": "2.0", "users": [], "metadata": {}}

app.include_router(router_v1)
app.include_router(router_v2)
```

### 2. Error Handling

```python
from fastapi import HTTPException, Request
from fastapi.responses import JSONResponse

class APIError(Exception):
    def __init__(self, status_code: int, detail: str):
        self.status_code = status_code
        self.detail = detail

@app.exception_handler(APIError)
async def api_error_handler(request: Request, exc: APIError):
    return JSONResponse(
        status_code=exc.status_code,
        content={"error": exc.detail}
    )
```

### 3. Request Validation

```python
from pydantic import BaseModel, validator, EmailStr

class UserCreate(BaseModel):
    name: str
    email: EmailStr
    password: str
    
    @validator('name')
    def name_must_not_be_empty(cls, v):
        if not v.strip():
            raise ValueError('name cannot be empty')
        return v
    
    @validator('password')
    def password_strength(cls, v):
        if len(v) < 8:
            raise ValueError('password must be at least 8 characters')
        return v
```

### 4. Response Models

```python
from pydantic import BaseModel

class UserResponse(BaseModel):
    id: int
    name: str
    email: str
    
    class Config:
        from_attributes = True  # For SQLAlchemy models

@app.get("/users/{user_id}", response_model=UserResponse)
async def get_user(user_id: int):
    return get_user_from_db(user_id)
```

## 🔗 Related Repositories

- [learning-internal-development-platform](https://github.com/vanHeemstraSystems/learning-internal-development-platform) - Main overview
- [learning-idp-python-azure-sdk](https://github.com/vanHeemstraSystems/learning-idp-python-azure-sdk) - Azure SDK fundamentals
- [learning-idp-test-driven-development](https://github.com/vanHeemstraSystems/learning-idp-test-driven-development) - API testing
- [learning-idp-containerization](https://github.com/vanHeemstraSystems/learning-idp-containerization) - API containerization
- [learning-idp-observability](https://github.com/vanHeemstraSystems/learning-idp-observability) - API monitoring

## 🤝 Contributing

This is a personal learning repository, but suggestions and improvements are welcome!

1. Fork the repository
1. Create a feature branch
1. Make your changes with tests
1. Ensure all tests pass
1. Submit a pull request

## 📄 License

This project is for educational purposes. See LICENSE file for details.

## 📧 Contact

Willem van Heemstra

- GitHub: [@vanHeemstraSystems](https://github.com/vanHeemstraSystems)
- LinkedIn: [Willem van Heemstra](https://www.linkedin.com/in/willemvanheemstra/)

-----

*Last updated: December 18, 2025*
*Part of the learning-internal-development-platform series*
