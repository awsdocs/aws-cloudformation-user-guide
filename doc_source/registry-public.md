# Using public extensions in CloudFormation<a name="registry-public"></a>

Public extensions are CloudFormation extensions, such as resource types, that are made available through the CloudFormation registry for use in your templates\. Public extensions can be published in the CloudFormation registry by third\-party publishers and Amazon\.

**Note**  
As with private extensions, public extensions from third\-party publishers may implement event handlers that runs during resource create, read, update, list, and delete stack operations\. Because of this, using these extensions in your CloudFormation stacks may incur charges to your account\. This is in addition to any charges incurred for the resources created\. For more information, see [AWS CloudFormation pricing](https://aws.amazon.com/cloudformation/pricing/)\.

*Public* extensions are CloudFormation extensions, such as resource types or modules, that are publicly published in the registry for use by all CloudFormation users\. This includes all extensions published by Amazon\. Third parties can also publish public extensions\.

There are two kinds of public extensions:
+ *Amazon public extensions*

  Extensions published by Amazon are always public, and activated by default, so you don't have to take any action before using them in your account\. In addition, Amazon controls the versioning of the extension, so you are always using the latest available version\.
+ *Third\-party public extensions*

  These are extensions made available for general use by publishers other than Amazon\. To use a public extension, you must first activate it in your account and region\.

  You can publish your own third\-party extensions to make them available to general CloudFormation users\. For more information, see [Publishing extensions](https://docs.aws.amazon.com/cloudformation-cli/latest/userguide/publish.html) in the *CloudFormation Command Line Interface User Guide*\.

## Activating public extensions for use in your account<a name="registry-public-enable"></a>

In order to use a public third\-party extension in your template, you must first *activate* the extension for the account and region in which you want to use it\. Enabling an extension makes it usable in stack operations in the account and region in which it's activated\. When you activate a public third\-party extension, CloudFormation creates an entry in your account's extension registry for the activated extension as a private extension\. This allows you to customize the extension *as it is activated in your account* in the following ways:
+ Specify an alias to use instead of the public third\-party extension name\. This can help avoid naming collisions between third\-party extensions\.
+ Specify whether the extension is automatically updated when a new minor or patch version becomes available\.
+ Specify the execution role CloudFormation uses to activate the extension, in addition to configure logging for the extension\.

When you activate a public third\-party extension, you can also set any configuration properties the extension includes\. Configuration properties define how the extension is configured for a given account and region\. For more information, see [Configuring extensions at the account level](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/registry-register.html#registry-set-configuration)\.

### Setting CloudFormation to automatically use new versions of extensions<a name="registry-public-enable-auto"></a>

When you activate an extension, you can also specify whether or not you want CloudFormation to automatically update to using a new minor version whenever one is released by the extension publisher\. For example, suppose you have specified auto\-update for an extension, and the publisher releases a new minor version after you activated the extension\. The next time you perform a stack operation, such as creating or updating a stack, using a template that includes that extension, CloudFormation uses the new minor version\.

Updating to a new extension version, either automatically or manually, does not affect any extension instances already provisioned in stacks\.

This applies only to minor version updates\. CloudFormation treats major version updates of extensions as potentially containing breaking changes, and so requires you to manually update to a new major version of an extension\.

Public extensions published by Amazon are activated by default for all accounts and regions in which they are available, and always use the latest version available in each AWS Region\.

**Important**  
Be aware that, because you can control if and when an activated public extension gets updated to the latest version, you could end up with different versions of the same extension deployed in different accounts and regions\. This might potentially lead to unexpected results when using the same template, containing that extension, across those accounts and regions\.

### Specifying aliases to refer to extensions<a name="registry-public-enable-alias"></a>

You cannot activate more than one extension with a given name in a given account and region\. Because different publishers may offer public extensions with the same extension name, CloudFormation lets you specify an alias for any third\-party public extension you activate\.

If you specify an alias for the extension, CloudFormation treats the alias as the extension type name within the account and region\. You must use the alias to refer to the extension in your templates, API calls, and CloudFormation console\.

Extension aliases must be unique within a given account and region\. You can activate the same public resource multiple times in the same account and region, using different type name aliases\.

**Important**  
While extension aliases are only required to be unique in a given account and region, we strongly recommend that users *not* assign the same alias to different third\-party public extensions across accounts and regions\. Doing so could lead to unexpected results when using a template that contains the extension alias across multiple accounts or regions\.

### Specifying an execution role when activating extensions<a name="registry-public-enable-execution-role"></a>

When activating a resource, you can specify the IAM execution role for CloudFormation to assume when invoking that extension in your account and region\.

In order for CloudFormation to assume the execution role, the role must have a trust policy defined with CloudFormation\. For example:

```
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Effect": "Allow",
      "Principal": {
        "Service": "resources.cloudformation.amazonaws.com"
      },
      "Action": "sts:AssumeRole"
    }
  ]
}
```

For more information, see [Modifying a role trust policy](https://docs.aws.amazon.com/IAM/latest/UserGuide/roles-managingrole-editing-console.html#roles-managingrole_edit-trust-policy) in the *AWS Identity and Access Management User Guide*\.

**To activate a public extension for use in your account using the CloudFormation console**

1. In the [CloudFormation console](https://console.aws.amazon.com/cloudformation), from the **CloudFormation** navigation pane, under **CloudFormation registry**, select **Public extensions**\.

   The registry displays the public extensions available in your account\.

1. Use the **Filter** to select the extension type, and select **Third party**\. \(Extensions published by Amazon are activated by default\.\)

1. Select the extension, then select **Activate**\.
**Note**  
If multiple versions of an extension are available, you can use the **Version** menu to select the version of the extension you want to activate\. The default is the most current version\.

1. Use the options on the **Activate extension** page to customize how the extension is activated in this account\.
   + To activate the extension using an extension type alias:

     1. Select **Override default**

     1. Enter the extension type alias you want to use with this extension\. Make sure the alias follows the recommended format for the extension type\.

     For more information, see [Specifying aliases to refer to extensions](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/registry-public.html#registry-public-enable-alias)\.
   + If you are enabling a private resource, you can specify the IAM role for CloudFormation to assume when invoking the extension\. For more information, see [Specifying an execution role when activating extensions](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/registry-register.html#registry-public-enable-execution-role)\.
   + Under **Logging config**, specify logging configuration information for an extension, if desired\.

     Be aware that the **logRoleArn** and **logGroupName** key names are case\-sensitive\. For example:

     ```
     {
         "logRoleArn": "arn:aws:iam::account:role/rolename",
         "logGroupName": "log-group-name"
     }
     ```
   + Use the options under **Versioning** to specify whether CloudFormation automatically updates the extension in this account and region when a new minor version is published\. For more information, see [Setting CloudFormation to automatically use new versions of extensions](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/registry-public.html#registry-public-enable-auto)\.

1. Specify the configuration data, if necessary \(optional\)\.

   If the extension requires additional configuration at the account and region level, CloudFormation includes the **Configuration** section on the **Activate extension** page\. You have the option to specify the configuration data now, or after the extension has been activated\.
   + To specify the configuration data while enabling the extension:

     1. Select **Configure now**, and then select **Activate extension and continue**\.

        CloudFormation displays the **Configure extension** page\. To view the current configuration schema for the extension, make sure **View configuration schema** is activated\.

     1. In the **Configuration JSON** text box, enter a JSON string that represents the configuration schema you want to specify for this extension\.

     1. Select **Configure extension**\.
   + To specify the configuration data later: 
     + Select **Configure later**, and then select **Activate extension**\.

     To specify configuration data for an extension that is already activated, see [Configuring extensions at the account level](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/registry-register.html#registry-set-configuration)\.

   If the extension does not require configuration, you will not see the **Configuration** section\. Select **Activate extension**\.

   Once the extension is successfully activated, CloudFormation displays the details page for that extension\.

**To update an activated public extension in your account using the CloudFormation console**

After you've activated an extension in your account and region, you can update the following properties of that extension as it is activated, including:
+ The configuration schema\.
+ Whether to activate automatic version updates\.
+ For private registered extensions, the execution role to use\.
+ The logging configuration information\.

1. Use the CloudFormation registry to [find the extension](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/registry.html#registry-view-procedure)\.

1. From the **Actions** menu, select **Edit**, and then the appropriate editing option:
   + To update the configuration schema, see [To specify configuration properties for an extension in the CloudFormation console](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/registry-register.html#registry-set-configuration-procedure)
   + To activate or deactivate automatic updates:

     1. Select **Edit automatic updates**\.

     1. Select **On** or **Off**, and then select **Save**\.
   + To update the execution role:

     1. Select **Edit execution role**\.

     1. Specify the ARN of the IAM role you want CloudFormation to use when invoking this extension, and then select **Save**\.
   + To update the logging configuration:

     1. Select **Edit logging config**\.

     1. Edit the logging configuration JSON, and then select **Save**\.

**To deactivate a public extension in your account using the CloudFormation console**

1. Use the CloudFormation registry to [find the extension](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/registry.html#registry-view-procedure)\.

1. From the **Actions** menu, select **Deactivate**\.

1. Select **Deactivate**\.

**To activate a public extension for use in your account using the AWS CLI**
+ Use `activate-type` to activate the extension, and specify whether to auto\-update the extension whenever a new minor version of the extension is published\.

  The example below specifies the public ARN of a public extension to activate for this account\. In addition, it specifies that CloudFormation auto\-update the extension whenever a new minor version is published\. CloudFormation returns an Amazon Resource Number \(ARN\) of the activated extension, specific to this account and region\.

  ```
  1. Prompt >aws cloudformation activate-type --public-type-arn public_extension_ARN --auto-update-activated
  2. {
  3.     "Arn": "624af370-311a-11e8-b6b7-500cexample"
  4. }
  ```

**To manually update the version of a public extension using the AWS CLI**
+ Use `activate-type` to activate the extension again\. Use the `--version-update` parameter to specify whether to update the extension to the newest major version, newest minor version, or update whether the extension gets automatically updated\. For more information, see [ActivateType](https://docs.aws.amazon.com/AWSCloudFormation/latest/APIReference/API_ActivateType.html)\.