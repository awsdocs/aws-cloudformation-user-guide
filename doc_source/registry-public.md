# Using public extensions in CloudFormation<a name="registry-public"></a>

Public extensions are CloudFormation extensions, such as resource types, that are made available through the CloudFormation registry for use in your templates\. Public extensions can be published in the CloudFormation registry by third\-party publishers and AWS\.

*Public* extensions are CloudFormation extensions, such as resource types or modules, that are publicly published in the registry for use by all CloudFormation users\. This includes all extensions published by AWS\. Third parties can also publish public extensions\.

There are two kinds of public extensions:
+ *AWS public extensions* – Extensions published by AWS are always public, and activated by default, so you don't have to take any action before using them in your account\. In addition, AWS controls the versioning of the extension, so you are always using the latest available version\.
+ *Third\-party public extensions* – These are extensions made available for general use by publishers other than AWS\. To use a public extension, you must first activate it in your account and region\.

  You can publish your own third\-party extensions to make them available to general CloudFormation users\. For more information, see [Publishing extensions](https://docs.aws.amazon.com/cloudformation-cli/latest/userguide/publish.html) in the *CloudFormation Command Line Interface User Guide*\.

**Note**  
As with private extensions, public extensions from third\-party publishers may implement event handlers that runs during resource create, read, update, list, and delete stack operations\. Because of this, using these extensions in your CloudFormation stacks may incur charges to your account\. This is in addition to any charges incurred for the resources created\. For more information, see [AWS CloudFormation pricing](https://aws.amazon.com/cloudformation/pricing/)\.

## Activating public extensions for use in your AWS account<a name="registry-public-enable"></a>

In order to use a public third\-party extension in your template, you must first *activate* the extension for the account and region in which you want to use it\. Enabling an extension makes it usable in stack operations in the account and region in which it's activated\. When you activate a public third\-party extension, CloudFormation creates an entry in your account's extension registry for the activated extension as a private extension\. This allows you to customize the extension *as it is activated in your account* in the following ways:
+ Specify an alias to use rather than the public third\-party extension name\. This can help avoid naming collisions between third\-party extensions\.
+ Specify whether the extension is automatically updated when a new minor or patch version becomes available\.
+ Specify the execution role CloudFormation uses to activate the extension, in addition to configure logging for the extension\.

When you activate a public third\-party extension, you can also set any configuration properties the extension includes\. Configuration properties define how the extension is configured for a given account and region\. See the following for more information about configuration:
+ [Defining the account\-level configuration of an extension](https://docs.aws.amazon.com/cloudformation-cli/latest/userguide/resource-type-model.html#resource-type-howto-configuration)
+ [Hooks configuration schema](https://docs.aws.amazon.com/cloudformation-cli/latest/userguide/hooks-structure.html#hook-configuration-schema)

### Setting CloudFormation to automatically use new versions of extensions<a name="registry-public-enable-auto"></a>

When you activate an extension, you can also specify the extension type to use the latest minor version\. Your extension type updates the minor version, whenever the publisher releases a new version on your activated extension\.

For example, the next time you perform a stack operation, such as creating or updating a stack, using a template that includes that extension, CloudFormation uses the new minor version\.

Updating to a new extension version, either automatically or manually and doesn't affect any extension instances already provisioned in stacks\.

CloudFormation treats major version updates of extensions as potentially containing breaking changes, and so requires you to manually update to a new major version of an extension\.

Extensions published by AWS are activated by default for all accounts and regions in which they're available, and always use the latest version available in each AWS Region\.

**Important**  
Because you control if and when extensions gets updated to the latest version in your account, you could end up with different versions of the same extension deployed in different accounts and regions\.  
This might potentially lead to unexpected results when using the same template, containing that extension, across those accounts and regions\.

### Specifying aliases to refer to extensions<a name="registry-public-enable-alias"></a>

You can't activate more than one extension with a given name in a given account and Region\. Because different publishers may offer public extensions with the same extension name, CloudFormation lets you specify an alias for any third\-party public extension you activate\.

If you specify an alias for the extension, CloudFormation treats the alias as the extension type name within the account and region\. You must use the alias to refer to the extension in your templates, API calls, and CloudFormation console\.

Extension aliases must be unique within a given account and Region\. You can activate the same public resource multiple times in the same account and Region, using different type name aliases\.

**Important**  
While extension aliases are only required to be unique in a given account and region, we strongly suggest that users *not* assign the same alias to different third\-party public extensions across accounts and regions\. Doing so could lead to unexpected results when using a template that contains the extension alias across multiple accounts or regions\.

### Specifying an execution role when activating extensions<a name="registry-public-enable-execution-role"></a>

When activating a resource, you can specify the IAM execution role for CloudFormation to assume when invoking that extension in your account and region\.

In order for CloudFormation to assume the execution role, the role must have a trust policy defined with CloudFormation\. In addition, permission to perform an operation is granted by creating an IAM policy and attaching to the execution role\. The required permissions are defined in the handler section of the extension schema\.

The following is an example IAM Role trust policy for the resource type extension:

```
{
    "Version": "2012-10-17",
    "Statement":[
        {
            "Effect": "Allow",
            "Principal":{
                "Service": "resources.cloudformation.amazonaws.com"
            },
            "Action":"sts:AssumeRole",
            "Condition":{
                "StringEquals":{
                    "aws:SourceAccount":"123456789012"
                },
                "StringLike":{
                    "aws:SourceArn":"arn:aws:cloudformation:us-east-1:123456789012:type/resource/Organization-Service-Resource/*"
                }
            }
        }
    ]
}
```

The following is an example IAM Role trust policy for the hook extension:

```
{
    "Version":"2012-10-17",
    "Statement":[
        {
            "Effect":"Allow",
            "Principal": {
                "Service": [
                    "resources.cloudformation.amazonaws.com",
                    "hooks.cloudformation.amazonaws.com"
                ]
            },
            "Action":"sts:AssumeRole",
            "Condition":{
                "StringEquals":{
                    "aws:SourceAccount":"123456789012"
                },
                "StringLike":{
                     "aws:SourceArn":"arn:aws:cloudformation:us-east-1:123456789012:type/hook/Organization-Service-Hook/*"
                }
            }
        }
    ]
}
```

For more information, see [Modifying a role trust policy](https://docs.aws.amazon.com/IAM/latest/UserGuide/roles-managingrole-editing-console.html#roles-managingrole_edit-trust-policy) in the *AWS Identity and Access Management User Guide*\.

### To activate a public extension in the registry<a name="registry-public-activate-extension"></a>

Activate your extension in the AWS CloudFormation registry so it's available for use\.

#### To activate a public extension for use in your account using the CloudFormation console<a name="registry-public-activate-extension-console"></a>

1. Sign in to the AWS Management Console and open the AWS CloudFormation console at [https://console\.aws\.amazon\.com/cloudformation](https://console.aws.amazon.com/cloudformation/)\.

1. From the **CloudFormation** navigation pane, under **CloudFormation registry**, select **Public extensions**\.

1. Use the **Filter** to select the extension type, and select **Third party**\. \(Extensions published by AWS are activated by default\.\)

1. Select the extension, then select **Activate**\.
**Note**  
If multiple versions of an extension are available, you can use the **Version** menu to select the version of the extension you want to activate\. The default is the most current version\.

1. Use the options on the **Activate extension** page to customize how the extension is activated in this account\.
   + To activate the extension using an extension type alias:

     1. Select **Override default**

     1. Enter the extension type alias you want to use with this extension\. The alias must follow the recommended format for the extension type\.

     For more information, see [Specifying aliases to refer to extensions](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/registry-public.html#registry-public-enable-alias)\.
   + If you are enabling a private resource, you can specify the IAM role for CloudFormation to assume when invoking the extension\. For more information, see [Specifying an execution role when activating extensions](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/registry-private.html#registry-public-enable-execution-role)\.
   + Under **Logging config**, specify logging configuration information for an extension, if desired\. For example:

     ```
     {
         "logRoleArn": "arn:aws:iam::account:role/rolename",
         "logGroupName": "log-group-name"
     }
     ```

     Logging configuration information isn't required but it's recommended for debugging purposes\. To use logging configuration with hooks, add the same trust policy as the execution role specified, so that the log role can write logs to your log group\.

     **logRoleArn** and **logGroupName** key names are case\-sensitive\.
   + Under **Versioning** specify how you receive updates\.
     + **On** – Automatically updates to the latest minor version\. Major versions are updated manually\.
     + **Off** – Never automatically update to the latest version\. All versions are updated manually\.

     For more information, see [Setting CloudFormation to automatically use new versions of extensions](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/registry-public.html#registry-public-enable-auto)\.

1. Specify the configuration data\.
**Note**  
This step is required for hooks\. You must specify `ALL` for the `TargetStack` property\. This operation enables the hook’s properties that are defined in the [hook’s schema properties](https://docs.aws.amazon.com/cloudformation-cli/latest/userguide/hooks-structure.html#hook-configuration-schema) section\.

   If the extension requires additional configuration at the account and Region level, CloudFormation includes the **Configuration** section on the **Activate extension** page\. You have the option to specify the configuration data now, or after the extension has been activated\. If the extension doesn't require configuration, you won't see the **Configuration** section\.
   + To specify the configuration data while enabling the extension:

     1. Select **Configure now**, and then select **Activate extension**\.

        CloudFormation displays the **Configure extension** page\. To view the current configuration schema for the extension, make sure **View configuration schema** is activated\.

     1. In the **Configuration JSON** text box, enter a JSON string that represents the configuration schema you want to specify for this extension\.

     1. Select **Configure extension**\.
   + To specify the configuration data later:
     + Select **Configure later**, and then select **Activate extension**\.

     To specify configuration data for an extension that's already activated, visit the activated extension's details page\.

   Once the extension is successfully activated, CloudFormation displays the details page for that extension\.

#### To update an activated public extension in your account using the CloudFormation console<a name="registry-public-update-extension-console"></a>

Update your extension in the AWS CloudFormation registry so it's available for use\.

After you've activated an extension in your account and region, you can update the following properties of that extension as it's activated, including:
+ The configuration schema\.
+ Whether to activate automatic version updates\.
+ For private registered extensions, the execution role to use\.
+ The logging configuration information\.

1. Sign in to the AWS Management Console and open the AWS CloudFormation console at [https://console\.aws\.amazon\.com/cloudformation](https://console.aws.amazon.com/cloudformation/)\.

1. From the **CloudFormation** navigation pane, under **CloudFormation registry**, select **Public extensions**\.

1. From the **Actions** menu, select **Edit**, and then the appropriate editing option:
   + To update the configuration schema, see [To specify configuration properties for an extension in the CloudFormation console](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/registry-private.html#registry-set-configuration-procedure)
   + To activate or deactivate automatic updates:

     1. Select **Edit automatic updates**\.

     1. Select **On** or **Off**, and then select **Save**\.
   + To update the execution role:

     1. Select **Edit execution role**\.

     1. Specify the ARN of the IAM role you want CloudFormation to use when invoking this extension, and then select **Save**\.
   + To update the logging configuration:

     1. Select **Edit logging config**\.

     1. Edit the logging configuration JSON, and then select **Save**\.

#### To activate a public extension for use in your account using the AWS CLI<a name="registry-public-activate-extension-cli"></a>

Activate your extension in the AWS CloudFormation registry through the AWS CLI\.

##### To activate hooks<a name="registry-public-activate-extension-hooks"></a>

After you've developed and registered your hook, you can activate your hook in your AWS account by publishing it to the registry\.
+ To activate a hook in your account, use the `[SetTypeConfiguration](https://docs.aws.amazon.com/AWSCloudFormation/latest/APIReference/API_SetTypeConfiguration.html)` operation\. This operation enables the hook’s properties that are defined in the hook’s schema `properties` section\.
**Note**  
By enabling hooks in your account, you are authorizing a hook to use defined permissions from your AWS account\. CloudFormation removes non\-required permissions before passing your permissions to the hook\. CloudFormation recommends customers or hook users to review the hook permissions and be aware of what permissions the hooks are allowed to before enabling hooks in your account\.

  Specify the configuration data for your registered hook extension in the same account and AWS Region\.

  ```
  aws cloudformation --region us-west-2 set-type-configuration \
    --configuration "{"CloudFormationConfiguration":{"HookConfiguration":{"TargetStacks": "ALL", "FailureMode": "FAIL", "Properties":{}}}}" \
    --type-arn $HOOK_TYPE_ARN
  ```
**Important**  
To enable your hook to proactively inspect the configuration of your stack, you must set the `TargetStacks` to `ALL` in the `HookConfiguration` section\.

##### To activate resource types and modules<a name="registry-public-activate-extension-type"></a>

**To activate a public extension for use in your account using the AWS CLI**
+ Use `activate-type` to activate the extension, and specify whether to auto update the extension whenever a new minor version of the extension is published\.

  The example below specifies the public Amazon Resource Name \(ARN\) of a public extension to activate for this account\. In addition, it specifies that CloudFormation updates the extension whenever a new minor version is published\.

  ```
  aws cloudformation activate-type \
    --public-type-arn public_extension_ARN \
    --auto-update true
  ```

  This command returns an ARN of the activated extension, specific to this account and Region\.

  ```
  {
      "Arn": "624af370-311a-11e8-b6b7-500cexample"
  }
  ```

##### To update the version of a public extension using the AWS CLI<a name="registry-public-update-extension-type"></a>

Use [https://docs.aws.amazon.com/cli/latest/reference/cloudformation/activate-type.html](https://docs.aws.amazon.com/cli/latest/reference/cloudformation/activate-type.html) to activate the extension again\.

Use the `--version-bump` parameter to specify whether to update the extension to the newest `MAJOR` version, newest `MINOR` version\.

```
aws cloudformation activate-type \
    --region us-west-2 \
    --type RESOURCE \
    --type-name Example::Test::1234567890abcdef0 \
    --type-name-alias Example::Test::Alias \
    --version-bump MAJOR
```

### To deactivate public extensions in your account<a name="registry-public-deactivate-extension"></a>

The following sections show how to deactivate public extensions in your account\.

#### To deactivate a public extension in your account using the CloudFormation console<a name="registry-public-deactivate-extension-console"></a>

1. Use the CloudFormation registry to [find the extension](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/registry.html#registry-view)\.

1. From the **Actions** menu, select **Deactivate**\.

1. Select **Deactivate**\.

#### To deactivate a public extension in your account using the AWS CLI<a name="registry-public-deactivate-extension-cli"></a>

To deactivate a public extension in your account, specify the [https://docs.aws.amazon.com/cli/latest/reference/cloudformation/deactivate-type.html](https://docs.aws.amazon.com/cli/latest/reference/cloudformation/deactivate-type.html)\. The following is an example of an AWS CLI deactivate command\.

```
aws cloudformation deactivate-type \
    --region us-west-2 \
    --type MODULE \
    --type-name Example::Test::Type::MODULE
```

#### To deactivate a hook in your account using the AWS CLI<a name="registry-public-deactivate-extension-cli-hook"></a>

Deactivating a hook prevents the hook from running your AWS account\.

`TargetStacks` set to `NONE` turns the hook off in your account, so it doesn't apply to stack operations\.

Use the `[set\-type\-configuration](https://docs.aws.amazon.com/cli/latest/reference/cloudformation/set-type-configuration.html)` operation and specify `TargetStacks` as `NONE` to deactivate a hook\.

The following example specifies the AWS Region and the Amazon Resource Name \(ARN\) of the hook that's being deactivated\.

```
aws cloudformation set-type-configuration \
  --region us-west-2 \
  --configuration "{"CloudFormationConfiguration":{"HookConfiguration":{"TargetStacks": "NONE", "FailureMode": "FAIL", "Properties":{}}}}" \
  --type-arn HOOK_TYPE_ARN
```