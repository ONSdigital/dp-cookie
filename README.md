# dp-cookie
Golang library for setting/getting specific cookies

## Setting a cookie using dp-cookies library

```
package handler

import (
    ...
    "github.com/ONSdigital/dp-cookies/cookies"
    ...
)

// Set user auth token cookie

func myHandler(w http.ResponseWriter, req *http.Request, ...) {
    ...
    cookies.SetUserAuthToken(w, userAuthToken, "www.domain.com")
    ...
}
```

## Getting a cookie using dp-cookies library

```
package handler

import (
    ...
    "github.com/ONSdigital/dp-cookies/cookies"
    ...
)

// Get user auth token value from cookie

func myHandler(w http.ResponseWriter, req *http.Request, ...) {
    ...
    token, err := cookies.GetUserAuthToken(req)
    ...
}
```