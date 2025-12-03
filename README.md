# IMPORTANT!
Please note that **this is not my code.** This code was written by [Bob Newell.](https://www.bobnewell.net/filez/poetry.el)

Please note that this is a literal poetry aid, and **NOT** to be confused with the [Python dependency package over here.](https://github.com/cybniv/poetry.el)

This is *technically* a fork now. I originally meant to only mirror the code, but I have made a change (please read below.)

## Changes from Original Package

I commented out line 244. When enabled, the line breaks visual formatting in `org-mode` because it derives from `text-mode`. 

So far, it works fine (Jinx seems to be highlighting the syllables as mispellings though) commented out, but if you forsee using `text-mode` mainly, I would recommend forking and uncommenting it.

I may explore a hook to re-enable in text-mode.

## How to use?

### Requirements

TODO: I will write this soon.

### Emacs Install
If you're using Emacs 29+, I **highly** recommend you use `package-vc`. This is built-in. You can just copy the following:

```el
(use-package poetry
  :vc (:url "https://github.com/subsevenx/poetry.el" :branch "main" :rev :newest))
```

You can also use straight.el:

```el
(use-package poetry
  :straight (poetry :type git :host github :repo "subsevenx/poetry.el" :branch "main"))
```

Or quelpa.el:

```el
(use-package poetry
  :quelpa (poetry :fetcher github :repo "subsevenx/poetry.el" :branch "main"))
```
