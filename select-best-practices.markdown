# Selecting Good Ember Patterns
## `{{view "select"}}`
- 2 way bindings by default
- No builtin in support for disabling options

## Building a new Ember select component
### Data Down, Actions Up:
- Initial selection flows down
- Change event bubbles up
- Selected is data, it flows down
- Dynamic attributes using handlebars helpers, `{{bind-attr}}` deprecated

### Closure actions
- `(action 'ActionName')`
- More explicit
- Don't need to bubble up manually in deeply nested components

### Dynamic keys
- A lot of overhead for dynamic keys using components
- `{{get foo bar}}` helper allows you to lookup a value directly in templates, don't
  need another component

## Getting two way bindings back
- `(action (mut X))` creates a two-way binding for an action
