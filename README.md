# Dotnet-GitHub-actions-test

This project is majorly for testing GitHub actions and different tagging structures in regards to Flux Toolkits image policies.

## Structure
Commits to PR builds and pushes an image to ACR with Flux structure `22c70de-1666677393` which is done with `SHORT_SHA-date +%s`.

Commits/merges to main builds and pushes an image to ACR with Flux structure `22c70de-1666677393` which is done with `SHORT_SHA-date +%s` as well as `latest`.

Push tags with semver `X.Y.Z` or `X.Y.Z-PRE` takes the latest image tag, pulls it down, retag with the given GitHub tag.

```
git tag --list #To check the last tags
git tag 1.0.0
git push --tags
```

**References**:
- https://fluxcd.io/flux/
- https://fluxcd.io/flux/guides/sortable-image-tags/
