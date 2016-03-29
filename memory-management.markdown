# Memory Management
## Garbage Collection
- Generational
  - Most objects are meant to be short lived
  - Two heaps, young and old
  - After a garbage collection pass, living young objects are moved to old heap
  - Searches through the object dependency graph. Garbage is anything that can't
    be reached from the root.
- Mark and sweep

## Memory Issues
- Not scoping variables correctly
- Too many allocations
- DOM changes

## Ember
- Run loops batch similar changes together
- Run loop queues:
  - Sync: update data bindings
  - Actions: propagate actions
  - Route transitions: don't render anything when navigating away from page
  - Render: only manipulate the DOM once
  - After Render: hook for utilizing DOM information
  - Destroy: cleans up things
