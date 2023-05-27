---
layout: post
title: WIP with Approvals
---

There's a pattern in Approval Tests that I like -  
Sometimes it makes sense to "approve" a temporary incorrect result as an intermediate step towards implementing the required behavior. This makes the correct result be highlighted by the diff tool when get there.

## Example

## Make it Explicit

I was talking to the very insightful Johan Lodin about this pattern and he immediately suggested this -

> So approve the diff itself. -Johan

What does it mean to "approve the diff itself"?

Usually with approvals the diff we're interested in this:

```
diff = received - approved
```

Where `diff` is ..., `received` is ..., and `approved` is ...

If `diff` is empty - the test passes.  
If `diff` is non-empty - the test fails, and we allow the developer to review the diff and decide whether to "approved" it or not.

Notice that `diff` is ephemeral here, it's lifetime is only for the duration of the approval process. With Johan's suggestion, we'll be adding persistent state for it.

In order to explicitly support the pattern discussed we want to temporarily "lock" an incorrect result, but not "approve" it quite yet. We need a new state for that. Let's call it `doing`.

And a new diff to go along with it -

```
doingDiff = received - doing
```

-   should the test fail or pass?
-   env var
-   on CI
