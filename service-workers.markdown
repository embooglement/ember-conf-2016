# Service Workers
## Hospital Run
- Open Source software for developing world hospitals

## Service Workers
- Like web workers, run in separate threads
- Run in separate context from main app
- HTTPS only
- https://serviceworke.rs/ by Mozilla
- Service worker debugging in Chrome inspector
- Hard refresh (`shift-cmd-r`) will make `navigator.serviceWorker.controller`
  return `null`
- `ember install broccoli-service-worker`
- Configuration
  - `fallback`: if offline, get different resources
  - `networkFirstRequest`: get from API if possible, fallback to cache
- Google service worker toolbox
- Handling saving and access data offline
- Handling not just _users_, but also _servers_ going offline, or poor wifi
  connection
- Running PouchDB in a service worker dramatically improves performance

## The Future of Ember and Service Workers
- Provide native push notifications to users
- Background sync: actions can be defered until users have stable connectivity
- Not a lot of unit testing for ember service workers
- Safari doesn't support service workers
- Edge is working on it
- Application Cache is deprecated and will be removed in Firefox
- Investigating using service workers with Ember Data
