# BoilerPlates.Mongo_Admin

![Docker](https://img.shields.io/badge/Docker-Ready-blue?logo=docker)
![MongoDB](https://img.shields.io/badge/MongoDB-7.0-green?logo=mongodb)
![License](https://img.shields.io/badge/License-MIT-yellow)

A boilerplate setup for running **MongoDB** with **Mongo Express** using Docker Compose.
This repository provides an easy way to spin up a MongoDB database along with a web-based admin interface for managing your collections and documents.

---

## 🚀 Features

- MongoDB database in a Docker container
- Mongo Express for web-based database administration
- Persistent storage with Docker volumes
- Simple configuration via environment variables

---

## 📂 Project Structure

```
BoilerPlates.Mongo_Admin/
│── docker-compose.yml
│── .env
│── README.md
```

---

## ⚙️ Setup

### 1. Clone the repository

```bash
git clone https://github.com/ThisIsTheWizard/BoilerPlates.Mongo_Admin.git
cd BoilerPlates.Mongo_Admin
```

### 2. Configure environment variables

Edit the `.env` file (sample provided) to set database credentials:

```env
# -------------------------
# MongoDB Settings
# -------------------------
MONGO_INITDB_ROOT_USERNAME=mongo
MONGO_INITDB_ROOT_PASSWORD=mongo
MONGO_INITDB_DATABASE=mongo

# -------------------------
# Mongo Express Settings
# -------------------------
# Login for Mongo Express UI
ME_CONFIG_BASICAUTH_USERNAME=mongo
ME_CONFIG_BASICAUTH_PASSWORD=mongo

# Connection to MongoDB
ME_CONFIG_MONGODB_ADMINUSERNAME=mongo
ME_CONFIG_MONGODB_ADMINPASSWORD=mongo
ME_CONFIG_MONGODB_ENABLE_ADMIN=true
ME_CONFIG_MONGODB_PORT=27017
ME_CONFIG_MONGODB_SERVER=mongo
```

### 3. Start services

```bash
docker-compose up -d
```

---

## 🌐 Access

- **MongoDB** → `localhost:27017`
- **Mongo Express** → [http://localhost:8081](http://localhost:8081)

  - Login with the credentials from `.env`

---

## 📖 Usage

1. Open Mongo Express in your browser.
2. Manage databases, collections, and documents directly in the UI.
3. To connect with **MongoDB Compass** (desktop app), use:

   ```
   mongodb://mongo:mongo@localhost:27017/
   ```

---

## 🛠️ Commands

- Start containers:

  ```bash
  docker-compose up -d
  ```

- Stop containers:

  ```bash
  docker-compose down
  ```

- View logs:

  ```bash
  docker-compose logs -f
  ```

---

## 📦 Volumes

Data is persisted via Docker volumes:

- `mongo_data` → Stores MongoDB database files
- `mongo_express_data` → Stores Mongo Express configuration

---

## 📝 License

This boilerplate is provided under the MIT License.
Feel free to use and modify it for your projects.

---

👋 Created by [Elias Shekh](https://eliasshekh.com)  
If you find this useful, ⭐ the repo or reach out!
