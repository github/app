# Feature flag configuration

[`feature-flags.json`](./feature-flags.json) is a global, disable-only list. `revision` must be a positive, monotonically increasing integer and increment with every payload change. `forceDisabledFlags` lists flag IDs to force off; an empty list restores normal resolution without enabling flags.
