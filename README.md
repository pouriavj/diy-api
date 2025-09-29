# DIY API - JokeAPI



**DIY API** is a simple RESTful API that serves a collection of 100 jokes. Users can retrieve jokes, filter by type, add new jokes, update existing ones, and delete jokes through various endpoints. Built with **Node.js** and **Express**.


## 🚀 Features

- Fetch a **random joke** from the collection.
- Retrieve a **specific joke** by its ID.
- **Filter jokes** by type (e.g., Puns, Science, Wordplay, Movies, etc.).
- **Add new jokes** to the collection using POST requests.
- **Update existing jokes** using PUT or PATCH requests.
- **Delete a specific joke** or **all jokes** (requires master key for all deletion).
- Fully documented with a **Postman collection** for testing.

---


## 💻 How to Run the Project

1. **Clone the repository**
```bash
git clone https://github.com/pouriavj/diy-api.git
cd diy-api
```
2. **Install dependencies**
```bash
npm install
```
3. **Start the server**
```bash
node index.js
```
<p>The API server will run on: http://localhost:3000</p>

---

## 🚀 API Endpoints

### 1. Get a random joke
**Endpoint:** `GET /random`  
**Description:** Returns a random joke from the collection.

### 2. Get a specific joke
**Endpoint:** `GET /jokes/:id`  
**Description:** Returns the joke that matches the specified `id`.

### 3. Filter jokes by type
**Endpoint:** `GET /filter?type=<jokeType>`  
**Description:** Returns all jokes of a specific type.  
**Example:** `/filter?type=Puns`

### 4. Add a new joke
**Endpoint:** `POST /jokes`  
**Body Parameters:**
- `type` (string): The type of the joke.
- `text` (string): The text of the joke.

**Description:** Adds a new joke to the collection and returns it.

### 5. Update a joke
**Endpoint:** `PUT /jokes/:id`  
**Body Parameters:**
- `type` (string): Updated joke type.
- `text` (string): Updated joke text.

**Description:** Replaces the joke with the specified `id`.

### 6. Update part of a joke
**Endpoint:** `PATCH /jokes/:id`  
**Body Parameters (optional):**
- `type` (string): Updated joke type.
- `text` (string): Updated joke text.

**Description:** Updates only the provided fields of the joke.

### 7. Delete a specific joke
**Endpoint:** `DELETE /jokes/:id`  
**Description:** Deletes the joke with the specified `id`.

### 8. Delete all jokes
**Endpoint:** `DELETE /all`  
**Headers:**
- `masterkey` (string): Required master key to delete all jokes.

**Description:** Deletes all jokes if the correct master key is provided.

---
## 📚 API Documentation

You can explore and test all endpoints using the provided **Postman collection** or by visiting the published API documentation.

**Postman Collection**  
- Download the Postman collection file from the repository: `diy-api.postman_collection.json`  
- Import it into Postman to see all endpoints pre-configured.

**Published Documentation**  
- A web version of the API documentation is available at: [API Docs Link](your-docs-link-here)  
- Browse all endpoints, example requests, and responses interactively.
---
