# strut-software

The `stadeum/software` bundle for [strut](https://github.com/stakwork/strut):
one thing to follow that brings a team's code to its box.

A bundle holds no code. Its `strut.yaml` lists other packages by the branch
each is followed at, and following this repository follows each of them:

| Package | Repository | What it brings |
| --- | --- | --- |
| `stadeum/github` | [strut-github](https://github.com/stakwork/strut-github) | A person connects their GitHub account; an admin picks repositories |
| `stadeum/pods` | [strut-pods](https://github.com/stakwork/strut-pods) | A machine of its own for every coding job |
| `stadeum/code` | [strut-code](https://github.com/stakwork/strut-code) | The repositories a box works on, their workspaces, and the Code app |

Each package moves on its own branch and waits for its own secrets, so a
release of one needs no release of this bundle. The person who follows the
bundle is the person of everything it brings.

A box follows the `stable` branch:

```text
git+https://github.com/stakwork/strut-software@stable
```

`stable` moves only on purpose. To move it to `main`:

```bash
git push origin main:stable
```

A team on another forge follows a bundle that lists that forge's package in
place of `stadeum/github`.
