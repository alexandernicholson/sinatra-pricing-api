# sinatra-pricing-api
A toy price API for fun.

# How to run
```
docker build -t sinatra-pricing-api:latest .
docker run -p 4567:4567 --rm -t docker.io/library/sinatra-pricing-api:latest
```

# API Pricing Rules
* Footwear is always the same price.
* Prices peak at 14:00 UTC and follow a bell curve distribution.
* In 1 in 20 calls, prices will spike by 2x.

# Built in API issues
* All calls have a random additional latency of up to 1s.
* 1 in 10 calls have a random additional latency of up to 10s.
* 1 in 100 calls have an additional latency of 61s.
* 1 in 10 calls will return a 500 error.
* 1 in 20 calls will return a 422 error.
