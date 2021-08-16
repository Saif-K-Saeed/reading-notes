# THE PAST, PRESENT & FUTURE OF LOCAL STORAGE FOR WEB APPLICATIONS

##  Web Storage (Present and Future)

Web Storage provides two objects with identical APIs: `window.localStorage` to retain persistent data and `code.sessionStorage`to retain session-only data which is lost when the tab is closed. Domain-specific strings are stored using name/value pairs. Unlike cookies, the storage limit is far larger (at least 5MB) and information is never transferred to the server.

```
// is localStorage available?
if (typeof window.localStorage != "undefined") {

 // store
 localStorage.setItem("hello", "Hello World!");

 // retrieve
 console.log(localStorage.getItem("hello"));

 // delete
 localStorage.removeItem("hello");
}
```

### The advantages of Web Storage

- easy to use with simple name/value pairs
- session and persistent storage options are available
- an event model is available to keep other tabs and windows synchronized
- wide support on desktop and mobile browsers including IE8+
- Web Storage polyfills are available for older browsers which fall-back to cookie and windows.name storage methods

### The disadvantages

- string values only — serialization may be necessary
- unstructured data with no transactions, indexing or searching facilties
- may exhibit poor performance on large datasets

by ***Saif Saeed***  [GitHup](https://github.com/Saif-K-Saeed)
