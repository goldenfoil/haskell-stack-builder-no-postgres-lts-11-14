# haskell-stack-builder-no-postgres-lts-11-14

Docker build container

**Donor** codebase lists most common dependencies. This approach drastically reduces build time

## How to update

1. Change dependencies

2. Commit, push to GitHub

3. Publish. You have 2 options:

    a. Wait for it to build automatically on dockerhub *(check if build is scheduled or trigger build manually)*. In this case tag will not include git commit hash - it will be just `latest`.

    b. Build, tag and push manually:

    ```bash
    # compatibility: both for bash and fish
    bash -c 'docker build -t goldenfoil/haskell-stack-builder-no-postgres-lts-11-14:latest goldenfoil/haskell-stack-builder-no-postgres-lts-11-14:$(git log -1 --pretty=%h) .'

    docker push goldenfoil/haskell-stack-builder-no-postgres-lts-11-14
    ```
