---
title: 'How to Include GroupDocs SDK and Use Login Method in Plugins'
date: Wed, 11 Sep 2013 07:38:25 +0000
draft: true
url: /?p=2656
author: 'Derek Hyland'
summary: ''
tags: ['API', 'document collaboration', 'document management', 'GroupDocs PHP SDK', 'GroupDocs Plugins', 'GroupDocs Viewer Plugin', 'online document management system', 'php api']
categories: ['GroupDocs.Total Product Family']
---

This article explains the basics of creating a plugin for the Contao CMS using the Contao GroupDocs Viewer plugin as an example. You can download the completed plugin [from Contao](https://contao.org/en/extension-list/view/groupdocs_viewer.10000099.en.html).

## Requirements

*   Contao CMS
*   PHP 5.3
*   GroupDocs [PHP SDK](https://github.com/groupdocs/groupdocs-php)
*   JavaScript

## PreparationTo create a GroupDocs Viewer plugin for Contao CMS:

1.  Install [Contao CMS](https://contao.org/en/). The installation of this CMS is simple.
2.  Allow GroupDocs <iframe> to appear:
    1.  Go to **Admin**, then **Setting** and **Security settings**, then finally **Allowed HTML tags**.
    2.  Add **<iframe>** at the end.

[Read about how to create this plugin](https://blog.groupdocs.com/how-to-create-groupdocs-plugin-for-cms).

## OverviewGroupDocs PHP SDK will be included in the plugin.  Dowload the SDK from our GitHub repository. For this example, we'll only need the **src** folder from this repository. GroupDocs SDK gives us the ability to work with a GroupDocs account directly from the plugin. We can do such things as file upload, list files in the account, log in to GroupDocs and more. In this article, we will stop only on how to log in to  a GroupDocs account from the plugin.

## Login logic

1.  When a user clicks the GroupDocs Viewer button, a pop-up with form opens.
2.  The user enter login and password.
3.  The entered data is transferred for processing.
4.  The controller receives the transfered data and includes the GroupDocs SDK.
5.  Call the Login method which takes the entered login and password details and sends a request to the GroupDocs API.
6.  The GroupDocs API return a User object which contains all the user info.

## ImplementationFirst we need the SDK in the plugin. Download it from GitHub and copy the src folder with all its content to the plugin folder. You should get this structure: \[caption id="attachment\_2660" align="alignnone" width="600" caption="Plugin structure"\][![Plugin structure](https://blog.groupdocs.com/wp-content/uploads/sites/4/2013/06/structure.png "Plugin structure")](https://blog.groupdocs.com/wp-content/uploads/sites/4/2013/06/structure.png)\[/caption\] OK. Now open the _**groupdocs\_viewer/config/config.php** file and replace all the content with this:_

```
<?php if (!defined('TL\_ROOT')) die('You can not access this file directly!');

/\*\*
 \* GroupDocs
 \*
 \* This program is free software: you can redistribute it and/or
 \* modify it under the terms of the GNU Lesser General Public
 \* License as published by the Free Software Foundation, either
 \* version 2.1 of the License, or (at your option) any later version.
 \*
 \* This program is distributed in the hope that it will be useful,
 \* but WITHOUT ANY WARRANTY; without even the implied warranty of
 \* MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the GNU
 \* Lesser General Public License for more details.
 \*
 \* You should have received a copy of the GNU Lesser General Public
 \* License along with this program. If not, please visit the Free
 \* Software Foundation website at http://www.gnu.org/licenses/.
 \*
 \* PHP version 5
 \* @copyright  2012
 \* @author     sales@groupdocs.com
 \* @license    GPL
 \*/
array\_insert($GLOBALS\['BE\_MOD'\]\['content'\], 3, array
(
	'groupdocs\_comparison' => array
	(
		'tables' => array('tl\_gdc'),
		'icon'   => 'system/modules/groupdocs\_comparison/html/groupdocs.gif'
	)
));
// Just add JS to Back End where using TinyMCE
$GLOBALS\['TL\_HOOKS'\]\['outputBackendTemplate'\]\[\] = array('ArticleAddGroupDocsComparison', 'javaScriptComparison');
class ArticleAddGroupDocsComparison{
    public function javaScriptComparison($strContent, $strTemplate)
    {
        if ($strTemplate == 'be\_main')
        {
            if($\_GET\['do'\]=='article' && $\_GET\['act'\]=='edit') {
?>
                <script language="JavaScript" >
                        //build GroupDocs Button just above Text Editor
                    setTimeout(function(){
                        place\_for\_button = document.getElementById('pal\_text\_legend');
                        legend = place\_for\_button.getElementsByTagName('legend')\[0\];
                        button=document.createElement('input');
                        button.type = 'button';
                        button.id = 'groupdocsc';
                        button.value = 'Embed GroupDocs Comparison';
                        button.onclick = function(){ window.open('system/modules/groupdocs\_comparison/html/form.php', 'GroupDocs Comparison', 'width=450,height=260,resizable=no,scrollbars=no')};
                        insertAfter(legend, button);
                    },500);

                    function insertAfter(referenceNode, newNode) {
                        referenceNode.parentNode.insertBefore(newNode, referenceNode.nextSibling);
                    }
                </script>
<?php
            }
        }
    }
}
?>
```

This code has mostly remained the same, but there are changes to the onClick action which now opens a pop-up with form. Also, in our plugin I've added two new files: **form.php** and **edit.php**. These files must be created in the **html** folder in the Viewer plugin's root folder.

### .htaccessNow lets create the missing files. First, create the **.htaccess** file in the **html** folder. The content of the **.htaccess** file:

```
order deny,allow
allow from all
```

### form.phpNow create the **form.php** file. This file generates a form and sends an Ajax request to the **edit.php** file. The Ajax request sends the user-entered data to **edit.php** for proccessing and returns user info. For example, we get the client ID and the user's Private key. We choose this data because these two parameters are used for all other methods such as Upload, GetFileList etc. So lets write the form. Here is code of the **form.php** file:

```
<!DOCTYPE html>
<html>
    <head>
        <title></title>
        <meta http-equiv="Content-Type" content="text/html; charset=UTF-8">
    </head>
    <body>
        <div>

            <h2><a href="http://groupdocs.com/">GroupDocs Viewer</a></h2>
            <form action="#" name="form">
                <label for='login'>GroupDocs Login</label>
                <br />
                <input type='text' name='login' value="" />
                <br />
                <label for='password'>GroupDocs Password</label>
                <br />
                <input type='password' name='password'  value="" />
                <br />
                <label for='id'>GroupDocs file GUID</label>
                <br />
                <input type='text' id='fileId'  value="" />
                <br />
                <input type="button" name="doRequest" value="Make request" onClick="getInfo();">
                <input type="button" name="cancel" value="Cancel" onClick="window.close();">
            </form>
            <br>
            <a target="blank" href="http://groupdocs.com/docs/display/gendoc/FAQs">See our FAQ</a> to learn how to use Comparison.
        </div>
    </body>
</html>
<script language="JavaScript" type="text/javascript">

    function getInfo()
    {
        form = document.forms.form;
        xhttp=new XMLHttpRequest();
        xhttp.onreadystatechange= function() {

            if (xhttp.readyState==4 && xhttp.status==200){
                result = eval( '('+xhttp.responseText+')' );
                guid = result\['guid'\];
                pkey = result\['pkey'\];
                fileId = result\['fileId'\];
                if (guid != null && pkey != null && fileId != null) {
                    var result = '<iframe src="http://apps.groupdocs.com/document-viewer/embed/'+ fileId + '" frameborder="0" width="500" height="650"></iframe> User ID = ' + guid + " User private Key = " + pkey;
                    var tinyMceContent = window.opener.tinyMCE.activeEditor.getContent();
                                // set content

                    window.opener.tinyMCE.activeEditor.setContent(tinyMceContent + result);
                } else if (error != "") {
                    var tinyMceContent = window.opener.tinyMCE.activeEditor.getContent();
                                // set content

                    window.opener.tinyMCE.activeEditor.setContent(tinyMceContent + error);
                }
                window.close();
            }
        }

        xhttp.open('POST','edit.php',true);
        xhttp.setRequestHeader('Content-Type','application/x-www-form-urlencoded');
        var str='login=' + form.login.value + '&password=' + form.password.value + '&guid=' + form.fileId.value;
        xhttp.send(str);
    }
</script>
```

As you can see, this file contains simple HTML and JavaScript. Let's take a look at the JavaScript. We have simple code which get entered to the form data by _document.forms.form_ where **form** is the name of the form. Then we made an Ajax request to the **edit.php** by POST. If the request has the status 200 we can, after processing, get data such as user ID and private key. In the response from the Ajax request we have a json string that we must convert to an object to access the data. To convert from a json string to the object, used the eval() method.  Then, after we have all the data, we can check whether it is OK. If it is, add an iframe with the entered file GUID to the active editor and put the user data there. I will not explain how to work with Ajax. If you need more information, there are a lot of docs and info in the web on this topic.

### edit.phpLets continue with **edit.php** file. Here is code of **edit.php**:

```
<?php

    $data = $\_POST;
    $login = $\_POST\['login'\];
    $password = $\_POST\['password'\];
    $fileId = $\_POST\['guid'\];
    if(!empty($login) && !empty($password)) {
        $fileId = strip\_tags(stripcslashes(trim($fileId)));
        include\_once('/../src/APIClient.php');
        include\_once('/../src/SharedAPI.php');
        include\_once('/../src/GroupDocsRequestSigner.php');

       //Create signer object
        $signer = new GroupDocsRequestSigner("123");
        //Create apiClient object
        $apiClient = new APIClient($signer);
        //Creaet Shared object
        $shared = new SharedApi($apiClient);
        //Set empty variable for result
        //Login and get user data
        $userData =  $shared->LoginUser($login, $password);
        //Check status
        if ($userData->status == "Ok") {
            //If status Ok get all user data
            $key = $userData->result->user->pkey;
            $guid = $userData->result->user->guid;
        } else {
            $error = $userData->error\_message;
        }
    } else {
        $error = "Please enter all parameters";
    }
    $result = array("pkey" => $key, "guid" => $guid, "error" => $error, "fileId" => $fileId);
    echo json\_encode($result);

?>
```

This file is most important. Here we include the GroupDocs SDK and use the Login method. Including the SDK is done as usual for PHP: _include\_once('/../src/APIClient.php');_ We must back up a level by using "/../" and then take a path to the SDK files. How to use the Login method you can find [here](https://blog.groupdocs.com/how-to-use-new-login-method-in-plugins-and-services). Let's understand how to return a json string to the pop-up. This magic is in this code:

```
 $result = array("pkey" => $key, "guid" => $guid, "error" => $error, "fileId" => $fileId);
 echo json\_encode($result);
```

The first line generates an array with all the data we want to return. The second string returns this array encoded in a json string.

## The plugin in actionLastly, here's a screenshots of the plugin in action. \[caption id="attachment\_2662" align="alignnone" width="600" caption="Form"\][![Form](https://blog.groupdocs.com/wp-content/uploads/sites/4/2013/06/form2.png "Form")](https://blog.groupdocs.com/wp-content/uploads/sites/4/2013/06/form2.png)\[/caption\]   \[caption id="attachment\_2663" align="alignnone" width="600" caption="Editor with added iframe and user data"\][![Editor with added iframe and user data](https://blog.groupdocs.com/wp-content/uploads/sites/4/2013/06/result1.png "Editor with added iframe and user data")](https://blog.groupdocs.com/wp-content/uploads/sites/4/2013/06/result1.png)\[/caption\]   The user data is replaced with example text for security reasons



