---
title: 'GroupDocs Apps v2.1.4.5315 - Features and Fixes'
date: Thu, 17 Jan 2013 17:44:35 +0000
draft: true
url: /?p=1224
author: 'Derek Hyland'
summary: ''
tags: ['document management', 'gr', 'GroupDocs Annotate', 'GroupDocs Signature', 'GroupDocs Viewer', 'online document viewer', 'zArchive']
---

We’ve implemented a few new features as well as fixed some major and minor bugs lately. Let’s have a detailed look:

## **[GroupDocs Annotation](http://groupdocs.com/apps/annotation)**

*   ### **New features implemented**
    *   #### **Major**
        *   Watermark tool: this tool lets you add text to a document and export.
    *   #### **Minor**
        *   It should not be possible to see more than one page when using the magnify button. Magnification below 50% is disabled.
        *   The comment mode toolbar should slide when the thumbnails are shown so that the thumbnails wouldn't hide it.
        *   New icons are applied for the Polyline annotation and Watermark modes.
*   ### **Bugs Fixed**
    *   #### **Critical**
        *   The application tries to get the built-in user profile and fails.
        *   Export feature in the embedded Annotation v.1 not working.
        *   Anonymous users are unable to open the embedded document annotations.
        *   Comments are not removed when the document is opened.
        *   Incorrect embed link in the Annotation v.2.
        *   Annotation v.2 - when opening embedded Annotation with UID and signed URL without being authenticated, login is required.
    *   #### **Minor**
        *   Copy to clipboard button to copy File ID.
        *   Annotation 2 - “Manage reviewers” color is always black.
        *   Annotation 2 - No "Name" field in "Manage reviewers".
        *   Annotation 2 - Tools menu links are non-functional.
        *   Annotation v.2 - Text fields created by the Typewriter tool do not disappear after loading another document using the Load button.
        *   The centering of page images in the Annotation v.2.
        *   Document loading fails when the color of a reviewer is null.
        *   If a comment type is selected during document loading, an error is shown.
        *   Annotation v.2 - when deleting an active annotation via broadcasting, replies remain on screen.

## [GroupDocs Viewer](http://groupdocs.com/apps/viewer)

*   ### **Bugs Fixed**
    *   #### **Critical**
        *   Broken layout in Viewer v.1 and v.2.
        *   IE8 viewer JS error.
        *   Viewer v.2 shows an error: "embedSource...("getViewmodel") not defined."

## **[GroupDocs Assembly](http://groupdocs.com/apps/assembly)**

*   ### **Bugs Fixed**
    *   #### **Minor**
        *   Removed collectors produce a generic error message.

## **[GroupDocs Signature](http://groupdocs.com/apps/signature)**

*   ### **New features implemented**
    *   Signature v2 envelopes dashboard
    *   Signature v2 create envelope wizard
    *   Signature v2 contacts
*   ### **Bugs Fixed**
    *   Wrong output when signing word document.
    *   Signing multiple documents returns single document ID as output.
    *   For single line and multi-line fields, the format dropdown shows regex for datetime validation.
    *   For datetime fields, the format dropdown shows all regex instead only those that are related with datetime validation.
    *   For checkbox fields, the format dropdown is displayed.
    *   If resize change single line field height, than can't return to original height.
    *   The hint value for fields is not stored.
    *   Watermark is not placed correctly in the signed document.
    *   Calling sign API method with a doc file, throws exception.
    *   Bad layout in empty contacts list.
    *   Contacts list is not refreshed after deleting selected contacts.

## **[GroupDocs Comparison](http://groupdocs.com/apps/comparison)**

*   ### **New features implemented**
    *   Excel comparison
*   ### **Bugs Fixed**
    *   When trying to compare two doc file, an error is displayed.
    *   PDF comparison failure.

## **[GroupDocs Conversion](http://groupdocs.com/apps/conversion)**

*   ### **Bugs Fixed**
    *   Create conversion popup and filter menu collision.
    *   Bad email parameters can cause the emails to be pending in each cycle in the pop3 handler.
    *   Convert link not working.

## **Platform**

*   ### **New features implemented**
    *   #### **Minor**
        *   Modal dialogs redesigned.
*   ### **Bugs Fixed**
    *   #### **Critical**
        *   Profile settings page doesn't open in IE8.
    *   #### **Minor**
        *   Typo in success-buy dialog.
        *   Subscription plan purchase dialog cannot re-try after an exception is thrown.
        *   Login form placeholders in IE9.
        *   Context menu not opening in IE8.
        *   Help doesn't include background in IE8.
        *   NaNKb for uploaded file in Open File dialog.

## **Dashboard**

*   ### **Bugs Fixed**
    *   #### **Critical**
        *   Cannot download both files and folders.
    *   #### **Minor**
        *   Dashboard tabs and filters are double lined in IE8.

## **[API](http://groupdocs.com/cloud)**

*   ### **New features implemented**
    *   Referrers tracking for embedded applications.
    *   Google cloud storage provider.
*   ### **Bugs Fixed**
    *   AddJobDocumentDataSource raises "Unable to parse value."
    *   Cannot upload doc file to **Dropbox Shortcut** folder.
    *   “400 Bad Request” error when accessing Questionnaire with DOC file.
    *   box.com - cannot copy folder to BoxNet Shortcut folder.
    *   GetAnnotation - collaborators returns null in owner ID.
    *   Unable to view documents right after the upload.
    *   Typewriter text fields are exported at the bottom of the page.
    *   Annotation v.2 – unable to save reviewers’ colors.

Please talk to us using our **[Live Chat support](http://groupdocs.com/)** or **[official feedback forum](http://groupdocs.com/Community/Forums/Default.aspx)**. Stay tuned for our blog and **newsletter.**



