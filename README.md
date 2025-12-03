
The [Touchpoints application](https://github.com/GSA/touchpoints) uses
a Rust-based HTML template render, since it's an order-of-magnitude faster then
the original Ruby one.

To enable the renderer on Cloud.gov's Cloud Foundry infrastructure, we use this
buildpack to install Rust and compile the renderer. We maintain our own buildpack
because there's no official Cloud Foundry buildpack, nor any well-maintained community-supported
buildpacks.

We have kept this buildpack implementation as simple as we can to minimize
any needs for maintenance and security updates. For example, we always use
the latest version of Rust.

This code is open-source to both comply with GSA policy, and to enable referencing
the buildpack in a Cloud Foundry manifest.
