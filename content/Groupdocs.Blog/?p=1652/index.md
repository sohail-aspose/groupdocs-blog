---
title: 'GroupDocs Apps v2.3 - Features and Fixes'
date: Fri, 08 Mar 2013 10:07:04 +0000
draft: true
url: /?p=1652
author: 'Derek Hyland'
summary: ''
tags: ['API', 'digital signature', 'document management', 'document upload', 'esignature', 'GroupDocs Annotate', 'GroupDocs Signature', 'GroupDocs Viewer', 'GroupDocs Viewer Plugin', 'online document management system', 'online document viewer', 'View documents online', 'zArchive']
---

We’ve implemented a few new features as well as fixed some major and minor bugs lately. Let’s have a detailed look:

## [GroupDocs Annotation](http://groupdocs.com/apps/annotation)**Features Implemented**

*   Major

*   \[ANNOTATION-194\] Annotation v.2. The resizing of Typewriter text fields and Watermarks
*   \[ANNOTATION-195\] Annotation v.2.Text color selection for Typewriter text fields and Watermarks
*   \[ANNOTATION-196\] Embedded application header customization feature
*   \[ANNOTATION-197\] Embedded application toolbar customization
*   \[ANNOTATION-199\] Custom cursors for embedded annotation tools configuration
*   \[ANNOTATION-182\] Full synchronization of Annotation instances
*   \[ANNOTATION-201\] Proper error-handling in embedded applications
*   \[ANNOTATION-198\] Embedded application real-time mode configuration

*   Minor

*   \[ANNOTATION-176\] Each new user should have a different default colour
*   \[ANNOTATION-191\] Annotation v.2. New icons and cursors.
*   \[ANNOTATION-216\] Annotation v.2. The annotation icons panel should have the correct scroll position set before it is shown

**Bugs fixed**

*   Critical:

*   \[ANNOTATION-185\] Annotation reply date is incorrect for replies posted by a collaborator
*   \[ANNOTATION-203\] Annotation v.2. The mouse position is set imprecisely on receivers when being broadcasted in the real-time mode
*   \[ANNOTATION-206\] Annotation v.2. Annotation lines remain pushed down after the annotation that pushed them down was deleted
*   \[ANNOTATION-207\] Annotation v.2. Connecting lines for annotations redraw after collapsing the RHS panel, creating a gap while the panel is collapsing
*   \[ANNOTATION-208\] Annotation v.2. Touches don't work on iPhone
*   \[ANNOTATION-190\] Export with annotations is not working
*   \[ANNOTATION-193\] Annotation v.2. Full synchronization does not work on iPhone
*   \[ANNOTATION-200\] Annotation v.1. SignalR gives the error "TypeError: annotationsHub is undefined"
*   \[ANNOTATION-212\] Annotation v.2. Area annotation marker movements are not broadcasted.
*   \[ANNOTATION-214\] Too many thumbnails are loaded initially for documents with many pages
*   \[ANNOTATION-217\] Annotation v.1. Point annotations can't be created
*   \[ANNOTATION-210\] Annotation v.2. Touches don't work on iPhone for the header buttons

*   Major:

*   \[ANNOTATION-204\] Annotation v.2. SignalR connection sometimes breaks in the real-time mode
*   \[ANNOTATION-205\] Annotation v.2. Markers and their lines are not redrawn when the browser window is resized
*   \[ANNOTATION-213\] Annotation v.2. Annotation lines remain short after activating an annotation and collapsinbg the RHS panel.
*   \[ANNOTATION-215\] Thumbnail progress spinners hang at the middle of the thumbnails panel
*   \[ANNOTATION-219\] Annotation v.2. Typewriter text field movements are not broadcasted.

*   Minor

*   \[ANNOTATION-147\] Typewriter change color doesn't work
*   \[ANNOTATION-162\] Disabled view permission should disable others
*   \[ANNOTATION-187\] Text selections and strikeouts are above typewriter fields (z order)
*   \[ANNOTATION-188\] Annotation v.2. When adding a new annotation, the comments panel should expand, switch to Comments tab, and then focus the comment field
*   \[ANNOTATION-209\] Annotation v.2. Annotation icons in the icons panel scrolling with lags in Chrome
*   \[ANNOTATION-218\] Annotation v.2. Document size is not changed when an annotation is activated and the RHS panel was collapsed

## [GroupDocs Viewer](https://blog.groupdocs.com/tag/online-document-viewer)**Features Implemented**

*   Minor

*   \[WEB-337\] Embedded application header customization feature

**Bugs fixed**

*   Minor

*   \[WEB-338\] Yes/No buttons position in Viewer tools

## **[GroupDocs Assembly](http://groupdocs.com/apps/assembly)****Features Implemented**

*   Minor

*   \[DA-141\] Output folder and email address options on the settings page
*   \[DA-143\] Generic answer option for single choice questions

**Bugs fixed**

*   Major:

*   \[DA-142\] Document upload through drag & drop area fails

## **[GroupDocs Signature](http://groupdocs.com/apps/signature)****Features Implemented**

*   \[SIGN-852\] Audit log for envelopes in signature 2
*   \[SIGN-843\] Signature 2: Click on delete icon for field, selects the field
*   \[SIGN-842\] Signature 2: In step 5, allow resizing selected field with Ctrl+arrow key
*   \[SIGN-841\] Signature 2: In step 5, allow switching between fields with tab
*   \[SIGN-833\] Draft envelope deletion in signature 2 envelope dashboard
*   \[SIGN-832\] Signature 2: Forms dashboard
*   \[SIGN-829\] Signature 2: In envelopes dashboard, click on envelope should perform same action as click on the view icon
*   \[SIGN-828\] Signature 2: In envelopes dashboard, when clicking on a recipient, display a popup with embed link for copy
*   \[SIGN-824\] Hide the Signature 2 form the main button, and add a banner in Signature 1 app for trying out the Signature 2
*   \[SIGN-822\] Signature 2: In step 2, completion functionality for quickly selection from the contacts
*   \[SIGN-803\] Signature 2: Templates dashboard
*   \[SIGN-802\] Signature 2: Signatures dashboard
*   \[SIGN-848\] Demo application using .NET signature SDK

**Improvements**

*   \[SIGN-846\] Log the client IP and display it for each signer in final signed document
*   \[SIGN-836\] Integrate latest design changes in envelope create wizard
*   \[SIGN-834\] Add referrer check for the signature demo

*   \[SIGN-860\] - When envelope has only one document, the envelope.documents.get API method should return the signed pdf not an archive
*   \[SIGN-898\] - Signature 2: Signing screen, add validation for the placed field
*   \[SIGN-899\] - Signature 2: Add sammyjs in the envelope wizard
*   \[SIGN-907\] - Signature 2: Wizard: In the summary step show list of fields per document and recipient
*   \[SIGN-908\] - Signature 2: Apply latest design changes in envelopes dashboard
*   \[SIGN-909\] - Signature 2: Embedded forms signing do not show next marker
*   \[SIGN-910\] - Signature 1: Update the embedded signing screen for forms
*   \[SIGN-931\] - In signing screen, when envelope has more than one recipients, show hint for the fields that do not belong to the signing recipient
*   \[SIGN-932\] - Show visual feedback during envelope signing
*   \[SIGN-915\] - Attach signed documents when send final notification email to all recipients
*   \[SIGN-837\] - Integrate step5 design in the create envelope wizard
*   \[SIGN-857\] - Implement archived envelopes in signature 2
*   \[SIGN-861\] - Implement create form wizard in signature 2
*   \[SIGN-877\] - Implement signature 2 sign screen
*   \[SIGN-880\] - Implement signature 2 archived forms view
*   \[SIGN-887\] - Signature 2 Forms: Apply latest design changes in forms dashboard and archived forms
*   \[SIGN-862\] - Integrate step1 in create form wizard
*   \[SIGN-863\] - Integrate step2 in create form wizard
*   \[SIGN-875\] - Integrate step 3 in create form wizard
*   \[SIGN-878\] - Integrate step 4 in create form wizard
*   \[SIGN-879\] - Integrate step 5 in create form wizard
*   \[SIGN-883\] - Watermark settings in step 2
*   \[SIGN-896\] - Signature 1 embedded signing changes
*   \[SIGN-900\] - Signature 2: Embedded forms signing
*   \[SIGN-918\] - Ensure that in signature all images for a documents are loaded from the S3 storage if set so

**Bugs fixed**

*   \[SIGN-853\] When envelope is signed from embeddable view, the notification to callback url is not sent
*   \[SIGN-845\] Signature 2: Placeholder of the search inputs in contacts are not visible
*   \[SIGN-844\] Signature 2: In envelope wizard the use can't return to previous step if the current step is not valid
*   \[SIGN-838\] With direct URL the user can go to the create envelop wizard even for envelopes that are not draft
*   \[SIGN-820\] SignalR issues in signature, comparison, conversion
*   \[SIGN-821\] Fix buttons tooltips in signature 2 step 1
*   \[SIGN-823\] Fix buttons tooltips in signature 2 wizard step 2 for edit, delete recipient

*   \[SIGN-859\] - If user is logged in and visit the embed signature - he can't see the fields in the document and can't sign
*   \[SIGN-865\] - Add regex validation dropdown in field settings area in signature 2
*   \[SIGN-866\] - Add default values for font name, font size, font color on add envelope field
*   \[SIGN-867\] - Send email notifications in signature do not respect the IsAlertsEnabled settings of the user account
*   \[SIGN-868\] - Signature 2 Wizard: Step2: While editing an recipient, hide the add recipient area as well as edited recipient row
*   \[SIGN-869\] - Make all validation messages dynamic (show/hide while user typing)
*   \[SIGN-870\] - Signature2 Wizard: Step 3 can continue with empty envelope name
*   \[SIGN-871\] - Signature 2 Wizard: Step 5: No validation for the field name.
*   \[SIGN-872\] - Signature 2 Wizard: Step 5: Implement Reset Fields functionality
*   \[SIGN-873\] - Signature 2 Wizard: Step 5: Move the documents and recipients drop-downs above the fields toolbar
*   \[SIGN-874\] - Signature 2 Wizard: Step 5: If there are no at least one field for each recipient and document do not allow user to go to next step nor to send the envelope
*   \[SIGN-876\] - The signature should not exit the cell on the summary page of the signed document
*   \[SIGN-881\] - Update the signature 1 embed signing
*   \[SIGN-885\] - Signature 1 embedded, click next do not stop on signature and checkbox field
*   \[SIGN-886\] - Signature 2: Forms, load only the data needed for the active tab
*   \[SIGN-888\] - Signature 2: Step 5: Field settings could not be saved
*   \[SIGN-889\] - Signature 2: Step 5: Adding items for drop down field do not work
*   \[SIGN-890\] - Signature 2: Step5: The pressing the tab key should cycle between fields
*   \[SIGN-891\] - Signature 2: Step 5: Esc key press should deactivate selected field and close field settings area.
*   \[SIGN-892\] - Public download signed documents do not return correct response
*   \[SIGN-893\] - Cannot edit signature
*   \[SIGN-894\] - Signature 2. Create form from template doesn't work
*   \[SIGN-895\] - Signature 2: Forms, fields settings doesn't work correctly as well as drop-down list management
*   \[SIGN-897\] - Signature 2: Step 4: Can't reorder selected fields for creating file name
*   \[SIGN-901\] - Signature 2: User should not be able to modify only fields for selected recipient in fields preparation screen in the wizard
*   \[SIGN-902\] - Signature 2: In the wizard the user can go to step "summary" without any fields set
*   \[SIGN-903\] - Signature 2: In the fields step there is a problem with the shift+tab switching of the fields
*   \[SIGN-904\] - Signature 2: Fields step: The date field do not have format settings
*   \[SIGN-905\] - Signature 2: Fields step: Exclude date formats from the format settings for single and multi-line fields
*   \[SIGN-906\] - Signature 2: Fields step: Tab and Shift+Tab should cycle only between fields for the selected recipient
*   \[SIGN-911\] - Signature 2: Forms: In embedded signing, the ordering of the fields is not correct
*   \[SIGN-912\] - Signature 2: Forms: Clicking on the form row in the dashboard should perform the default action
*   \[SIGN-913\] - Signature 2: Forms: In dashboard, add "Download all" action for the completed forms
*   \[SIGN-914\] - Forms: Embedded signing, do not load data for the filled fields on reload
*   \[SIGN-916\] - Signature 2: Forms: In the wizard, creating new field location doesn't work
*   \[SIGN-917\] - Signature 2: Forms: In step 3 in the wizard, the tab/shift+tab do not work correctly
*   \[SIGN-920\] - Signature 2: Envelope wizard step1, sometimes do not show documents even if the envelope has documents
*   \[SIGN-921\] - Loading signature documents from amazon s3 storage
*   \[SIGN-922\] - Signature 2: Do not show error message if something went wrong during the API call
*   \[SIGN-923\] - Signature 2: In sign envelope screen, when start entering data for a field, the whole field move down few pixels
*   \[SIGN-924\] - Signature 2: Tab, Shift+ Tab should move between fields
*   \[SIGN-925\] - Signature 2: Signing screen, if document has more than one page, on scrolling down the pages after fist page didn't load
*   \[SIGN-926\] - Signature 2: In sign envelope screen, the thumbnails side bar do not work
*   \[SIGN-928\] - Adding fields for a user with role CC should not be possible
*   \[SIGN-930\] - Signature 2: When performing Save as draft, the owner of the envelope is added
*   \[SIGN-933\] - Signature 1: Switching recipient role in the envelope preparation wizard doesn't work
*   \[SIGN-934\] - Envelope ModifyFieldLocation Api method doesn't work
*   \[SIGN-936\] - Select all checkbox in signature 2 dashboards (envelopes, forms, archived forms) doesn't work correctly
*   \[SIGN-937\] - Signature 2: Envelope wizard step2: Add from contacts do not show any contacts in the popup

## **[GroupDocs Comparison](http://groupdocs.com/apps/comparison)****Features Implemented**

*   \[DOCOMPARE-200\] Embeddable comparison result
*   \[DOCOMPARE-195\] Comparison 2 viewer
*   \[DOCOMPARE-197\] Comparison 2: User workflow changes, add ability to start new comparison
*   \[DOCOMPARE-206\] Embed button in comparison 2

**Bugs fixed**

*   \[DOCOMPARE-194\]\[DOCOMPARE-201\] Comparison of two doc file fails
*   \[DOCOMPARE-208\] Fixing issues in comparison 2 embed link generation and showing
*   \[DOCOMPARE-205\] Can't load the output document after comparison is completed and the UI is blocked
*   \[DOCOMPARE-204\] After first comparison, the GetChanges method is called many times
*   \[DOCOMPARE-203\] Doc files comparison fails when in the source or target has attached template
*   \[DOCOMPARE-202\] Doc files comparison fails when there are embed images and ole objects
*   \[DOCOMPARE-196\] Download result do not work in comparison 2

## **Platform****Features Implemented**

*   Major

*   \[CORE-823\] Pricing plans update
*   \[CORE-834\] Document split and view commands for the Conversion service

*   Minor

*   \[CORE-830\] Output folder and email address job options

**Bugs fixed**

*   Minor

*   \[CORE-805\] -1 Users
*   \[CORE-822\] Google Cloud redirect is interrupted after submitting popup
*   \[CORE-654\] Thumbnail for DOC file on share screen

## **Dashboard****Bugs fixed**

*   Critical:

*   \[CORE-828\] File move/copy operations do not work on the dashboard

*   Minor

*   \[CORE-800\] File/folder context menu is visible through delete confirm dialog

## **[API](http://groupdocs.com/cloud)****Features Implemented**

*   \[CORE-818\] File storage synchronization service integration
*   \[CORE-824\] Migration to the latest Banckle Billing platform
*   \[CORE-835\] Google Cloud. Cannot create folder
*   \[CORE-826\] Subscription plan purchase response extension

*   \[SIGN-825\] Webhook notification for signature API
*   \[SIGN-847\] Create envelope from a document in the API
*   \[SIGN-826\]\[SIGN-851\] Changes in envelope.send method
*   \[SIGN-850\] Changes in envelope.recipient resource
*   \[SIGN-827\] Send webhook notification when all recipients signed the envelope

**Bugs fixed**

*   \[CORE-861\] Number of users is not updated for Enterprise subscriptions
*   \[CORE-872\] Free space is improperly calculated on documents upload
*   \[CORE-634\] Document viewing service concurrency problem
*   \[CORE-808\] GetQuestionnaireExecutions returns null in questionnaire\_guid
*   \[CORE-809\] GetQuestionnaires always returns empty questionnaires array
*   \[CORE-810\] UpdateQuestionnaireExecution doesn't update executive/approver/owner
*   \[CORE-812\] Typo in Swagger documentation for AddQuestionnaireCollector
*   \[CORE-814\] UpdateQuestionnaireMetadata returns 0 in questionnaire\_id
*   \[CORE-815\] UpdateQuestionnaireMetadata doesn't actually update metadata
*   \[CORE-825\] The checkDocumentOwnership flag allows an API user to convert files indefinitely
*   \[CORE-827\] Document viewing fails when splitting is not possible
*   \[CORE-836\] Google Cloud. Folder is shown like file
*   \[CORE-829\] Document upload fails for the root folder

Your support and feedback are important for us. Talk to us through our **[official feedback forum](http://groupdocs.com/Community/Forums/Default.aspx)** or **[Live Chat support](http://groupdocs.com/)**. Stay tuned for our blog and **newsletter**.



