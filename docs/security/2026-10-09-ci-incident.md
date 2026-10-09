# CI incident containment — 2026-10-09

Repository: `ThreeAndTwo/initia`
Branch: `feat/oracle`
Inspected head: `bce603fc65c1cc6f9ee11a99beddd02a35138622`

Actions were disabled before this cleanup. Keep them disabled until the repository owner explicitly approves restoration.

The owner confirmed that this personal repository must not contain GitHub Actions workflows. This change removes every file under `.github/workflows` on this branch, regardless of its name.

Files removed in this change:

- `.github/workflows/docker.yml` — original Git object `57734e03ff676c985cdb6fe9560f4ca7026a23fb`.
- `.github/workflows/lint.yml` — original Git object `91070b54aae839b51c0ecd8dc2f5b5d4f73f2155`.
- `.github/workflows/test.yml` — original Git object `904165def8ba7502ae155c2de6d1a85de1a521ed`.

Evidence and limits

- Unauthorized workflows were observed attempting credential or repository-history disclosure. A successful workflow run alone does not prove data receipt or credential validity.
- Existing Git history is retained as evidence. No release, tag, force push, or history rewrite is part of this cleanup.
- Revoking a GitHub token does not rotate credentials issued by other services.
- The initial credential compromise and the authentication method used for the mass write remain under investigation.
- This record supersedes any earlier note suggesting that personal-repository workflows should be retained.
