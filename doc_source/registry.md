# Using the CloudFormation Registry<a name="registry"></a>

The CloudFormation registry lists the resources, both private and public \(AWS\), that are available for use in your CloudFormation account\.

## Private and Public Resource Providers<a name="registry-public-private"></a>

*Private* resource providers are those resource providers that you have explicitly registered for use in your AWS account\. These may be resource providers you've created yourself, as well as ones shared with you\. You can use the [CloudFormation CLI](https://github.com/aws-cloudformation/aws-cloudformation-rpdk), an open\-source tool for resource management, to create private resource providers\. For more information, see the [CloudFormation Command Line Interface User Guide](https://docs.aws.amazon.com/cloudformation-cli/latest/userguide/what-is-cloudformation-cli.html)\.

**Note**  
Private resource providers implement custom logic that runs during resource create, read, update, list, and delete operations\. Because of this, using private resource providers in your CloudFormation stacks incurs charges to your account\. This is in additon to any charges incurred for the resources created\. For more informaiton, see [AWS CloudFormation Pricing](https://aws.amazon.com/cloudformation/pricing/)\.

*Public* resource providers are those provided by AWS to manage specific AWS service resources\. While the registry lists AWS resources implemented using the open\-source resource provider framework, all the resources included in the [Resource and Property Types Reference](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-template-resource-type-ref.html) are available for use in your CloudFormation account\.

## Registering Resource Providers in CloudFormation<a name="registry-register"></a>

To use private resource providers\-\-either ones you develop yourself, or providers shared with you\-\-you must first register them with CloudFormation, in the accounts and regions in which you want to use them\. Once you're registered a resource provider, it will appear in the CloudFormation registry for that account and region, and you can use it in your stack templates\.

You can register a resource provider using the [register\-type](https://docs.aws.amazon.com/cli/latest/reference/cloudformation/register-type.html) command of the AWS CLI, or using the `[submit](https://docs.aws.amazon.com/cloudformation-cli/latest/userguide/resource-type-cli-submit.html)` command of the CloudFormation CLI\. To register a resource provider using the CloudFormation CLI, see [Registering Resource Providers](https://docs.aws.amazon.com/cloudformation-cli/latest/userguide/resource-type-register.html) in the *CloudFormation CLI User Guide*\. 

**To Register a Resource Provider Using the AWS CLI**

1. Locate the S3 bucket that contains the resource provider package for the resource provider you want to register in your account\.

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

### Specifying Which Version of a Resource Provider to Use<a name="registry-set-version"></a>

Over time, you may register multiple versions of the same resource provider\. You can specify which version of the resource provider you want to use for CloudFormation operations\.

**To Specify Which Version of a Resource Provider to Use Using the AWS CLI**
+ Use the `[set\-type\-default\-version](https://docs.aws.amazon.com/cli/latest/reference/cloudformation/set-type-default-version.html)` command to specify which version of the resource provider to use for CloudFormation operations in your account\.

  For example, the following command sets the default version of the `My::Resource::Example` resource type to `00000003` for the current account\.

  ```
  aws cloudformation set-type-default-version --type RESOURCE --type-name My::Resource::Example --version-id 00000003
  ```

## Viewing Registered Resource Providers in CloudFormation<a name="registry-view"></a>

Once you've registered a resource provider in an account, you can view the details of that resource provider in the CloudFormation console\. Private resource providers are displayed in the **Private** section of the CloudFormation registry\.

**To View Registered Resource Providers in the CloudFormation Console**

1. In the [AWS CloudFormation console](https://console.aws.amazon.com/cloudformation), from the **CloudFormation** navigation pane, under **CloudFormation registry**, select **Resource types**\.

1. On the **Resource types** page, under **Resource types**, select **Public** or **Private**\.