## BoxyHQ Enhancement Requests

All of the enhancement and feature requests for *[BoxyHQ](https://boxyhq.com/)* are listed here, and community can pick the ones they want to complete and be rewarded for completing them.

## Index

1. [Code Enhancement/Feature Requests](#code-enhancementfeature-requests)
    - [Return version in health check endpoint](#1-return-version-in-health-check-endpoint)
    - [Build docker image for arm64](#2-build-docker-image-for-arm64)
    - [Guard against email not being present in the attributes](#3-guard-against-email-not-being-present-in-the-attributes)
    - [OpenTelemetry Tracing](#4-opentelemetry-tracing)
    - [Guard against providers that expect users to provide a unique SP entityId](#5-guard-against-providers-that-expect-users-to-provide-a-unique-sp-entityid)


## Code Enhancement/Feature Requests
---

### **1. Return version in health check endpoint**

**Is your proposal related to a problem?**
Need a way to check which version is running.

**Describe the solution you'd like**
Return the version in the health check endpoint.

  - **Posted by**: *[@deepakprabhakara](https://github.com/deepakprabhakara)*
  - <img src="https://img.shields.io/endpoint?url=https%3A%2F%2Faviyel-request-board.herokuapp.com%2Fboxyhq%2F142">
  - **Standard**: *Unpaid*
  - **[Issue Link](https://github.com/boxyhq/jackson/issues/142)**

---

### **2. Build docker image for arm64**


**Is your proposal related to a problem?**
Apple M1 uses arm64 arch, we are currently only building amd64.

**Describe the solution you'd like**
Use qemu and buildx to build both architectures and push the images.

**Additional context**
How is cosign affected by this? We'll need to ensure signing is intact for both arch.

 - **Posted by**: *[@deepakprabhakara](https://github.com/deepakprabhakara)*
 - <img src="https://img.shields.io/endpoint?url=https%3A%2F%2Faviyel-request-board.herokuapp.com%2Fboxyhq%2F124">
 - **Standard**: *Unpaid*
 - **[Issue Link](https://github.com/boxyhq/jackson/issues/124)**

---

### **3. Guard against email not being present in the attributes**

**Is your proposal related to a problem?**
If email is not present then throw an error, it is very likely a bad SAML configuration. Also some providers do not provide an email by default unless the mapping is added.
 
 - **Posted by**: *[@deepakprabhakara](https://github.com/deepakprabhakara)*
 - <img src="https://img.shields.io/endpoint?url=https%3A%2F%2Faviyel-request-board.herokuapp.com%2Fboxyhq%2F116">
 - **Standard**: *Unpaid*
 - **[Issue Link](https://github.com/boxyhq/jackson/issues/116)**

---

### **4. OpenTelemetry Tracing**
 
**Is your proposal related to a problem?**
Add tracing via OpenTelemetry
 
 - **Posted by**: *[@deepakprabhakara](https://github.com/deepakprabhakara)*
 - <img src="https://img.shields.io/endpoint?url=https%3A%2F%2Faviyel-request-board.herokuapp.com%2Fboxyhq%2F112">
 - **Standard**: *Unpaid*
 - **[Issue Link](https://github.com/boxyhq/jackson/issues/112)**

---

### **5. Guard against providers that expect users to provide a unique SP entityId**

**Is your proposal related to a problem?**
SAML Identity Providers are mean to provide their own unique entityId but JumpCloud expects this to come from the SP. This could lead to mistakes and collisions which need to be guarded against.

**Describe the solution you'd like**
Check if entityId already exists and then throw an error if the details don't match. Also provide instructions for providers like JumpCloud, entityId could be generated on the back of the tenant and product to keep it unique.
 
 - **Posted by**: *[@deepakprabhakara](https://github.com/deepakprabhakara)*
 - <img src="https://img.shields.io/endpoint?url=https%3A%2F%2Faviyel-request-board.herokuapp.com%2Fboxyhq%2F117">
 - **Standard**: *Unpaid*
 - **[Issue Link](https://github.com/boxyhq/jackson/issues/117)**

---
