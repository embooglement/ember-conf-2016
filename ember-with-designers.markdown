# Ember Between Design and Development
Lisa Grindl and Francesco Novy

### Collaboration
- Designers should be able to understand code
  - Make HTML/CSS templates
- Engineers should be able to understand design
  - Take those templates and make them Ember-y

### CSS Structure
- Use a consistent naming convention
- Keep the data model separate from the UI, naming wise
- Structure
  - Core Files: variables, etc
  - Modules: for individual components

### Documentation
- Use a living style guide to maintain consistency and communication
- Easier to cross-browser test Components
- Better for onboarding new engineers and designers
- Must always be in sync with the code base
  - JSDoc for Ember or UIDoc (works well with Ember)
    - Use handlebars examples in the comments for that Component
    - Markdown syntax can be used to make more detailed documentation in the code
  - Living Style Guide
    - Start with a UI inventory, look for all instances of a UI Element (buttons, etc)
    - Design Sheet: outline of basic UI direction
    - Make a CSS Partial for every element (\_button.scss, etc.)
    - Add a document to match each file (\_button.md)
    - Gets built together nicely in broccoli-livingstyleguide
- Component Library
  - An additional route in the main app
  - Its template is just a list of all components
  - Also can include code blocks for examples of implementation
    - Include syntax highlighting
  - Gets deployed within the app so make sure to restrict it to just internal users
  
