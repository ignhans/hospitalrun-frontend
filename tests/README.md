### How to write Unit tests in Ember
TODO

### How Hospital Run implements unit tests 
TODO

### How to run unit tests
* Run the ember test server: `ember test --server` 
  - This will monitor for changes to the source or the test and run them automatically.
* Hint: Add `&nocontainer=hidden` to testem results viewer to get rid of nasty white div:
http://localhost:7357/8986/tests/index.html?module=NavMenuComponent&nojshint=true&nocontainer=hidden

### Troubleshooting
* in order to troubleshoot some strange failures use recommendations from [the Ember debugging page](https://guides.emberjs.com/v2.18.0/configuring-ember/debugging/). Particularly, for promises add the following in the `test-helper.js`

```javascript
import { assert } from '@ember/debug';
import RSVP from 'rsvp';

RSVP.on('error', function(error) {
  assert(error, false);
});
```