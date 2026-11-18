# Copyright 2026 Chainguard, Inc.
# SPDX-License-Identifier: Apache-2.0
#
# Remote-access violation fixture.
#
# Installs dropbear (a banned remote-access package) so the
# RemoteAccessServices OVAL check must detect the package record under
# /usr/lib/apk/db/installed and every RemoteAccessServices-backed rule
# must FAIL.
FROM cgr.dev/chainguard/wolfi-base:latest@sha256:e9b8c3739e5fb5fc778843a2ce74f8620588c9ddc9c44918cead527abcb0b628

LABEL dev.orbstack.add-ca-certificates=false

USER root

RUN apk add --no-cache dropbear
