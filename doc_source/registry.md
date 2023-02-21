# Using the AWS CloudFormation registry<a name="registry"></a>

The CloudFormation registry lets you manage extensions, both public and private, such as resources, modules, and hooks that are available for use in your AWS account\. Currently, you can use the following extension types in the AWS registry: [resources types](https://docs.aws.amazon.com/cloudformation-cli/latest/userguide/resource-types.html), [modules](https://docs.aws.amazon.com/cloudformation-cli/latest/userguide/modules.html), and [hooks](https://docs.aws.amazon.com/cloudformation-cli/latest/userguide/hooks.html)\. The registry makes it easier to discover and provision extensions in your AWS CloudFormation templates in the same manner you use AWS\-provided resources\.

## Public and private extensions<a name="registry-public-private"></a>

Extension types are registered as either public or private\. Currently, the registry offers the following extension types:
+ *[Resource types](https://docs.aws.amazon.com/cloudformation-cli/latest/userguide/resource-types.html)* – model and provision custom logic as a resource, using stacks in CloudFormation\.
+ *[Modules](https://docs.aws.amazon.com/cloudformation-cli/latest/userguide/modules.html)* – package resource configurations for inclusion across stack templates, in a transparent, manageable, and repeatable way\.
+ *[Hooks](https://docs.aws.amazon.com/cloudformation-cli/latest/userguide/hooks.html)* – proactively inspect the configuration of your AWS resources before provisioning\.

### Public extensions types<a name="registry-public-extensions"></a>

*Public* extensions are those publicly published in the registry for use by all CloudFormation users\. This includes extensions published by AWS and third\-party extension publishers\.

There are two kinds of public extensions:
+ *AWS public extensions* – Extensions published by AWS are always public, and activated by default, so you don't have to take any action before using them in your account\. In addition, AWS controls the versioning of the extension, so you are always using the latest available version\.
+ *Third\-party public extensions* – These are extensions made available for general use by publishers other than AWS\.

For more information, see [Using public extensions](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/registry-public.html)\.

### Private extensions types<a name="registry-private-extensions"></a>

*Private* extensions are those extensions from third parties that you have explicitly activated for use in your AWS account\.

There are two kinds of private extensions:
+ *Activated private extensions* – Are the local copies of third\-party extensions that you have activated for your account and region\. When you activate a third\-party public extension, CloudFormation creates a local copy of that extension in your account's registry\.
+ *Registered private extensions* – Can also activate private extensions that aren't listed in the public CloudFormation registry\. These may be extensions you've created yourself, or ones shared with you by your organization or other third party\. To use such a private extension in your account, you must first register it\. Registering the extension uploads a copy of it to the CloudFormation registry in your account and activates it\.

For more information, see [Using private extensions](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/registry-private.html)\.

## Managing extensions through the CloudFormation registry<a name="registry-view"></a>

Use the CloudFormation registry to manage the extensions in your account, including:
+ Viewing the available and activated extensions\.
+ Registering private extensions\.
+ Activating public extensions\.

### To view extensions in the CloudFormation console<a name="registry-view-procedure"></a>

1. Sign in to the AWS Management Console and open the AWS CloudFormation console at [https://console\.aws\.amazon\.com/cloudformation](https://console.aws.amazon.com/cloudformation/)\.

1. From the **CloudFormation** navigation pane, under **Registry**, select what extension category you want to view:
   + **Public extensions** displays the public extensions available in your account\.

     1. Choose your extension type: **Resource types**, **Modules**, or **Hooks**\.

     1. Choose your Publisher: **AWS** or **Third party**\.

     1. Use the **Filter** options to further select the extensions to view\.
   + **Activated extensions** displays the public and private extensions activated in your account\.

     1. Choose your extension type: **Resource types**, **Modules**, or **Hooks**\.

     1. Use the **Filter** drop\-down menu to further select the extensions to view:
        + **AWS** – lists extensions published by AWS\. Extensions published by AWS are activated by default\.
        + **Third\-party** – lists any public extensions from publishers other than AWS that you have activated in this account\.
        + **Registered** – lists any private extensions you have activated in this account\.
   + **Publisher** displays any public extensions that you have published using this account\. For more information, see [Publishing extensions](https://docs.aws.amazon.com/cloudformation-cli/latest/userguide/publish-extension.html) in the *User Guide for Extension Development*\.

1. Search or select the extension name to view extension details\.

## Record resource types in AWS Config<a name="registry-config-record"></a>

You can specify that AWS Config automatically track your private resource types and record changes to those resources as *configuration items*\. This enables you to view configuration history for these private resource types, in addition to write AWS Config Rules rules to verify configuration best practices\. AWS Config is required for the hook extension\.

To have AWS Config automatically track your private resource types:
+ Manage the resources through CloudFormation\. This includes performing all resource create, updated, and delete operations through CloudFormation\.
**Note**  
If you use an IAM role to perform your stack operations, that IAM role must have permission to call the following AWS Config actions:  
[PutResourceConfig](https://docs.aws.amazon.com/config/latest/APIReference/API_PutResourceConfig.html)
[DeleteResourceConfig](https://docs.aws.amazon.com/config/latest/APIReference/API_DeleteResourceConfig.html)
+ Configure AWS Config to record all resource types\. For more information, see [Record configurations for third\-party resources](https://docs.aws.amazon.com/config/latest/developerguide/customresources.html) in the *AWS Config Developer Guide*\.
**Note**  
AWS Config doesn't support recording of private resources containing properties defined as both required *and* write\-only\.  
By design, resource properties defined as write\-only aren't returned in the schema used to create AWS Config configuration item\. Because of this, including a property that's defined as both write\-only and required will cause the configuration item creation to fail, as a required property will not be present\. To view the schema that will be used to create the configuration item, you can review the `schema` property of the [DescribeType](https://docs.aws.amazon.com/AWSCloudFormation/latest/APIReference/API_DescribeType.html) action\.

For more information about configuration items, see [Configuration items](https://docs.aws.amazon.com/config/latest/developerguide/config-concepts.html#config-items) in the *AWS Config Developer Guide*\.

### Preventing sensitive properties being recorded in a configuration item<a name="registry-config-record-sensitive"></a>

Your resource type may contain properties that you consider sensitive information, such as passwords, secrets, or other sensitive data, that you don't want recorded as part of the configuration item\. To prevent a property from being recorded in the configuration item, you can include that property in the `writeOnlyproperties` list in your resource type schema\. Resource properties listed as `writeOnlyproperties` can be specified by the user, but won't be returned by a `read` or `list` request\.

For more information, see [Resource Provider Schema](https://docs.aws.amazon.com/cloudformation-cli/latest/userguide/resource-type-schema.html#schema-properties-writeonlyproperties) in the *CloudFormation Command Line Interface User Guide*\.

## Confused deputy prevention<a name="cross-service-confused-deputy-prevention"></a>

The confused deputy problem is a security issue where an entity that doesn't have permission to perform an action can coerce a more\-privileged entity to perform the action\. In AWS, cross\-service impersonation can result in the confused deputy problem\. Cross\-service impersonation can occur when one service \(the *calling service*\) calls another service \(the *called service*\)\. The calling service can be manipulated to use its permissions to act on another customer's resources in a way it shouldn't otherwise have permission to access\. To prevent this, AWS provides tools that help you protect your data for all services with service principals that have been given access to resources in your account\.

We recommend using the [https://docs.aws.amazon.com/IAM/latest/UserGuide/reference_policies_condition-keys.html#condition-keys-sourcearn](https://docs.aws.amazon.com/IAM/latest/UserGuide/reference_policies_condition-keys.html#condition-keys-sourcearn) and [https://docs.aws.amazon.com/IAM/latest/UserGuide/reference_policies_condition-keys.html#condition-keys-sourceaccount](https://docs.aws.amazon.com/IAM/latest/UserGuide/reference_policies_condition-keys.html#condition-keys-sourceaccount) global condition context keys in resource policies to limit the permissions that AWS CloudFormation gives another service to the extension\. If the `aws:SourceArn` value doesn't contain the account ID, such as an Amazon S3 bucket Amazon Resource Name \(ARN\), you must use both global condition context keys to limit permissions\. If you use both global condition context keys and the `aws:SourceArn` value contains the account ID, the `aws:SourceAccount` value and the account in the `aws:SourceArn` value must use the same account ID when used in the same policy statement\. Use `aws:SourceArn` if you want only one resource to be associated with the cross\-service access\. Use `aws:SourceAccount` if you want to allow any resource in that account to be associated with the cross\-service use\.

The value of `aws:SourceArn` must use the extension's ARN\.

The most effective way to protect against the confused deputy problem is to use the `aws:SourceArn` global condition context key with the full ARN of the resource\. If you don't know the full ARN of the extension or if you are specifying multiple extensions, use the `aws:SourceArn` global context condition key with wildcards \(`*`\) for the unknown portions of the ARN\. For example, `arn:aws:cloudformation:*:123456789012:*`\.

**Note**  
For registry services, CloudFormation makes calls to AWS Security Token Service \(AWS STS\) to assume a role in your account\. This role is configured for `ExecutionRoleArn` in the [RegisterType](https://docs.aws.amazon.com/AWSCloudFormation/latest/APIReference/API_RegisterType.html) operation and `LogRoleArn` set in the [LoggingConfig](https://docs.aws.amazon.com/AWSCloudFormation/latest/APIReference/API_LoggingConfig.html) operation\.

The following example shows how you can use the `aws:SourceArn` and `aws:SourceAccount` global condition context keys in AWS CloudFormation to prevent the confused deputy problem\.

```
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Effect": "Allow",
      "Principal": {
        "Service": [
          "resources.cloudformation.amazonaws.com"
        ]
      },
      "Action": "sts:AssumeRole",
      "Condition": {
        "StringEquals": {
          "aws:SourceAccount": "123456789012"
        },
        "StringLike": {
          "aws:SourceArn": "arn:aws:cloudformation:us-east-1:123456789012:type/resource/Organization-Service-Resource/*"
        }
      }
    }
  ]
}
```