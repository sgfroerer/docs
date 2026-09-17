# 👾 React

<details>

<summary>Cursor - Dynamic Standalone</summary>



```
cd Downloads\FetchGrist\Widgets\OwnerProperties-Standalone && python -m http.server 8080 
```



</details>

<details>

<summary>Property Email Generator</summary>

```
npx create-react-app property-email-generator
cd property-email-generator

npm install lucide-react
npm install -D tailwindcss
npx tailwindcss init
```

**Replace** the Code:

* Open the `src` folder inside your new project.
* Find the `App.js` file.
* Delete everything in that file and paste the code from the artifact into it.

```
npm start
```

**Batch File**

```bash
@echo off
cd %USERPROFILE%\Desktop\Server-Projects\React\Projects\property-email-generator
npm start
```

</details>

<details>

<summary>create-react-app is deprecated</summary>

Yes, Create React App (CRA) is officially deprecated as of February 2025. The React team has moved away from recommending it for new projects due to limitations in performance, lack of support for modern features, and the availability of better alternatives like [Vite](https://www.google.com/search?rlz=1C1VDKB_enUS1100US1100\&cs=0\&sca_esv=6d0ad94c53cfdd66\&sxsrf=AE3TifPvFZzjENBdd1xCF6vYv8g4H3xWww%3A1751055336545\&q=Vite\&sa=X\&ved=2ahUKEwiBu_-5tZKOAxWQrokEHd5qFRkQxccNegQIAhAC\&mstk=AUtExfB05qpQGAcWkVP-duYprR2nMWkQPscTN2uowIfh1Iw95TY_7xuUwmht6C0SWjAcSkDCPXoh4mRIvLbdDEEgI2U-BgujBv5GfO0BiaISZzNcOZyf_qWK3K9S8I-aH5wRYU2GN4IGwYUfbWKGDpxGExM_LsFZFerXLvnms55t6qmhRhA\&csui=3), [Next.js](https://www.google.com/search?rlz=1C1VDKB_enUS1100US1100\&cs=0\&sca_esv=6d0ad94c53cfdd66\&sxsrf=AE3TifPvFZzjENBdd1xCF6vYv8g4H3xWww%3A1751055336545\&q=Next.js\&sa=X\&ved=2ahUKEwiBu_-5tZKOAxWQrokEHd5qFRkQxccNegQIAhAD\&mstk=AUtExfB05qpQGAcWkVP-duYprR2nMWkQPscTN2uowIfh1Iw95TY_7xuUwmht6C0SWjAcSkDCPXoh4mRIvLbdDEEgI2U-BgujBv5GfO0BiaISZzNcOZyf_qWK3K9S8I-aH5wRYU2GN4IGwYUfbWKGDpxGExM_LsFZFerXLvnms55t6qmhRhA\&csui=3), and [Remix](https://www.google.com/search?rlz=1C1VDKB_enUS1100US1100\&cs=0\&sca_esv=6d0ad94c53cfdd66\&sxsrf=AE3TifPvFZzjENBdd1xCF6vYv8g4H3xWww%3A1751055336545\&q=Remix\&sa=X\&ved=2ahUKEwiBu_-5tZKOAxWQrokEHd5qFRkQxccNegQIAhAE\&mstk=AUtExfB05qpQGAcWkVP-duYprR2nMWkQPscTN2uowIfh1Iw95TY_7xuUwmht6C0SWjAcSkDCPXoh4mRIvLbdDEEgI2U-BgujBv5GfO0BiaISZzNcOZyf_qWK3K9S8I-aH5wRYU2GN4IGwYUfbWKGDpxGExM_LsFZFerXLvnms55t6qmhRhA\&csui=3). While existing CRA projects will continue to work, new projects should utilize these newer tools. Reasons for Deprecation:

* **Performance Issues:**&#x43;RA relies on Webpack, which can be slower compared to newer bundlers like Vite and esbuild, leading to slower build times.
* **Lack of Modern Features:**&#x43;RA lacks out-of-the-box support for features like server-side rendering (SSR) and efficient code splitting.
* **No Active Maintainers:**&#x54;he React team no longer actively maintains Create React App, meaning it won't receive updates or bug fixes.
* **Better Alternatives Exist:**&#x46;rameworks like Vite, Next.js, and Remix offer faster builds, improved developer experience, and better performance.&#x20;

What to do instead:

* [**Vite:**.Opens in new tab](https://www.google.com/search?rlz=1C1VDKB_enUS1100US1100\&cs=0\&sca_esv=6d0ad94c53cfdd66\&sxsrf=AE3TifPvFZzjENBdd1xCF6vYv8g4H3xWww%3A1751055336545\&q=Vite\&sa=X\&ved=2ahUKEwiBu_-5tZKOAxWQrokEHd5qFRkQxccNegQIJhAD\&mstk=AUtExfB05qpQGAcWkVP-duYprR2nMWkQPscTN2uowIfh1Iw95TY_7xuUwmht6C0SWjAcSkDCPXoh4mRIvLbdDEEgI2U-BgujBv5GfO0BiaISZzNcOZyf_qWK3K9S8I-aH5wRYU2GN4IGwYUfbWKGDpxGExM_LsFZFerXLvnms55t6qmhRhA\&csui=3)A fast, modern build tool that provides instant hot module replacement (HMR) and optimized builds. It's a great choice for learning React or building single-page applications.
* [**Next.js**](https://www.google.com/search?rlz=1C1VDKB_enUS1100US1100\&cs=0\&sca_esv=6d0ad94c53cfdd66\&sxsrf=AE3TifPvFZzjENBdd1xCF6vYv8g4H3xWww%3A1751055336545\&q=Next.js\&sa=X\&ved=2ahUKEwiBu_-5tZKOAxWQrokEHd5qFRkQxccNegQIJBAB\&mstk=AUtExfB05qpQGAcWkVP-duYprR2nMWkQPscTN2uowIfh1Iw95TY_7xuUwmht6C0SWjAcSkDCPXoh4mRIvLbdDEEgI2U-BgujBv5GfO0BiaISZzNcOZyf_qWK3K9S8I-aH5wRYU2GN4IGwYUfbWKGDpxGExM_LsFZFerXLvnms55t6qmhRhA\&csui=3)**:**.Opens in new tabA full-stack framework with built-in routing, optimized builds, and server-side rendering.
* [**Remix:**.Opens in new tab](https://www.google.com/search?rlz=1C1VDKB_enUS1100US1100\&cs=0\&sca_esv=6d0ad94c53cfdd66\&sxsrf=AE3TifPvFZzjENBdd1xCF6vYv8g4H3xWww%3A1751055336545\&q=Remix\&sa=X\&ved=2ahUKEwiBu_-5tZKOAxWQrokEHd5qFRkQxccNegQIKBAD\&mstk=AUtExfB05qpQGAcWkVP-duYprR2nMWkQPscTN2uowIfh1Iw95TY_7xuUwmht6C0SWjAcSkDCPXoh4mRIvLbdDEEgI2U-BgujBv5GfO0BiaISZzNcOZyf_qWK3K9S8I-aH5wRYU2GN4IGwYUfbWKGDpxGExM_LsFZFerXLvnms55t6qmhRhA\&csui=3)A framework built on web standards that prioritizes performance and developer experience.&#x20;

In summary, while Create React App was a popular tool for bootstrapping React projects, it has been deprecated due to performance limitations and the availability of better alternatives. Developers should now consider using Vite, Next.js, or Remix for new React projects. <br>

</details>

#### **Grist On-Markets Report**

{% hint style="info" %}
Navigate into folder and click on the `.bat` file

{% code fullWidth="true" %}
```bash
cd Desktop\Server-Projects\On-Market Report Python\On-Markets Report - TRAE\Grist-Conversion\start_server.bat
```
{% endcode %}

```bash
start_server.bat
```
{% endhint %}

***

#### **Tenant-Profiles**

{% hint style="info" %}
Navigate into directory & Start the development server:

```bash
cd Desktop\Server-Projects\ActiveDevelopment\Tenant-Profiles\tenant-profiles
```

```bash
npm run dev
```
{% endhint %}

***

**tenant-location-lens**

{% hint style="info" %}
Navigate into directory & Start the development server:

```bash
cd Desktop\Server-Projects\ActiveDevelopment\grist-tenants-costar\tenant-location-lens
```

```bash
npm run dev
```
{% endhint %}

**tenant-locations-matcher**

{% hint style="info" %}
Navigate into directory & Start the development server:

```bash
cd Desktop\Server-Projects\ActiveDevelopment\grist-tenants-costar\tenant-locations-matcher
```

```bash
npm run dev
```
{% endhint %}

***

**Centers-Bolt**

{% hint style="info" %}
Navigate into directory & Start the development server:

```bash
cd Desktop\Server-Projects\ActiveDevelopment\bolt-centers
```

```bash
cd project && npm install && npm run dev
```
{% endhint %}

***

<details>

<summary>Lovable Dev</summary>

[Instant CRE Valuation](https://lovable.dev/projects/2c9719e8-e5d1-4f6f-950f-a5bdcede1357)



[Owner Contacts & Emails](https://lovable.dev/projects/40dd6b5d-8461-41f2-b8e5-04948c33a634)

***

**Kickz**

[CRE Buyer Matcher](https://lovable.dev/projects/6cccbafb-846c-4ce3-8221-9aae770b47b4)

</details>

