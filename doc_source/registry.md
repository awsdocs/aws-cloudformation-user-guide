# Using the AWS CloudFormation registry<a name="registry"></a>

The CloudFormation registry lists the extensions, both private and public \(AWS\), that are available for use in your CloudFormation account\. An extension is an artifact, registered in the CloudFormation Registry, which augments the functionality of CloudFormation in a native manner\. Extensions can be written by Amazon, APN partners, Marketplace sellers, and the developer community\. Extensions include CloudFormation items such as resource types and modules\.

## Private and public extensions<a name="registry-public-private"></a>

*Private* extensions are those extensions that you have explicitly registered for use in your AWS account\. These may be extensions you've created yourself, as well as ones shared with you\. You can use the [CloudFormation CLI](https://github.com/aws-cloudformation/aws-cloudformation-rpdk), an open\-source tool for resource management, to create private extensions\. For more information, see the [CloudFormation Command Line Interface User Guide](https://docs.aws.amazon.com/cloudformation-cli/latest/userguide/what-is-cloudformation-cli.html)\.

**Note**  
Using private *resource* types, a specific kind of extension, in your CloudFormation stacks incurs charges to your account\. This is because private resource types implement custom logic that runs during resource create, read, update, list, and delete operations\. This is in addition to any charges incurred for the resources created\. For more information, see [AWS CloudFormation pricing](https://aws.amazon.com/cloudformation/pricing/)\.

*Public* extensions are those provided by AWS to manage specific AWS service resources\. 

## Registering extensions in CloudFormation<a name="registry-register"></a>

To use private extensions\-\-either ones you develop yourself, or types shared with you\-\-you must first register them with CloudFormation, in the accounts and regions in which you want to use them\. Once you're registered an extension, it will appear in the CloudFormation registry for that account and region, and you can use it in your stack templates\.

You can register an extension using the [register\-type](https://docs.aws.amazon.com/cli/latest/reference/cloudformation/register-type.html) command of the AWS CLI, or using the `[submit](https://docs.aws.amazon.com/cloudformation-cli/latest/userguide/resource-type-cli-submit.html)` command of the CloudFormation CLI\. To register an extension using the CloudFormation CLI, see [Registering extensions](https://docs.aws.amazon.com/cloudformation-cli/latest/userguide/resource-type-register.html) in the *CloudFormation CLI User Guide*\. 

### IAM permissions for registering a resource type<a name="registry-register-permissions"></a>

As part of registering a resource type, you specify an S3 bucket which contains the schema handler package\. This package contains the schema, event handlers, and associated files for the resource type you want to register\. The user registering the resource type must be able to access the the schema handler package in that S3 bucket\. That is, the user needs to have [GetObject](https://docs.aws.amazon.com/AmazonS3/latest/API/API_GetObject.html) permissions for the schema handler package\.

This is true whether you're either using the [register\-type](https://docs.aws.amazon.com/cli/latest/reference/cloudformation/register-type.html) command of the AWS CLI, or the `[submit](https://docs.aws.amazon.com/cloudformation-cli/latest/userguide/resource-type-cli-submit.html)` command of the CloudFormation CLI\.

For more information, see [Actions, Resources, and Condition Keys for Amazon S3](https://docs.aws.amazon.com/IAM/latest/UserGuide/list_amazons3.html) in the *AWS Identity and Access Management User Guide*\.

**To register a resource type using the AWS CLI**

1. Locate the S3 bucket that contains the resource type package for the resource provider you want to register in your account\.

1. Use the [register\-type](https://docs.aws.amazon.com/cli/latest/reference/cloudformation/register-type.html) command to register the resource provider in your account:

   `RegisterType` is an asynchronous action, and returns a registration token you can use to track the progress of your registration request\. 
**Note**  
If your resource type calls AWS APIs in any of its handlers, you must create an IAM execution role that includes the necessary permissions to call those AWS APIs, and provision that execution role in your account\. You can then specify this execution role using the `--execution-role-arn` parameter\. CloudFormation then assumes that execution role to provide your resource type with the appropriate credentials\.

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

### Specifying which version of an extension to use<a name="registry-set-version"></a>

Over time, you may register multiple versions of the same extension\. You can specify which version of the extension you want to use for CloudFormation operations\.

**To specify which version of an extension to use using the AWS CLI**
+ Use the `[set\-type\-default\-version](https://docs.aws.amazon.com/cli/latest/reference/cloudformation/set-type-default-version.html)` command to specify which version of the extension to use for CloudFormation operations in your account\.

  For example, the following command sets the default version of the `My::Resource::Example` resource type to `00000003` for the current account\.

  ```
  aws cloudformation set-type-default-version --type RESOURCE --type-name My::Resource::Example --version-id 00000003
  ```

## Viewing registered extensions in CloudFormation<a name="registry-view"></a>

Once you've registered an extension in an account, you can view the details of that extension in the CloudFormation console\. Private extensions are displayed in the **Private** section of the CloudFormation registry\.

**To view registered extensions in the CloudFormation console**

1. In the [AWS CloudFormation console](https://console.aws.amazon.com/cloudformation), from the **CloudFormation** navigation pane, under **CloudFormation registry**, select the appropriate extension\. For example, select **Resource types** or **Modules**\.

1. Select **Public** or **Private**\.

## Record resource types in AWS Config<a name="registry-config-record"></a>

You can specify that AWS Config automatically track your private resource types and record changes to those resources as *configuration items*\. This enables you to view configuration history for these private resource types, as well as write Config rules to verify configuration best practices\. 

To have AWS Config automatically track your private resource types:
+ Manage the resources through CloudFormation\. This includes performing all resource create, updated, and delete operations through CloudFormation\.
**Note**  
If you use an IAM role to perform your stack operations, that IAM role must have permission to call the following AWS Config actions:  
[PutResourceConfig](https://docs.aws.amazon.com/config/latest/APIReference/API_PutResourceConfig.html)
[DeleteResourceConfig](https://docs.aws.amazon.com/config/latest/APIReference/API_DeleteResourceConfig.html)
+ Configure AWS Config to record all resource types\. For more information, see [Record configurations for third\-party resources](https://docs.aws.amazon.com/config/latest/developerguide/customresources.html) in the *AWS Config Developer Guide*\.
**Note**  
Config does not support recording of private resources containing properties defined as both required *and* write\-only\.   
By design, resource properties defined as write\-only are not returned in the schema used to create the Config configuration item\. Because of this, including a property that is defined as both write\-only and required will cause the configuration item creation to fail, as a required property will not be not present\. To view the schema that will be used to create the configuration item, you can review the `schema` property of the [DescribeType](https://docs.aws.amazon.com/AWSCloudFormation/latest/APIReference/API_DescribeType.html) action\. 

For more information on configuration items, see [Configuration items](https://docs.aws.amazon.com/config/latest/developerguide/config-concepts.html#config-items) in the *AWS Config Developer Guide*\.

### Preventing sensitive properties being recorded in a configuration item<a name="registry-config-record-sensitive"></a>

Your resource type may contain properties that you consider sensitive information, such as passwords, secrets, or other sensitive data, that you don't want recorded as part of the configuration item\. To prevent a property from being recorded in the configuration item, you can include that property in the `writeOnlyproperties` list in your resource type schema\. Resource properties listed as `writeOnlyproperties` can be specified by the user, but will not be returned by a `read` or `list` request\.

For more information, see [Resource Provider Schema](https://docs.aws.amazon.com/cloudformation-cli/latest/userguide/resource-type-schema.html#schema-properties-writeonlyproperties) in the *CloudFormation Command Line Interface User Guide*\.