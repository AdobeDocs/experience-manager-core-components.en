---
title: Text Component (v1)
seo-title: Text Component (v1)
description: null
seo-description: The Text Component is a rich text editing and composing component that features in-place editing.
uuid: b787ebac-fa85-416a-b96b-9d2ee85428ec
content-type: reference
products: SG_EXPERIENCEMANAGER/CORECOMPONENTS-new
discoiquuid: d5e37dc7-dfd4-4a44-89b6-c15651472c43
disttype: dist5
gnavtheme: light
groupsectionnavitems: no
hidemerchandisingbar: inherit
hidepromocomponent: inherit
modalsize: 426x240
noindex: true
index: y
internal: n
snippet: y
---

# Text Component (v1){#text-component-v}

The Text Component is a rich text editing and composing component that features in-place editing.

## Usage {#usage}

The Text Component offers a robust rich text editor that allows for easy text editing in a simplified, in-line editor as well as a full screen format.

The [edit dialog](text-v1.md#main-pars_title) features in-line editing with limited options with full functionality available in the full-screen edit dialog. Using the [design dialog](text-v1.md#main-pars_title_1995166862), text formatting options such as headings, special characters, and paragraph styles can be configured for the template for the content author.

## Version and Compatibility {#version-and-compatibility}

This document describes v1 of the Text Component, originally introduced with release 1.0.0 of the Core Components with AEM 6.3.

The following table lists the compatibility of v1 of the Text Component.

|AEM Version|Text Component v1|
|--- |--- |
|6.3|Compatible|
|6.4|Compatible|

>[!CAUTION]
>
>This document describes v1 of the Text Component.
>
>For details of the current version of the Text Component, see the [Text Component](text.md) document.

## Sample Component Output {#sample-component-output}

The following is sample taken from [We.Retail](https://helpx.adobe.com/experience-manager/6-4/sites/developing/using/we-retail.html).

### Screenshot {#screenshot}

![](assets/chlimage_1-27.png) 

### HTML {#html}

```
<div class="cmp cmp-text aem-GridColumn aem-GridColumn--default--12">
<p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer porttitor ante a tortor volutpat maximus. Donec eu porta eros. Aenean sit amet eleifend arcu, eu vestibulum magna. Fusce eget nisi tincidunt, tristique felis quis, tincidunt est. Aliquam consequat aliquam quam non eleifend. Phasellus ut magna luctus, aliquam risus eget, fermentum augue. Aliquam lobortis accumsan magna, quis efficitur enim dictum eu. Pellentesque iaculis felis eget felis commodo, non euismod dolor euismod. Quisque nec arcu rutrum, mollis tortor non, sollicitudin odio. Sed dictum nulla mauris, eu pretium dui vulputate a. Maecenas lacus massa, egestas vitae tincidunt eu, interdum et magna. Lorem ipsum dolor sit amet, consectetur adipiscing elit. In eleifend ex lacus, in consectetur nunc interdum et. Donec interdum mi vitae dolor pretium mattis. In quis arcu sapien. Phasellus at metus vitae nisi tincidunt varius.<br />
</p>
</div>
```

### JSON {#json}

```
"text": {
              "columnClassNames": "aem-GridColumn aem-GridColumn--default--12",
              "text": "<p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer porttitor ante a tortor volutpat maximus. Donec eu porta eros. Aenean sit amet eleifend arcu, eu vestibulum magna. Fusce eget nisi tincidunt, tristique felis quis, tincidunt est. Aliquam consequat aliquam quam non eleifend. Phasellus ut magna luctus, aliquam risus eget, fermentum augue. Aliquam lobortis accumsan magna, quis efficitur enim dictum eu. Pellentesque iaculis felis eget felis commodo, non euismod dolor euismod. Quisque nec arcu rutrum, mollis tortor non, sollicitudin odio. Sed dictum nulla mauris, eu pretium dui vulputate a. Maecenas lacus massa, egestas vitae tincidunt eu, interdum et magna. Lorem ipsum dolor sit amet, consectetur adipiscing elit. In eleifend ex lacus, in consectetur nunc interdum et. Donec interdum mi vitae dolor pretium mattis. In quis arcu sapien. Phasellus at metus vitae nisi tincidunt varius.</p>\n",
              "richText": true,
              ":type": "weretail/components/content/text"
            }
```

>[!NOTE]
>
>JSON export from the Core Components requires release 1.1.0 of the Core Components. Please see the [compatibility information for Core Components v1](versions.md#main-pars_title_236368006) for more information.

## Edit Dialog {#edit-dialog}

The edit dialog offers the standard rich text formatting tools a user would expect to compose text.

![](assets/chlimage_1-52.png)

* Bold

  ![](assets/chlimage_1-53.png)

  Used to apply bold formatting to selected text or boldly format text entered after the cursor.

  **Ctrl+B** can be used as a keyboard shortcut.

* Italic

  ![](assets/chlimage_1-54.png)

  Used to apply italicized formatting to selected text or italicize text entered after the cursor.

  **Ctrl+I** can be used as a keyboard shortcut.

* Underline

  ![](assets/chlimage_1-55.png)

  Used to apply underlined formatting to selected text or underline text entered after the cursor.

  **Ctrl+U** can be used as a keyboard shortcut.

* Subscript

  ![](assets/chlimage_1-56.png)

  Used to format selected text or text entered after the cursor as subscript.

* Superscript

  ![](assets/chlimage_1-57.png)

  Used to format selected text or text entered after the cursor as superscript.

* Paste as Text

  ![](assets/chlimage_1-58.png)

  Pastes any copied text as plain text without any formatting.

  When selecting this option a window opens where the text can be pasted as plain text with no formatting as a preview before it is inserted into the text. Accept by tapping or clicking the checkmark, cancel by tapping or clicking the x.

  ![](assets/chlimage_1-59.png)

* Paste from Word

  ![](assets/chlimage_1-60.png)

  When selecting this option a window opens where the text can be pasted maintaining its formatting as a preview before it is inserted into the text. Accept by tapping or clicking the checkmark, cancel by tapping or clicking the x.

  ![](assets/chlimage_1-61.png)

* Hyperlink

  ![](assets/chlimage_1-62.png)

  Use this option to convert the selected text into a hyperlink or modify an already defined link. This option is only active when text is already selected and opens a window with additional options for setting the link.

  ![](assets/chlimage_1-63.png)

    * Enter the location

        * Use the Open Selection Dialog to choose a path in AEM
        * If the link is not within AEM, enter the absolute URL (non-absolute paths are interpreted as relative to AEM)

    * Enter alternative descriptive text for the link
    * Select link behavior

        * Target
        * Same Tab
        * New Tab
        * Parent Frame
        * Top Frame

  Tap or click the checkmark to apply the link or the x to cancel.

* Unlink

  ![](assets/chlimage_1-64.png)

  Use this option to remove a link already applied to the selected text. This option is only active when a link is already selected.

* Find

  ![](assets/chlimage_1-65.png)

  Use this option to search the text for occurrences of a specified text string. Selecting this option opens a window for specifying the search options.

  ![](assets/chlimage_1-66.png)

  Enter the text for which you want to search and tap or click **Find** to begin the search. Tap or click the x to cancel.

  If you wish to do an exact match according to the case, select the option **Match Case** before starting the search.

  If a match is found, it is highlighted and the search dialog is dimmed. Tap or click the **Find** button again in the dimmed dialog to search for the next occurrence.

  ![](assets/chlimage_1-67.png)

  If no additional occurrences are found, a message will be displayed and the search will restart from the beginning of the text.

  ![](assets/chlimage_1-68.png)

* Replace

  ![](assets/chlimage_1-69.png)

  Use this option to search the text for occurrences of a specified text string and replace the matches with another string. Selecting this option opens a window for specifying the search and replace options.

  ![](assets/chlimage_1-70.png)

  Enter the text for which you want to search as well as the text with which it should be replaced.

  Tap or click **Find** to begin the search. Click or tap the x to cancel.

  If you wish to do an exact match according to the case, select the option **Match Case** before starting the search.

  If a match is found, it is highlighted and the search dialog is dimmed. Click the **Find** button again in the dimmed dialog to search for the next occurrence or select the **Replace** button to replace the highlighted, matched text. Note that the **Replace** button is only active once a match is made.

  Select **Replace all** to replace all occurrences of the text at once.

* Align Text Left

  ![](assets/chlimage_1-71.png)

  Used to align the text to the left margin.

* Center Text

  ![](assets/chlimage_1-72.png)

  Used to center the text.

* Align Text Right

  ![](assets/chlimage_1-73.png)

  Used to align the text to the right margin.

* Bullet

  ![](assets/chlimage_1-74.png)

  Used to format the selected text as a bulleted list or begin the insertion of a bulleted list after the cursor.

  To end a bulleted list, tap or click the **Bullet** button again or enter two carriage returns.

* Numbered

  ![](assets/chlimage_1-75.png)

  Used to format the selected text as a numbered list or begin the insertion of a numbered list after the cursor.

  To end a numbered list, tap or click the **Numbered** button again or enter two carriage returns.

* Outdent

  ![](assets/chlimage_1-76.png)

  Used to decrease the indentation level of the selected text or text entered after the cursor.

  Only active if the selected text or position of the cursor is already indented.

* Indent

  ![](assets/chlimage_1-77.png)

  Used to increase the indentation level of the selected text or text entered after the cursor.

* Table

  ![](assets/chlimage_1-78.png)

  Used to insert a table into the text. Selecting this option opens a window for specifying the details of the table.

  ![](assets/chlimage_1-79.png)

    * **Columns** - The number of columns of the table (required)
    * **Rows** - The number of rows of the table (required)
    * **Width** - The width of the table
    * **Height** - The height of the table
    * **Cell paddin**g - The space around the cell content
    * **Cell spacing** - The space between cells
    * **Border** - The weight of the border lines of the table
    * If for the header of the table:

        * The first row should be used
        * The first column should be used
        * The first row and first column should be used
        * Or no header should be used.

    * **Caption** - The caption of the table

* Check Spelling

  ![](assets/chlimage_1-80.png)

  Used to check the spelling of the text content. Possible misspellings are underlined with broken, red lines.

* Special Characters

  ![](assets/chlimage_1-81.png)

  Used to insert special characters into the text. Selecting this option opens a window where the available characters are displayed.

  ![](assets/chlimage_1-82.png)

  Tap or click the desired character to insert it into the text after the cursor. Multiple characters can be inserted. Tap or click the x to close the selection window.

* Source Edit

  ![](assets/chlimage_1-83.png)

  Used to view and modify the HTML source of the text.

  Tap or click the **Source Edit** icon to change the content of the text from the formatted view to view the raw HTML. In this mode, all other formatting options are disabled. Tap or click the **Source Edit** icon again to return to the formatted view.

  >[!CAUTION]
  >
  >As always the case with access to raw HTML, care must be exercised when using the **Source Edit** option!
  >
  >
  >HTML entered via **Source Edit** is scanned for XSS risks and any scripts that are inserted are removed and will not appear on the resulting page. However malformed HTML entered in **Source Edit** can break the template for the page resulting in unexpected formatting or rendering the resulting page unusable.

* Paragraph Format

  ![](assets/chlimage_1-84.png)

  Used to apply paragraph formatting to the selected text or to text inserted after the cursor. Selecting this options opens a dropdown from which the paragraph format is selected.

  ![](assets/chlimage_1-85.png)

The text component can be edited in-line as well, but due to space restraints, not all formatting options are available in-line. To see all options, switch to full-screen mode.

![](assets/chlimage_1-86.png) 

## Design Dialog {#design-dialog}

The design dialog allows the template author to define which text formatting options are available to the content authors.

### Features {#features}

![](assets/chlimage_1-28.png)

The following features can be activated or deactivated for the component.

* Paste plain text
* Past from word
* Find and replace
* Spell checker
* Source editing

### Formatting {#formatting}

![](assets/chlimage_1-29.png)

The following formatting options can be activated or deactivated for the component.

* Table
* Lists
* Alignment
* Bold, italic, underline
* Links
* Sub/superscript

### Paragraph Styles {#paragraph-styles}

![](assets/chlimage_1-30.png)

Paragraph styles can be activated or deactivated for the component. When activated, the allowed formats can be defined.

* Tap or click the **Add** button to insert a new style.
* Enter the code of the style and a description that will be displayed in the edit dialog.
* To remove a style tap or click the **Delete** button.
* To rearrange the order of the formats tap or click and drag the handles.

### Special Characters {#special-characters}

![](assets/chlimage_1-31.png)

The option to insert special characters can be activated or deactivated for the component. When activated, the allowed characters can be defined.

* Tap or click the **Add** button to insert a new character.
* Enter the HTML code of the character and a description that will be displayed in the edit dialog.
* To remove a character tap or click the **Delete** button.
* To rearrange the order of the characters tap or click and drag the handles.

## Technical Details {#technical-details}

The latest technical documentation about the Text Component [can be found on GitHub](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/text/v1/text).

The entire core components project can be downloaded from GitHub.

Further details about developing Core Components can be found in the [Core Components developer documentation](developing.md). 
