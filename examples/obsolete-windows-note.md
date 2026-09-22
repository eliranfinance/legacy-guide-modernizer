# Example: modernizing an obsolete note

## Input

> “Use Run, open `regedit`, change the Internet Settings values, and restart Windows XP to make the browser faster.”

## Safe modernization

**Status:** Likely obsolete  
**Risk:** Medium — registry edits can damage configuration and the claimed performance effect is unsupported.  
**Source:** `old-browser-tips.doc`

### Result

Do not apply the registry edit. First measure the current problem, then use supported browser and operating-system updates, remove unwanted extensions, and check network latency separately from browser performance.

### Verify

Compare a clean browser profile and the normal profile on the same site, record page-load timing, and confirm that the issue is reproducible before changing configuration.

### Why this is better

The historical intent—improve browsing speed—is preserved, while the version-specific command is rejected because it lacks current evidence, is not safely reversible for most users, and confuses browser performance with network performance.
