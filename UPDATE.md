# UPDATE

* Replaced 'https' library with 'request' for http requests
* Added proxy options to the request

## Old interface: 
```javascript
let board = new LeanKitBoard({
    email: 'my.name@leankit.com',
    pass: 'abcd1234',
    host: 'myaccount.leankit.com',
    port: 1234,
    boardId: '01234567'
})
```

## New interface:
```javascript
let board = new LeanKitBoard({
    email: 'my.name@leankit.com',
    pass: 'abcd1234',
    url: 'myaccount.leankit.com',
    boardId: '108628328',
    proxy: {                // Optional if you need to send request through a proxy
        host: 'my.company.proxy:1234',          // Required if using proxy
        user: 'myCompanyNetworkUsername',       // Optional, but may be necessary 
        pass: "myCompanyNetworkPassword1234"    // Optional, but may be necessary
    }
})
```