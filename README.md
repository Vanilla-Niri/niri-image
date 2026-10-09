# Vanilla Niri Image

Containerfile for building a Vanilla Niri image.

> [!IMPORTANT]
> This image is not intended to be used directly. It is used as a base image for other images.
> Like the Vanilla Niri DMS image, etc.
>
> This image is NOT officially regulated by Vanilla OS.

This image is based on top of [`vanillakde/base`](https://github.com/Vanilla-KDE/base-image/pkgs/container/base) and offers the Vanilla OS Desktop experience with Niri WM.

## Build

```bash
vib build recipe.yml
podman image build -t vanillaniri/niri .
```

## Verify Image Build Provenance Attestation

All the image builds/pushes are attested for build provenance and integrity using the [attest-build-provenance`](https://github.com/actions/attest-build-provenance) action. The attestations can be verified [here](https://github.com/Vanilla-Niri/niri-image/attestations) or by having the latest version of [GitHub CLI](https://github.com/cli/cli/releases/latest) installed in your system. Then, execute the following command:

```sh
gh attestation verify oci://ghcr.io/vanilla-niri/niri:latest --owner Vanilla-Niri
```