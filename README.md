# kit-build

Builds OpenClaw Enterprise controller and runtime images from a source commit, the way upstream's
`.github/workflows/container-check.yml` builds them (BuildKit, same build arguments, same smoke test), for the
private installer kit `zanetworker/oce-openshift-install`. linux/amd64 only.

This branch shares no history with `main`, so upstream's own workflows don't run here. A push to it builds the
source named in `kit-build.json`. Images go to `ghcr.io/<owner>/oce-{controller,runtime}:sha-<commit>`; the run
summary lists their digests.
