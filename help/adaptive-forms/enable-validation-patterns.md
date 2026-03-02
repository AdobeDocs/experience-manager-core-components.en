---
title: Enable and Use Text Input Validation Patterns in Adobe Experience Manager Adaptive Forms
description: Learn how to configure template policies to expose validation patterns like Phone Numbers, Social Security Numbers, and Zip Codes, then use them in your Adaptive Forms.
hide: yes
hidefromtoc: yes
exl-id: e4500666-1346-4558-861d-da9541dcef51
---
# Enable and Use Text Input Validation Patterns in Adobe Experience Manager Adaptive Forms

## Overview

In Adobe Experience Manager (Adobe Experience Manager) Forms, specific validation formats (like Social Security Numbers, Email addresses, or Zip Codes) for Text Input components are controlled at the Template Policy level. This guide explains how to:

1. Access the template editor and configure the Text Input component policy to expose validation patterns.
2. Create an Adaptive Form and apply those validation patterns to a Text Input component.

## Prerequisites

- Access to an Adobe Experience Manager instance with Forms enabled.
- Permissions to edit Templates (usually part of the `template-authors` group).
- Permissions to create and edit Adaptive Forms.

## Part 1: Enable Validation Patterns in the Template

>[!VIDEO](https://video.tv.adobe.com/v/3480390/)

### Step 1: Access the Templates Console

1. From the Adobe Experience Manager Home screen, click **Tools** (the hammer icon) in the left sidebar.
2. Navigate to **General > Templates**.
3. Select the folder containing your project templates (for example, Core Components Examples).
4. Locate the specific template you wish to modify (for example, AF Blank) and select it.
5. Click **Edit** (or open the template directly).

### Step 2: Access the Component Structure

1. Ensure you are in the **Structure** view (select "Structure" from the mode dropdown in the top right if necessary).
2. Locate the main **Layout Container** or the specific container where your Text Input component is allowed.
3. Click on the container to reveal the allowed components list.
4. Find the **Adaptive Form Text Box** component in the list.
5. Click the **Policy** icon (represented by a file/drawer symbol) next to the component name.

### Step 3: Configure the Text Input Component Policy

1. In the policy editor, click the **Formats** tab on the right side of the window.
2. You will see a list of available validation patterns. Check the boxes for the formats you want to enable:
   - Phone Number
   - Social Security Number
   - Email Alphanumeric
   - Zip Code

### Step 4: Define and Save the Policy

1. Switch back to the **Policy** tab (or check the left-hand settings).
2. In the **Policy Title** field, enter a clear name (for example, `new-textinput-default-policy`).
3. Click the **Done** (checkmark) icon in the top right corner to save your changes.

## Part 2: Create a Form and Use Validation Patterns

Now that validation patterns are enabled in the template, you can create an Adaptive Form and apply them to Text Input components.

>[!VIDEO](https://video.tv.adobe.com/v/3480391/)

### Step 1: Create an Adaptive Form

1. Navigate to the **Forms & Documents** interface.
2. Click the **Create** button in the top right corner.
3. Select **Adaptive Form** from the dropdown options.
4. Choose the template where you enabled the validation patterns (for example, **Blank**) and click **Next**.
5. On the Add Properties screen:
   - Enter a **Title** for your form (for example, "testPolicy"). The **Name** field auto-populates based on the title.
   - Ensure the correct **Theme Client Library** is selected (for example, `adaptiveform.theme.canvas3`).
6. Click **Create**. A success message appears.
7. Click **Edit** to open the form in the editor.

### Step 2: Add a Text Input Component

1. In the form editor, locate the **Components** browser in the left sidebar.
2. Use the search bar to find the **Adaptive Form Text Box** component. Typing "text" filters the list.
3. Click and drag the **Adaptive Form Text Box** component onto the main canvas area.

### Step 3: Configure Component Formatting

1. Click on the newly added **Text Input** component to select it.
2. Click the **Configure** icon (represented by a wrench) in the toolbar that appears above the component.
3. In the properties dialog, navigate to the **Formats** tab.
4. Locate the **Type** dropdown menu and change the selection to **Phone Number** (or another enabled format).

### Step 4: Configure Data Validation

1. While still in the component configuration dialog, navigate to the **Validation** tab.
2. Locate the **Validation Pattern** section.
3. Click the **Type** dropdown menu.
4. Select **Phone Number** from the list of validation patterns. This ensures the form produces an error if the user inputs text that does not match a valid phone number format.
5. Click the **Done** (checkmark) icon in the top right of the dialog box to save your changes.

## Verification

To verify that validation patterns are working correctly:

1. Preview the form in the editor.
2. Enter test data in the **Text Input** component.
3. Confirm that:
   - The enabled validation patterns appear in the component's Formats and Validation tabs.
   - Invalid input triggers appropriate error messages.
   - Valid input is accepted without errors.

## Troubleshooting

- **Issue:** The validation patterns do not appear in the form component.
  - **Solution:** Ensure that the template policy was saved correctly and that you are using the correct template when creating the form.

- **Issue:** Unable to access the template editor.
  - **Solution:** Verify that you have the necessary permissions to edit templates (membership in the `template-authors` group).

- **Issue:** The Text Input component does not validate input correctly.
  - **Solution:** Recheck the validation pattern settings in the component's Validation tab and ensure the correct pattern is selected.

## Next Steps

After enabling and using text input validation patterns in your Adobe Experience Manager Adaptive Forms:

- Configure additional validation patterns for other data types.
- Explore other component policies to customize form behavior.
- Set up form submission handling and data processing logic.
