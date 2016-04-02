# Idiomatic Ember
### Overview
1. Data Down Actions Up
2. Bye Bye Controllers
3. Declarative and Composable Templates

### Data Down Actions Up
Two way bindings can cause an infinite loop of updates, avoid this by using a DDAU model.

Only the data owner should modify the data
- All changes to the data made in the UI should send actions that bubble up to the data owner

### Controllers
The latest version of Ember is getting rid of controllers in favor of Routable Components.
- Use a top level app component to future-proof your app
- Move all data-modifying actions to routes
  - UI-related actions can stay in the component
- Prefer closure actions

### Ember Templating Helpers (available in 1.13)
- `get`, `concat`, `add`
- define computed properties, use services, etc.
- when defining helpers, its the only time its ok to use observers
- Theres an ember addon for composable helpers
- Helpers are best suited for UI logic and small repeatable actions

Computed Properties - observed changes are implicit

### Component Hooks
- Can be tricky to use
- Life cycle hooks are good for side-effects instead of putting them in a computed property or callback
- Use them instead of observers
- Must be stable so they can be called every time the run loop executes (can cause infinite loops - be careful!)
