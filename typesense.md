# Typesense Enhancement Requests

Enhancement and feature requests for _[Typesense](https://typesense.org/)_ are listed here, and community can pick the ones they want to complete and be rewarded for completing them.

**BEFORE PICKING UP AN ISSUE, PLEASE ENSURE IT'S OPEN FOR CONTRIBUTIONS.**

## Index

### [Code Enhancement/Feature Requests](#code-enhancementfeature-requests)
 1. [Unable to use negation filter to integer field](#1-unable-to-use-negation-filter-to-integer-field)
 2. [Ability to apply filters to overrides and pinned hits](#2-ability-to-apply-filters-to-overrides-and-pinned-hits)
 3. [Curation API and filters](#3-curation-api-and-filters)
 4. [Ranking based on Relevance and Popularity connected to Override](#4-ranking-based-on-relevance-and-popularity-connected-to-override)
 5. [Default Value When Optional = "True"](#5-default-value-when-optional--true)
### [Creation of Templates and Demos](#creating-templates-and-demos)
 1. [Create a Demo of Anime instant-search app](#1-create-a-demo-of-anime-instant-search-app)
 2. [Build a search application with Typesense, React and Tailwind](#2-build-a-search-application-with-typesense-react-and-tailwind)
 3. [Build an instant full-text search in JavaScript with Typesense](#3-build-an-instant-full-text-search-in-javascript-with-typesense)
 4. [Adding Typesense search to an Astro Static Generated Website](#4-adding-typesense-search-to-an-astro-static-generated-website)
 5. [Building a search UI with Typesense](#5-building-a-search-ui-with-typesense)

## Code Enhancement/Feature Requests

---

### **1. Unable to use negation filter to integer field.**

**Description**
Can not use negation filter to numeric field.

**Steps to reproduce**
Use status:!=1 on numeric field (type: int32 or int64).

**Expected Behavior**
Return results that field value not 1.

**Actual Behavior**
status:!=1 error:
Error with filter field status: Numerical field has an invalid comparator.

**status:<>1 error**:
Error with filter field status: Not an int32.

**Metadata**
Typsense Version:
0.22.2

**OS**:
Ubuntu 20.04

- **Posted by**: _[@xpader](https://github.com/xpader)_
- <img src="https://img.shields.io/endpoint?url=https%3A%2F%2Faviyel-request-board.herokuapp.com%2Ftypesense%2F576">
- **Standard**: _Unpaid_
- **[Issue Link](https://github.com/aviyelverse/Open-Source-Requests/issues/49)**

---

### **2. Ability to apply filters to overrides and pinned hits**

This feature allows curated / pinned hits to only be triggered if the pinned hit satisfies the current filter_by query. Available in `0.23.0.rc45`.

**Example Usage**:

```
curl "http://localhost:8108/collections/products/overrides/customize-apple" -X PUT -H "Content-Type: application/json" \
-H "X-TYPESENSE-API-KEY: ${TYPESENSE_API_KEY}" -d '{
  "rule": {
    "query": "apple",
    "match": "exact"
  },
  "includes": [
    {"id": "422", "position": 1},
    {"id": "54", "position": 2}
  ],
  "filter_curated_hits": true
}'
```

```
curl "http://localhost:8108/collections/products/documents/search?q=apple&query_by=name&pinned_hits=422:1&filter_curated_hits=true"
```

- **Posted by**: _[@jasonbosco](https://github.com/jasonbosco)_
- <img src="https://img.shields.io/endpoint?url=https%3A%2F%2Faviyel-request-board.herokuapp.com%2Ftypesense%2F549">
- **Standard**: _Unpaid_
- **[Issue Link](https://github.com/aviyelverse/Open-Source-Requests/issues/50)**

---

### **3. Curation API and filters**

When curating documents it does not seem to be possible to set rules for filter_by values of the search.

For example we would like to curate different document for search `search?q=hamburg&query_by=title&filter_by=language:en` and one where filter_by is `filter_by=language:de`.

- **Posted by**: _[@mikran](https://github.com/mikran)_
- <img src="https://img.shields.io/endpoint?url=https%3A%2F%2Faviyel-request-board.herokuapp.com%2Ftypesense%2F536">
- **Standard**: _Unpaid_
- **[Issue Link](https://github.com/aviyelverse/Open-Source-Requests/issues/51)**

---

### **4. Ranking based on Relevance and Popularity connected to Override**

If the user searches "environmentally friendly cotton t-shirts". I want to be able to re-rank the results to boost the more environmentally friendly products. (perhaps using sort_by with buckets)

```
override = {
"rule": {
"query": "environment",
"match": "contains"
},
"sort_by"="_text_match(buckets: 10):desc, environment_score:desc"
}
```

P.S.
At the same time it would also be very useful if you could apply overrides to a combination of filterable attributes as well as the query itself.

e.g.

Apply overrides to an entire product category in combination with a query. So if the user searches for t-shirt and then filters by the material cotton you can apply overides to pin/hide/boost certain items.

- **Posted by**: _[@aaroncueckermann](https://github.com/aaroncueckermann)_
- <img src="https://img.shields.io/endpoint?url=https%3A%2F%2Faviyel-request-board.herokuapp.com%2Ftypesense%2F525">
- **Standard**: _Unpaid_
- **[Issue Link](https://github.com/aviyelverse/Open-Source-Requests/issues/52)**

---

### **5. Default Value When Optional = "True"**

**Description**
Default value option when a field optional = true. In my dataset it is possible to have field with null data, but we still need to index it.

**Steps to reproduce**
Expected Behavior
We can define default value for a field, so if there is no data when adding documents, it will filled with that default value.

**Actual Behavior**
We can't create optional field if we want it to be indexed.

**Metadata**
Typsense Version: cloud.

- **Posted by**: _[@panoet](https://github.com/panoet)_
- <img src="https://img.shields.io/endpoint?url=https%3A%2F%2Faviyel-request-board.herokuapp.com%2Ftypesense%2F346">
- **Standard**: _Unpaid_
- **[Issue Link](https://github.com/aviyelverse/Open-Source-Requests/issues/53)**

---

## Creating Templates and Demos

### **1. Create a Demo of Anime instant-search app**

   - **Posted by**: Aviyel Team
   - [Check Status](https://sturdy-locust-74a.notion.site/Typesense-43e84e9df7ea4e44889d3cb1f1c4c6c1)
   - **Standard**: _Unpaid_
   - **[Issue Link](https://github.com/aviyelverse/Open-Source-Requests/issues/69)**

### **2. Build a search application with Typesense, React and Tailwind**

   - **Posted by**: Aviyel Team
   - [Check Status](https://sturdy-locust-74a.notion.site/Typesense-43e84e9df7ea4e44889d3cb1f1c4c6c1)
   - **Standard**: _Unpaid_
   - **[Issue Link](https://github.com/aviyelverse/Open-Source-Requests/issues/70)**
      
### **3. Build an instant full-text search in JavaScript with Typesense**

   - **Posted by**: Aviyel Team
   - [Check Status](https://sturdy-locust-74a.notion.site/Typesense-43e84e9df7ea4e44889d3cb1f1c4c6c1)
   - **Standard**: _Unpaid_
   - **[Issue Link](https://github.com/aviyelverse/Open-Source-Requests/issues/71)**

### **4. Adding Typesense search to an Astro Static Generated Website**

   - **Posted by**: Aviyel Team
   - [Check Status](https://sturdy-locust-74a.notion.site/Typesense-43e84e9df7ea4e44889d3cb1f1c4c6c1)
   - **Standard**: _Unpaid_
   - **[Issue Link](https://github.com/aviyelverse/Open-Source-Requests/issues/73)**

### **5. Building a search UI with Typesense**

   - **Posted by**: Aviyel Team
   - [Check Status](https://sturdy-locust-74a.notion.site/Typesense-43e84e9df7ea4e44889d3cb1f1c4c6c1)
   - **Standard**: _Unpaid_
   - **[Issue Link](https://github.com/aviyelverse/Open-Source-Requests/issues/74)**
      
---      
