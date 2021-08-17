# Using private extensions in CloudFormation<a name="registry-register"></a>

*Private* extensions are those extensions from third parties that you have explicitly activated for use in your AWS account\. 

There are two kinds of private extensions:
+ *Activated private extensions*

  These are the local copies of third\-party extensions that you have activated for your account and region\. When you activate a third\-party public extension, CloudFormation creates a local copy of that extension in your account's registry\.
+ *Registered private extensions*

  You can also activate private extensions that are not listed in the public CloudFormation registry\. These may be extensions you've created yourself, or ones shared with you by your organization or other third party\. To use such a private extension in your account, you must first register it\. 

  For information on developing private extensions of your own, see [Creating resource types](https://docs.aws.amazon.com/cloudformation-cli/latest/userguide/resource-types.html) in the *CloudFormation Command Line Interface User Guide*\.

## Registering private extensions<a name="registry-register-private"></a>

To use private extensions that are not listed in the CloudFormation registry\-\-either ones you develop yourself, or ones that have been shared with you\-\-you must first *register* them with CloudFormation, in the accounts and regions in which you want to use them\. Registering the extension uploads a copy of it to the CloudFormation registry in your account, and activates it\. Once you're registered a private extension, it will appear in the CloudFormation registry for that account and region, and you can use it in your stack templates\.

You can register an extension using the [register\-type](https://docs.aws.amazon.com/cli/latest/reference/cloudformation/register-type.html) command of the AWS CLI, or using the `[submit](https://docs.aws.amazon.com/cloudformation-cli/latest/userguide/resource-type-cli-submit.html)` command of the CloudFormation CLI\. To register a private extension using the CloudFormation CLI, see [Registering extensions](https://docs.aws.amazon.com/cloudformation-cli/latest/userguide/resource-type-register.html) in the *CloudFormation CLI User Guide*\. 

### IAM permissions for registering a private extension<a name="registry-register-permissions"></a>

As part of registering a private extension, you specify an S3 bucket which contains the extension project package\. This package contains any source files necessary for the extension you want to register\. The user registering the extension must be able to access the project package in that S3 bucket\. That is, the user needs to have [GetObject](https://docs.aws.amazon.com/AmazonS3/latest/API/API_GetObject.html) permissions for the extension package\.

This is true whether you're either using the [register\-type](https://docs.aws.amazon.com/cli/latest/reference/cloudformation/register-type.html) command of the AWS CLI, or the `[submit](https://docs.aws.amazon.com/cloudformation-cli/latest/userguide/resource-type-cli-submit.html)` command of the CloudFormation CLI\.

For more information, see [Actions, Resources, and Condition Keys for Amazon S3](https://docs.aws.amazon.com/IAM/latest/UserGuide/list_amazons3.html) in the *AWS Identity and Access Management User Guide*\.

**To register a resource type using the AWS CLI**

1. Locate the S3 bucket that contains the project package for the private extension you want to register in your account\.

1. Use the [register\-type](https://docs.aws.amazon.com/cli/latest/reference/cloudformation/register-type.html) command to register the extension in your account:

   `RegisterType` is an asynchronous action, and returns a registration token you can use to track the progress of your registration request\. 
**Note**  
If your extension calls AWS APIs as part of its functionality, you must create an IAM execution role that includes the necessary permissions to call those AWS APIs, and provision that execution role in your account\. You can then specify this execution role using the `--execution-role-arn` parameter\. CloudFormation then assumes that execution role to provide your resource type with the appropriate credentials\.

   For example\. the following command registers the `My::Resource::Example` resource type in the current AWS account:

   ```
   aws cloudformation register-type --type-name My::Resource::Example --schema-handler-package [s3 object path] --type RESOURCE
   
                   
   {
       "RegistrationToken": "f5525280-104e-4d35-bef5-8f1fexample"
   }
   ```

1. Optional: Use the registration token with the `[describe\-type\-registration](https://docs.aws.amazon.com/cli/latest/reference/cloudformation/describe-type-registration.html)` command to track the progress of your registration request\.

   When CloudFormation completes the registration request, it sets the progress status of the request to `COMPLETE`\.

   The following example uses the registration token returned by the RegisterType command above to return registration status information\.

   ```
   aws cloudformation describe-type-registration --registration-token f5525280-104e-4d35-bef5-8f1fexample
   
   {
       "ProgressStatus": "COMPLETE",
       "TypeArn": "arn:aws:cloudformation:us-east-1:012345678910:type/resource/My-Resource-Example",
       "Description": "Deployment is currently in DEPLOY_STAGE of status COMPLETED; ",
       "TypeVersionArn": "arn:aws:cloudformation:us-east-1:012345678910:type/resource/My-Resource-Example/00000001"
   }
   ```

## Configuring extensions at the account level<a name="registry-set-configuration"></a>

An extension can include configuration properties meant to apply to all instances of the extension in a given account and region\. For example, if the extension needs to access a third\-party web service, the extension author might have included properties in the extension configuration definition where you can specify your credentials for that service\. When you set configuration properties, CloudFormation saves this information at the account and region level\. From then on, CloudFormation can access those configuration properties during operations involving any instances of that extension in your account and region\. This way, configuration properties are available to CloudFormation during all extension operations, and not just ones that explicitly involve a stack template\. For example, CloudFormation can access the configuration properties during `read` and `list` events, operations that don't explictly involve the stack template\.

If the configuration properties of an extension include any properties that are required, you must specify those properties before you can use the extension in your account and region\.

For more information about defining configuration data when developing an extension, see [Defining the account\-level configuration of an extension](https://docs.aws.amazon.com/cloudformation-cli/latest/userguide/resource-type-model.html#resource-type-howto-configuration) in the *CloudFormation CLI User Guide*\.<a name="registry-set-configuration-procedure"></a>

**To specify configuration properties for an extension in the CloudFormation console**

1. Use the CloudFormation registry to [find the extension](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/registry.html#registry-view-procedure)\.

1. From **Actions**, select **Edit**, and then select **Edit configuration**\.

   CloudFormation displays the **Configure extension** page\. To view the current configuration schema for the extension, make sure **View configuration schema** is activated\.

1. In the **Configuration JSON** text box, enter a JSON string that represents the configuration schema you want to specify for this extension\.

1. Select **Configure extension**\.

**To specify configuration properties for an extension using the AWS CLI**
+ Use the `[set\-type\-configuration](https://docs.aws.amazon.com/cli/latest/reference/cloudformation/set-type-configuration.html)` command to specify the configuration settings to be used with the extension in this account and region\. The JSON you pass to specify the configuration properties must validate against the schema defined in the typeConfiguration element of the extension's schema\. 

**To view the current configuration data for an extension in the CloudFormation console**

1. Use the CloudFormation registry to [find the extension](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/registry.html#registry-view-procedure)\.

1. Select the extension name to view extension details\.

1. On the extension details page, select the **Configuration** tab\.

**To view the current configuration data for an extension in the AWS CLI**
+ Use the [describe\-type](cli/latest/reference/cloudformation/describe-type.html) command to return detailed information about the extension\. The `ConfigurationSchema` element contains the current configuration properties of the extension in a given account and region\.

## Specifying which version of a private extension to use<a name="registry-set-version"></a>

Over time, you may register multiple versions of the same extension\. You can specify which version of the extension you want to use for CloudFormation operations\.

**To specify which version of an extension to use using the AWS CLI**
+ Use the `[set\-type\-default\-version](https://docs.aws.amazon.com/cli/latest/reference/cloudformation/set-type-default-version.html)` command to specify which version of the extension to use for CloudFormation operations in your account\.

  For example, the following command sets the default version of the `My::Resource::Example` resource type to `00000003` for the current account\.

  ```
  aws cloudformation set-type-default-version --type RESOURCE --type-name My::Resource::Example --version-id 00000003
  ```