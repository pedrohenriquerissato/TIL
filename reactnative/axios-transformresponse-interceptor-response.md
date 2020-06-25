# Axios - transformResponse and Interceptor Response

Do not use transformResponse at endpoint call if you have a
interceptor.response.use.

Interceptor receives a complete response from server, while transformeResponse
only receives data and headers.

If an error occurs (anything != from 2xx status code) on transformResponse, it
will try to transformData anyways AND won't bypass error status code to
interceptor, since it does not have it.

Instead, use it like this:

```javascript
axios.get($endpoint, data).then((response) => {
  /*do your data transform*/
});
```

[source](https://stackoverflow.com/questions/53727709/handling-401-in-axios-when-using-both-interceptors-and-transformresponse)  
[source](https://blog.logrocket.com/how-to-make-http-requests-like-a-pro-with-axios/)
