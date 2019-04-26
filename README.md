# haskell-stack-builder-no-postgres-lts-11-14

Docker build container

**Donor** codebase lists most common dependencies. This approach drastically reduces build time

## How to update

1. Change dependencies

2. Commit, push to GitHub
3. Build, tag and push image to DockerHub

```bash
docker build -t donor .
docker tag donor goldenfoil/haskell-stack-builder-no-postgres-lts-11-14:1
docker push goldenfoil/haskell-stack-builder-no-postgres-lts-11-14:1
# :1 is a version tag. it better be changed in the future
```
