## Medusa Enhancement Requests

All of the enhancement and feature requests for _[Medusa](https://medusajs.com/)_ are listed here, and community can pick the ones they want to complete and be rewarded for completing them.

## Index

### [Non-Code Enhancement/Feature Requests](#non-code-enhancementfeature-requests)
   1. [Create an Ecommerce App with Medusa and React Native](#1-create-an-ecommerce-app-with-medusa-and-react-native)
   2. [Integrate Medusa with x tool - a how-to guide](#2-integrate-medusa-with-x-tool---a-how-to-guide)
   3. [Create an iOS Ecommerce App with Medusa](#3-create-an-ios-ecommerce-app-with-medusa)
   4. [Create an Android Ecommerce App with Medusa](#4-create-an-android-ecommerce-app-with-medusa)
   5. [Create an Ecommerce App with Flutter and Medusa](#5-create-an-ecommerce-app-with-flutter-and-medusa)

### [Code Enhancement/Feature Requests](#code-enhancementfeature-requests)
   1. [Support filtering price lists by customer groups](#1-support-filtering-price-lists-by-customer-groups)
   2. [API: Complete a batch operation](#2-api-complete-a-batch-operation)
   3. [API: Cancel a batch operation](#3-api-cancel-a-batch-operation)
   4. [API: List batch operations](#4-api-list-batch-operations)
   5. [API: Get a batch job](#5-api-get-a-batch-job)
   6. [API: Create a batch operation](#6-api-create-a-batch-operation)
   7. [Implement OrderExportHandler](#7-implement-orderexporthandler)
   8. [Implement ProductImportHandler](#8-implement-productimporthandler)
   9. [Batch job *Handlers](#9-batch-job-handlers)
   10. [BatchJob entity model](#10-batchjob-entity-model)
   11. [Add DELETE /store/auth to @medusajs/medusa-js](#11-add-delete-storeauth-to-medusajsmedusa-js)
   12. [WebSocket/Server sent events implementation](#12-websocketserver-sent-events-implementation)
   13. [Update FileService to allow for protected uploads/downloads + streaming](#13-update-fileservice-to-allow-for-protected-uploadsdownloads--streaming)
   14. [Implement BatchJobService](#14-implement-batchjobservice)
   15. [Add POST/DELETE /admin/collections/:id/products/batch endpoints to @medusajs/medusa-js and medusa-react](#15-add-postdelete-admincollectionsidproductsbatch-endpoints-to-medusajsmedusa-js-and-medusa-react)
   16. [Enhancement: Ability to use admin middleware in custom APIs](#16-enhancement-ability-to-use-admin-middleware-in-custom-apis)
   17. [Select discount.rule.valid_for products by collection, type, and tags](#17-select-discountrulevalid_for-products-by-collection-type-and-tags)
  
### [Creation of Templates](#creation-of-templates-1)
   1. [How to set up Gatsby source plugin for building websites using Medusa as data source](#2-how-to-integrate-brightpearl-into-medusa)
   2. [How to integrate Brightpearl into Medusa](#2-how-to-integrate-brightpearl-into-medusa)
   3. [How to integrate Algolia with Medusa](#3-how-to-integrate-algolia-with-medusa)
   4. [How to add third party apps and plugins to Medusa Store](#4-how-to-add-third-party-apps-and-plugins-to-medusa-store)

## Non-Code Enhancement/Feature Requests

---

### **1. Create an Ecommerce App with Medusa and React Native**

Apps has been of long time interest, we are looking to do a cool write up on it but are no experts ourselves.

- **Posted by**: _MedusaJS_
- [Check Status](https://medusajs.notion.site/Topics-2653fe684b1a4640b94e253f1d6bc3d9)
- **Standard**: _Paid_
- **[Issue Link](https://github.com/aviyelverse/Open-Source-Requests/issues/110)**

---

### **2. Integrate Medusa with x tool - a how-to guide**

Please include a repo or build a real integration for it that we can share along with the article.

- **Posted by**: _MedusaJS_
- [Check Status](https://medusajs.notion.site/Topics-2653fe684b1a4640b94e253f1d6bc3d9)
- **Standard**: _Paid_
- **[Issue Link](https://github.com/aviyelverse/Open-Source-Requests/issues/111)**

---

### **3. Create an iOS Ecommerce App with Medusa**

Most people shop on their phones, so it’s important to have an app for your store. Due to Medusa’s headless architecture, it should be as easy as creating a website!

- **Posted by**: _MedusaJS_
- [Check Status](https://medusajs.notion.site/Topics-2653fe684b1a4640b94e253f1d6bc3d9)
- **Standard**: _Paid_
- **[Issue Link](https://github.com/aviyelverse/Open-Source-Requests/issues/112)**

---

### **4. Create an Android Ecommerce App with Medusa**

Flutter is a popular cross-platform framework that many love and use. This tutorial will help them learn how to create an ecommerce app using flutter and Medusa.

- **Posted by**: _MedusaJS_
- [Check Status](https://medusajs.notion.site/Topics-2653fe684b1a4640b94e253f1d6bc3d9)
- **Standard**: _Paid_
- **[Issue Link](https://github.com/aviyelverse/Open-Source-Requests/issues/113)**

---

### **5. Create an Ecommerce App with Flutter and Medusa**

Apps has been of long time interest, we are looking to do a cool write up on it but are no experts ourselves.

- **Posted by**: _MedusaJS_
- [Check Status](https://medusajs.notion.site/Topics-2653fe684b1a4640b94e253f1d6bc3d9)
- **Standard**: _Paid_
- **[Issue Link](https://github.com/aviyelverse/Open-Source-Requests/issues/114)**

---

## Code Enhancement/Feature Requests

---

### **1. Support filtering price lists by customer groups**

We want to add support for filtering by customer groups. We should extend the `FitlerablePriceListProps` here to include a `customer_group_id?` field of type `string[]` which would include the list of customer group ids to filter by.

- **Posted by**: _[@zakariaelas](https://github.com/zakariaelas)_
- <img src="https://img.shields.io/endpoint?url=https%3A%2F%2Faviyel-request-board.herokuapp.com%2Fmedusa%2F1286">
- **Standard**: _Unpaid_
- **[Issue Link](https://github.com/aviyelverse/Open-Source-Requests/issues/32)**

---

### **2. API: Complete a batch operation**

Completes a previously dry_run'ed job.

```
POST /admin/batch/:id/complete
```

**DoD**

- [ ] should be idempotent - i.e. if trying to complete a job that is currently processing the completion step then nothing should happen and endpoint should respond 200
- [ ] only your own jobs can be completed i.e. `req.user.id === batch.created_by` must be true
- [ ] should call `BatchJobService.complete` which in turn calls the underlying handler.
- [ ] Endpoint should not wait for the actual processing of the job to complete

- **Posted by**: _[@srindom](https://github.com/srindom)_
- <img src="https://img.shields.io/endpoint?url=https%3A%2F%2Faviyel-request-board.herokuapp.com%2Fmedusa%2F1277">
- **Standard**: _Unpaid_
- **[Issue Link](https://github.com/aviyelverse/Open-Source-Requests/issues/33)**

---

### **3. API: Cancel a batch operation**

Cancels an operation that is in progress.

```
POST /admin/batch/:id/cancel
```

**DoD**

- [ ] endpoint should be idempotent - e.g. calling cancel on an already canceled job is allowed and responds with 200
- [ ] BatchJobs in a completed state should not be cancelable - should fail with 422
- [ ] Should call BatchJobService.cancel; which in turn potentially cancels the jobs in the worker that are currently being processed.

- **Posted by**: _[@srindom](https://github.com/srindom)_
- <img src="https://img.shields.io/endpoint?url=https%3A%2F%2Faviyel-request-board.herokuapp.com%2Fmedusa%2F1276">
- **Standard**: _Unpaid_
- **[Issue Link](https://github.com/aviyelverse/Open-Source-Requests/issues/34)**

---

### **4. API: List batch operations**

Lists the BatchJobs created by the authenticated user.

```
GET /admin/batch

Response
- count
- limit
- offset
- batch_jobs - { id, status, progress, ... }
```

**DoD**

- [ ] should respond with the batch jobs that are created by the user
- [ ] calls `BatchJobService.listAndCount`

- **Posted by**: _[@srindom](https://github.com/srindom)_
- <img src="https://img.shields.io/endpoint?url=https%3A%2F%2Faviyel-request-board.herokuapp.com%2Fmedusa%2F1275">
- **Standard**: _Unpaid_
- **[Issue Link](https://github.com/aviyelverse/Open-Source-Requests/issues/35)**

---

### **5. API: Get a batch job**

Gets a BatchJob. This endpoint may be used for polling the status of a batch operation. To retrieve the BatchJob with id the authenticated user must be the user identified by `created_by`.

```
GET /admin/batch/:id

Response
- batch_job - { id, status, progress, ... }
```

**DoD**

- [ ] should respond with the correct batch job
- [ ] if the authenticated user is not the creator of the batch job they should not be able to retrieve the job

- **Posted by**: _[@srindom](https://github.com/srindom)_
- <img src="https://img.shields.io/endpoint?url=https%3A%2F%2Faviyel-request-board.herokuapp.com%2Fmedusa%2F1274">
- **Standard**: _Unpaid_
- **[Issue Link](https://github.com/aviyelverse/Open-Source-Requests/issues/36)**

---

### **6. API: Create a batch operation**

Creates a batch operation. The type of batch operation determines what should be included in the context. If the batch job is created with dry_run: true final confirmation through /batch/:id/complete will be required before the final data is uploaded to the DB.

- **Posted by**: _[@srindom](https://github.com/srindom)_
- <img src="https://img.shields.io/endpoint?url=https%3A%2F%2Faviyel-request-board.herokuapp.com%2Fmedusa%2F1273">
- **Standard**: _Unpaid_
- **[Issue Link](https://github.com/aviyelverse/Open-Source-Requests/issues/37)**

---

### **7. Implement OrderExportHandler**


add OrderExportHandler class for processing orders batch export which implements the common batch job handler interface

depends on: [#1264](https://github.com/medusajs/medusa/issues/1264)

- **Posted by**: _[@fPolic](https://github.com/fPolic)_
- <img src="https://img.shields.io/endpoint?url=https%3A%2F%2Faviyel-request-board.herokuapp.com%2Fmedusa%2F1267">
- **Standard**: _Unpaid_
- **[Issue Link](https://github.com/aviyelverse/Open-Source-Requests/issues/38)**

---

### **8. Implement ProductImportHandler**

add ProductImportHandler class for processing products batch import which implements the common batch job handler interface
depends on: [#1264](https://github.com/medusajs/medusa/issues/1264)

- **Posted by**: _[@fPolic](https://github.com/fPolic)_
- <img src="https://img.shields.io/endpoint?url=https%3A%2F%2Faviyel-request-board.herokuapp.com%2Fmedusa%2F1265">
- **Standard**: _Unpaid_
- **[Issue Link](https://github.com/aviyelverse/Open-Source-Requests/issues/39)**

---

### **9. Batch job *Handlers**

- add support for loading *Handler classes into the Awilix container
   - Awiilix container is allowed to have a single instance of each type of handler
   - enable custom batch job types/handlers from plugins by identifying service using BatchJob type
- create a common interface that batch job handlers implement:

- **Posted by**: _[@fPolic](https://github.com/fPolic)_
- <img src="https://img.shields.io/endpoint?url=https%3A%2F%2Faviyel-request-board.herokuapp.com%2Fmedusa%2F1264">
- **Standard**: _Unpaid_
- **[Issue Link](https://github.com/aviyelverse/Open-Source-Requests/issues/40)**

---

### **10. BatchJob entity model**

We should introduce a new BatchJob entity to model the status of a batch upload job (unit of batch upload or download work).

- **Posted by**: _[@fPolic](https://github.com/fPolic)_
- <img src="https://img.shields.io/endpoint?url=https%3A%2F%2Faviyel-request-board.herokuapp.com%2Fmedusa%2F1263">
- **Standard**: _Unpaid_
- **[Issue Link](https://github.com/aviyelverse/Open-Source-Requests/issues/41)**

---

### **11. Add DELETE /store/auth to @medusajs/medusa-js**


In medusa-js, add signOut() to the [store AuthResource](https://github.com/medusajs/medusa/blob/master/packages/medusa-js/src/resources/auth.ts).

- **Posted by**: _[@olivermrbl](https://github.com/olivermrbl)_
- <img src="https://img.shields.io/endpoint?url=https%3A%2F%2Faviyel-request-board.herokuapp.com%2Fmedusa%2F1094">
- **Standard**: _Unpaid_
- **[Issue Link](https://github.com/aviyelverse/Open-Source-Requests/issues/42)**

---

### **12. WebSocket/Server sent events implementation**


We want to implement some notion of server transmitted data, as we want to be able to transmit to the client when a batch job is completed, and as an example notify that a file is now ready to be downloaded. Should expandable upon later, such as pushing a notification when a user is mentioned in a comment on an order, etc.

Part of this ticket is investigating how we should approach this, as WebSocket/SSE is not very "RESTy". One idea would be to subscribe to an event, and when detected push to the client "you should GET /admin/batch/<some_id>", to keep it slim and still make use of the existing RESTFUL API.

- **Posted by**: _[@kasperkristensen](https://github.com/kasperkristensen)_
- <img src="https://img.shields.io/endpoint?url=https%3A%2F%2Faviyel-request-board.herokuapp.com%2Fmedusa%2F1270">
- **Standard**: _Unpaid_
- **[Issue Link](https://github.com/aviyelverse/Open-Source-Requests/issues/43)**

---

### **13. Update FileService to allow for protected uploads/downloads + streaming**


Part of this ticket is to research how providers such as S3, DO, etc. so the FileService can serve as an abstraction over how these handle protected upload/downloads and streaming.
   - Update the current FileService to allow for protected uploads/downloads.
   - Also update the service so files can be streamed

- **Posted by**: _[@kasperkristensen](https://github.com/kasperkristensen)_
- <img src="https://img.shields.io/endpoint?url=https%3A%2F%2Faviyel-request-board.herokuapp.com%2Fmedusa%2F1269">
- **Standard**: _Unpaid_
- **[Issue Link](https://github.com/aviyelverse/Open-Source-Requests/issues/44)**

---

### **14. Implement BatchJobService**

Add a BatchJobService.

- **Posted by**: _[@kasperkristensen](https://github.com/kasperkristensen)_
- <img src="https://img.shields.io/endpoint?url=https%3A%2F%2Faviyel-request-board.herokuapp.com%2Fmedusa%2F1268">
- **Standard**: _Unpaid_
- **[Issue Link](https://github.com/aviyelverse/Open-Source-Requests/issues/45)**

---

### **15. Add POST/DELETE /admin/collections/:id/products/batch endpoints to @medusajs/medusa-js and medusa-react**

The new batch endpoints introduced by [#1032](https://github.com/medusajs/medusa/pull/1032) are missing in the client and medusa-react.

- **Posted by**: _[@srindom](https://github.com/srindom)_
- <img src="https://img.shields.io/endpoint?url=https%3A%2F%2Faviyel-request-board.herokuapp.com%2Fmedusa%2F1089">
- **Standard**: _Unpaid_
- **[Issue Link](https://github.com/aviyelverse/Open-Source-Requests/issues/46)**

---

### **16. Enhancement: Ability to use admin middleware in custom APIs**

It appears that right now all custom APIs are insecure by default. It would be nice if I could reuse the same middleware that the admin api uses in my custom api.

- **Posted by**: _[@dwene](https://github.com/dwene)_
- <img src="https://img.shields.io/endpoint?url=https%3A%2F%2Faviyel-request-board.herokuapp.com%2Fmedusa%2F859">
- **Standard**: _Unpaid_
- **[Issue Link](https://github.com/aviyelverse/Open-Source-Requests/issues/47)**

---

### **17. Select discount.rule.valid_for products by collection, type, and tags**

We should allow users to select a discount's applicable products by collection, type, and tags.

More to come

- **Posted by**: _[@olivermrbl](https://github.com/olivermrbl)_
- <img src="https://img.shields.io/endpoint?url=https%3A%2F%2Faviyel-request-board.herokuapp.com%2Fmedusa%2F419">
- **Standard**: _Unpaid_
- **[Issue Link](https://github.com/aviyelverse/Open-Source-Requests/issues/48)**

---

## Creation of templates

### **1. How to set up Gatsby source plugin for building websites using Medusa as data source**

   - **Posted by**: Aviyel Team
   - [Check Status](https://sturdy-locust-74a.notion.site/Medusa-4b4228a60d824da98ffe56d2715a1969)
   - **Standard**: _Unpaid_
   - **[Issue Link]()**

### **2. How to integrate Brightpearl into Medusa**

   - **Posted by**: Aviyel Team
   - [Check Status](https://sturdy-locust-74a.notion.site/Medusa-4b4228a60d824da98ffe56d2715a1969)
   - **Standard**: _Unpaid_
   - **[Issue Link]()**

### **3. How to integrate Algolia with Medusa**

   - **Posted by**: Aviyel Team
   - [Check Status](https://sturdy-locust-74a.notion.site/Medusa-4b4228a60d824da98ffe56d2715a1969)
   - **Standard**: _Unpaid_
   - **[Issue Link]()**

### **4. How to add third party apps and plugins to Medusa Store**

   - **Posted by**: Aviyel Team
   - [Check Status](https://sturdy-locust-74a.notion.site/Medusa-4b4228a60d824da98ffe56d2715a1969)
   - **Standard**: _Unpaid_
   - **[Issue Link]()**

