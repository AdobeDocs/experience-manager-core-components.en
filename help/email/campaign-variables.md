---
title: Campaign Variables
description: Use campaign variables as placeholders to compose personalized email content.
role: Developer, Admin, User
exl-id: 124ff5bf-6612-4baf-b0ff-6b1a95b455c1
index: false
TQID: https://experienceleague.adobe.com/MB6K-S4DZbsD3puXls8w4rWi6posFFLxJRewKORMkxA
product_v2:
  - id: c45915cf-e157-4af7-a80d-97b905bcb3a5
    internal-label: Experience Manager Sites
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
    internal-label: Experience Manager
feature_v2:
  - id: eb3ad9f8-54a2-45f3-abb1-d3976415a718
    internal-label: Personalization
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
topic_v2:
  - id: ce44533e-8ec8-4e11-a9e9-78b0fe561832
    internal-label: Content structure
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
    internal-label: Personalization
---
# Campaign Variables {#campaign-variables}

Use campaign variables to compose personalized email content. Campaign variables act as placeholders for Adobe Campaign values which you can insert into your email content. When the content is sent via Adobe Campaign, Campaign replaces those variables with the personalized content of the recipient.

## Usage {#usage}

The Email Core Components make campaign variables easily accessible via personalization buttons next to common text fields. When pressed, a dialog appears from which you can select a personalization field.

The list of available personalization fields is synchronized with your Adobe Campaign instance. The fields are managed in Adobe Campaign in the schema `nms:seedMember`. All fields in `nms:seedMember` must also be present in your recipient table.

## Select Adobe Campaign Variable Dialog {#dialog}

The Select Adobe Campaign Variable dialog is available in many edit dialogs of the Email Core Components. To use it simply click on the **Select Adobe Campaign Variable** icon next to the applicable field. This icon can take two forms.

![Adobe Campaign button](/help/email/assets/campaign-button.png)
![Select Adobe Campaign Variable icon](/help/email/assets/select-adobe-campaign-variable-icon.png)

Clicking both icons opens the **Select Adobe Campaign Variable** dialog.

![Select Adobe Campaign Variable dialog](assets/select-campaign-variable-dialog.png)

Use the column view to locate the variable that you wish to insert. Clicking a node in a column shows its children in a new column to the right. In this way, you can navigate the variable content structure.

Select the variable that you wish to insert and then click the checkmark at the top-right of the dialog.

![Adobe Campaign Variable selected](assets/select-campaign-variable-dialog-selected.png)

The variable is then inserted into the field of the edit dialog of the Email Core Component.

![Campaign variable inserted into edit dialog](assets/campaign-variable.png)

Click the X at the top-left of the dialog at any time to cancel and close the dialog.
