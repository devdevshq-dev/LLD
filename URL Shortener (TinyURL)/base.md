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

### Insides of the Primary Server
- prefix of long url: Not a valid approach
- random number generator 10^9 10 characters
    - base62 encoding, 0-9, A-Z, a-z
    - 62^6 = 56B
    - Birthday paradox
    - 880k collisions
    - we just need to check for collisions first
- Hash of the long url
    - md5(longUrl) -> hash -> base62(hash)[:6]
    - same as above
- Counter
    - incrementing a counter -> base62
    - predictibility whichi is bad for security
        - "warning, do no shorten private urls"
        - rate limiting (users cannot scrape all urls)
    - bijective function (base62 the number generated from counter)
        - squids.ord

## Design fulfilling non functional requirements
<img width="1051" height="891" alt="HLD rate limiter drawio" src="https://github.com/user-attachments/assets/d546fd58-8adf-4e67-961b-3bebb4b2dd4c" />
