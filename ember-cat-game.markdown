# Building a Game in Ember Starring Your Cat
## Why Build a Game in Ember
- You are special
- Games require many boiler plate things that Ember can provide

## The Game
- The game is playable at <https://www.croissantthepizzacat.com/>

### Game Menus
- Constructed with routes
- Uses Liquid Fire
  - Take up the whole screen
  - Allows you to specify animations for route transitions
  - Outlets done with `{{liquid-outlet}}`

### Pausing the game
- Game logic and state written as a `Ember.Service`, because it is a long
  lived object that exists regardless of route transitions
- This service has `play` and `pause` methods, and kicks of the game loop
- This service is injected into the menu route.

### Game Loop
- Use `requestAnimationFrame` for drawing things on screen, which is more
  performant and accurate than `setInterval` for rendering

### Deploying
- Web, mobile, and desktop
- `ember-cli-deploy` allows deployments and rollbacks for the web
- `ember-cli-cordova` for mobile deployments
- `ember-electron` for desktop deployments
