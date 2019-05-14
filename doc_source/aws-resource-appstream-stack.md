# AWS::AppStream::Stack<a name="aws-resource-appstream-stack"></a>

The `AWS::AppStream::Stack` resource creates a stack to start streaming applications to Amazon AppStream 2\.0 users\. A stack consists of an associated fleet, user access policies, and storage configurations\. 

## Syntax<a name="aws-resource-appstream-stack-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-appstream-stack-syntax.json"></a>

```
{
  "Type" : "AWS::AppStream::Stack",
  "Properties" : {
      "[ApplicationSettings](#cfn-appstream-stack-applicationsettings)" : [ApplicationSettings](aws-properties-appstream-stack-applicationsettings.md),
      "[AttributesToDelete](#cfn-appstream-stack-attributestodelete)" : [ String, ... ],
      "[DeleteStorageConnectors](#cfn-appstream-stack-deletestorageconnectors)" : Boolean,
      "[Description](#cfn-appstream-stack-description)" : String,
      "[DisplayName](#cfn-appstream-stack-displayname)" : String,
      "[FeedbackURL](#cfn-appstream-stack-feedbackurl)" : String,
      "[Name](#cfn-appstream-stack-name)" : String,
      "[RedirectURL](#cfn-appstream-stack-redirecturl)" : String,
      "[StorageConnectors](#cfn-appstream-stack-storageconnectors)" : [ [StorageConnector](aws-properties-appstream-stack-storageconnector.md), ... ],
      "[Tags](#cfn-appstream-stack-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[UserSettings](#cfn-appstream-stack-usersettings)" : [ [UserSetting](aws-properties-appstream-stack-usersetting.md), ... ]
    }
}
```

### YAML<a name="aws-resource-appstream-stack-syntax.yaml"></a>

```
Type: AWS::AppStream::Stack
Properties : 
﻿  [ApplicationSettings](#cfn-appstream-stack-applicationsettings) : 
    [ApplicationSettings](aws-properties-appstream-stack-applicationsettings.md)
﻿  [AttributesToDelete](#cfn-appstream-stack-attributestodelete) : 
    - String
﻿  [DeleteStorageConnectors](#cfn-appstream-stack-deletestorageconnectors) : Boolean
﻿  [Description](#cfn-appstream-stack-description) : String
﻿  [DisplayName](#cfn-appstream-stack-displayname) : String
﻿  [FeedbackURL](#cfn-appstream-stack-feedbackurl) : String
﻿  [Name](#cfn-appstream-stack-name) : String
﻿  [RedirectURL](#cfn-appstream-stack-redirecturl) : String
﻿  [StorageConnectors](#cfn-appstream-stack-storageconnectors) : 
    - [StorageConnector](aws-properties-appstream-stack-storageconnector.md)
﻿  [Tags](#cfn-appstream-stack-tags) : 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
﻿  [UserSettings](#cfn-appstream-stack-usersettings) : 
    - [UserSetting](aws-properties-appstream-stack-usersetting.md)
```

## Properties<a name="aws-resource-appstream-stack-properties"></a>

`ApplicationSettings`  <a name="cfn-appstream-stack-applicationsettings"></a>
The persistent application settings for users of the stack\. When these settings are enabled, changes that users make to applications and Windows settings are automatically saved after each session and applied to the next session\.   
*Required*: No  
*Type*: [ApplicationSettings](aws-properties-appstream-stack-applicationsettings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AttributesToDelete`  <a name="cfn-appstream-stack-attributestodelete"></a>
The stack attributes to delete\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DeleteStorageConnectors`  <a name="cfn-appstream-stack-deletestorageconnectors"></a>
 *This parameter has been deprecated\. *   
Deletes the storage connectors currently enabled for the stack\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Description`  <a name="cfn-appstream-stack-description"></a>
The description to display\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DisplayName`  <a name="cfn-appstream-stack-displayname"></a>
The stack name to display\.  
*Required*: No  
*Type*: String  
*Maximum*: `100`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FeedbackURL`  <a name="cfn-appstream-stack-feedbackurl"></a>
The URL that users are redirected to after they click the Send Feedback link\. If no URL is specified, no Send Feedback link is displayed\.  
*Required*: No  
*Type*: String  
*Maximum*: `1000`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-appstream-stack-name"></a>
The name of the stack\.  
*Required*: No  
*Type*: String  
*Pattern*: `^[a-zA-Z0-9][a-zA-Z0-9_.-]{0,100}$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`RedirectURL`  <a name="cfn-appstream-stack-redirecturl"></a>
The URL that users are redirected to after their streaming session ends\.  
*Required*: No  
*Type*: String  
*Maximum*: `1000`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StorageConnectors`  <a name="cfn-appstream-stack-storageconnectors"></a>
The storage connectors to enable\.  
*Required*: No  
*Type*: List of [StorageConnector](aws-properties-appstream-stack-storageconnector.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-appstream-stack-tags"></a>
An array of key\-value pairs\. For more information, see [Using Cost Allocation Tags](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html) in the *AWS Billing and Cost Management User Guide*\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`UserSettings`  <a name="cfn-appstream-stack-usersettings"></a>
The actions that are enabled or disabled for users during their streaming sessions\. By default, these actions are enabled\.   
*Required*: No  
*Type*: List of [UserSetting](aws-properties-appstream-stack-usersetting.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See Also<a name="aws-resource-appstream-stack--seealso"></a>
+  [CreateStack](https://docs.aws.amazon.com/appstream2/latest/APIReference/API_CreateStack.html) in the *Amazon AppStream 2\.0 API Reference* 