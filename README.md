<img align="left" width="250"  src="https://kivigo.github.io/img/logo-kivigo.png" alt="KiviGo Logo" />

# KiviGo Backends

This repository contains all backend modules for the [KiviGo](https://github.com/kivigo/kivigo) key-value store library for Go. Each backend is implemented as a separate Go module, providing a unified interface and minimal dependencies for your applications.

**📄 Documentation**

Full documentation for KiviGo, including backend usage and examples, is available at [https://kivigo.github.io/](https://kivigo.github.io/)

## 📦 Available Backends

See the [Backends overview](https://kivigo.github.io/docs/backends/overview) for a complete list of available backends.

- **[badger](https://kivigo.github.io/kivigo/docs/backends/badger)**: High-performance local storage using BadgerDB
- **[consul](https://kivigo.github.io/kivigo/docs/backends/consul)**: Distributed backend using Consul
- **[etcd](https://kivigo.github.io/kivigo/docs/backends/etcd)**: Distributed backend using etcd
- **[local](https://kivigo.github.io/kivigo/docs/backends/local)**: Simple local storage (BoltDB)
- **[redis](https://kivigo.github.io/kivigo/docs/backends/redis)**: Redis-based backend
- **[azurecosmos](https://kivigo.github.io/kivigo/docs/backends/azurecosmos)**: Azure Cosmos DB backend
- **[dynamodb](https://kivigo.github.io/kivigo/docs/backends/dynamodb)**: AWS DynamoDB backend
- **[memcached](https://kivigo.github.io/kivigo/docs/backends/memcached)**: Memcached backend
- **[mongodb](https://kivigo.github.io/kivigo/docs/backends/mongodb)**: MongoDB backend
- **[mysql](https://kivigo.github.io/kivigo/docs/backends/mysql)**: MySQL backend
- **[postgresql](https://kivigo.github.io/kivigo/docs/backends/postgresql)**: PostgreSQL backend

Each `<backend-name>` directory contains:

- Backend source code
- Unit and integration tests
- A `go.mod` file for dependency management

## 🛠️ Usage

To use a specific backend in your Go project:

```bash
go get github.com/kivigo/backends/<backend>
```

Example for Badger:

```bash
go get github.com/kivigo/backends/badger
```

## 🧪 Testing

Each backend provides its own test suite. To run tests for a backend:

```bash
cd <backend-name>
go test ./...
```

Some backends (Redis, Consul, etcd) require Docker for integration tests.

## 🤖 Continuous Integration

CI checks:

- Build and test for each backend
- Code linting
- Per-backend release publication

See `.github/workflows/` for full configuration.

## 🤝 Contributing

1. Fork the repo and create a branch.
2. Add or improve a backend in `backend/<name>/`.
3. Add tests and update documentation as needed.
4. Ensure all tests and lint checks pass.
5. Open a Pull Request.

Please follow the [main KiviGo project instructions](https://github.com/kivigo/) to ensure consistency and quality.

---

© KiviGo Project – MIT License
