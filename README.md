# strut-software

Everything a team needs to code with agents on Stadeum, in one package:
GitHub, your repos, and a cloud machine for each job.

A bundle holds no code. Its `strut.yaml` lists other packages by the branch
each is followed at, and following this repository follows each of them:

| Package | Repository | What it brings |
| --- | --- | --- |
| `stadeum/github` | [strut-github](https://github.com/stakwork/strut-github) | GitHub integration for the Stadeum GitHub App. Run agents in your repos and open PRs |
| `stadeum/pods` | [strut-pods](https://github.com/stakwork/strut-pods) | A cloud machine for each coding job, with your repos cloned and your app running, so agents can run and test it |
| `stadeum/code` | [strut-code](https://github.com/stakwork/strut-code) | Your team's repos and workspaces, kept up to date, so agents can read and change your code |

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
