# URL Shortener

A simple URL shortener written in Go. This application generates short URLs using an MD5 hash and allows redirection to the original URLs.

## Features
- Generate short URLs for long URLs
- Store and retrieve shortened URLs in memory
- Redirect users from short URLs to the original URLs

## Installation
### Prerequisites
- Install [Go](https://golang.org/dl/)

### Clone the Repository
```sh
git clone https://github.com/alokkcode/GoShortly
cd GoShortly
```

### Initialize the Project
```sh
go mod init url-shortener
go mod tidy
```

## Usage
### Run the Server
```sh
go run main.go
```
The server will start on port `3000`.

### API Endpoints
#### 1. Shorten a URL
**Endpoint:** `POST /shorten`

**Request:**
```json
{
  "url": "https://example.com"
}
```

**Response:**
```json
{
  "short_url": "d9736711"
}
```

#### 2. Redirect to Original URL
**Endpoint:** `GET /redirect/{short_url}`

Example:
```sh
curl -L http://localhost:3000/redirect/d9736711
```

## License
This project is open-source and available under the MIT License.

## Contributing
Feel free to submit issues and pull requests!

## Author
[Alok Kumar](https://github.com/alokkcode)

