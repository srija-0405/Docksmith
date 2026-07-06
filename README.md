# Docksmith

Docksmith is a lightweight Docker-inspired container build and runtime system developed as part of a collaborative systems programming project.

It demonstrates the core concepts behind containerization, including image building, content-addressed storage, build caching, layered file systems, and Linux process isolation. The project provides a simplified implementation of Docker's image creation and execution workflow for educational purposes.

---

## Features

- Build container images using a **Docksmithfile**
- Support for Docker-like instructions:
  - `FROM`
  - `COPY`
  - `RUN`
  - `WORKDIR`
  - `ENV`
  - `CMD`
- Deterministic build caching
- Content-addressed immutable image layers
- Linux process isolation using `chroot` and `unshare`
- Lightweight runtime without a background daemon
- Local image management under `~/.docksmith/`

---

## Tech Stack

**Language**
- C++

**Operating System**
- Linux

**Concepts**
- Containerization
- Process Isolation
- Filesystem Layering
- Build Caching

**Tools**
- Git
- GitHub
- Make
- GCC

---

## Project Structure

```text
Docksmith/
├── include/
├── src/
├── sample_app/
├── tests/
├── Makefile
├── Docksmithfile
└── README.md
```

---

## Installation

Clone the repository

```bash
git clone https://github.com/srija-0405/Docksmith.git
```

Build the project

```bash
make
```

Run Docksmith

```bash
./docksmith
```

A sample application is included in the `sample_app` directory to demonstrate image building and container execution.

---

## How It Works

Docksmith follows a simplified container workflow:

1. Reads and parses a Docksmithfile.
2. Builds container image layers.
3. Stores layers using content-addressed storage.
4. Reuses cached layers when possible.
5. Launches isolated processes using Linux namespaces and `chroot`.

---

## My Contribution

This project was developed collaboratively as part of a course project.

My contributions included:

- Implementing assigned features and functionality.
- Collaborating on system integration.
- Testing and debugging.
- Using Git and GitHub for collaborative development.

---

## Future Enhancements

- Networking support
- Volume mounting
- Multi-stage builds
- Image registry support
- Container monitoring
- Resource limits (CPU and memory)

---

## License

This project was developed for academic purposes as part of a systems programming course.
