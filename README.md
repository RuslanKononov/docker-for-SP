# Docker Setup for SmartPay-MVP React App

## Directory Structure

To run Docker properly, make sure the following two directories are on the same level:

```
www/
├── SmartPay-MVP/         # React application
│   ├── package.json
│   ├── src/
│   ├── public/
│   └── tailwind.config.js
└── docker-for-SP/        # Docker files
    ├── docker-compose.yml
    └── Docker/react/Dockerfile
```

> If your directories have different names, update the paths in `docker-compose.yml` and `Dockerfile` accordingly.

---

## Quick Start

1. Navigate to the Docker Compose directory:

```bash
cd docker-for-SP
```

2. Build and start the containers:

```bash
docker-compose up -d --build
```

3. Install dependencies inside the container (optional if already installed during build):

```bash
docker-compose run --rm react-app-dev sh -c "npm install"
```

4. The React application will then be accessible at:

```
http://localhost:3000
```

---

## Notes

- `node_modules` is mounted inside the container, so no need to keep it on the host.
- Any changes in React code are automatically reflected in the container through volumes.
- To stop the container:

```bash
docker-compose down
```

