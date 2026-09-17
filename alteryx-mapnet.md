# Alteryx / MapNet

<details>

<summary>MapNet</summary>

1. Demographic Report by Property Type.yxwz - [http://mapnet/gallery/#!/app/Demographic-Report-by-Property-Type/6137de75d6996d1cb88011fc](http://mapnet/gallery/#!/app/Demographic-Report-by-Property-Type/6137de75d6996d1cb88011fc)
2. See if GLM-4.6 Can read/access the generated PDF. If not, then go to Stirling PDF to run the ‘PDF to Image’ tool - [http://localhost:8181/pdf-to-img](http://localhost:8181/pdf-to-img)



</details>

<details>

<summary>GLM-4.6</summary>

```
Please help me transform these demographic slides into a more professional, modern, and high-quality presentation. There are 4 main demographic slides covering geographical information, socioeconomic data, major employers, and statistical tables.

- **Modern Design**: Clean, professional layout with consistent color scheme and typography
- **Better Organization**: Information is logically grouped and easier to digest
- **Enhanced Visual Hierarchy**: Important data points are highlighted for quick comprehension
- **Improved Data Visualization**: Charts and tables are formatted for clarity
- **Professional Styling**: Consistent with modern corporate presentation standards
```

***

1. **Cover Slide**: A clean, professional title slide with "Mountain Home Demographic Report" and subtitle "Comprehensive Socioeconomic Analysis"
2. **Geographic Overview**: An enhanced map of the Mountain Home area with improved visual clarity, highlighting key transportation infrastructure including:
   * Mountain Home Municipal Airport
   * Highway 67, Highway 84, and Highway 20
   * Surrounding geographical features
3. **Socioeconomic Data**: A visually organized dashboard presenting six key metrics:
   * Population
   * Employment
   * Households
   * Housing
   * Income
   * Education
4. **Major Employers**: A split-screen layout featuring:
   * Map showing employer locations
   * Ranked list of top 10 employers with employee counts
5. **Statistical Tables**: Organized data presentation showing:
   * Population and household data by distance (1/3/5 miles)
   * Retail spending patterns
   * Demographic profiles including age and education distributions
   * Key metrics like Total Population and Average Household Income

</details>

***

<details>

<summary>🧠 Prompt: “PDF Market Name Replacer App”</summary>

> I have PDF demographic reports automatically generated from an Alteryx workflow.\
> These PDFs contain placeholder text like “your selected area,” “your selected geography,” “the selected area,” etc., which I want to automatically replace with the correct city or market name (e.g., “Kennewick, WA” or “Portland Market”) after generation.
>
> I don’t have access to the Alteryx workflow itself — only the finished PDFs.
>
> Please write a **standalone Python application** that:
>
> #### 🧩 Functionality
>
> 1. Lets me **drag and drop one or multiple PDF files** (or select them via file dialog).
> 2. Prompts me to **enter the market name** (e.g., “Kennewick, WA”).
> 3. Automatically **finds and replaces** all instances of the following phrases (case-insensitive):
>    * “your selected area”
>    * “your selected geography”
>    * “the selected area”
>    * “the selected geography”
>    * “the selected territory”
>    * “your selected territory”
> 4. Performs **in-place text replacement** that visually maintains formatting, using an open-source PDF library (such as **PyMuPDF**, also known as `fitz`).
> 5. Saves the modified files to an **“updated\_reports”** folder (created automatically next to the script), appending `" - Updated.pdf"` to each filename.
> 6. Prints or displays confirmation when complete.
>
> #### 🖥️ Interface
>
> * Use **Tkinter** or a simple Python GUI that:
>   * Has a **drop zone** for PDFs or a “Select Files” button.
>   * Has a **text input box** for the market name.
>   * Has a **“Process PDFs” button**.
>   * Displays progress or success messages.
>
> #### ⚙️ Technical Details
>
> * Use **PyMuPDF (fitz)** for reading and editing the PDF text.
> * Replace all matching phrases across all pages of each document.
> * Make replacements case-insensitive and apply redaction or overlay text where necessary to ensure the visible text changes.
> * Maintain document layout and formatting as closely as possible.
> * Save all updated PDFs locally without needing any external services.
>
> #### 🎯 Goal
>
> The result should be a **drag-and-drop desktop tool** I can use repeatedly:
>
> * I generate reports with Alteryx
> * Drop them into the app
> * Enter the city/market name
> * Get cleaned PDFs ready to send to clients
>
> Please provide the **complete working Python code** in one script, with installation instructions (pip install commands) and any packaging recommendations if I later want to convert it into a standalone `.exe` or `.app` using `pyinstaller`.
>
> > Bonus:
> >
> > * Include a progress bar.
> > * Automatically detect and skip files that are already updated (contain the replacement term).
> > * Allow batch processing via folder selection.
> > * Make the app remember the last used market name.

</details>
