---
title: 'GroupDocs Apps v2.5 and v2.7 - Features and Fixes'
date: Mon, 17 Jun 2013 08:15:56 +0000
draft: true
url: /?p=2559
author: 'Derek Hyland'
summary: ''
tags: ['API', 'document collaboration', 'document management', 'document upload', 'GroupDocs Annotate', 'GroupDocs API', 'GroupDocs Assembly', 'GroupDocs Signature', 'GroupDocs Viewer', 'online document viewer', 'View documents online', 'zArchive']
---

We’ve implemented a few new features as well as fixed some major and minor bugs lately. Let’s have a detailed look:

## [GroupDocs Annotation](http://groupdocs.com/apps/annotation)**Features Implemented**

*   Major

*   \[training:ANNOTATION - 233\] Show Document Name option for embedded Annotation.

*   Minor
    *   \[training:ANNOTATION-243\] A redirect to annotation v2.0 for annotations v1.0 requests.

**Bugs fixed**

*   Critical:
    *   \[training:ANNOTATION-239\] Annotation v.2. An error occurs: "Parameter is not valid. at System.Drawing.Image.FromStream".
    *   \[training:ANNOTATION-240\] Annotation v.2. Text can't be selected when using the text annotation tool.
    *   \[training:ANNOTATION-241\] Annotation v.2. When moving an annotation:, an error occurs: "AnonymousType cannot be serialized".
    *   \[training:ANNOTATION-252\] Annotation v.2. Annotations can't be created for images.

*   Major:
    *   \[training:ANNOTATION-233\] Annotations export doesn't work.
    *   \[training:ANNOTATION-235\] Annotation v.2 does not work in Internet Explorer.
    *   \[training:ANNOTATION-236\] Annotation v.2. The document is not scrolled when an annotation is selected.
    *   \[training:ANNOTATION-237\] Annotation v.2. Page images are sometimes corrupted on iPad.
    *   \[training:ANNOTATION-238\] Annotation v.2. The page footer scrolls with the document.
    *   \[training:ANNOTATION-244\] After comment is removed, new ones cannot be added.
    *   \[training:ANNOTATION-245\] Annotation v.2. When an anonymous user adds or deletes a reply, the operation is not broadcasted.

*   Minor

*   \[training:ANNOTATION-242\] Annotation delete button is not disabled.

## [GroupDocs Viewer](http://groupdocs.com/apps/viewer)**Features Implemented**

*   Major

*   \[training:WEB-357\] Show Document Name option for embedded Viewer.

*   Minor
    *   \[training:WEB-342\] Update document viewer 1.0 header.
    *   \[training:WEB-361\] Make jSaaspose.Widgets.Thumbnails.js work in multiple instances of the Viewer.

**Bugs fixed**

*   Critical
    *   \[training:WEB-358\] Page images become blank when zooming.
    *   \[training:WEB-377\] Download and print options for embedded viewer don't work.
    *   \[training:WEB-415\] "Uncaught TypeError: Cannot call method 'visible' of undefined" in Viewer when opening a document having single page.
*   Major
    *   \[training:WEB-356\] Scroll View and Double Page Flip buttons do not work.
    *   \[training:WEB-425\] Page numbers in the URL hash don't work for the scroll mode.
*   Minor

*   \[training:WEB-344\] Embedded Viewer Help widget cannot be disabled.

## [GroupDocs Viewer for .NET](http://groupdocs.com/dot-net)**Features Implemented**

*   Major
    *   \[training:WEB-349\] Server side code for the installable Viewer.
    *   \[training:WEB-350\] Multiple instances of Viewer on one page.
    *   \[training:WEB-353\] The Navigation widget for the installable Viewer.
    *   \[training:WEB-354\] The Thumbnails widget for the installable Viewer.
    *   \[training:WEB-355\] The file open dialog for the installable Viewer.
    *   \[training:WEB-359\] Document Viewer HTML creation inside the jGroupdocs.DocViewer.js.
    *   \[training:WEB-360\] Remove element IDs from installableViewer.js to make it work in multiple instances.
    *   \[training:WEB-364\] The GetImageUrlsHandler for the installable Viewer.
    *   \[training:WEB-365\] A setting that determines whether to use an MVC controller or HTTP handlers for the installable Viewer.
    *   \[training:WEB-366\] Make it possible to load scripts and CSS for the installable Viewer from a directory set in options.
    *   \[training:WEB-372\] Installable Viewer. Setup guide and release notes.
    *   \[training:WEB-383\] Installable Viewer. The Aspose licensing system.
    *   \[training:WEB-389\] Installable Viewer. Zooming Widget.
    *   \[training:WEB-401\] Installable Viewer. Pre-load Behaviour.
    *   \[training:WEB-402\] Installable Viewer. Limit the number of pages in the Demo version.
    *   \[training:WEB-407\] Installable Viewer. Merge all the assemblies into one.
*   Minor
    *   \[training:WEB-367\] Installable Viewer: Remove the dependency on Groupdocs.Common.
    *   \[training:WEB-370\] Installable Viewer: A setting in web.config for the root storage path.
    *   \[training:WEB-373\] Demo version of Groupdocs Viewer for .NET deployment.
    *   \[training:WEB-374\] Installable Viewer: Scripts and CSS minification.
    *   \[training:WEB-376\] Installable Viewer: Embed all resources.
    *   \[training:WEB-378\] .NET helpers for loading and calling Groupdocs Viewer for .NET client code.
    *   \[training:WEB-379\] A trial banner for the installable Viewer.
    *   \[training:WEB-380\] Installable Viewer: A trial watermark on the first document page.
    *   \[training:WEB-385\] The ability to disable the mouse's right-click menu.
    *   \[training:WEB-386\] Options of the installable viewer helper for creating its client side code should be set by method calls.
    *   \[training:WEB-387\] Installable Viewer: Default Zoom setting (including auto-fit).
    *   WEB-388\] Installable Viewer: Thumbnails State On Load Setting.
    *   \[training:WEB-393\] Installable Viewer: Download document functionality.
    *   \[training:WEB-397\] Installable Viewer: Hide/show top toolbar buttons.
    *   \[training:WEB-399\] Switching between scroll and page flip layout.
    *   \[training:WEB-400\] Installable Viewer: Default Viewer Style - set the default style to Scroll Viewer or Flip View.
    *   \[training:WEB-409\] Installable Viewer: Options for the client script loader helper via method calls.

**Bugs fixed**

*   Critical
    *   \[training:WEB-363\] The installable Viewer works unstable when multiple instances of it are created.
    *   \[training:WEB-369\] Installable Viewer: Navigation buttons don't work.
    *   \[training:WEB-384\] Page images always have width of 852 pixels regardless of the window size.
    *   \[training:WEB-416\] Installable Viewer: A license cannot be applied to the Aspose components in an ASP.NET application.
*   Major
    *   \[training:WEB-371\] Installable Viewer: Visual issues.
    *   \[training:WEB-375\] Installable Viewer: Files from sub folders can't be opened through the file browser.

## [GroupDocs Assembly](http://groupdocs.com/apps/assembly)**Features Implemented**

*   Major
    *   \[training:DA-158\] Instant HTML rendering for single/multiple choice questions.
    *   \[training:DA-162\] Questionnaire execution page UX enhancements.
    *   \[training:DA-163\] Allow print and download options.
    *   \[training:DA-169\] Questionnaire builder 2.0 UX improvements .
*   Minor
    *   \[training:DA-164\] Error messages are not shown for failed assemblies.
    *   \[training:DA-166\] Copy to clipboard UX improvements .

**Bugs Fixed**

*   Critical
    *   \[training:DA-154\] Questionnaire assembly hangs.
    *   \[training:DA-167\] Questionnaire execution fails for anonymous users.
    *   \[training:DA-168\] Answers are not added for single/multiple choice questions.
    *   \[training:DA-170\] Paragraph tag is added to the single/multiple choice answers on rendering.
    *   \[training:DA-171\] Web hook notifications are not broadcasted.
    *   \[training:DA-172\] Empty paragraphs are added to assembled documents.
    *   \[training:DA-173\] Questionnaire results page fails to open for a collector.
    *   \[training:DA-177\] Email addresses are duplicated for email collectors.
*   Major
    *   \[training:DA-149\] File drag and drop fails for accounts with unlimited subscription.
    *   \[training:DA-165\] Questionnaire collectors results cannot be exported.
    *   \[training:DA-175\] Tool tips are not removed when a new page is opened.
    *   \[training:DA-176\] Questionnaire collector list is not refreshed when a new collector is added .
*   Minor
    *   \[training:DA-123\] Assembly 2. Edit and Settings of field are similar.
    *   \[training:DA-156\] Table text alignment.
    *   \[training:DA-157\] Radio buttons with check boxes replacement.
    *   \[training:DA-159\] Text is not properly aligned on the questionnaire execution page.
    *   \[training:DA-160\] Questionnaire fulfillment completion message is not properly aligned.
    *   \[training:DA-161\] On click event handler for the questionnaire result number.
    *   \[training:DA-178\] The dashboard is not opened using the **My Assembly** breadcrumbs link.
    *   \[training:DA-179\] Sorting by the template name doesn't work.
    *   \[training:DA-180\] Clicking on the assign questions table header redirects to dashboard.

## [GroupDocs Signature](http://groupdocs.com/apps/signature)**Features Implemented**

*   \[training:SIGN-1137\] - Signature 2 default.
*   \[training:SIGN-1107\] - Integrate the new signature pad in signature 2 sign dialog.
*   \[training:SIGN-1042\] - Implement documents verify API method.
*   \[training:SIGN-1088\] - User-specific settings for webhook notifications.
*   \[training:SIGN-1044\] - Stamp each page of signed document.
*   \[training:SIGN-1043\] - New last page of the signed document.
*   \[training:SIGN-1061\] - Lock the signed PDF file.
*   \[training:SIGN-1087\] - Implement new signature creation dialog.
*   \[training:SIGN-1116\] - Implement SVG signing in signature API.
*   \[training:SIGN-1124\] - Add option in user account for disabling the groupdocs watermark in the signed document.
*   \[training:SIGN-1078\] - Webhook ensures delivery and notification of the support.

**Improvement**

*   \[training:SIGN-1047\] - Improve the field parsing in PDF, so field can be assigned to any recipient.
*   \[training:SIGN-1024\] - Signature 2: Implement 'delete multiple contact'.
*   \[training:SIGN-1025\] - Signature 2: Ensure that recipients with role CC are not included in the recipients drop-down list in the step 5 in templates.
*   \[training:SIGN-1026\] - Signature 2: Templates: Do not show fields summary on step 6 in template preparation wizard.
*   \[training:SIGN-1028\] - Signature 2: Implement 'delete multiple templates'.
*   \[training:SIGN-1029\] - Signature 1: Ensure that recipients with role CC are not included in the recipients drop-down list in the fields preparation page for templates.
*   \[training:SIGN-1030\] - Signature 2: Implement 'delete multiple signatures'.
*   \[training:SIGN-1056\] - Integrate the new loading spinner in signature 2 templates dashboard.
*   \[training:SIGN-1057\] - Integrate the new loading spinner in signature 2 forms dashboard.
*   \[training:SIGN-1058\] - Integrate the new loading spinner in signature 2 contacts dashboard.
*   \[training:SIGN-1059\] - Integrate the new loading spinner in signature 2 signatures dashboard.
*   \[training:SIGN-1062\] - Low performance while creating envelope, for a user with many envelopes.
*   \[training:SIGN-1064\] - Change the reference key in the final signed document.
*   \[training:SIGN-1075\] - Signature 2: In add from contacts popup, implement search functionality.
*   \[training:SIGN-1112\] - Show the old signature pad for browsers that do not support SVG.
*   \[training:SIGN-1118\] - Get vector version of signature field background.
*   \[training:SIGN-1134\] - Add async progress spinner in prepare envelope wizard in signature 2.
*   \[training:SIGN-1136\] - Add async progress spinner in prepare form wizard in signature 2.

**Bugs Fixed**

*   \[training:SIGN-1035\] - JavaScript errors in IE8 in signature 1 and signature 2.
*   \[training:SIGN-1040\] - Filter by date in envelopes/forms dashboards doesn't work in IE8.
*   \[training:SIGN-1045\] - Unable to sign non PDF documents with document.sign API method.
*   \[training:SIGN-1046\] - Forms: Show progress loading indicator during form signing.
*   \[training:SIGN-1048\] - Signature 2: Fields can't be shrunk with the keyboard keys.
*   \[training:SIGN-1049\] - If field is renamed, it can't be cloned.
*   \[training:SIGN-1050\] - Signature 2: Templates: Step5: Saving fields settings should hide settings area.
*   \[training:SIGN-1051\] - Signature 1: Templates: Adding fields to document not working.
*   \[training:SIGN-1052\] - Signature 2: Templates: Moving field leads to field disappearance.
*   \[training:SIGN-1053\] - Signature 1: Forms: Unable to place field.
*   \[training:SIGN-1054\] - Signature 2: Forms: Moving field leads to field disappearance.
*   \[training:SIGN-1060\] - Signature 2: The page scrolling does not work properly in envelopes dashboard.
*   \[training:SIGN-1063\] - Forms: When user signs a form document and try to download the signed document, the system returns a zip file.
*   \[training:SIGN-1069\] - Unable to download the signed documents after switching to WebAPI.
*   \[training:SIGN-1070\] - Signature 2: Missing icon in forms dashboard.
*   \[training:SIGN-1071\] - Signature 2: Download all for completed forms in forms dashboard does not work.
*   \[training:SIGN-1072\] - Signature 1: Broken header in archived envelopes.
*   \[training:SIGN-1073\] - Signature 2: Hide add new button in archived envelopes dashboard.
*   \[training:SIGN-1074\] - Signature2: Envelope wizard, step2, update the design of the add from contacts popup.
*   \[training:SIGN-1076\] - Signature 2: Envelope wizard, improve the system behavior.
*   \[training:SIGN-1077\] - Ensure that all placed signatures could be converted to images before signing is scheduled.
*   \[training:SIGN-1079\] - Signature 2: Update the design of the embed link popup.
*   \[training:SIGN-1080\] - Signature 2: Forms: Update the design of the embed link popup.
*   \[training:SIGN-1081\] - Signature 2: Ensure that while loading the sign page, all buttons (start, next) are invisible during loading.
*   \[training:SIGN-1082\] - Signature 2: Embed sign, after clicking on confirm signature button, the start button appear.
*   \[training:SIGN-1083\] - Signature 2: Signed embed initial state is wrong.
*   \[training:SIGN-1084\] - Signature 2: Signed screen initial state is wrong.
*   \[training:SIGN-1085\] - Signature 2: In sign popup, the logged in user name should be filled by default.
*   \[training:SIGN-1086\] - Embed signature issues in IE10.
*   \[training:SIGN-1089\] - Signature dialog: If Expand/shrink the dialog, the drawn signature disappeared.
*   \[training:SIGN-1091\] - Signature dialog: If add to "My signature" is selected, and there is already signature with the same name, show confirmation dialog for selecting new signature name.
*   \[training:SIGN-1094\] - Envelopes can't be deleted or archived issue.
*   \[training:SIGN-1096\] - Envelope Name Issue.
*   \[training:SIGN-1097\] - Tab not getting selected issue.
*   \[training:SIGN-1099\] - Remove swagger attributes from public API methods.
*   \[training:SIGN-1100\] - Review the PublicDeleteSignature API method.
*   \[training:SIGN-1101\] - Double slash in some API method definitions.
*   \[training:SIGN-1102\] - Review public GetSignatureEnvelopeFieldData API method.
*   \[training:SIGN-1103\] - Review PublicGetEnvelopeRecipients API method.
*   \[training:SIGN-1104\] - Add swagger attributes to the PublicVerifyDocument API method.
*   \[training:SIGN-1105\] - The new signature pad doesn't work on android devices.
*   \[training:SIGN-1108\] - Modify the PDF detection in sign document method.
*   \[training:SIGN-1109\] - Lock signature field to be able to be resized only with constant aspect ratio in signature 2.
*   \[training:SIGN-1110\] - Fixing issues with new signature pad in IE9/10.
*   \[training:SIGN-1113\] - Can't add metadata to some PDF files.
*   \[training:SIGN-1117\] - Review signature code for incorrectly disposed documents.
*   \[training:SIGN-1122\] - SVG signature is not placed correctly in the signed document.
*   \[training:SIGN-1123\] - Signature 2: Can't move placed field with down arrow.
*   \[training:SIGN-1125\] - JS error in embedded sign in signature1 and signature2.
*   \[training:SIGN-1126\] - JS error in all signature dashboards in signature2 related with new signature pad.
*   \[training:SIGN-1127\] - Add/Edit signature dialog do not work correctly.
*   \[training:SIGN-1128\] - Signature 1. incorrect position for Field types.
*   \[training:SIGN-1129\] - Fix document viewer styling in signature1.
*   \[training:SIGN-1130\] - Fix the signature document viewer styling in signature 2.
*   \[training:SIGN-1131\] - Copied envelope can't be signed.
*   \[training:SIGN-1132\] - Can't add/edit signatures in signature 2.
*   \[training:SIGN-1133\] - SVG signatures are not displayed at all in sign page in signature 1.
*   \[training:SIGN-1135\] - JS error in embed form sign in signature 2 related with new signature pad.
*   \[training:SIGN-1138\] - Signature 2: On activating step 5 in envelope preparation wizard reload all fields.
*   \[training:SIGN-1139\] - Wrong URL in the main button in signature 2.
*   \[training:SIGN-1140\] - The sign link in main dashboard should link to signature2.
*   \[training:SIGN-1141\] - Wrong rendering fields preparation step during initial loading.
*   \[training:SIGN-1142\] - The resizing of signature field with keyboard keys - should keep the aspect ratio.
*   \[training:SIGN-1143\] - Incorrect rendering of the sign page in signature 1 when SVG is used.
*   \[training:SIGN-1144\] - In envelope, dashboard use statusDateTime for modified column.
*   \[training:SIGN-1145\] - The async indicator stays on in templates preparation wizard if error occur.
*   \[training:SIGN-1146\] - The user should not be able to add two recipients with same nicknames while preparing a template.
*   \[training:SIGN-1147\] - Wrong position of the datepicker popup in signature1 and signature2.
*   \[training:SIGN-1148\] - Wrong progress display in templates wizard.
*   \[training:SIGN-1149\] - Fix the add contact dialog style.
*   \[training:SIGN-1150\] - Fix the style of add from template dialog in forms preparation wizard.
*   \[training:SIGN-1151\] - Fix the style of create signature dialog.
*   \[training:SIGN-1152\] - If the envelope preparation wizard is reloaded, the current step is not rendered at all.
*   \[training:SIGN-1153\] - Signature 2: Forms preparation wizard do not load.
*   \[training:SIGN-1154\] - Place a badge in signature 2 that point to signature 1.
*   \[training:SIGN-1155\] - Unable to copy envelope in signature 2.
*   \[training:SIGN-1156\] - Remove buttons for a template in templates dashboard.
*   \[training:SIGN-1157\] - Wrongly displayed subject and message in Step 3 in template preparation.
*   \[training:SIGN-1158\] - Can't create envelope from template.
*   \[training:SIGN-1159\] - In add from template dialog, show only completed templates.
*   \[training:SIGN-1160\] - Signature 1: Embed sign: Signature field filled in signature 2, but displayed in signature 1 is behaving as not filled.
*   \[training:SIGN-1161\] - Signature 2: Add publish now button for form in forms dashboard.
*   \[training:SIGN-1162\] - Fix initial layout rendering in signature 2 dashboards.
*   \[training:SIGN-1163\] - Javascript error in archived envelopes and archived forms.
*   \[training:SIGN-1164\] - Default value settings for fields in Signature 2 envelope wizard is missing.
*   \[training:SIGN-1165\] - Forms: Add default font name and size for fields.
*   \[training:SIGN-1166\] - Forms: Add default value settings for each field except signature field.
*   \[training:SIGN-1167\] - Add default value settings for fields in Signature 2 template wizard.

## Platform**Features Implemented**

*   Major
    *   \[training:CORE-914\] Accounts monthly usage report.

**Bugs Fixed**

*   Major
    *   \[training:CORE-909\] Document viewing fails when splitting is not possible.
*   Minor
    *   \[training:CORE-890\] Subscription upgrade cosmetic changes.
    *   \[training:CORE-897\] User name in header is improperly laid out.
    *   \[training:CORE-907\] Login cookies are not updated.

## [API](http://groupdocs.com/cloud)**Features Implemented**

*   \[training:CORE-862\] Direct links to document pages image for Windows Azure and Google Cloud storage.
*   \[training:CORE-846\] Document system information stripping.
*   \[training:CORE-870\] Сoncurrent documents processing inside conversion service commands.
*   \[training:CORE-904\] Allow print and download options for document questionnaires.
*   \[training:CORE-906\] Document textual representation API.
*   \[training:CORE-922\] Banckle forum users creation for new sign ups.
*   \[training:CORE-923\] Files metadata synchronization option for remote storages.

**Bugs fixed**

*   \[training:CORE-883\] Google Cloud Storage sync. Folders are not removed.
*   \[training:CORE-896\] Annual subscription purchase fails.
*   \[training:CORE-898\] Serving images from Windows Azure doesn't work.
*   \[training:CORE-899\] Folder is duplicated when uploading files to an existing Google Cloud folder.
*   \[training:CORE-905\] Web documents cannot be moved.
*   \[training:CORE-913\] Document objects are not disposed.
*   \[training:CORE-540\] Null byte in folder name.
*   \[training:CORE-811\] Inconsistency in email field in GetQuestionnaireCollector and GetQuestionnaireCollectors responses.
*   \[training:CORE-915\] Document viewing service doesn't lock a document accessed from different threads.
*   \[training:CORE-916\] File last modified date is incorrect for Google cloud entities.
*   \[training:CORE-920\] Document cannot be viewed when splitting into pages partially fails.

## Refactoring

*   \[training:CORE-891\] Local file storage separation.
*   \[training:CORE-895\] Document viewing service without dependencies on internal libraries.
*   \[training:CORE-903\] WCF Rest Starter Kit with Web API replacement.



