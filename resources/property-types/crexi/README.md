# 🔍 Crexi



<details>

<summary>Kickz - Gmail</summary>

```
Access
Authorized
Access granted
Virtual Deal Room access
```



</details>

**Top Ranking**

```
https://www.crexi.com/properties?sort=Relevance&term=Top%20Ranking&pageSize=100
```

Top Performing

Percentage Rent

Percent of Sales

EV charging station

Cell Tower

EV Charger

Attractive Owner Financing

Sale Leaseback

Sale-Leaseback

Bank Foreclosure Sale

```
2% to Broker
$120K Buyside Fee
Up to 4% Buyside Fee
$100k Fee to Buyer Broker
3% Buyside Fee at List Price
```

EV as Ancillary

**Zero Cash Flow**

* ZCF Property
* Zero Cashflow

AVG STORE SALES



<details>

<summary>Crexi URL Manipulation &#x26; Parameter Injection Guide</summary>

Always set view to 100



**Instructions Prompt for Generating Crexi URL Manipulation Guide/Script/Tool (for For-Sale Properties)**

**Prompt:**

You are an expert in reverse-engineering commercial real estate platforms like Crexi.com. Your task is to create a **complete, production-ready instructions guide** (or Python/JS script + documentation) for manipulating the search URL on [https://www.crexi.com/properties](https://www.crexi.com/properties) to filter **for-sale properties** with extreme precision. This guide/script must cover **every documented and inferred URL parameter**, based on public examples, scraper tools (e.g., Apify Crexi scrapers), DOM inspections, and real-world saved searches.

Focus **exclusively on for-sale properties** (e.g., exclude pure leases where possible, but note how to blend). The goal is to enable **bulk batching, custom slicing, and automation** (e.g., for Chrome extensions, Puppeteer, or macros) to bypass Crexi's <1,000-result export limit.

Use the following real example as a baseline saved search URL (for NNN retail/special purpose car washes, on-market):

text

```
https://www.crexi.com/properties?leaseTypes%5B%5D=NNN&leaseTypes%5B%5D=Absolute%20Net&sort=New%20Listings&subtypes%5B%5D=Car%20Wash&tenantCredits%5B%5D=Franchisee&tenantCredits%5B%5D=Credit%20Rated&tenantCredits%5B%5D=Corporate%20Guarantee&tradingStatuses%5B%5D=On-Market&types%5B%5D=Retail&types%5B%5D=Special%20Purpose&pageSize=60
```

**Structure your output as follows:**

#### 1. **URL Structure Overview**

* Explain the base: https://www.crexi.com/properties? + query string.
* How arrays work: Multi-select filters use param%5B%5D=value (URL-encoded \[]).
* How to decode/encode: Always use encodeURIComponent for values with spaces/special chars.
* Pagination: pageSize=60 (default), but override to pageSize=1000 for exports (when <1k results).
* For-sale focus: Use tradingStatuses%5B%5D=On-Market + property types\[] to target sales. Note: Crexi mixes sale/lease; filter leaseTypes\[] to empty or specific to force sales.

#### 2. **Core Parameter Categories & Breakdown**

Break down **all** parameters into categories. For each:

* **Name**: Exact param (e.g., types\[]).
* **Description**: What it does.
* **Supported Values**: List examples (from docs, attempts, scrapers).
* **How to Manipulate**: Single value, array, ranges.
* **Example Addition**: How to append to a base URL.
* **For-Sale Relevance**: Why it matters for sales.

**Categories (must cover all):**

**A. Property Types (Core for Sales)**

* types\[]: Main categories (e.g., Retail, Office, Industrial, Multifamily, Special Purpose, Land, Hotel, Healthcare).
  * Example: \&types%5B%5D=Retail\&types%5B%5D=Special%20Purpose.
* subtypes\[]: Sub-types (e.g., Car Wash, Convenience Store, Restaurant).
  * Example: \&subtypes%5B%5D=Car%20Wash.

**B. Location Filters (Most Powerful for Batching)**

* states\[]: US states (e.g., TX, FL, CA).
  * Example: \&states%5B%5D=TX\&states%5B%5D=FL.
* placeIds\[]: Google Place IDs for cities/markets (e.g., ChIJvypWkWV2wYgR0E7HW9MTLvc for specific areas).
  * Example: \&placeIds%5B%5D=ChIJPV4oX\_65j4ARVW8IJ6IJUYs.
* term=: Keyword/location search (e.g., term=seattle or term=car+wash).
  * Example: \&term=Seattle.
* cities\[] or markets\[]: Inferred from scrapers (test as array).

**C. Financial Filters (Numeric Ranges for Slicing)**

* priceFrom= \&priceTo=: Asking price (e.g., \&priceFrom=0\&priceTo=2000000).
* capRateFrom= \&capRateTo=: Cap rate (e.g., \&capRateFrom=5\&capRateTo=8).
* noiFrom= \&noiTo=: Net Operating Income.
* pricePerSqFtFrom= \&pricePerSqFtTo=: Price per SF.

**D. Physical/Size Filters (Great for Batch Slicing)**

* sqFtFrom= \&sqFtTo=: Building square footage (e.g., \&sqFtFrom=0\&sqFtTo=3000).
* lotSizeFrom= \&lotSizeTo=: Lot acres.
* yearBuiltMin= \&yearBuiltMax=: Construction year (e.g., \&yearBuiltMin=1980\&yearBuiltMax=2000).
* storiesFrom= \&storiesTo=: Building stories.

**E. Tenant & Lease Filters (For NNN/Investment Sales)**

* leaseTypes\[]: NNN, Absolute Net, Gross, Modified Gross.
* tenantCredits\[]: Franchisee, Credit Rated, Corporate Guarantee.
* tenantNames\[]: Specific tenants (e.g., Mister Car Wash).
* leaseTermRemainingFrom= \&leaseTermRemainingTo=: Years left on lease.

**F. Status & Listing Filters**

* tradingStatuses\[]: On-Market (key for active sales).
* marketStatuses\[]: For Sale, Under Contract.
* saleStatuses\[]: Inferred for pure sales.

**G. Sorting & Display**

* sort=: New Listings, Price Low to High, Cap Rate High to Low, Sq Ft High to Low.
* pageSize=: 60 (default) → 1000 for max batch.
* showMap=true: Toggle map view.

**H. Advanced/Hidden Filters (From Reverse Engineering)**

* opportunityZone=true/false.
* ownerType\[]: Private, Institutional.
* buildingClass\[]: A, B, C.
* latitude= \&longitude= \&radius=: Geo bounding.
* minBeds= \&maxBeds=, minBaths= \&maxBaths=: For multifamily.

#### 3. **Advanced Manipulation Techniques**

* **Dynamic Batching for Exports** (Critical for >1k results):
  * **Price Slicing**: Loop priceFrom=0\&priceTo=2M, then 2M-4M, etc. (adapt via binary search on result count).
  * **Size Slicing**: sqFtFrom=0\&sqFtTo=3000, etc.
  * **State Slicing**: states\[]=TX (small batches).
  * **Hybrid**: State + price (e.g., TX:0-4M).
  * **Dynamic Algo**: Start priceFrom=0, binary shrink priceTo until <1k results (from DOM count: span\[data-cy="resultsCount"].count).
* **URL Mutation Rules**:
  * Preserve base params, append only.
  * Use URLSearchParams in JS to edit.
  *   Example JS snippet:JavaScript

      ```
      let url = new URL(baseUrl);
      url.searchParams.set('priceFrom', 0);
      url.searchParams.set('priceTo', 2000000);
      window.location.href = url.toString();
      ```
* **Result Count Detection**: Parse span\[data-cy="resultsCount"].count → parseInt(text.replace(/\D/g, '')).
* **Export Trigger**: Click a\[crxanalyticsevent="Aggregate - Export Results"] when <1k.
* **Pagination Fallback**: If ranges fail, use \&page=1\&pageSize=1000 (but export still needs <1k visible).

#### 4. **Examples Library (10+ Real Manipulations)**

Provide copy-paste URLs for:

* All retail NNN in TX under $5M.
* Car washes in CA/FL with cap >6%.
* New listings <3k SF.
* Etc.

####



</details>



<details>

<summary><strong>Saved Searches</strong></summary>

* Top %
* Foreclosure
* Billboards
* Food Cart Pod - OR, WA

</details>

<details>

<summary>Query URLs</summary>

```
Top Ranking
https://www.crexi.com/properties?sort=Relevance&term=Top%20Ranking&pageSize=100
```



<pre><code>Top Performing
https://www.crexi.com/properties?sort=New%20Listings&#x26;term=Top%20Performing

Percentage Rent
https://www.crexi.com/properties?sort=New%20Listings&#x26;term=Percentage%20Rent

Percentage of Sales
https://www.crexi.com/properties?term=Percentage%20of%20Sales&#x26;sort=New%20Listings
<strong>
</strong>Percent of Sales
https://www.crexi.com/properties?sort=New%20Listings&#x26;term=Percent%20of%20Sales


EV charging station
https://www.crexi.com/properties?sort=New%20Listings&#x26;term=EV%20charging%20station

Cell Tower
https://www.crexi.com/properties?sort=New%20Listings&#x26;term=Cell%20Tower

EV Charger
https://www.crexi.com/properties?sort=New%20Listings&#x26;term=EV%20Charger

Assumable
</code></pre>



```
Attractive Owner Financing
https://www.crexi.com/properties?sort=New%20Listings&term=Owner%20Financing
https://www.crexi.com/properties?sort=Relevance&term=Attractive%20Owner%20Financing
```

Sale Leaseback

Sale-Leaseback

Bank Foreclosure Sale

```
2% to Broker
$120K Buyside Fee
Up to 4% Buyside Fee
$100k Fee to Buyer Broker
3% Buyside Fee at List Price
```

EV as Ancillary

**Zero Cash Flow**

* ZCF Property
* Zero Cashflow

AVG STORE SALES



</details>
