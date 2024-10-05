[Golang]

The CORS issue can be solve by returning a heading in response from the server


```go
	w.Header().Set("Access-Control-Allow-Origin", "http://localhost:5500")
	w.Header().Set("Access-Control-Allow-Methods", "POST")
	w.Header().Set("Access-Control-Allow-Headers", "Origin, Content-Type, Accept")
	w.Header().Set("Access-Control-Allow-Credentials", "true")
	
```


The above code set's the allow origin header to the host and port from where the request should be accepted, The above is enough to solve the CORS issue without any external libraries.