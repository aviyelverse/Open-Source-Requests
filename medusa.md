## Medusa Enhancement Requests

All of the enhancement and feature requests for *[Medusa](https://medusajs.com/)* are listed here, and community can pick the ones they want to complete and be rewarded for completing them.

## Index

1. [Non-Code Enhancement/Feature Requests](#non-code-enhancementfeature-requests)
    - [Create an Ecommerce App with Medusa and React Native](#1-create-an-ecommerce-app-with-medusa-and-react-native)
    - [Integrate Medusa with x tool - a how-to guide](#2-integrate-medusa-with-x-tool---a-how-to-guide)
    - [Create an iOS Ecommerce App with Medusa](#3-create-an-ios-ecommerce-app-with-medusa)
    - [Create an Android Ecommerce App with Medusa](#4-create-an-android-ecommerce-app-with-medusa)
    - [Create an Ecommerce App with Flutter and Medusa](#5-create-an-ecommerce-app-with-flutter-and-medusa)
2. [Code Enhancement/Feature Requests](#code-enhancementfeature-requests)
    - [Support filtering price lists by customer groups](#1-support-filtering-price-lists-by-customer-groups)
    - [API: Complete a batch operation](#2-api-complete-a-batch-operation)
    - [API: Cancel a batch operation](#3-api-cancel-a-batch-operation)
    - [API: List batch operations](#4-api-list-batch-operations)
    - [API: Get a batch job](#5-api-get-a-batch-job)

## Non-Code Enhancement/Feature Requests
---

### **1. Create an Ecommerce App with Medusa and React Native**

Apps has been of long time interest, we are looking to do a cool write up on it but are no experts ourselves.

  - **Posted by**: *MedusaJS*
  - **Status**: *Not assigned*
  - **Standard**: *Paid*
  - **[Gig Link](https://medusajs.notion.site/Topics-2653fe684b1a4640b94e253f1d6bc3d9?p=73825e914cc440d0b5e2e942d9a291e4)**

---

### **2. Integrate Medusa with x tool - a how-to guide**

Please include a repo or build a real integration for it that we can share along with the article.

  - **Posted by**: *MedusaJS*
  - **Status**: *Not assigned*
  - **Standard**: *Paid*
  - **[Gig Link](https://medusajs.notion.site/Topics-2653fe684b1a4640b94e253f1d6bc3d9?p=d17936d35e9441e9b95aec752bab638f)**

---

### **3. Create an iOS Ecommerce App with Medusa**

Most people shop on their phones, so it’s important to have an app for your store. Due to Medusa’s headless architecture, it should be as easy as creating a website!

  - **Posted by**: *MedusaJS*
  - **Status**: *Not assigned*
  - **Standard**: *Paid*
  - **[Gig Link](https://medusajs.notion.site/Topics-2653fe684b1a4640b94e253f1d6bc3d9?p=054a101c3b614daca6c1445c52c830fa)**

---

### **4. Create an Android Ecommerce App with Medusa**

Flutter is a popular cross-platform framework that many love and use. This tutorial will help them learn how to create an ecommerce app using flutter and Medusa.

  - **Posted by**: *MedusaJS*
  - **Status**: *Not assigned*
  - **Standard**: *Paid*
  - **[Gig Link](https://medusajs.notion.site/Topics-2653fe684b1a4640b94e253f1d6bc3d9?p=ac865d4ce2ff42d4934ee4c22a8c4619)**

---

### **5. Create an Ecommerce App with Flutter and Medusa**

Apps has been of long time interest, we are looking to do a cool write up on it but are no experts ourselves.

  - **Posted by**: *MedusaJS*
  - **Status**: *Not assigned*
  - **Standard**: *Paid*
  - **[Gig Link](https://medusajs.notion.site/Topics-2653fe684b1a4640b94e253f1d6bc3d9?p=73825e914cc440d0b5e2e942d9a291e4)**

---


## Code Enhancement/Feature Requests
---

### **1. Support filtering price lists by customer groups**

We want to add support for filtering by customer groups. We should extend the `FitlerablePriceListProps` here to include a `customer_group_id?` field of type `string[]` which would include the list of customer group ids to filter by.

  - **Posted by**: *[@zakariaelas](https://github.com/zakariaelas)*
  - <img src="https://img.shields.io/endpoint?url=https%3A%2F%2Faviyel-request-board.herokuapp.com%2Fmedusa%2F1286">
  - **Standard**: *Unpaid*
  - **[Issue Link](https://github.com/medusajs/medusa/issues/1286)**

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

 - **Posted by**: *[@srindom](https://github.com/srindom)*
 - <img src="https://img.shields.io/endpoint?url=https%3A%2F%2Faviyel-request-board.herokuapp.com%2Fmedusa%2F1277">
 - **Standard**: *Unpaid*
 - **[Issue Link](https://github.com/medusajs/medusa/issues/1277)**

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
 
 - **Posted by**: *[@srindom](https://github.com/srindom)*
 - <img src="https://img.shields.io/endpoint?url=https%3A%2F%2Faviyel-request-board.herokuapp.com%2Fmedusa%2F1276">
 - **Standard**: *Unpaid*
 - **[Issue Link](https://github.com/medusajs/medusa/issues/1276)**

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
 
 - **Posted by**: *[@srindom](https://github.com/srindom)*
 - <img src="https://img.shields.io/endpoint?url=https%3A%2F%2Faviyel-request-board.herokuapp.com%2Fmedusa%2F1275">
 - **Standard**: *Unpaid*
 - **[Issue Link](https://github.com/medusajs/medusa/issues/1275)**

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
 
 - **Posted by**: *[@srindom](https://github.com/srindom)*
 - <img src="https://img.shields.io/endpoint?url=https%3A%2F%2Faviyel-request-board.herokuapp.com%2Fmedusa%2F1274">
 - **Standard**: *Unpaid*
 - **[Issue Link](https://github.com/medusajs/medusa/issues/1274)**

---
