---
title: 'How to Create GroupDocs Add-On for cloudControl'
date: Mon, 12 Aug 2013 08:36:18 +0000
draft: false
url: /?p=3487
author: 'Derek Hyland'
summary: ''
tags: ['API', 'cloud api', 'cloudControl', 'GroupDocs API', 'GroupDocs Cloud Api', 'zArchive']
---

[CloudControl](https://www.cloudcontrol.com/) is a cloud platform much like [Heroku](https://www.heroku.com/). Creating a cloudControl add-on is very similar to creating a Heroku add-on but there are some differences. This article explains those differences.

## IntroductionGroupDocs' add-on for cloudControl is a web tool that can be installed on any web application to provide GroupDocs functionality:

*   Create a new GroupDocs user with a free plan and get the user ID and private key for this user. This is done automatically when the add-on is installed.
*   The user can change the payment plan using the add-on's **change plan** function.
*   Access to any methods from the GroupDocs API using the client ID and private key (which you can get from the add-on). We created [this example](http://groupdocspython.cloudcontrolapp.com/) which shows how to use add-on and GroupDocs Python SDK for some basic actions.

## Requirements

*   Kensa tool
*   cloudControl tool
*   Python 2.7
*   cloudControl aplication

## Creating the Add-onThe process for creating a cloudControl add-on is the same as for [creating a Heroku add-on](https://devcenter.heroku.com/articles/building-a-heroku-add-on), but, as I said earlier, with a couple of differences. We will not go into how to create the add-on because Heroku has a lot of documentation for this and you decide how you build it. I will only show what exactly the differences are. Lets assume that we already have a cool Heroku add-on and we want to rebuild it for cloudControl:

1.  Install the [Kensa](https://github.com/heroku/kensa) and cloudControl tools. They help you manage add-on and cloudControl applications. Find out how to [install the cloudControl tool](https://www.cloudcontrol.com/dev-center/Quickstart).
2.  After installing the tools, change the **addon-manifest.json** file. This contains all the basics information for add-on installation, such as which environment variables will be created and from where to download and install add-on files. 
    *   Before you upload the edited **addon-manifest.json** file, set the environment variable ADDONS\_URL=[https://api.cloudcontrol.com:](https://api.cloudcontrol.com/doc/).
    *   Specify the production server. Heroku required you to specify the production server, and then constructed the URL used to provision your add-on by appending "/heroku/resources" to it. Now, provide a hash instead of a string and change "/heroku/resources" to "/cloudcontrol/resources".
    *   Add "sso\_salt":"PASSWORD" and "production": {"base\_url":"https://your.add-on.com/cloudcontrol/resources", "sso\_url":"https://your.add-on.com/cloudcontrol/resources"}.
3.  Change "heroku\_id" to "cloudcontrol\_id" in the add-on files.
4.  When the changes have been made, test the add-on with Kensa tests by running it in the console: kensa test provision and kensa deprovision test. \[caption id="attachment\_3488" align="alignnone" width="600" caption="Kensa tests"\]![Kensa tests](https://blog.groupdocs.com/wp-content/uploads/sites/4/2013/08/Kensa-tests.png "Kensa tests")\[/caption\]
5.  If the tests pass, push **addon-manifest.json** to cloudControl with kensa push -f addon-manifest.json. \[caption id="attachment\_3489" align="alignnone" width="600" caption="Kensa push"\] ![Kensa push](https://blog.groupdocs.com/wp-content/uploads/sites/4/2013/08/kensa_push.png "Kensa push")\[/caption\]
6.  Install the add-on to your cloudControl application: cctrlapp YOUR\_APP\_NAME addon.add YOUR\_ADDON\_NAME.PLANE

Now we have published a cloudControl add-on and installed it. So far, so good. How do we get the environment variables that the add-on creates? Let's find out.

## How to Get Environment VariablesIn Heroku, this is easy. For example, in Python we can do this with the line os.environ\_\['VARIABLE NAME'\]. If you try this in cloudControl, you get only a few basics Python properties and not your add-on variables. In cloudControl, all environment variables created by the add-on are written to the **json** file which we can get by usingCRED\_FILE. This is the name of a system property that contains the path to the JSON file with environment variables. To get our data, all we need is to read this JSON file and decode the JSON string. In Python, we can do this with this code:

```
credentialsFile = os.getenv('CRED\_FILE')
    credentials = open(credentialsFile)
    data = json.load(credentials)
    credentials.close()
    clientId = data\['GROUPDOCS'\]\['GROUPDOCS\_CID'\]
    privateKey = data\['GROUPDOCS'\]\['GROUPDOCS\_PKEY'\]
```

That's how we get the client ID and private key of the GroupDocs add-on user. And that's all. You now know what the difference is between Heroku and cloudControl add-ons.



