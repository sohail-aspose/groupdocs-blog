---
title: 'GroupDocs Apps v2.4 - Features and Fixes'
date: Fri, 19 Apr 2013 13:34:04 +0000
draft: true
url: /?p=2017
author: 'Derek Hyland'
summary: ''
tags: ['API', 'document collaboration', 'document management', 'document upload', 'GroupDocs Annotate', 'GroupDocs Signature', 'GroupDocs Viewer', 'GroupDocs Viewer Plugin', 'online document management system', 'online document viewer', 'View documents online', 'zArchive']
---

We've implemented a few new features as well as fixed some major and minor bugs lately. Let’s have a detailed look:

## [GroupDocs Annotation](http://groupdocs.com/apps/annotation)**Features Implemented**

*   Major

*   \[ANNOTATION-232\] Broadcast of horizontal scroll, broadcast of window size percentage when scaling, and support for master and slaves in real-time mode.

**Bugs fixed**

*   Critical:

*   \[ANNOTATION-220\] If a user is registered as a reviewer for multiple documents, he will receive all broadcasted operations into each open document.
*   \[ANNOTATION-226\] Export "Normal" raises an error.
*   \[ANNOTATION-230\] Downloading an annotated document by using a direct file link fails.

*   Major:

*   \[ANNOTATION-225\] The background color of the pages and thumbnails is transparent, which creates flashes when they are being loaded.
*   \[ANNOTATION-228\] Annotation v.2. The document should expand when the RHS toolbar is collapsed.
*   \[ANNOTATION-223\] Annotation v.2. An iPhone-styled button for switching between broadcast and screen drag, disable pinch to shrink and pullout to magnify, and a setting for removing the toolbar completely.
*   \[ANNOTATION-222\] Annotation 2. Search doesn't find the searched text.

*   Minor

*   \[ANNOTATION-224\] Text selection is shifted 1 pixel to the right and 1-2 pixels up from the correct position.
*   \[ANNOTATION-227\] The "standard header is always shown" option.

## [GroupDocs Viewer](http://groupdocs.com/apps/viewer)**Features Implemented**

*   Major

*   \[WEB-346\] Client side code for the installable Viewer.
*   \[WEB-347\] JavaScript-based NavigationWidget.
*   \[WEB-348\] JavaScript-based ZoomingWidget.
*   \[WEB-351\] Installable Viewer: JS document viewer adapter without user ID / private key dependencies, working when some widgets are disabled.

*   Minor
    *   \[WEB-342\] Update document viewer 1.0 header.
    *   \[WEB-352\] The PortalService for the installable Viewer.

**Bugs fixed**

*   Minor

*   \[WEB-343\] Document print doesn't work in the embedded viewer.

## [GroupDocs Assembly](http://groupdocs.com/apps/assembly)**Features Implemented**

*   Major

*   \[DA-144\] WYSIWYG support for questionnaire answers.
*   \[DA-148\] Web hook for the document assembly job.

**Bugs fixed**

*   Major:

*   \[DA-145\] Long questions and answers word-wrap.

## [GroupDocs Signature](http://groupdocs.com/apps/signature)**Features Implemented**

*   \[SIGN-967\] - Signature2: Signed view for envelopes.
*   \[SIGN-968\] - Signature 2: Signed embedded view for envelopes.

**Improvements**

*   \[SIGN-942\] - Signature 2: New status icons for envelopes and forms.
*   \[SIGN-949\] - Implement async signing of the signature envelopes.
*   \[SIGN-950\] - Adopt signed screen and signed embedded screen to work with async envelope signing process.
*   \[SIGN-956\] - Signature 2: Implement envelope-embed signing.
*   \[SIGN-957\] - Signature 2: Improve the user experience after clicking "New Envelope" in the envelopes dashboard.
*   \[SIGN-961\] - Signature 2: Improve the user experience after clicking "New Form" in the forms dashboard.
*   \[SIGN-980\] - Implement changes in _envelope.create_ and _envelope.modify_
*   \[SIGN-981\] - New settings while preparing envelope in signature 1 and signature 2.
*   \[SIGN-983\] - Signature 2: Implement embed signed screen.
*   \[SIGN-995\] - Implement create envelope from envelope in signature 1 and signature 2.
*   \[SIGN-999\] - Increase recipient name's length for envelopes.
*   \[SIGN-1005\] - Default value for "Include embed link .." settings for envelope should be true.
*   \[SIGN-940\] - Signature 2: Implement template preparation wizard.
*   \[SIGN-969\] - Signature 2: Forms: recheck that the forms signing is working and apply fixes if not.
*   \[SIGN-998\] - Display error messages in embedded signature as a popup.
*   \[SIGN-1014\] - Signatrure 1: From archived envelopes, the user should be able to copy the envelope and start over.
*   \[SIGN-1015\] - Signature 1: Ensure that recipients with role CC are not included in the recipients' dropdown list in fields preparation.
*   \[SIGN-1016\] - Signature 1: For CC recipients, show the embed link button in envelopes dashboard only when envelope is completed.
*   \[SIGN-1018\] - Signature 1: Do not show embed link button in envelopes dash board for envelopes with status expired and draft.
*   \[SIGN-1019\] - Signature 1: In forms dashboard, add Publish Form in the context menu for draft forms.
*   \[SIGN-1027\] - Signature 2: Envelopes: Do not show fields summary on step 6 in envelope preparation wizard.

**Bugs fixed**

*   \[SIGN-853\] When envelope is signed from the embeddable view, the notification to callback url is not sent.
*   \[SIGN-919\] - Demo performance.
*   \[SIGN-927\] - Signature 2: Envelopes dashboard, and statuses overlaps the envelope name.
*   \[SIGN-935\] - Forms: Form preparation wizard, fields settings: remove all jquery selectors.
*   \[SIGN-944\] - Signature 2: Envelopes dashboard, the paging on scrolling does not work properly.
*   \[SIGN-945\] - Fix _template.recipient.add_ and _template.recipient_ api methods response.
*   \[SIGN-946\] - Sign embed requires login.
*   \[SIGN-947\] - Demo signature on send envelope shows error message.
*   \[SIGN-951\] - Create public API method to retrieve envelope details.
*   \[SIGN-952\] - Fix the signatureEnvelopeDetails widget to use public API method if the viewing mode is public.
*   \[SIGN-953\] - Clear the signed document thumbnails, so the most recent pages to be shown in the viewer.
*   \[SIGN-954\] - Signature 2: In the sign envelope screen, in the signature creation popup, the font for written signature are not initialized correctly.
*   \[SIGN-955\] - Signature 2: If we close the signature popup with ESC key, it can't be shown anymore.
*   \[SIGN-962\] - Signature 2: If archived forms list is empty, the select all checkbox is selected.
*   \[SIGN-963\] - AddContactIntegration raises error.
*   \[SIGN-964\] - Add drop-down field doesn't set acceptableValues and defaultValue.
*   \[SIGN-966\] - Inconsistency in signature API boolean parameters.
*   \[SIGN-970\] - Comparing word files with revisions information in them is failing.
*   \[SIGN-971\] - Cannot add two files with the same name, but different extension to envelope.
*   \[SIGN-972\] - If there is drop-down field without list with values, the envelope should not be able to be send.
*   \[SIGN-973\] - If there is a drop-down field without list with values, the form should not be able to be published
*   \[SIGN-974\] - Drop-down value is reset to the default value on reload even if there is already-set user's value.
*   \[SIGN-975\] - If envelope is with status completed, the URL in embed popup should lead to signed envelope.
*   \[SIGN-976\] - Signature 1: Incorrect behavior of tab key in signing screen.
*   \[SIGN-978\] - Signature 2: Ensure that if error is returned from the web service, the corresponded error message will be displayed.
*   \[SIGN-979\] - Extend audit logging to log send and sign events.
*   \[SIGN-982\] - Cleanup code in the signature 1 and signature 2 controllers.
*   \[SIGN-984\] - Forms: Incorrect document displayed after signing.
*   \[SIGN-985\] - Incorrect full name calculation.
*   \[SIGN-986\] - CreateSignatureTemplate multiple issues.
*   \[SIGN-987\] - AddSignatureTemplateRecipient returns null in template identifier.
*   \[SIGN-988\] - Signature 1: Broken layout in templates dashboard if there are no any templates.
*   \[SIGN-989\] - DeleteSignatureTemplateDocument raises error.
*   \[SIGN-990\] - Upload file in create template wizard fails.
*   \[SIGN-991\] - Signature 2: After confirm signing, the user is redirected to login screen if not logged in before.
*   \[SIGN-992\] - After the envelope is sent, the owner is included as signer even if it was not set as signer while preparing the nvelope.
*   \[SIGN-993\] - UpdateSignatureFormFromTemplate raises error.
*   \[SIGN-994\] - Typo in signature envelope API methods.
*   \[SIGN-996\] - The final email notification for signed envelope is not send at all.
*   \[SIGN-997\] - The owner of the envelope could not see the signed documents if he is not in the signers list.
*   \[SIGN-1000\] - Embed signature is not working in IE8.
*   \[SIGN-1001\] - Document viewer in signature 2 throws javascript error.
*   \[SIGN-1002\] - After envelope deletion, files associated with the envelope are staying.
*   \[SIGN-1003\] - After template deletion, files associated with the template are staying.
*   \[SIGN-1004\] - After form deletion, files associated with the form are staying.
*   \[SIGN-1007\] - Replace using of GetTempFileName with GetRandomFileName.
*   SIGN-1013\] - Signature 1: Audit log layout is broken.
*   \[SIGN-1017\] - Signature 1: Embed sign: Always shows the error popup, even if no error.
*   \[SIGN-1020\] - Notification emails are not send to the recipient with role CC.
*   \[SIGN-1021\] - Change the title of the audit log popup.
*   \[SIGN-1022\] - Signature 2: Javascript error in the signed envelope page.
*   \[SIGN-1031\] - Do not include the recipients that have role canSign false at the last page of the signed document.
*   \[SIGN-1033\] - Fixes in embed signing.
*   \[SIGN-1034\] - Signature template API: fields should not be assigned to the recipient with role CC.
*   \[SIGN-1036\] - Fix the viewer in signature 1.
*   \[SIGN-1037\] - Signature 2: Embed sign screen shows start button on each page.
*   \[SIGN-1038\] - Signature 2: Embed signed screen is not working in IE 8.
*   \[SIGN-1039\] - All dashboards in signature do not work IE8.

## **[GroupDocs Comparison](http://groupdocs.com/apps/comparison)****Features Implemented**

*   \[DOCOMPARE-200\] - Embeddable comparison result.

**Improvements**

*   \[DOCOMPARE-211\] - Confirm and embed dialog design update in comparison 2.

**Bugs fixed**

*   \[DOCOMPARE-202\] - Doc files comparison fails when there are embed images and ole objects.
*   \[DOCOMPARE-204\] - After first comparison, the GetChanges method is called multiple times.
*   \[DOCOMPARE-205\] - Can't load the output document after comparison is completed and the UI is blocked.
*   \[DOCOMPARE-206\] - Add embed button in comparison 2.
*   \[DOCOMPARE-208\] - Fixing issues in comparison 2 embed link generation and display.
*   \[DOCOMPARE-212\] - Comparing two different docx files fails.
*   \[DOCOMPARE-213\] - Comparing simple Excel files fails.
*   \[DOCOMPARE-214\] - Comparing pdf files fails.
*   \[DOCOMPARE-215\] - Comparing html files fails.
*   \[DOCOMPARE-216\] - Calling job-output API method with empty or null jobId should not be possible.
*   \[DOCOMPARE-217\] - Comparison 1: After the comparison completion, the results are not displayed.
*   \[DOCOMPARE-219\] - Comparison viewer not working because of changes in the viewer adapter.

## **Platform****Features Implemented**

*   Major

*   \[CORE-859\] Asynchronous PDF to XML conversion.
*   \[CORE-858\] Reusable file open dialog.
*   \[CORE-873\] Web hook trigger for the document viewing job.

*   Minor

*   \[CORE-885\] Integration with Aspose forums.

**Bugs fixed**

*   Critical

*   \[CORE-884\] Multiple instances of explorer plug-in do not work on the same page.
*   \[CORE-892\] Server-side processing fails for non-pdf file formats.

*   Minor
    *   \[CORE-853\] Custom-embedded logo cannot be reset.

## **Dashboard****Features Implemented**

*   Major
    *   \[CORE-831\] Document post-upload processing indicator.

**Bugs fixed**

*   Major:

*   \[CORE-840\] Google Cloud. Dashboard convert redirects to null.
*   \[CORE-882\] "Upgrade" link points to old profile settings page.

*   Minor

*   \[CORE-733\] Folder lacks "Archive" context menu entry.
*   \[CORE-793\] Context menu for the last file is not full visible.
*   \[CORE-844\] Dashboard. Cannot cancel conversion.
*   \[CORE-887\] Chrome drag & drop fail to upload multiple files.

## **[API](http://groupdocs.com/cloud)****Features Implemented**

*   \[CORE-838\] Dynabic subscription cancellation event handler.
*   \[CORE-833\] Pulling document pages image out of a 3rd-party storage.
*   \[CORE-865\] Generic prices for subscription plans support.
*   \[CORE-869\] Random file name generation function for storage providers.
*   \[CORE-888\] Document version number for document page image URL.
*   \[CORE-889\] Path.GetTempFileName replacement.
*   \[CORE-893\] Access level validation for file system folders.

**Bugs fixed**

*   \[CORE-855\] Large file uploads to Amazon S3 fails.
*   \[CORE-866\] Cannot upload PDF file.
*   \[CORE-837\] CSV file cannot be viewed.
*   \[CORE-839\] Update account user method creates users those already exist in the system.
*   \[CORE-861\] Number of users is not updated for Enterprise subscriptions.
*   \[CORE-864\] Thumbnails are not uploaded to Amazon when switching udf-pdf option on/off.
*   \[CORE-871\] Output document format is wrong for assembly jobs.
*   \[CORE-872\] Free space is improperly calculated on documents upload.
*   \[CORE-387\] _datasource.remove_ returns 400 Bad Request
*   \[CORE-389\] _doc.questionnaire.remove_ returns 400 Bad Request

We'll bring you latest news on "Features & Fixes" upon each new release, so stay tuned!



