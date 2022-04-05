---
title: 'GroupDocs Apps v2.9 - Features and Fixes'
date: Tue, 13 Aug 2013 07:17:55 +0000
draft: true
url: /?p=3504
author: 'Vaseem Mansoor'
summary: ''
tags: ['GrouDocs cloud API', 'GroupDocs Annotation', 'GroupDocs Assembly', 'GroupDocs Signature', 'GroupDocs update', 'GroupDocs Viewer', 'new features', 'zArchive']
---

The GroupDocs team is constantly working to improve the functionality of our online document management apps. Today we introduce a set of new features and bug fixes. Let's take a closer look:

## [GroupDocs Annotation](http://groupdocs.com/apps/annotation)**Features implemented**

*   **Major**
    *   \[ANNOTATION-266\] Icon and color customization

**Bugs Fixed**

*   **Critical**
    *   \[ANNOTATION-251\] Annotation 1/2. Only point annotation works.
    *   \[ANNOTATION-263\] Annotations cannot be created.

*   **Major**
    *   \[ANNOTATION-249\] Annotation 2. Cannot delete reply.
    *   \[ANNOTATION-252\] Annotation v.2. Annotations can't be created for images.
    *   \[ANNOTATION-253\] Text selection works incorrectly.
    *   \[ANNOTATION-254\] The book page flip mode does not have book covers.
    *   \[ANNOTATION-255\] Fit Height works incorrectly after rotating iPhone.
    *   \[ANNOTATION-256\] Annotation v.2. Broadcast vertical size in the real-time mode.
    *   \[ANNOTATION-257\] Annotation v.2. The cursor position is broadcasted imprecisely in the real-time mode.
    *   \[ANNOTATION-259}\] When Annotation is opened from the Apps menu, an error is shown "Exception in external component"
    *   \[ANNOTATION-260\] "Add Document Reviewer" is not working in Annotation v.2.
    *   \[ANNOTATION-262\] Annotation icons are shifted in the embedded Annotation.
    *   \[ANNOTATION-265\] The icons on the RHS panel are scrolled to the first page even if another page is open.
    *   \[ANNOTATION-269\] Annotation v.2. The document is scrolled to the top when an annotation is selected.

*   **Minor**
    *   \[ANNOTATION-264\] A page specified in the URL hash does not open.
    *   \[ANNOTATION-267\] The navigation buttons are not disabled for the first and last pages.

## [GroupDocs Viewer](http://groupdocs.com/apps/viewer)**Features Implemented**

*   **Minor**
    *   \[WEB-465\] The ability to disable right-click of mouse pointer menu in the standard Viewer.
    *   \[WEB-483\] A bottom margin for pages.
    *   \[WEB-484} Reduce the side margins for pages.

**Bugs Fixed**

*   **Critical**
    *   \[WEB-426\] "ploc is undefined" when loading Viewer.
    *   \[WEB-481\] Signature fields are not shown in the Viewer for Signature.

*   **Major**
    *   \[WEB-425\] Page numbers in the URL hash do not work for the scroll mode.
    *   \[WEB-429\] Search does not work.
    *   \[WEB-434\] The page number in the URL hash is not getting updated when scrolling.
    *   \[WEB-413\] Embedded Options does not hide help in the Embedded Viewer.
    *   \[WEB-428\] Double page flip breaks single page documents.
    *   \[WEB-457\] Text selection is not working in page flip mode.
    *   \[WEB-458\] The document scrolls incorrectly when navigating to a page by setting a page number.
    *   \[WEB-476\] HTML 5 Viewer. The thumbnails have incorrect size for landscape documents.
    *   \[WEB-477\] HTML 5 Viewer. Some pages are shifted down after zooming out in Chrome.
    *   \[WEB-478}\] HTML 5 Viewer. Documents with multi-byte characters are divided into pages incorrectly.

*   **Minor**
    *   \[WEB-418\] Incorrect help for Viewer.
    *   \[WEB-479\] The loading background has a size, which is different from the page size.
    *   \[WEB-480\] The loading background is not centered.
    *   \[WEB-482\] The navigation buttons are not disabled for the first and last pages.
    *   \[WEB-489\] Pages are in one column in the standard Viewer.

## [GroupDocs Viewer for .NET](http://groupdocs.com/dot-net)**Features Implemented**

*   **Major**
    *   \[WEB-407\] Installable Viewer. Merge all the assemblies into one.
    *   \[WEB-453\] Installable Viewer. Open a document from a URL.
    *   \[WEB-454\] Installable Viewer. Open a document from a stream.
    *   \[WEB-471\] Installable Viewer. iPhone compatibility.
    *   \[WEB-474\] HTML 5 Viewer client code.
    *   \[WEB-475\] HTML 5 Viewer server code integration.
    *   \[WEB-488\] An installer for the installable Viewer.

*   **Minor**
    *   \[WEB-423\] Installable Viewer. Make the client code be automatically called when DOM loads.
    *   \[WEB-430\] Installable Viewer. Change the word "trial" to "unlicensed" in the messages for users without licenses.
    *   \[WEB-432\] Installable Viewer. Make the text selection rectangle invisible.
    *   \[WEB-404\] Installable Viewer. Improve Evaluation Banner (HTML).
    *   \[WEB-440\] Installable Viewer. Script debugging support.
    *   \[WEB-455\] Installable Viewer. Make the resource URLs for the installable Viewer unique.
    *   \[WEB-460\] Dynamic creation of the installable Viewer from code.
    *   \[WEB-463\] Installable Viewer. Create a step-by-step example of Viewer setup.

**Bugs Fixed**

*   **Critical**
    *   \[WEB-427\] Installable Viewer. An error is shown: "The controls collection cannot be modified".
    *   \[WEB-431\] Installable Viewer. An error is shown when selecting an area: "this.options.txtarea is undefined".
    *   \[WEB-433\] Installable Viewer is not working in the Integrated mode of IIS.
    *   \[WEB-435\] Installable Viewer. Pages jump down and right when trying to turn them in the Page Flip mode.
    *   \[WEB-438\] Installable Viewer. Zoom is working incorrectly.
    *   \[WEB-441\] Installable Viewer. Pages from a second instance of the installable Viewer appear in a first instance.
    *   \[WEB-443\] The second instance of the Installable Viewer is not working.
    *   \[WEB-446\] Installable Viewer does not work on URLs with paths relative to host names.
    *   \[WEB-462\] Installable Viewer. An error "JSON is undefined" occurs in IE.
    *   \[WEB-464\] Installable Viewer. An error "Member not found" occurs in IE when scrolling.
    *   \[WEB-490\] Installable Viewer. Licenses are not working.
    *   \[WEB-501\] The license black list can't be loaded when the installable Viewer assembly resources are encrypted.
    *   \[WEB-502\] An error about an incorrect parameter is shown when viewing an Excel file.

*   **Major**
    *   \[WEB-424\] Installable Viewer. A page number is shown in the URL hash though there can be multiple instances of Viewer on the page.
    *   \[WEB-436\] Installable Viewer. The Page Flip book is too wide initially.
    *   \[WEB-437\] Installable Viewer. The height/width ratio in the page flip mode is incorrect.
    *   \[WEB-442\] Fit Width and Fit Height Zoom work incorrectly for the Page Flip mode.
    *   \[WEB-448\] Page numbers in the navigation and thumbnail widgets do not change when turning pages using the bars in the page flip mode.
    *   \[WEB-450\] The document scrolls incorrectly when navigating to a page by setting a page number.
    *   \[WEB-451\] Thumbnails do not load after navigating to a page.by setting the page number.
    *   \[WEB-459\] Installable Viewer. Image URLs are incorrect when the installable Viewer is on a URL with a virtual directory suffix.
    *   \[WEB-467\] Installable Viewer. Fit Height works incorrectly after setting the page flip mode and opening another document.
    *   \[WEB-468\] Installable Viewer. The page flip mode works incorrectly in IE8.
    *   \[WEB-469\] Installable Viewer. The document name is not shown in the flip mode.
    *   \[WEB-470\] Installable Viewer. BackgroundColor does not change the color of the Thumbs button.
    *   \[WEB-495\] Document updates are not reflected by the Installable Viewer.
    *   \[WEB-503\] Installable Viewer. Pages have incorrect proportions after zooming out and loading another documents.
*   **Minor**
    *   \[WEB-439\] Installable Viewer. The URL hash contains folder names.
    *   \[WEB-447\] Installable Viewer. Documents are opened with gray letters instead of black when the Open File dialog is used.
    *   \[WEB-449\] The page number changes when switching between the scroll mode and page flip mode.
    *   \[WEB-452\] Installable Viewer. Zoom out works as zoom in if a document was opened with Fit Height.
    *   \[WEB-456\] Installable Viewer. The application URL used in the requests in ASP.NET host applications contains the name of the site's default page.
    *   \[WEB-485\] Installable Viewer. Fit Width does not take the scroll bar width into account.
    *   \[WEB-486\] Installable Viewer. Fit Height does not take the bottom margin into account
    *   \[WEB-497\] Installable Viewer. The page number is not changing when scrolling the installable Viewer with hidden thumbnails
    *   \[WEB-498\] The "Loading your content" text is not centered in the regular Viewer

## [GroupDocs Assembly](http://groupdocs.com/apps/assembly)**Features Implemented**

*   **Major**
    *   \[DA-187\] Conditional logic for questionnaire execution.

**Bugs Fixed**

*   **Critical**
    *   \[DA-174\] The layout of the questionnaire executions page is broken.
    *   \[DA-183\] Assembly 2. Cannot upload file in Firefox.
    *   \[DA-184\] Assigned questions cannot be saved.

*   **Minor**
    *   \[DA-181\] Progress overlay does not covert the whole content.

## [GroupDocs Signature](http://groupdocs.com/apps/signature)**Features Implemented**

*   \[SIGN-1224\] - Implementation of desktop notifications in signature 2.
*   \[SIGN-1237\] - Automatic envelope status update in envelopes dashboard.
*   \[SIGN-1240\] - Notify logged-in recipients about the new envelope received for signing.
*   \[SIGN-1247\] - Show desktop notification to the form owner when the signer opens the form for signing.
*   \[SIGN-1202\] - Sign document from Google drive in signature 2.
*   \[SIGN-1255\] - Signature in different colors.
*   \[SIGN-1274\] - Implemented envelope.document.rename API method.
*   \[SIGN-1275\] - Implemented document rename in envelope preparation wizard.
*   \[SIGN-1336\] - Implemented cancel envelope in envelopes dashboard.

*   \[SIGN-1349\] - Implemented template.document.rename API method.
*   \[SIGN-1350\] - Implemented rename document in the template preparation wizard.
*   \[SIGN-1353\] - Enhanced in-person signing process
*   \[SIGN-1376\] - Added new options for a form (notify owner on sign, attach signed document in notification email, etc.)

**Improvement**

*   \[SIGN-1185\] - Implemented async signing for forms.
*   \[SIGN-1186\] - Implemented async signing of documents.
*   \[SIGN-1234\] - Modified verify document API method to return additional data for the document.
*   \[SIGN-1245\] - Remove clone,delete, archive, restart buttons for envelopes if the currently logged user is not an owner.
*   \[SIGN-1248\] - Implemented auto update of the number of signers in forms.
*   \[SIGN-1251\] - Modified envelope/form API methods for create/update field location to support alignment.
*   \[SIGN-1252\] - Implemented changes in the final PDF generation to support fields alignment.
*   \[SIGN-1254\] - When changing font properties for a field in field preparation, make the changes visible for the user.
*   \[SIGN-1256\] - Restrict fonts in fields preparation to the font supported natively in the Aspose components
*   \[SIGN-1257\] - Set predefined list of standard colors in fields preparation
*   \[SIGN-1258\] - Add entry in the audit log for envelope for each notification that has been sent.
*   \[SIGN-1262\] - Implemented fields navigation in normal envelope sign.
*   \[SIGN-1265\] - Implemented create template from an envelope in the UI.
*   \[SIGN-1269\] - Add a drop down for filtering audit logs in envelope.
*   \[SIGN-1270\] - When creating a template from an envelope, set recipient's name by the role.
*   \[SIGN-1279\] - Extend the recipient info in the recipient tool tip to include information for the current recipient status and timestamp of the last action.
*   \[SIGN-1284\] - In embed link dialog in envelopes/forms dashboard, added information for the target.
*   \[SIGN-1287\] - Implemented changes in envelope.document.add API method.
*   \[SIGN-1288\] - Implemented changes in template.document.addd
*   \[SIGN-1289\] - Implemented changes in form.document.add.
*   \[SIGN-1290\] - Added parse fields option in add document step for envelope, template, and form.
*   \[SIGN-1304\] - Make the message of the validation popup more specific when exiting from step 5.
*   \[SIGN-1308\] - Added tool tip for recipient in the envelope dashboard and the recipient role.
*   \[SIGN-1309\] - Implemented changes in envelope.create.
*   \[SIGN-1310\] - Implemented changes in envelope.modify.
*   \[SIGN-1311\] - Added new option in step 3 in the envelope preparation wizard.
*   \[SIGN-1316\] - Implemented changes in envelope.field.modify.
*   \[SIGN-1317\] - Added guidance text field in the field settings area.
*   \[SIGN-1319\] - Implemented changes in template.field.add.
*   \[SIGN-1320\] - Implemented changes in template.field.modify.
*   \[SIGN-1321\] - Implemented changes in form.field.add.
*   \[SIGN-1323\] - Added guidance text field in field settings area for templates.
*   \[SIGN-1324\] - Added guidance text field in field settings area for forms.
*   \[SIGN-1325\] - If the owner is set as the only signer in an envelope, add new option on last step of the preparation wizard: sign now.
*   \[SIGN-1329\] - Added in-person sign option for envelopes.
*   \[SIGN-1330\] - Implemented the breadcrumb in dashboards and wizards in signature 2.
*   \[SIGN-1333\] - Implemented envelope.cancel API method.
*   \[SIGN-1334\] - Fixed the templates references in database.
*   \[SIGN-1335\] - Attached font style and text alignment buttons to the API calls.
*   \[SIGN-1351\] - If there are changes in field settings and the user tries to select other field, display confirmation message and offer to save changes for Forms preparation.
*   \[SIGN-1352\] - In envelope and template preparation wizard, if there are field changes, the wizard switching step should first display a confirmation dialog.

**Bugs Fixed**

*   \[SIGN-816\] - Made single line field content, centered horizontally.
*   \[SIGN-1190\] - Forms: Embed signing, the tool tip of sign button do not display correct information.
*   \[SIGN-1191\] - Cloning field location on different page do not work.
*   \[SIGN-1192\] - Encoding issues in signature fields.
*   \[SIGN-1193\] - Fixing issues in envelope preparation wizard related with new page hash in the URL introduced.
*   \[SIGN-1194\] - Fixing all links in tools menus to lead to signature 2.
*   \[SIGN-1195\] - Review integration with Google drive and point all actions to signature 2.
*   \[SIGN-1196\] - Forms wizard layout broken on first load.
*   \[SIGN-1197\] - Sequential signing do not work correctly.
*   \[SIGN-1198\] - Problem with verifying signed document.
*   \[SIGN-1199\] - Navigation issue in templates wizard.
*   \[SIGN-1200\] - Fixing viewer in signature 1.
*   \[SIGN-1201\] - Forms: Preparation wizard step 3, after refresh, the user is returned to step1.
*   \[SIGN-1203\] - Review all API methods and swagger attributes.
*   \[SIGN-1204\] - Performance issues in envelope/template add document.
*   \[SIGN-1208\] - SVG signature signing document from Google drive does not work.
*   \[SIGN-1209\] - Low resolution of signature on the last page when svg is used.
*   \[SIGN-1210\] - In fields preparation, the fields tool tip stays on while dragging the field.
*   \[SIGN-1211\] - Change the signature color and background in final signed document.
*   \[SIGN-1212\] - In fields preparation, the fields tool tip stays on while resizing the field.
*   \[SIGN-1214\] - Improve tool tips for required messages.
*   \[SIGN-1215\] - Validate drop down fields settings when exiting at step 5.
*   \[SIGN-1216\] - Typed signature bleed outside the rectangle for some fonts.
*   \[SIGN-1217\] - Ensure that the drawing, typing signature works correctly on tablets.
*   \[SIGN-1218\] - In embed sign envelope, the sign button tool tip is hidden too fast and can't be clicked.
*   \[SIGN-1219\] - Improve hot keys behavior in fields preparation.
*   \[SIGN-1221\] - Update the style of verify signed document dialog in signed and signed embedded.
*   \[SIGN-1222\] - For envelopes created from template, validate the recipients on step2 and during the send step.
*   \[SIGN-1223\] - Editing and saving a recipient in template preparation, shows duplicated order message.
*   \[SIGN-1225\] - Click on a signature in signatures dashboard should open an edit dialog.
*   \[SIGN-1226\] - Ensure that import contacts is working.
*   \[SIGN-1227\] - Implement ordering template recipient in the UI.
*   \[SIGN-1228\] - Fix the style of the import contacts dialog.
*   \[SIGN-1229\] - Fixing styles on various places in signature.
*   \[SIGN-1230\] - Fixing document sharing for envelope recipients.
*   \[SIGN-1232\] - Can't reset uploaded signature to blank.
*   \[SIGN-1233\] - The data for fields for recipients who already signed the envelope are not loaded in the sign screen.
*   \[SIGN-1235\] - Can't select from a drop down field in Firefox.
*   \[SIGN-1236\] - Order envelopes by modified date in envelopes dashboard.
*   \[SIGN-1239\] - Drop a file in the new verify signed document page doesn't work.
*   \[SIGN-1241\] - Problems in the forms with selecting next field or finish button.
*   \[SIGN-1242\] - Fixing invalid markup in embed sign/signed in signature 2.
*   \[SIGN-1246\] - Signature 1: In envelope/form embed sign, the tool tip of the sign button disappear very quickly,
*   \[SIGN-1249\] - Forms: After document is uploaded, some hints are still visible,
*   \[SIGN-1250\] - Integrate new dialogs styles for verifying documents in signed and signed embedded envelopes.
*   \[SIGN-1253\] - Fixing styles in signature 2 and signature verification page.
*   \[SIGN-1259\] - On step 2, in envelope preparation, clicking quickly on add me button adds the owner as recipient twice.
*   \[SIGN-1260\] - Creating signature from the right toolbar doesn't work.
*   \[SIGN-1261\] - Integrate svg signing in forms.
*   \[SIGN-1263\] - Signature 1: In IE8, embed envelope sign, the start button is not displayed.
*   \[SIGN-1264\] - Sign and reminder manager crashing the converter service.
*   \[SIGN-1266\] - Desktop notifications for forms in chrome doesn't work.
*   \[SIGN-1267\] - Fields summary for templates are not visible during final step of preparation.
*   \[SIGN-1268\] - When moving/resizing fields with keyboard in envelope/template/form preparation, the tool tips should be hidden.
*   \[SIGN-1271\] - Low performance on loading forms dashboard.
*   \[SIGN-1272\] - Embed sign envelope: when clicking the confirm signature button, the start button reappears.
*   \[SIGN-1273\] - Remove the background of typed signature and make the generated signature transparent.
*   \[SIGN-1276\] - When the audit log popup is visible, and start scrolling, the page behind the popup is scrolling too.
*   \[SIGN-1277\] - Display confirmation dialog before restarting an envelope from the dashboard.
*   \[SIGN-1278\] - The envelopes list in dashboard is resetting to top position before any action that displays confirmation dialog.
*   \[SIGN-1281\] - Issue with field positioning in the landscape documents.
*   \[SIGN-1283\] - In signed and signed embed, the start button is always visible.
*   \[SIGN-1285\] - Investigate and fix the issues with the viewer in signature.
*   \[SIGN-1286\] - Display confirmation dialog before copying a form in forms dashboard.
*   \[SIGN-1291\] - Validate that all recipients with role signer/owner have fields when exiting from step 5 in envelope preparation wizard.
*   \[SIGN-1292\] - Save recipients order in envelope preparation wizard when exiting from step 2.
*   \[SIGN-1293\] - Save envelope name in envelope preparation wizard when exiting from step 3
*   \[SIGN-1294\] - Save form name in form wizard when exiting from step 2
*   \[SIGN-1295\] - If document is renamed in the envelope, and this envelope is copied, the new document name is lost.
*   \[SIGN-1296\] - Investigating issue with viewer in comparison.
*   \[SIGN-1298\] - Review all tool tips in signature and ensure that they are using the styled view.
*   \[SIGN-1300\] - When adding documents to form, parse the detects for the fields markups.
*   \[SIGN-1301\] - Envelope preparation wizard has issue with removing document with fields.
*   \[SIGN-1302\] - In embed sign in signature 1, if there is no logged in user, the fields load and disappears.
*   \[SIGN-1303\] - In embed sign in signature 1 if there is not logged in user, the fields load and disappears.
*   \[SIGN-1305\] - The recipient name is not populated in signature 2 embed signing.
*   \[SIGN-1307\] - Issue with signature embed sign in IE 9.
*   \[SIGN-1312\] - Recipients with role CC should not be able to open the envelope before it has been signed.
*   \[SIGN-1313\] - Only the owner should see the embed link popup when clicking the recipients buttons in envelopes dashboard.
*   \[SIGN-1314\] - Fixing issues in form and templates related with parsing fields in document settings.
*   \[SIGN-1315\] - Implement changes in envelope.field.add.
*   \[SIGN-1326\] - Validation for set fields for a recipient do not work correctly.
*   \[SIGN-1327\] - Can't add owner as recipient.
*   \[SIGN-1328\] - Reorder buttons at the last step of envelope wizard when only owner is recipient
*   \[SIGN-1331\] - Fix the dashboards breadcrumb.
*   \[SIGN-1332\] - Incorrect behavior of the upload tool tip in envelope wizard.
*   \[SIGN-1337\] - Error "The given Key does not exist in Dictionary" when creating form from template.
*   \[SIGN-1338\] - Forms created from template cannot be assigned if those contain text field.

*   \[SIGN-1280\] - Issue with sent emails from production.
*   \[SIGN-1340\] - The cancel envelope event is not displayed correctly in the audit log.
*   \[SIGN-1341\] - Make the records for the sent emails in the audit log more specific and point the recipient email.
*   \[SIGN-1342\] - In sign envelope screen, the fields tool tips do not load the correct text set during preparation.
*   \[SIGN-1344\] - In fields preparation, when toolbar for a field is visible, dragging the toolbar should not move the field.
*   \[SIGN-1345\] - Style and align settings for a field should be immediately previewed once set.
*   \[SIGN-1346\] - If there are changes in field settings and the user try to select other field, display confirmation message and offer to save changes.
*   \[SIGN-1347\] - When copy a form, sometimes the form fields are duplicated
*   \[SIGN-1348\] - In the forms dashboard, paging do not work.
*   \[SIGN-1356\] - In forms fields preparation, the field settings toolbar has incorrect behavior.
*   \[SIGN-1357\] - If reload the browser when in step 3 of forms preparation, the document is not loaded
*   \[SIGN-1360\] - Wrong font size for the second recipients in the signature dialog, when envelope is in-person sign.
*   \[SIGN-1361\] - Hide the error message that is displayed if the user reloads the browser during in-person signing.
*   \[SIGN-1362\] - The sign button in envelope sign screen is not enabled even if all fields are filled.
*   \[SIGN-1370\] - When only one document is in an envelope, the drop down for selecting documents should not be visible in sign and embed sign.
*   \[SIGN-1377\] - Forms can't be deleted.
*   \[SIGN-1379\] - Ensure that the placed fields width/height are constrained to the field type minimal width/height.
*   \[SIGN-1382\] - Remove the document drop down in signature 1 sign/embed sign if only one document is in envelope.
*   \[SIGN-1383\] - Fixes in signature API.
*   \[SIGN-1385\] - Signature fields guidance text limits.

## Platform**Features Implemented**

*   **Major**
    *   \[CORE-914\] Accounts' monthly usage report.
    *   \[CORE-932\] Signups per day report.
    *   \[CORE-944\] Mail merge for PowerPoint documents.
    *   \[CORE-933\] Subscription plan promo codes support.
    *   \[CORE-952\] Documents content re-indexing tool.

*   **Minor**
    *   \[CORE-917\] Google analytics integration and enhancement.
    *   \[CORE-926\] A link to Support forum in the footer.
    *   \[CORE-941\] Recovery options for windows services setup on installation.
    *   \[CORE-943\] Document assembly with regions API usage sample.
    *   \[CORE-946\] A new Welcome email template.

**Bugs Fixed**

*   **Critical**
    *   \[CORE-925\] Banckle forum cookies are not refreshed on logging in/out.
    *   \[CORE-957\] Upload on dashboard fails.
    *   \[CORE-965\] New user registration fails.
    *   \[CORE-970\] Context menu does not work on dashboard.
    *   \[CORE-966\] Files cannot be removed from the Dashboard.

*   **Major**
    *   \[CORE-355\] Documents with the same name get uploaded even without a warning.
    *   \[CORE-945\] File name is wrong in remove file dialog box.
    *   \[CORE-930\] Sub-folders cannot be created on dashboard.

*   **Minor**
    *   \[CORE-935\] A typo in applications help widget.

## [API](http://groupdocs.com/cloud)**Features Implemented**

*   \[CORE-922\] Banckle forum users creation for new signs up.
*   \[CORE-923\] File.metadata synchronization option for remote storages.
*   \[CORE-929\] SDK method for authorization operation from the shared endpoint.
*   \[CORE-939\] Subscription promo code simulation API.
*   \[CORE-945\] Subscription cancellation Dynabic event handler.
*   \[CORE-928\] Questionnaire conditional logic API.
*   \[CORE-931\] HTML5 document viewing service.
*   \[CORE-936\] Document page HTML representation retrieval API.
*   \[CORE-937\] Document viewing request for HTML5 viewer.
*   \[CORE-964\] Extra fields for the system notifications entity.
*   \[CORE-954\] Documents password protection API.
*   \[CORE-955\] Document password setting API.
*   \[CORE-956\] Questionnaire expiration time validation.

**Bugs Fixed**

*   \[CORE-726\] Sign up when Dynabic is unavailable issue.
*   \[CORE-868\] Cannot upload XLS file on EU.
*   \[CORE-918\] BadRequest when shared with wrong email.
*   \[CORE-919\] Cannot create folder.
*   \[CORE-920\] Document cannot be viewed when splitting into pages, partially fails.
*   \[CORE-942\] Unnecessary temp files are not removed by the document viewing service.
*   \[CORE-934\] Subscription state change event is rejected.
*   \[CORE-391\] questionnaire.remove raises error "Unable to remove questionnaire from the database.
*   \[CORE-949\] Null thumbnail generated for UploadWeb.
*   \[CORE-951\] External component has thrown an exception.
*   \[CORE-971\] Parameter order is wrong in swagger specs.
*   \[CORE-953\] Folders with spaces cannot be created.



