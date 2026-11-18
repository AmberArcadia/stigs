# Copyright 2026 Chainguard, Inc.
# SPDX-License-Identifier: Apache-2.0
#
# PackageSignature violation fixture.
#
# Injects a non-https repository URL into /etc/apk/repositories so the
# textfilecontent54 pattern ^(?!\s*#)(?!.*https://).+$ must match at
# least one line and the rule must FAIL.
FROM cgr.dev/chainguard/wolfi-base:latest@sha256:e9b8c3739e5fb5fc778843a2ce74f8620588c9ddc9c44918cead527abcb0b628

LABEL dev.orbstack.add-ca-certificates=false

USER root

RUN printf '# vendor-mirror\nhttp://insecure.example.com/alpine\n' >> /etc/apk/repositories
