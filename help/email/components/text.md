---
title: Email Text Component
description: The Email Text Component is a rich text editing and composing component that features in-place editing.
role: Architect, Developer, Admin, User
---

# Email Text Component{#email-text-component}

The Email Text Component is a rich text editing and composing component that features in-place editing.

## Usage {#usage}

The Email Text Component offers a robust rich text editor that allows for easy text editing in a simplified, in-line editor as well as a full screen format.

The [edit dialog](#edit-dialog) features in-line editing with limited options with full functionality available in the full-screen edit dialog. Using the [design dialog,](#design-dialog) text formatting options such as headings, special characters, and paragraph styles can be configured for the template for the content author.

## Version and Compatibility {#version-and-compatibility}

The current version of the Email Text Component is v1, which was introduced with release X of the Email Core Components in October 2022, and is described in this document.

The following table details all supported versions of the component, the AEM versions with which the versions of the component is compatible, and links to documentation for previous versions.

|Component Version|AEM 6.5|AEM as a Cloud Service|
|---|---|---|
|v1|Compatible|Compatible|

For more information about Core Component versions and releases, see the document [Email Core Components Versions.](/help/email/versions.md)

## Sample Component Output {#sample-component-output}

To experience the Text Component as well as see examples of its configuration options as well as HTML and JSON output, visit the [Component Library](https://adobe.com/go/aem_cmp_library_email_text).

### Technical Details {#technical-details}

The latest technical documentation about the Email Text Component [can be found on GitHub](https://adobe.com/go/aem_cmp_tech_email_text_v1).

Further details about developing Core Components can be found in the [Core Components developer documentation](/help/developing/overview.md).

## The Email Text Component and the Rich Text Editor {#the-text-component-and-the-rich-text-editor}

The Email Text Component leverages the AEM Rich Text Editor (RTE). The RTE provides content authors with a wide range of functionality for editing their text content. The RTE is very flexible in its configuration and offers a number of options. Further details about how the RTE can be configured can be found in the articles [Configure the Rich Text Editor](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/configuring-and-extending/rich-text-editor.html) and [Configure the Rich Text Editor plug-ins](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/configuring-and-extending/configure-rich-text-editor-plug-ins.html).

The remainder of this document demonstrates the standard configuration of the Email Text Component with the out-of-the-box RTE configuration.

>[!NOTE]
>
>Only options enabled by [UI configurations of the RTE](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/configuring-and-extending/configure-rich-text-editor-plug-ins.html) are available in the Email Text Component.

## Edit Dialog {#edit-dialog}

![Text Component's edit dialog](/help/email/assets/email-text-edit.png)

### Formatting Options {#options}

The edit dialog offers the standard rich text formatting tools a user would expect to compose text.

#### Bold

![Bold icon](/help/assets/text-bold.png)

Used to apply bold formatting to selected text or boldly format text entered after the cursor.

**Ctrl+B** can be used as a keyboard shortcut.

#### Italic

![Italic icon](/help/assets/text-italic.png)

Used to apply italicized formatting to selected text or italicize text entered after the cursor.

**Ctrl+I** can be used as a keyboard shortcut.

#### Underline

![Underline icon](/help/assets/text-underline.png)

Used to apply underlined formatting to selected text or underline text entered after the cursor.

**Ctrl+U** can be used as a keyboard shortcut.

#### Subscript

![Subscript icon](/help/assets/text-subscript.png)

Used to format selected text or text entered after the cursor as subscript.

#### Superscript

![Superscript icon](/help/assets/text-superscript.png)

Used to format selected text or text entered after the cursor as superscript.

#### Paste as Text

![Paste as text icon](/help/assets/text-paste-text.png)

Pastes any copied text as plain text without any formatting.

When selecting this option a window opens where the text can be pasted as plain text with no formatting as a preview before it is inserted into the text. Accept by tapping or clicking the check mark, cancel by tapping or clicking the x.

![Paste as text example](/help/assets/text-paste-text-example.png)

#### Paste from Word

![Paste from Word icon](/help/assets/text-paste-word.png)

When selecting this option a window opens where the text can be pasted maintaining its formatting as a preview before it is inserted into the text. Accept by tapping or clicking the check mark, cancel by tapping or clicking the x.

![Paste from Word example](/help/assets/text-paste-word-example.png)

#### Hyperlink

![Hyperlink icon](/help/assets/text-hyperlink.png)

Use this option to convert the selected text into a hyperlink or modify an already defined link. This option opens a window with additional options for setting the link.

![Hyperlink example](/help/assets/text-hyperlink-example.png)

* Enter the path
  * Use the **Open Selection** dialog to choose a path in AEM
  * If the link is not within AEM, enter the absolute URL
    * Non-absolute paths are interpreted as relative to AEM
* Enter alternative descriptive text for the link
* Select link behavior
  * Target
  * Same Tab
  * New Tab
  * Parent Frame
  * Top Frame

Tap or click the check mark to apply the link or the x to cancel.

#### Unlink

![Unlink icon](/help/assets/text-unlink.png)

Use this option to remove a link already applied to the selected text. This option is only active when a link is already selected.

#### Anchor {#anchor}

![Anchor icon](/help/email/assets/anchor.png)

Use this option to insert an anchor into the text.

#### Find

![Find icon](/help/assets/text-find.png)

Use this option to search the text for occurrence of a specified text string. Selecting this option opens a window for specifying the search options.

![Find example](/help/assets/text-find-example.png)

Enter the text for which you want to search and tap or click **Find** to begin the search. Tap or click the x to cancel.
If you wish to do an exact match according to the case, select the option **Match Case** before starting the search.
If a match is found, it is highlighted and the search dialog is dimmed. Tap or click the **Find** button again in the dimmed dialog to search for the next occurrence.

![Find example found](/help/assets/text-find-example-found.png)

If no additional occurrences are found, a message will be displayed and the search will restart from the beginning of the text.

![Find example no more occurrences](/help/assets/text-find-example-found-end.png)

#### Replace

![Replace icon](/help/assets/text-replace.png)

Use this option to search the text for occurrences of a specified text string and replace the matches with another string. Selecting this option opens a window for specifying the search and replace options.

![Replace example](/help/assets/text-replace-example.png)

Enter the text for which you want to search as well as the text with which it should be replaced.

* Tap or click **Find** to begin the search. Click or tap the x to cancel.
* If you wish to do an exact match according to the case, select the option **Match Case** before starting the search.
* Select **Replace all** to replace all occurrences of the text at once.

If a match is found, it is highlighted and the search dialog is dimmed. Click the **Find** button again in the dimmed dialog to search for the next occurrence or select the **Replace** button to replace the highlighted, matched text. Note that the **Replace** button is only active once a match is made.

The find and replace dialog becomes transparent when find is clicked and becomes opaque when replace is clicked. This allows the author to review the text that the author will replace.

>[!NOTE]
>
>When using the replace functionality, the string to be replaced should be entered at the same time as the string to be found. However you can still click find to search for the string before replacing it. If the replace string is entered after clicking find, the search is reset to the beginning of the text.

#### Undo

![Undo icon](/help/email/assets/undo.png)

Used to undo the last edit in the rich text editor.

#### Redo

![Redo icon](/help/email/assets/redo.png)

Used to undo an edit undone by using the undo icon.

#### Align Text Left

![Align left icon](/help/assets/text-left.png)

Used to align the text to the left margin.

#### Center Text

![Center text icon](/help/assets/text-center.png)

Used to center the text.

#### Align Text Right

![Align right icon](/help/assets/text-right.png)

Used to align the text to the right margin.

#### Bullet

![Bullet icon](/help/assets/text-bullet.png)

Used to format the selected text as a bulleted list or begin the insertion of a bulleted list after the cursor.

To end a bulleted list, tap or click the **Bullet** button again or enter two carriage returns.

#### Numbered

![Numbered list icon](/help/assets/text-numbered.png)

Used to format the selected text as a numbered list or begin the insertion of a numbered list after the cursor.

To end a numbered list, tap or click the **Numbered** button again or enter two carriage returns.

#### Outdent

![Outdent icon](/help/assets/text-outdent.png)

Used to decrease the indentation level of the selected text or text entered after the cursor.

Only active if the selected text or position of the cursor is already indented.

#### Indent

![Indent icon](/help/assets/text-indent.png)

Used to increase the indentation level of the selected text or text entered after the cursor.

#### Table

![Table icon](/help/assets/text-table.png)

Used to insert a table into the text. Selecting this option opens a window for specifying the details of the table.

![Table example](/help/assets/text-table-example.png)

* **Columns** - The number of columns of the table (required)
* **Rows** - The number of rows of the table (required)
* **Width** - The width of the table
* **Height** - The height of the table
* **Cell padding** - The space around the cell content
* **Cell spacing** - The space between cells
* **Border** - The weight of the border lines of the table
  * If for the header of the table:
    * The first row should be used
    * The first column should be used
    * The first row and first column should be used
    * Or no header should be used.
* **Caption** -  The caption of the table

#### Image

![Image icon](/help/email/assets/image-icon.png)

Used to align an inserted image.

#### Check Spelling

![Check spelling icon](/help/assets/text-spellcheck.png)

Used to check the spelling of the text content. Possible misspellings are underlined with broken, red lines.

Further details about spell checking and customizing spell check dictionaries can be found in the document [Configure the Rich Text Editor Plug-Ins](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/configuring-and-extending/configure-rich-text-editor-plug-ins.html).

#### Special Characters {#special-characters}

![Special characters icon](/help/assets/text-special-characters.png)

Used to insert special characters into the text. Selecting this option opens a window where the available characters are displayed.

![Special characters example](/help/assets/text-special-characters-example.png)

Tap or click the desired character to insert it into the text after the cursor. Multiple characters can be inserted. Tap or click the x to close the selection window.

#### Source Edit

![Source edit icon](/help/assets/text-source.png)

Used to view and modify the HTML source of the text.

Tap or click the **Source Edit** icon to change the content of the text from the formatted view to view the raw HTML. In this mode, all other formatting options are disabled. Tap or click the **Source Edit** icon again to return to the formatted view.

>[!CAUTION]
>
>As always the case with access to raw HTML, care must be exercised when using the **Source Edit** option!
>
>HTML entered via **Source Edit** is scanned for XSS risks and any scripts that are inserted are removed and will not appear on the resulting page. However malformed HTML entered in **Source Edit** can break the template for the page resulting in unexpected formatting or rendering the resulting page unusable.

>[!NOTE]
>
>Because HTML entered via **Source Edit** is scanned for XSS risks and any scripts and automatically removes those found, the actual content persisted may vary from what was entered in **Source Edit**. For this reason, in order to save changes made using **Source Edit**, you must first exit **Source Edit** to view the text in the normal editor before saving.

#### Paragraph Format

![Paragraph format icon](/help/assets/text-paragraph.png)

Used to apply paragraph formatting to the selected text or to text inserted after the cursor. Selecting this options opens a dropdown from which the paragraph format is selected.

![Paragraph format example](/help/assets/text-paragraph-example.png)

#### Select Adobe Campaign Variable

![Select Adobe Campaign Variable icon](/help/email/assets/select-adobe-campaign-variable-icon.png)

Opens the [Select Adobe Campaign Variable](/help/email/campaign-variables.md) dialog to insert dynamic content from Adobe Campaign.

### In-Line Editing {#in-line-editing}

The text component can be edited in-line as well. To edit in-line, select the Email Text Component on the content page.

![Select Email Text component](/help/email/assets/email-text-select-component.png)

Then tap or click the **Edit** icon on the toolbar that pops up over the component. The toolbar changes to show limited text formatting options (including access to the **Select Adobe Campaign Variable** option) and you can edit the text in-line.

![In-line edit example](/help/email/assets/email-text-edit-inline-example.png)

Tap or click the checkmark in the toolbar to save your changes or the X to discard.

Due to space restraints, not all formatting options are available in-line. To see all options, switch to full-screen mode.

### Setting an ID {#setting-id}

This option allows to control the unique identifier of the component in the HTM.

* If left blank, a unique ID is automatically generated for you and can be found by inspecting the resulting page.
* If an ID is specified, it is the responsibility of the author to make sure that it is unique.
* Changing the ID can have an impact on CSS.

## Design Dialog {#design-dialog}

The design dialog allows the template author to define which text formatting options are available to the content authors.

### Plugins Tab {#plugins-tab}

The **Plugins** tab is used to enable and disable various text formatting options available to the content authors.

### Features {#features}

![Design dialog features](/help/assets/text-design-features.png)

The following features can be activated or deactivated for the component.

* Paste plain text
* Past from word
* Find and replace
* Undo and redo
* Spell checker
* Inserted image modification options
* HTML source editing

### Formatting {#formatting}

![Design dialog formatting](/help/assets/text-design-formatting.png)

The following formatting options can be activated or deactivated for the component.

* Table
* Lists (bullet, number, indent, outdent)
* Alignment (left, right, centered)
* Bold, italic, underline
* Linking (and unlinking)
* Sub/superscript

### Paragraph Styles {#paragraph-styles}

![Design dialog paragraph styles](/help/assets/text-design-paragraph.png)

Paragraph styles can be activated or deactivated for the component. When activated, the allowed formats can be defined.

* Tap or click the **Add** button to insert a new style.
* Enter the code of the style and a description that will be displayed in the edit dialog.
* To remove a style tap or click the **Delete** button.
* To rearrange the order of the formats tap or click and drag the handles.

### Special Characters {#configuring-special-characters}

![Design dialog special characters](/help/assets/text-design-special-characters.png)

The option to insert special characters can be activated or deactivated for the component. When activated, the allowed characters can be defined.

* Tap or click the **Add** button to insert a new character.
* Enter the HTML code of the character and a description that will be displayed in the edit dialog.
* To remove a character tap or click the **Delete** button.
* To rearrange the order of the characters tap or click and drag the handles.

## Styles Tab {#styles-tab}

The Email Text Component supports the AEM [style system](/help/get-started/authoring.md#component-styling).
