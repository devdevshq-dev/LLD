# URL Shortner

## Requirements
### Functional Requirmenets
- create a short url from a long url
    - optionally support custom alias
    - optionally support an expiration time
- be redirected to the original url from the short url

### Non-functional Requirements
- Low latency on redirects (~200ms)
- Scale to support 100 DAU and 1B urls
- Ensure uniqueness of short codes
- High availability, eventual consistency for url shortening

## Core Entities
- Original url
- Short url
- User

## API
- shorten a url
POST /urls -> shortUrl
{
    originalUrl,
    alias?,
    expirationTime?
}

-  redirection
GET /{shortUrl} -> Redirect to OriginalUrl

## High Level Design
<img width="870" height="359" alt="Urlshortner drawio" src="https://github.com/user-attachments/assets/a525e1ba-377e-4eb8-8565-7b6423b6950f" />
