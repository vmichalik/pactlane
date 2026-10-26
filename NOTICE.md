# Sources and attribution

The product idea is inspired by [ZKP2P](https://www.zkp2p.xyz/). This project is an independent Stellar application and does not claim affiliation.

The active proof integration targets [TLSNotary’s browser extension](https://github.com/tlsnotary/tlsn-extension), release `0.1.0.1501`, source commit `68bbd380d6e1a89d79748e5294661c752f5d1205`, with TLSNotary `0.1.0-alpha.15`. The local verifier patch is derived from that pinned upstream source. `scripts/prepare-tlsn.py` fetches the source and released runtime into ignored local tooling, checks hashes and preserves upstream files. Downloaded proof runtimes remain outside Git. The app separately includes pinned browser bundles and the demo composition retains its existing GSAP runtime and licence header. Review upstream licensing and dependency notices before redistributing them.

The archived experiment reproduces the older Reclaim claim-envelope encoding independently and uses [Soroban SDK](https://github.com/stellar/rs-soroban-sdk) `29.0.1`. It is retained as a signature-compatibility reference. The active flow has no Reclaim SDK or service dependency.

Useful primary references:

- [TLSNotary extension quickstart](https://tlsnotary.org/docs/quick_start/browser_extension/)
- [TLSNotary plugins](https://tlsnotary.org/docs/extension/plugins/)
- [TLSNotary verifier](https://tlsnotary.org/docs/extension/verifier/)
- [Stellar developer documentation](https://developers.stellar.org/)
- [HackMeridian build guide](https://www.hackmeridian.com/build)

This public review snapshot does not grant a reuse license to the project’s original code. Third-party code retains its own terms.

## Browser bundle notices

Portions © 2025 Reown, Inc. All Rights Reserved.

- The pinned Freighter API 6.0.1 bundle is covered by [Apache-2.0](licenses/freighter-api-6.0.1-APACHE-2.0.txt), copied from its npm release’s upstream source commit.
- WalletConnect 2.26.0 components retain the [WalletConnect Community License](licenses/bundled/_walletconnect_universal-provider-2.26.0-LICENSE.md). They are not relicensed under Pactlane’s terms.
- [Bundled dependency inventory](licenses/wallet-bundle-manifest.json) lists the packages and copied license files for the exact committed wallet bundle; its in-memory rebuild matched the committed bytes.
- [uint8arrays attribution](licenses/uint8arrays-3.1.1-MIT.txt) retains the MIT declaration and author information where the upstream package supplies no separate license file.
- TLSNotary’s pinned [upstream README](https://github.com/tlsnotary/tlsn-extension/blob/68bbd380d6e1a89d79748e5294661c752f5d1205/README.md#license) offers Apache-2.0 or MIT. The included patch is a Pactlane modification of that source; the [Apache-2.0 terms](licenses/freighter-api-6.0.1-APACHE-2.0.txt) are retained here. The complete upstream runtime is fetched separately rather than bundled.

Existing Manrope OFL files and the GSAP runtime’s license header remain with their assets.
