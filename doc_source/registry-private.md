# Using private extensions in CloudFormation<a name="registry-private"></a>

*Private* extensions are extensions that you have explicitly allowed for use in your AWS account\.

There are two kinds of private extensions:
+ *Activated private extensions* – Are the local copies of third\-party extensions that you have activated for your account and region\. When you activate a third\-party public extension, CloudFormation creates a local copy of that extension in your account's registry\.
+ *Registered private extensions* – Can also activate private extensions that aren't listed in the public CloudFormation registry\. These may be extensions you've created yourself, or ones shared with you by your organization or other third party\. To use such a private extension in your account, you must first register it\. Registering the extension uploads a copy of it to the CloudFormation registry in your account and activates it\.

Any use of private extensions in your account is analogous to using it in a sandbox environment\. This is because extensions are version\-controlled, and provisioning behavior is version\-specific, which means that private extensions behave the same as if they were made public\.

**Note**  
Private extensions, and activated public extensions from third\-party publishers, may implement event handlers that runs during create, read, update, list, and delete operations\. Because of this, using these extensions in your CloudFormation stacks incurs charges to your account\. This is in addition to any charges incurred for the resources created\. For more information, see [AWS CloudFormation pricing](https://aws.amazon.com/cloudformation/pricing/)\.

For information about developing private extensions of your own, see [CloudFormation Command Line Interface User Guide](https://docs.aws.amazon.com/cloudformation-cli/latest/userguide/what-is-cloudformation-cli.html)\.

## Registering private extensions<a name="registry-register-private"></a>

To use private extensions that aren't listed in the CloudFormation registry\-\-either ones you develop yourself, or ones that have been shared with you\-\-you must first *register* them with CloudFormation, in the accounts and regions in which you want to use them\. Registering the extension uploads a copy of it to the CloudFormation registry in your account, and activates it\. Once you're registered a private extension, it will appear in the CloudFormation registry for that account and region, and you can use it in your stack templates\.

You can register an extension using the [register\-type](https://docs.aws.amazon.com/cli/latest/reference/cloudformation/register-type.html) command of the AWS CLI, or using the `[submit](https://docs.aws.amazon.com/cloudformation-cli/latest/userguide/resource-type-cli-submit.html)` command of the CloudFormation CLI\.

To register a private extension using the CloudFormation CLI, see [Registering extensions](https://docs.aws.amazon.com/cloudformation-cli/latest/userguide/resource-type-register.html) in the *CloudFormation CLI User Guide*\.

### IAM permissions for registering a private extension<a name="registry-register-permissions"></a>

As part of registering a private extension, you specify an Amazon S3 bucket which contains the extension project package\. This package contains any source files necessary for the extension you want to register\. The user registering the extension must be able to access the project package in that Amazon S3 bucket\. That's, the user needs to have [GetObject](https://docs.aws.amazon.com/AmazonS3/latest/API/API_GetObject.html) permissions for the extension package\.

This is true whether you're either using the [register\-type](https://docs.aws.amazon.com/cli/latest/reference/cloudformation/register-type.html) command of the AWS CLI, or the `[submit](https://docs.aws.amazon.com/cloudformation-cli/latest/userguide/resource-type-cli-submit.html)` command of the CloudFormation CLI\.

For more information, see [Actions, Resources, and Condition Keys for Amazon S3](https://docs.aws.amazon.com/IAM/latest/UserGuide/list_amazons3.html) in the *AWS Identity and Access Management User Guide*\.

### Registering extensions<a name="registry-register-extension-types"></a>

Register your extension in the AWS CloudFormation registry so it's available for use\.

#### To register a hook using the AWS CLI<a name="registry-register-private-hook"></a>

Register your hook with CloudFormation, so it's available for use in the AWS CloudFormation registry\.

1. \(Optional\) Configure your default AWS Region name to `us-west-2`, by submitting the `[configure](https://docs.aws.amazon.com/cli/latest/reference/configure/)` operation\.

   ```
   aws configure
   AWS Access Key ID [None]: <Your Access Key ID>
   AWS Secret Access Key [None]: <Your Secret Key>
   Default region name [None]: us-west-2
   Default output format [None]: json
   ```

1. \(Optional\) The following command builds and packages your hook project without registering it\.

   ```
   $ cfn submit --dry-run
   ```

1. Register your hook by using the CloudFormation CLI `cfn submit`\.

   ```
   cfn submit --set-default
   ```

   The command returns the following command\.

   ```
   {‘ProgressStatus’: ‘COMPLETE’}
   ```

   *Results*: You've successfully registered your hook\.

#### To register a resource type using the AWS CLI<a name="registry-register-private-resource-type"></a>

Register your resource type with CloudFormation, so it's available for use in the AWS CloudFormation registry\.

1. Locate the Amazon S3 bucket that contains the project package for the private extension you want to register in your account\.

1. Use the [register\-type](https://docs.aws.amazon.com/cli/latest/reference/cloudformation/register-type.html) command to register the extension in your account:

   `RegisterType` is an asynchronous operation, and returns a registration token you can use to track the progress of your registration request\.
**Note**  
If your extension calls AWS APIs as part of its functionality, you must create an IAM execution role that includes the necessary permissions to call those AWS APIs, and provision that execution role in your account\. You can then specify this execution role using the `--execution-role-arn` parameter\. CloudFormation then assumes that execution role to provide your resource type with the appropriate credentials\.

   For example, the following command registers the `My::Resource::Example` resource type in the current AWS account:

   ```
   aws cloudformation register-type --type-name My::Resource::Example --schema-handler-package [s3 object path] --type RESOURCE                
   {
       "RegistrationToken": "f5525280-104e-4d35-bef5-8f1fexample"
   }
   ```

1. Optional: Use the registration token with the `[describe\-type\-registration](https://docs.aws.amazon.com/cli/latest/reference/cloudformation/describe-type-registration.html)` command to track the progress of your registration request\.

   When CloudFormation completes the registration request, it sets the progress status of the request to `COMPLETE`\.

   The following example uses the registration token returned by the `describe-type-registration` command above to return registration status information\.

   ```
   aws cloudformation describe-type-registration --registration-token f5525280-104e-4d35-bef5-8f1fexample
   {
       "ProgressStatus": "COMPLETE",
       "TypeArn": "arn:aws:cloudformation:us-east-1:012345678910:type/resource/My-Resource-Example",
       "Description": "Deployment is currently in DEPLOY_STAGE of status COMPLETED; ",
       "TypeVersionArn": "arn:aws:cloudformation:us-east-1:111122223333:type/resource/My-Resource-Example/00000001"
   }
   ```

## Configuring extensions at the account level<a name="registry-set-configuration"></a>

An extension can include configuration properties meant to apply to all instances of the extension for a given account and Region\. The extension author defines these in the extension's definition configuration\. If there are any required properties in the extension's configuration definition, you must specify those properties before you can use the extension in your account and Region\.

**Note**  
If your type configuration includes dynamic references to values stored in AWS Systems Manager or AWS Secrets Manager, any role used to provision the type \(for example, when creating or updating a stack\) must have the proper permissions to retrieve that value\. Specifically:  
If the type configuration contains a parameter stored in AWS Systems Manager Parameter Store, the user or role used to provision the type must have permissions to call [GetParameter](https://docs.aws.amazon.com/systems-manager/latest/APIReference/API_GetParameter.html)\.
If the type configuration contains a secret stored in AWS Secrets Manager, the user or role used to provision the type must have permissions to call [GetSecretValue](https://docs.aws.amazon.com/secretsmanager/latest/apireference/API_GetSecretValue.html)\. 
For more information on dynamic references, see [Using dynamic references to specify template values](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/dynamic-references.html)\.

For more information about how configuration definitions are defined when developing an extension, see [Defining the account\-level configuration of an extension](https://docs.aws.amazon.com/cloudformation-cli/latest/userguide/resource-type-model.html#resource-type-howto-configuration) in the *CloudFormation User Guide for Extension Development*\.

**To view the current configuration data for an extension in the CloudFormation console**

1. Use the CloudFormation registry to [find the extension](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/registry.html#registry-view)\.

1. Choose the extension to view the extension details\.

1. On the extension details page, choose the **Configuration** tab\.

1. Expand the **Configuration schema** tab to see the configuration schema defined for the extension\.

1. Expand the **Configuration** tab to see the current configuration that you have set for this extension\.

**To view the current configuration data for an extension in the AWS CLI**
+ Use the [describe\-type](cli/latest/reference/cloudformation/describe-type.html) command to return detailed information about the extension\. The `ConfigurationSchema` element of the output contains the current configuration definition of the extension in a given Region\.

  Alternatively, use the [https://docs.aws.amazon.com/cli/latest/reference/cloudformation/batch-describe-type-configurations.html](https://docs.aws.amazon.com/cli/latest/reference/cloudformation/batch-describe-type-configurations.html) command to return configuration data about multiple extensions\.

### To specify configuration properties for extension types<a name="registry-set-configuration-procedure"></a>

#### To specify configuration properties for an extension using the CloudFormation console<a name="registry-set-configuration-procedure-console"></a>

1. Use the CloudFormation registry to [find the extension](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/registry.html#registry-view-procedure) in your account's activated extensions\.

1. Select the extension to view the extension details\.

1. On the extension details page, from the **Configuration** tab, select **Edit configuration**\.

   Alternatively, from **Actions**, select **Edit**, and then select **Edit configuration**\.

   CloudFormation displays the **Configure extension** page\. Make sure that **View configuration schema** is toggled on to see the extension's current configuration definition schema\.

1. In the **Configuration JSON** text box, enter a JSON string that represents the configuration schema you want to set for this extension\. It must validate against the schema defined in **Configuration schema**\.

1. Select **Configure extension**\.

#### To specify configuration properties for an extension using the AWS CLI<a name="registry-set-configuration-procedure-cli"></a>
+ Use the `[set\-type\-configuration](https://docs.aws.amazon.com/cli/latest/reference/cloudformation/set-type-configuration.html)` command to specify the configuration to be used with the extension in your account and Region\.

  The JSON you pass for `--configuration` must validate against the extension's configuration definition schema\. The following is an example of a `[set\-type\-configuration](https://docs.aws.amazon.com/cli/latest/reference/cloudformation/set-type-configuration.html)` command that specifies the configuration\.

  ```
  aws cloudformation set-type-configuration \
      --region us-west-2 \
      --type RESOURCE \
      --type-name My::Resource::Example \
      --configuration-alias default \
      --configuration "{"CredentialKey": "testUserCredential"}"
  ```

## Specifying a version of a private extension to use using the AWS CLI<a name="registry-set-version"></a>

Over time, you may register multiple versions of the same extension\. You can specify which version of the extension you want to use for CloudFormation operations\.

### To specify a version of an extension<a name="registry-set-version-extension"></a>

Use the `[set\-type\-default\-version](https://docs.aws.amazon.com/cli/latest/reference/cloudformation/set-type-default-version.html)` command to specify which version of the extension to use for CloudFormation operations in your account\.

For example, the following command sets the default version of the `My::Resource::Example` resource type to `00000003` for the current account\.

```
aws cloudformation set-type-default-version \
  --type RESOURCE \
  --type-name My::Resource::Example \
  --version-id 00000003
```

## To specify the default hook version<a name="registry-set-version-hook-default"></a>

To specify the default version of your hook in your account, use the `[set\-type\-default\-version](https://docs.aws.amazon.com/cli/latest/reference/cloudformation/set-type-default-version.html)` command and specify the type, type name, and version ID\.

```
aws cloudformation set-type-default-version \
    --type HOOK \
    --type-name MyCompany::Testing::MyTestHook \
    --version-id 00000003
```