# Using the AWS CloudFormation registry<a name="registry"></a>

The CloudFormation registry lets you manage the extensions, both public and private, that are available for use in your CloudFormation account\.

## Public and private extensions<a name="registry-public-private"></a>
+ *Public* extensions are those publicly published in the registry for use by all CloudFormation users\. This includes all extensions published by Amazon, as well as third\-party extension publishers\. 

  There are two kinds of public extensions:
  + *Amazon public extensions*

    Extensions published by Amazon are always public, and activated by default, so you don't have to take any action before using them in your account\. In addition, Amazon controls the versioning of the extension, so you are always using the latest available version\.
  + *Third\-party public extensions*

    These are extensions made available for general use by publishers other than Amazon\. 

    To use a public extension, you must first activate it in your account and region\. When you activate a public third\-party extension, CloudFormation creates an entry in your account's extension registry for the activated extension as a private extension\. This allows you to customize the extension *as it is activated in your account* in the following ways:
    + You can specify an alias to use instead of the public third\-party extension name\. This can help avoid naming collisions between third\-party extensions\.
    + You can specify whether the extension is automatically updated when a new minor or patch version becomes available\.

    For more information, see [Using public extensions](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/registry.html#registry-public)\.

    You can publish your own third\-party extensions to make them available to general CloudFormation users\. For more information, see [Publishing extensions](https://docs.aws.amazon.com/cloudformation-cli/latest/userguide/publish.html) in the *CloudFormation Command Line Interface User Guide*\.
+ *Private* extensions are those extensions from third parties that you have explicitly activated for use in your AWS account\. 

  There are two kinds of private extensions:
  + *Activated private extensions*

    These are the local copies of third\-party extensions that you have activated for your account and region\. When you activate a third\-party public extension, CloudFormation creates a local copy of that extension in your account's registry\.
  + *Registered private extensions*

    You can also activate private extensions that are not listed in the public CloudFormation registry\. These may be extensions you've created yourself, or ones shared with you by your organization or other third party\. To use such a private extension in your account, you must first register it\. Registering the extension uploads a copy of it to the CloudFormation registry in your account and activates it\.

    For more information, see [Using private extensions](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/registry.html#registry-register)\.

    For information on developing private extensions of your own, see [Creating resource types](https://docs.aws.amazon.com/cloudformation-cli/latest/userguide/resource-types.html) in the *CloudFormation Command Line Interface User Guide*\.

**Note**  
Private extensions, and activated public extensions from third\-party publishers, may implement event handlers that runs during create, read, update, list, and delete operations\. Because of this, using these extensions in your CloudFormation stacks incurs charges to your account\. This is in addition to any charges incurred for the resources created\. For more information, see [AWS CloudFormation pricing](https://aws.amazon.com/cloudformation/pricing/)\.

## Managing extensions through the CloudFormation registry<a name="registry-view"></a>

Use the CloudFormation registry to manage the extensions in your account, including:
+ View the available and activated extensions\.
+ Register private extensions\.
+ Activate public extensions\.<a name="registry-view-procedure"></a>

**To view extensions in the CloudFormation console**

1. In the [AWS CloudFormation console](https://console.aws.amazon.com/cloudformation), from the **CloudFormation** navigation pane, under **CloudFormation registry**, select what extension category you want to view:
   + **Public extensions** displays the public extensions available in your account\.

     Use the **Filter** options to further select the extensions to view\.
   + **Activated extensions** displays the public and private extensions activated in your account\.

     Use the **Filter** drop\-down menu to further select the extensions to view:
     + **AWS** lists extensions published by Amazon\. Extensions published by Amazon are activated by default\.
     + **Third\-party** lists any public extensions from publishers other than Amazon that you have activated in this account\.
     + **Registered** lists any private extensions you have activated in this account\.
   + **Publisher** displays any public extensions that you have published using this account\. For more information, see [Publishing extensions](https://docs.aws.amazon.com/cloudformation-cli/latest/userguide/publish-extension.html) in the *CFN\-CLI User Guide for Extension Development*\.

1. Select the extension name to view extension details\.

## Record resource types in AWS Config<a name="registry-config-record"></a>

You can specify that AWS Config automatically track your private resource types and record changes to those resources as *configuration items*\. This enables you to view configuration history for these private resource types, as well as write AWS Config Rules rules to verify configuration best practices\.

To have AWS Config automatically track your private resource types:
+ Manage the resources through CloudFormation\. This includes performing all resource create, updated, and delete operations through CloudFormation\.
**Note**  
If you use an IAM role to perform your stack operations, that IAM role must have permission to call the following AWS Config actions:  
[PutResourceConfig](https://docs.aws.amazon.com/config/latest/APIReference/API_PutResourceConfig.html)
[DeleteResourceConfig](https://docs.aws.amazon.com/config/latest/APIReference/API_DeleteResourceConfig.html)
+ Configure AWS Config to record all resource types\. For more information, see [Record configurations for third\-party resources](https://docs.aws.amazon.com/config/latest/developerguide/customresources.html) in the *AWS Config Developer Guide*\.
**Note**  
AWS Config does not support recording of private resources containing properties defined as both required *and* write\-only\.  
By design, resource properties defined as write\-only are not returned in the schema used to create AWS Config configuration item\. Because of this, including a property that is defined as both write\-only and required will cause the configuration item creation to fail, as a required property will not be not present\. To view the schema that will be used to create the configuration item, you can review the `schema` property of the [DescribeType](https://docs.aws.amazon.com/AWSCloudFormation/latest/APIReference/API_DescribeType.html) action\. 

For more information on configuration items, see [Configuration items](https://docs.aws.amazon.com/config/latest/developerguide/config-concepts.html#config-items) in the *AWS Config Developer Guide*\.

### Preventing sensitive properties being recorded in a configuration item<a name="registry-config-record-sensitive"></a>

Your resource type may contain properties that you consider sensitive information, such as passwords, secrets, or other sensitive data, that you don't want recorded as part of the configuration item\. To prevent a property from being recorded in the configuration item, you can include that property in the `writeOnlyproperties` list in your resource type schema\. Resource properties listed as `writeOnlyproperties` can be specified by the user, but will not be returned by a `read` or `list` request\.

For more information, see [Resource Provider Schema](https://docs.aws.amazon.com/cloudformation-cli/latest/userguide/resource-type-schema.html#schema-properties-writeonlyproperties) in the *CloudFormation Command Line Interface User Guide*\.