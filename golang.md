# Golang

## Check a golang map for a specific key
```
if val, ok := dict["foo"]; ok {
    //key found - do somehting
} else {
    //Key does not exist
}
```

## echo - decode json from request body
```
func addDog(c echo.Context) errr {
    dog := Dog{}

    err := c.Bind(&dog)
    if err != nil {
        log.Printf("Failed processing addDog request: %s\n", err)
        return echo.NewHTTPError(http.StatusInternalServerError)
    }
    log.Printf("This is your dog: %#v\n", dog)
    return c.String(http.StatusOK, "Got your dog!")
}
```
