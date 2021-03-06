## BoxyHQ Requests

All of the  requests for _[BoxyHQ](https://boxyhq.com/)_ are listed here, and community can pick the ones they want to complete.

**BEFORE PICKING UP AN ISSUE, PLEASE ENSURE IT'S OPEN FOR CONTRIBUTIONS.**

## Index

### [Code Enhancement/Feature Requests](#code-enhancementfeature-requests)
   1. [Guard against email not being present in the attributes](#1-guard-against-email-not-being-present-in-the-attributes)
   2. [OpenTelemetry Tracing](#2-opentelemetry-tracing)
   3. [Guard against providers that expect users to provide a unique SP entityId](#3-guard-against-providers-that-expect-users-to-provide-a-unique-sp-entityid)

### [Creation of Templates](#creation-of-templates-1)
   1. [How to add SAML Single Sign-On service to a Laravel application?](#1-how-to-add-saml-single-sign-on-service-to-a-laravel-application)
   2. [How to add SAML Single Sign-On service to an Angular application?](#2-how-to-add-saml-single-sign-on-service-to-an-angular-application)
   3. [How to add SAML Single Sign-On service to a Svelte application?](#3-how-to-add-saml-single-sign-on-service-to-a-svelte-application)
   4. [How to build and deploy SAML service on AWS?](#4-how-to-build-and-deploy-saml-service-on-aws)
   5. [How to build and deploy SAML service on Docker?](#5-how-to-build-and-deploy-saml-service-on-docker)
   6. [How to deploy SAML Jackson as a separate service?](#6-how-to-deploy-saml-jackson-as-a-separate-service)
   7. [How to integrate SAML Jackson with Express.js and Auth0?](#7-how-to-integrate-saml-jackson-with-expressjs-and-auth0)
   8. [How to integrate SAML Jackson with the Nodejs application?](#8-how-to-integrate-saml-jackson-with-the-nodejs-application)
   9. [How to build and deploy SAML service on Digital Ocean?](#9-how-to-build-and-deploy-saml-service-on-digital-ocean)
   10. [How to build and deploy SAML service on Vercel?](#10-how-to-build-and-deploy-saml-service-on-vercel)
   11. [How to add SAML Single Sign-On service to a Vuejs application?](#11-how-to-add-saml-single-sign-on-service-to-a-vuejs-application)
   12. [How to add SAML Single Sign-On service to a Nextjs app?](#12-how-to-add-saml-single-sign-on-service-to-a-nextjs-app)
   13. [How to add SAML Single Sign-On service to a Reactjs app?](#13-how-to-add-saml-single-sign-on-service-to-a-reactjs-app)
   14. [How to integrate SAML Jackson with Supertokens and Express.js?](#14-how-to-integrate-saml-jackson-with-supertokens-and-expressjs)

## Code Enhancement/Feature Requests

### **1. Guard against email not being present in the attributes**

**Is your proposal related to a problem?**
If email is not present then throw an error, it is very likely a bad SAML configuration. Also some providers do not provide an email by default unless the mapping is added.

- **Posted by**: _[@deepakprabhakara](https://github.com/deepakprabhakara)_
- <img src="https://img.shields.io/endpoint?url=https%3A%2F%2Faviyel-request-board.herokuapp.com%2Fboxyhq%2F116">
- **Standard**: _Unpaid_
- **[Issue Link](https://github.com/aviyelverse/Open-Source-Requests/issues/56)**

---

### **2. OpenTelemetry Tracing**

**Is your proposal related to a problem?**
Add tracing via OpenTelemetry

- **Posted by**: _[@deepakprabhakara](https://github.com/deepakprabhakara)_
- <img src="https://img.shields.io/endpoint?url=https%3A%2F%2Faviyel-request-board.herokuapp.com%2Fboxyhq%2F112">
- **Standard**: _Unpaid_
- **[Issue Link](https://github.com/aviyelverse/Open-Source-Requests/issues/57)**

---

### **3. Guard against providers that expect users to provide a unique SP entityId**

**Is your proposal related to a problem?**
SAML Identity Providers are mean to provide their own unique entityId but JumpCloud expects this to come from the SP. This could lead to mistakes and collisions which need to be guarded against.

**Describe the solution you'd like**
Check if entityId already exists and then throw an error if the details don't match. Also provide instructions for providers like JumpCloud, entityId could be generated on the back of the tenant and product to keep it unique.

- **Posted by**: _[@deepakprabhakara](https://github.com/deepakprabhakara)_
- <img src="https://img.shields.io/endpoint?url=https%3A%2F%2Faviyel-request-board.herokuapp.com%2Fboxyhq%2F117">
- **Standard**: _Unpaid_
- **[Issue Link](https://github.com/aviyelverse/Open-Source-Requests/issues/58)**

---

## Creation of templates

### **1. How to add SAML Single Sign-On service to a Laravel application?**

   - **Posted by**: Aviyel Team
   - [Check Status](https://sturdy-locust-74a.notion.site/BoxyHQ-b4940ecefc574ac0a85833b5aeebc82f)
   - **Standard**: _Unpaid_
   - **[Issue Link](https://github.com/aviyelverse/Open-Source-Requests/issues/94)**

### **2. How to add SAML Single Sign-On service to an Angular application?**

   - **Posted by**: Aviyel Team
   - [Check Status](https://sturdy-locust-74a.notion.site/BoxyHQ-b4940ecefc574ac0a85833b5aeebc82f)
   - **Standard**: _Unpaid_
   - **[Issue Link](https://github.com/aviyelverse/Open-Source-Requests/issues/96)**

### **3. How to add SAML Single Sign-On service to a Svelte application?**

   - **Posted by**: Aviyel Team
   - [Check Status](https://sturdy-locust-74a.notion.site/BoxyHQ-b4940ecefc574ac0a85833b5aeebc82f)
   - **Standard**: _Unpaid_
   - **[Issue Link](https://github.com/aviyelverse/Open-Source-Requests/issues/98)**

### **4. How to build and deploy SAML service on AWS?**

   - **Posted by**: Aviyel Team
   - [Check Status](https://sturdy-locust-74a.notion.site/BoxyHQ-b4940ecefc574ac0a85833b5aeebc82f)
   - **Standard**: _Unpaid_
   - **[Issue Link](https://github.com/aviyelverse/Open-Source-Requests/issues/99)**

### **5. How to build and deploy SAML service on Docker?**

   - **Posted by**: Aviyel Team
   - [Check Status](https://sturdy-locust-74a.notion.site/BoxyHQ-b4940ecefc574ac0a85833b5aeebc82f)
   - **Standard**: _Unpaid_
   - **[Issue Link](https://github.com/aviyelverse/Open-Source-Requests/issues/100)**

### **6. How to deploy SAML Jackson as a separate service?**

   - **Posted by**: Aviyel Team
   - [Check Status](https://sturdy-locust-74a.notion.site/BoxyHQ-b4940ecefc574ac0a85833b5aeebc82f)
   - **Standard**: _Unpaid_
   - **[Issue Link](https://github.com/aviyelverse/Open-Source-Requests/issues/101)**
  
### **7. How to integrate SAML Jackson with Express.js and Auth0?**

   - **Posted by**: Aviyel Team
   - [Check Status](https://sturdy-locust-74a.notion.site/BoxyHQ-b4940ecefc574ac0a85833b5aeebc82f)
   - **Standard**: _Unpaid_
   - **[Issue Link](https://github.com/aviyelverse/Open-Source-Requests/issues/102)**

### **8. How to integrate SAML Jackson with the Nodejs application?**

   - **Posted by**: Aviyel Team
   - [Check Status](https://sturdy-locust-74a.notion.site/BoxyHQ-b4940ecefc574ac0a85833b5aeebc82f)
   - **Standard**: _Unpaid_
   - **[Issue Link](https://github.com/aviyelverse/Open-Source-Requests/issues/103)**

### **9. How to build and deploy SAML service on Digital Ocean?**

   - **Posted by**: Aviyel Team
   - [Check Status](https://sturdy-locust-74a.notion.site/BoxyHQ-b4940ecefc574ac0a85833b5aeebc82f)
   - **Standard**: _Unpaid_
   - **[Issue Link](https://github.com/aviyelverse/Open-Source-Requests/issues/104)**

### **10. How to build and deploy SAML service on Vercel?**

   - **Posted by**: Aviyel Team
   - [Check Status](https://sturdy-locust-74a.notion.site/BoxyHQ-b4940ecefc574ac0a85833b5aeebc82f)
   - **Standard**: _Unpaid_
   - **[Issue Link](https://github.com/aviyelverse/Open-Source-Requests/issues/105)**

### **11. How to add SAML Single Sign-On service to a Vuejs application?**

   - **Posted by**: Aviyel Team
   - [Check Status](https://sturdy-locust-74a.notion.site/BoxyHQ-b4940ecefc574ac0a85833b5aeebc82f)
   - **Standard**: _Unpaid_
   - **[Issue Link](https://github.com/aviyelverse/Open-Source-Requests/issues/106)**

### **12. How to add SAML Single Sign-On service to a Nextjs app?**

   - **Posted by**: Aviyel Team
   - [Check Status](https://sturdy-locust-74a.notion.site/BoxyHQ-b4940ecefc574ac0a85833b5aeebc82f)
   - **Standard**: _Unpaid_
   - **[Issue Link](https://github.com/aviyelverse/Open-Source-Requests/issues/107)**

### **13. How to add SAML Single Sign-On service to a Reactjs app?**

   - **Posted by**: Aviyel Team
   - [Check Status](https://sturdy-locust-74a.notion.site/BoxyHQ-b4940ecefc574ac0a85833b5aeebc82f)
   - **Standard**: _Unpaid_
   - **[Issue Link](https://github.com/aviyelverse/Open-Source-Requests/issues/108)**

### **14. How to integrate SAML Jackson with Supertokens and Express.js?**

   - **Posted by**: Aviyel Team
   - [Check Status](https://sturdy-locust-74a.notion.site/BoxyHQ-b4940ecefc574ac0a85833b5aeebc82f)
   - **Standard**: _Unpaid_
   - **[Issue Link](https://github.com/aviyelverse/Open-Source-Requests/issues/109)**

---
