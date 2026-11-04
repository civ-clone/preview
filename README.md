# civ.one preview

Builds any branch of [web-renderer](https://github.com/civ-clone/web-renderer) and serves it at **https://civ.one/preview/**, to try a change (on a phone, say) before it's merged.

Run **Deploy a preview** from the Actions tab, or:

```bash
gh workflow run preview.yml --repo civ-clone/preview -f ref=<branch, tag or commit>
```

Each run replaces the last, so there is one preview at a time. The run's summary names the commit it built.

**It shares civ.one's browser storage.** It's the same site, so imported assets, saves and options are shared with the live game. That means no re-import, but a branch that changes the save format can write a save the live game can't read.

This repository holds only the workflow. Nothing from the build is committed here.
