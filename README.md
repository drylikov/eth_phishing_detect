# eth_phishing_detect

Utility for detecting phishing domains targeting Ethereum users.

### basic usage

```js
const checkForPhishing = require('eth_phishing_detect')

const value = checkForPhishing('etherclassicwallet.com')
console.log(value) // true
```

### advanced usage

```js
const PhishingDetector = require('eth_phishing_detect/src/detector')

const detector = new PhishingDetector({ whitelist, blacklist, fuzzylist, tolerance })
const value = detector.check('etherclassicwallet.com')
console.log(value)
/*
{
  type: "blacklist",
  result: true,
}
*/
```