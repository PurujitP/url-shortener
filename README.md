## Express Short URL Generator

This Node.js application utilizes Express and MySQL to create a simple short URL generator. Here's a brief summary of the key functionalities:

### Features:

1. **Database Connection:**
   - Connects to a MySQL database on the local server.

2. **Create Short URL:**
   - Generates a unique short URL ID for a given long URL.
   - Inserts the long URL and its corresponding short URL ID into the database.

3. **Retrieve All Short URLs:**
   - Retrieves all entries from the "links" table in the database.

4. **Redirect Short URL:**
   - Redirects to the original long URL when a valid short URL is accessed.
   - Updates the access count in the database.

### How to Use:

1. **Installation:**
   - Install the required dependencies by running `npm install` in the terminal.

2. **Database Setup:**
   - Set up a MySQL database named "shorturls" with a table named "links."
   - The "links" table should have columns: `id`, `longurl`, `shorturlid`, and `count`.

3. **Run the Application:**
   - Execute the application using `node yourFileName.js` in the terminal.
   - The application listens on port 3000.

4. **Access the Application:**
   - Open a web browser and go to [http://localhost:3000](http://localhost:3000) to access the index page.
   - Create short URLs using the provided form.

5. **API Endpoints:**
   - `/api/create-short-url`: POST endpoint to create a new short URL.
   - `/api/get-all-short-urls`: GET endpoint to retrieve all short URLs.

6. **Short URL Redirection:**
   - Accessing `http://localhost:3000/{shorturlid}` redirects to the original long URL.
   - Updates the access count in the database.

### Notes:

- The short URL ID is generated randomly and is unique for each entry.
- Database connection details (host, user, password) are specified during the MySQL connection setup.

Feel free to explore, use, and modify this simple short URL generator for your projects!
