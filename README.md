# ZMK Firmware: Personal fork

This is my personal ZMK fork containing various experimental features. It is regularly
rebased onto the latest upstream. Below is a list of features
currently included in the `main` branch *on top of* the official ZMK master branch.

* **mouse** (PR #778) - latest rebase: https://github.com/ftc/zmk/tree/mouse-ftc
* **masked-mods** (PR #1412) - PR branch: https://github.com/urob/zmk/tree/fix-mod-morph
* **global-quick-tap-ms** (PR #1387) - PR branch: https://github.com/andrewjrae/zmk/tree/min-prior-ms
* **num-word** (PR #1451) - PR branch: https://github.com/urob/zmk/tree/improve-caps-word
* **positional-hold-tap-on-release** (PR #1423) - PR branch: https://github.com/urob/zmk/tree/positional-hold-tap-on-release

In order to use this branch with Github Actions, replace the contents of `west.yml` in
your `zmk-config/config` directory with the following contents:
```
manifest:
  remotes:
    - name: urob
      url-base: https://github.com/urob
  projects:
    - name: zmk
      remote: urob
      revision: main
      import: app/west.yml
  self:
    path: config
```
