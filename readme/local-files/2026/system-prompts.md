# 📃 System Prompts



<details>

<summary>On-Markets HTML</summary>



Please reference the index.html file, as well as the us-state-filter sub folder it integrates. These are both from a different investor application I put together. I have an entirely new set of properties with additional information/values for each, for a different investor client. The OM's for these are found in the OMs subfolder, and I exported my list of properties to both the Properties.xlsx and Properties.json files in the root folder. Please look through this to understand the new schema, and then update the index.html to match and showcase these new properties please.

**All States filter**

* You can get rid of the All States filter component altogether please since these only contain properties in OR & WA anyways.&#x20;
* Also please add more functionality/features such as filters for single tenant, center, or multi. Also add a badge to the top right of each property image to show the status (active, under contract, etc.). And for a lot of the multi tenants and centers, they don't have Options or rental increases or lease expiration since there's so many tenants, so as you can see in the attached image, it doesn't look good since those are the values displayed on the property cards -- so please update ones that don't have values for those fields to just display other notable fields.



**OMs**

* Do not open the OMs in a new tab, the end result is that I will be uploading the entire folder to be hosted with Netlify, so the pdf file names will also need to be changed so they are formatted correctly. So don't waste time dealing with the local file CORs issues since the OMs and code will all be hosted with Netlify

***

**Tenant Badge Components**

<figure><img src="../../../.gitbook/assets/image (291).png" alt=""><figcaption></figcaption></figure>

The tenant(s) should be displayed as clean & modern badge components, as seen in the attached image.&#x20;



</details>

<details>

<summary>Embeds - G-Maps &#x26; Placer AI</summary>





Can you please add the following embed from Placer AI: Property Area Insights:

```
"https://embedded-widget.placer.ai/widgets/v1/zip-code-map/?zipCode=" + str($Zip) + "&address=" + ($Property_Address + ", " + $City + ", " + $State + " " + str($Zip)).replace(" ", "+").replace(",", "%2C") + "&utm_source=https%3A%2F%2Fwww.placer.ai%2Fexplore%2Fpoints-of-interest"
```



</details>

<details>

<summary>Netlify - PDF Renaming</summary>



{% code overflow="wrap" %}
```
Please remember to re-name the PDF's in the OMs subfolder so they are properly formatted/structured to be uploaded to Netlify for hosting. This means get rid of the parenthesis, commas, etc. to ensure proper validation and formatting that matches the required formatting for Netlify. This means you'll also have to update the referenced PDF's in the actual application as well. 
```
{% endcode %}



</details>

```
Full Address: 290 E Monte Vista Ave, Vacaville, CA 95688
Latitude: 38.35884350645177
Longitude: -121.99016774110447

Google Maps Embed Code:
    <iframe src="https://maps.google.com/maps?q=38.3588435,-121.9901677&t=k&z=18&ie=UTF8&iwloc=&output=embed" width="100%" height="450" style="border:0;" allowfullscreen="" loading="lazy"></iframe>

Placer AI Embed Code:
    <iframe src="https://embedded-widget.placer.ai/widgets/v1/zip-code-map/?zipCode=95688&address=290%20E%20Monte%20Vista%20Ave%2C%20Vacaville%2C%20CA%2095688&utm_source=https%3A%2F%2Fwww.placer.ai%2Fexplore%2Fpoints-of-interest" width="100%" height="450" style="border:1px solid #e5e7eb;border-radius:10px" loading="lazy" title="Property Area Insights" allowfullscreen="true" allow="clipboard-write" referrerpolicy="origin" scrolling="no"></iframe>
```



**Embed Pro:**

```
file:///C:/Users/Admin/Desktop/Dynamic%20HTML/HTML-Project/Google%20Maps%20+%20Placer.ai%20Embed%20Generator.html
```



