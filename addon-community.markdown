# Ember Addon Community
## Finding Ember Addons
- Searching `npm` with the keyword `ember-addon`
- <http://emberobserver.com>

## How to Choose Addons
- Use Ember Observer
- Every dependency is a liability (think `left-pad`)
- Filter by score
  - Sustainability: how frequently the addon is updated, how many maintainers
  - Popularity: top 10% of downloads for all addons
  - Interest: top 10% of github stars
  - Maintained: commits and releases in the last 3 months
  - Being "active": having a repo, open source
  - Tested: having tests, and having continous integration builds
  - Documentation: how to use addon
- Eliminate addons that haven't been updated in the last 6 months
- Examine the API and code
- Look at issues and PRs
- Try it out

## Maintaing an Addon
- Maintainers want 10/10 on Ember Observer scores, causes people to improve the
  quality of the addons
- Testing is important
- Don't bring in unnecessary dependencies
- Test against different Ember versions using `ember-try`
- Test against Ember canary versions
- Collaborate with other addon maintainers to create general solutions
- Write good documentation
- Semantic versioning makes it easier to understand when breaking changes
  happens
- Have a 1.0
- Beware of private Ember APIs, don't use them unless absolutely necessary,
  potentially only experimenting with the addon
- Don't pollute logs and build outputs, make logging configurable
- Be aware of deprecations, fix deprecated code quickly
- Be open to community contribution
- Your addon might spawn it's own addon ecosystem (for example
  `ember-cli-deploy`, `liquid-fire`)
- Fill out everything in `package.json` for searchability

## Experiments and Proof of Concepts
- `ember-concurrency`
- `ember-engines`
- `ember-computed-decorators`

## Polyfills
- Support legacy classes
- Allow using new features in older versions

## Running `ember-try` Against Top Addons
- Ember Observer now runs `ember-try` against top addons to determine which
  versions of Ember addons support
- Experimenting with running against Ember Canary to determine if updates break
  addons
