# EONKit (binary)

Prebuilt `EONKit.xcframework` for the EON TV Apple TV client. This package contains no
source, only the compiled framework and a `Package.swift` that exposes it as a binary target.
Both are committed by the release script in the private EONKit source repository, one tag per
version, so don't edit them here.

## Usage

Add `https://github.com/hpstuff/EONKit-Binary.git` as a Swift package dependency (up to next
major version) and link the `EONKit` product, then configure the SDK once at launch:

```swift
import EONKit

EONSDK.configure(credentials: ClientCredentials(
  androidTVClientID: "...", androidTVClientSecret: "...",
  webClientID: "...", webClientSecret: "..."
))
```

Requires Xcode 27.1 or later and targets tvOS 26.

## License

Copyright © 2026 Rumen Rusanov. All rights reserved. The binary is published so the EON TV
app can be built without access to the SDK source. It may not be redistributed or used in
other products without permission.
