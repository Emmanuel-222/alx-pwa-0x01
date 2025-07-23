# MoviesDatabase API Integration

This README provides a comprehensive overview of how to use the MoviesDatabase API available on RapidAPI. It covers endpoints, request/response formats, authentication, error handling, and usage best practices.

---

## API Overview

The **MoviesDatabase API** is a free and easy-to-use API that allows you to search and fetch information about movies, TV shows, actors, and film crews. It provides data such as movie titles, release years, genres, poster URLs, and cast lists. This API is useful for building entertainment-related apps, movie search tools, and media catalogues.

---

## Version

The current version of the API (as listed on RapidAPI) is: **v2.2.1**

---

## Available Endpoints

Below are the key endpoints provided by the API:

- **`GET /titles/search/title/{title}`**  
  Search for movies or shows by title.

- **`GET /titles/{titleId}`**  
  Get detailed information about a specific title using its unique ID.

- **`GET /titles/random`**  
  Fetch a random movie or show.

- **`GET /titles`**  
  Get a paginated list of movies or shows.

- **`GET /titles/search/keyword/{keyword}`**  
  Search for titles by keyword.

- **`GET /titles/x/upcoming`**  
  Get upcoming titles (e.g., movies releasing soon).

- **`GET /actors/{actorId}`**  
  Get detailed information about an actor.

- **`GET /actors/{actorId}/titles`**  
  Get a list of titles associated with a particular actor.

---

## Request and Response Format

### Example Request:
```http
GET https://moviesdatabase.p.rapidapi.com/titles/search/title/avengers

## Authentication
To access the MoviesDatabase API, you must:

Subscribe to the API on RapidAPI.

Use the following headers in each request:

http
Copy
Edit
X-RapidAPI-Key: YOUR_API_KEY
X-RapidAPI-Host: moviesdatabase.p.rapidapi.com

## Error Handling
Common error responses:

401 Unauthorized:
You didn't provide a valid API key or the key has been revoked.
✅ Fix: Ensure you're passing the correct headers.

403 Forbidden:
Access to the endpoint is not allowed, possibly due to subscription tier.
✅ Fix: Check your RapidAPI plan and endpoint permissions.

404 Not Found:
The resource (title, actor, etc.) does not exist.
✅ Fix: Verify the ID or search term.

429 Too Many Requests:
You've exceeded the usage limits.
✅ Fix: Implement rate limiting or retry logic.

Usage Limits and Best Practices
Limits:
The free tier typically allows 500 requests per month.

Each request should comply with the rate limit set by your subscription.