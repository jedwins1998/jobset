# Release Process

The Kubernetes Template Project is released on an as-needed basis. The process is as follows:

1. An issue is proposing a new release with a changelog since the last release
2. All [OWNERS](OWNERS) must LGTM this release
3. An OWNER runs `git tag -s $VERSION` and inserts the changelog and pushes the tag with `git push $VERSION`
4. The release issue is closed
5. An announcement email is sent to `dev@kubernetes.io` with the subject `[ANNOUNCE] kubernetes-template-project $VERSION is released`
