---
title: Adaptive Forms Core Component - Review Component
description: Using or customizing the Adaptive Forms Review Core Component.
role: Architect, Developer, Admin, User
hide: yes
hidefromtoc: yes
---

# Review Component

The Review Component in Adaptive Forms allows users to review and verify the information they have entered before submitting the form. It serves as a summary page, providing a read-only view of all fields and their values in a structured and user-friendly format. This feature ensures that users can identify and correct any errors or omissions before finalizing their submission, enhancing the overall form experience. By clicking the edit icon, they can modify the entered information before form submission.

**Example**

![Review Component](/help/adaptive-forms/assets/review-component.png){width=50%, align=center}

## Usage 

Below are the reasons to use Review component in an Adaptive Form:

- **Improved data accuracy**: The Review Component allows users to review all the data they have entered before submission. It helps reduce the chances of errors or omissions, ensuring the submitted data is accurate.
- **Enhanced user experience**: Users get a clear, organized summary of all the information they have filled out, hence giving them confidence that the form is complete and accurate before final submission, improving the overall experience.
- **Error detection and correction**: It provides ability to edit information at the panel or field level allows users to correct mistakes without navigating back through multiple tabs. Clicking the **Edit** icon next to a panel or field makes it easy to go back and fix any issues.
- **Increased user confidence**: Users can review the entered data, assuring them that the information they are submitting is correct, which leads to fewer submission errors and greater trust in the form’s functionality.
- **Prevent unintentional submissions**: Users often click **Submit** without reviewing all details. The **Review** component gives them a final chance to verify their data, reducing the likelihood of unintentional submissions.


## Technical Details {#technical-details}

Get the latest information on the Adaptive Forms Review Core Component in the technical documentation on [GitHub](https://github.com/adobe/aem-core-forms-components/tree/master/ui.af.apps/src/main/content/jcr_root/apps/core/fd/components/form/textinput/v1/textinput). For more on developing Core Components, check out the [Core Components developer documentation](/help/developing/overview.md).

## Configure Dialog {#configure-dialog}

You can easily customize the experience for visitors with the Configure Dialog for a seamless user experience.

![Configure Dialog](/help/adaptive-forms/assets/review-component-configure-dialog.png)

-   **Name** - You can identify a form component easily with its unique name both in the form and in the rule editor, but the name must not contain spaces or special characters.

-   **Title** - With its Title, you can easily identify a component in a form and by default, the title appears on top of the component. If you do not add a title, the name of the component is displayed instead of the title text.
-   **Hide Title** - Select the option to hide the component's Title.
-   **Enable edit mode actions for** - The **Enable Edit Mode Actions for** options allow users to modify the entered information. Users can edit the information either at the field level or the panel level.
    - When users select the **Field** option, they can edit individual form fields during the review.
    - When users select the **Panel** option, they can edit all fields within a specific section (panel).
    - When users select the **Field and Panel** option, they can click the edit icon next to a field to modify specific information or next to a panel to edit all fields within that panel.
    - When users select the **None** option, they can edit any field or panel within the entire form.

    By default, the **Panel** option is selected.

- **Link Panels** -  The **Link Panels** option allows users to select the panels for review. When panels are linked, users can review the entered information of the selected panel(s) and modify it before submission.

## Usecase

Take an example of a **Loan Application Form** consisting of four tabs, where each tab collects specific information about the user:

- **Personal Details**: Collects the user's basic personal details, such as name, date of birth, contact information, and address.

- **Loan Details**: Gathers information related to the loan, including the type of loan, desired amount, repayment period, and automatically calculated fields like interest rate and monthly EMI.

- **Additional Documents**: Allows the user to upload required documents, such as ID proof, address proof, and income proof. It also includes a declaration checkbox to confirm agreement with the terms.

- **Review and Submit Form**: Features a Review Component summarizing all inputs from the previous tabs. Users can verify and edit their data before submitting the form. This tab also includes the **Submit** button to submit the application.

The video below demonstrates how to configure the **Review** component so that it provides the user with the flexibility to edit information:

## Related Articles {#related-articles}

{{more-like-this}}

## See Also {#see-also}

{{see-also}}

