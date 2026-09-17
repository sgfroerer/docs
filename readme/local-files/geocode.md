---
layout:
  width: default
  title:
    visible: true
  description:
    visible: false
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: true
  metadata:
    visible: true
  tags:
    visible: true
  actions:
    visible: true
  anchors:
    visible: true
---

# 🌏 GeoCode

<details>

<summary>Table - Comparison</summary>

<table data-header-hidden><thead><tr><th width="129.0909423828125">Website</th><th width="216.9090576171875">Free Tier Limits</th></tr></thead><tbody><tr><td><a href="http://developer.here.com/geocoder">HERE</a></td><td>10,000 per day<br>(30,000 Monthly)</td></tr><tr><td><a href="https://locationiq.com/pricing"><strong>Location IQ</strong></a><br><a href="https://docs.locationiq.com/reference/search-structured">API Reference</a></td><td>5000 requests /day</td></tr><tr><td><a href="http://census.gov/">Census.gov</a></td><td>10,000 records | 5MB</td></tr><tr><td><a href="https://dash.geocod.io/">Geocodio</a></td><td>2,500 per day</td></tr><tr><td><a href="https://www.geoapify.com/tools/geocoding-online/">Geoapify</a></td><td>3,000 requests/day</td></tr><tr><td><a href="https://dev.placekey.io/home">Placekey</a></td><td>10,000</td></tr><tr><td><a href="https://dashboard.radar.com/maps/api-explorer/geocoding?project=67b129f251edcf0444aca489&#x26;live=false">Radar</a></td><td>100,000 Monthly</td></tr></tbody></table>

</details>

<details>

<summary><a href="https://geocoding.geo.census.gov/geocoder/locations/addressbatch?form">Batch Geocoding Census</a></summary>

**Sample CSV File**

```html
1,4600 Silver Hill Road,Washington,DC,20233
2,99999 Calle A,San Juan,PR,00926,URB Juan Smith
```

**Headers**

```html
Input #	Input Address	Match?	Exact?	Standardized Address	Long,Lat	Tigerline ID	Tigerline ID Side	STATE CODE	COUNTY CODE	TRACT CODE	BLOCK CODE
```

</details>

<a href="file:///C:/Users/Admin/Desktop/Dynamic%20HTML/HTML-Project/Misc%20Projects/Census%20Batch%20Geocoder%20Prep.html" class="button primary" data-icon="broom-wide">Census Batch Geocoder Prep</a>

***

<details>

<summary>Retail_Geocoder</summary>

{% code fullWidth="true" %}
```bash
cd Desktop\Server-Projects\ActiveDevelopment\grist-tenants-costar\retail_geocoder
```
{% endcode %}

{% code fullWidth="true" %}
```python
python launcher_script.py
```
{% endcode %}

***

**Command Line**

Basic Usage

{% code overflow="wrap" fullWidth="true" %}
```python
python retail_geocoder.py input_addresses.csv --address-col "address" --tenant-col "tenant_name" --locationiq-key "pk.6037eb194b590405140c1b9e9c123be7" --output geocoded_results.csv
```
{% endcode %}

Command Line Arguments

* `input_file`: Path to CSV with addresses
* `-address-col` / `a`: Column containing addresses
* `-tenant-col` / `t`: Column containing tenant names
* `-locationiq-key` / `k`: LocationIQ API key (recommended)
* `-workers` / `w`: Number of parallel workers
* `-output` / `o`: Output CSV file path



</details>

***



{% embed url="https://www.geoapify.com/tools/geocoding-online/" %}
3,000 requests/day
{% endembed %}

> The maximum number of rows that will be processed is 500. Please split larger files or try the [Geocoding API](https://www.geoapify.com/geocoding-api/) (up to 3000 requests/day for free).

{% embed url="https://dash.geocod.io/" %}
2,500 per day
{% endembed %}

> Upload via .tsv file
