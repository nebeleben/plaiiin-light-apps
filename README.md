# PlaiiinLight — App Downloads

Public download host for the **PlaiiinLight** native client apps. This repo
holds no source — the apps are built from a private repository and published
here as signed, verifiable release assets.

Control your PlaiiinLight LED lamps from a native app: discover them on your
network, compose effects with AI, stream images live, and manage on-device
scripts.

## Download

Grab the latest build from the [**Releases**](../../releases/latest) page.

| Platform | Asset | Notes |
|---|---|---|
| macOS | `PlaiiinLight-<version>.dmg` | Universal (Apple Silicon + Intel), macOS 14 Sonoma or later |

More platforms (iOS, Android, Windows, Linux) are published from their own
channels — see the project site.

## Install (macOS)

1. Download `PlaiiinLight-<version>.dmg` from the latest release.
2. Open the `.dmg` and drag **PlaiiinLight** into **Applications**.
3. Launch it. On first run macOS asks for **Local Network** access — this is
   required to discover lamps over Bonjour. Approve it.

The app is signed with an Apple **Developer ID** certificate and **notarized**
by Apple, so it opens normally with no Gatekeeper override or right-click
workaround.

## Verify your download

Every release includes a `SHA256SUMS` file. Check your download against it:

```bash
shasum -a 256 -c SHA256SUMS
```

You can also confirm the notarization ticket is stapled:

```bash
spctl -a -vvv -t install /Applications/PlaiiinLight.app
# → source=Notarized Developer ID
```

## Requirements

- **macOS 14 Sonoma** or later.
- A PlaiiinLight lamp running firmware **1.2.0 or newer** (network discovery
  was added there).

## Releases

Builds are produced and published automatically by CI when a release is cut;
assets here are the exact artifacts Apple notarized. Issues with the apps
themselves are tracked in the main project.

## License

See [`LICENSE`](LICENSE).
