# Local Storage

## [Local Storage and How To Use It On Websites](https://www.smashingmagazine.com/2010/10/local-storage-and-how-to-use-it/)

### [Adding State To The Web: The “Why” Of Local Storage](https://www.smashingmagazine.com/2010/10/local-storage-and-how-to-use-it/#adding-state-to-the-web-the-why-of-local-storage)

- HTTP is stateless, meaning nothing is saved by the protocol
- Usually session informaiton is stored server-side, but typically requires a user to sign up
- **Local storage** is saved to the user's computer

### [C Is For Cookie. Is That Good Enough For Me?](https://www.smashingmagazine.com/2010/10/local-storage-and-how-to-use-it/#c-is-for-cookie-is-that-good-enough-for-me)

Cookies can be used for local storage but have limitations:

> - They add to the load of every document accessed on the domain.
> - They allow up to only 4 KB of data storage.
> - Because cookies have been used to spy on people’s surfing behavior, security-conscious people and companies turn them off or request to be asked every time whether a cookie should be set.

### [Using Local Storage In HTML5-Capable Browsers](https://www.smashingmagazine.com/2010/10/local-storage-and-how-to-use-it/#using-local-storage-in-html5-capable-browsers)

In modern browsers local storage can be used by JavaScript via the `localStorage` object using the `setItem()` and `getItem()` methods. For example:

 ``` javascript
 localStorage.setItem('favoriteflavor','vanilla');
 ```

If you read out the favoriteflavor key, you will get back “vanilla”:

``` javascript
var taste = localStorage.getItem('favoriteflavor');
// -> "vanilla"
```

To remove the item, you can use — can you guess? — the `removeItem()` method:

 ``` javascript
localStorage.removeItem('favoriteflavor');
var taste = localStorage.getItem('favoriteflavor');
// -> null
 ```

`sessionStorage` can be used instead of `localStorage` to maintain the data only until the browser window closes.

### [Working Around The “Strings Only” Issue](https://www.smashingmagazine.com/2010/10/local-storage-and-how-to-use-it/#working-around-the-strings-only-issue)

- A shortcoming of the local storage is that it can only hold data in strings.
- `JSON.stringify()` and `JSON.parse()` native methods are used to convert and parse objects as strings

### Use Cases

1. [Local Storage of Web Service Data](https://www.smashingmagazine.com/2010/10/local-storage-and-how-to-use-it/#use-case-1-local-storage-of-web-service-data)
    1. Local caching can save time later for longer/slower downloads once they've already been downloaded once
    2. Limit the frequency with which data is downloaded, potentiallu saving bandwith and compute costs.
2. [Maintaining The State Of An Interface The Simple Way](https://www.smashingmagazine.com/2010/10/local-storage-and-how-to-use-it/#use-case-2-maintaining-the-state-of-an-interface-the-simple-way)

### [The Dark Side Of Local Storage](https://www.smashingmagazine.com/2010/10/local-storage-and-how-to-use-it/#the-dark-side-of-local-storage)

> Research shows there's a need to look at HTML5’s features and add-ons from a security perspective very soon to make sure that people can’t record user actions and information without the user’s knowledge.

---

1. Why would a developer use local storage for a web application? **HTTP is stateless, meaning nothing is saved by the protocol. Local storage can preserve/maintain state between sessions.**
2. What information should not be stored in local storage? **Local storage should never be used for sensitive information such as passwords or personal information**
3. Local storage can store what type of data? How would you convert it to that type before storing? **Local storage can store object properties that have been stringify-ed.**

---

## Further Reading

[The Past, Present, and Future of Local Storage for Web Applications](http://diveinto.html5doctor.com/storage.html)
