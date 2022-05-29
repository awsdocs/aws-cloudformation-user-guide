# Using dynamic references to specify template values<a name="dynamic-references"></a>

*Dynamic references* provide a compact, powerful way for you to specify external values that are stored and managed in other services, such as the Systems Manager Parameter Store and AWS Secrets Manager, in your stack templates\. When you use a dynamic reference, CloudFormation retrieves the value of the specified reference when necessary during stack and change set operations\.

CloudFormation currently supports the following dynamic reference patterns:
+ [`ssm`](#dynamic-references-ssm), for plaintext values stored in AWS Systems Manager Parameter Store\.
+ [`ssm-secure`](#dynamic-references-ssm-secure-strings), for secure strings stored in AWS Systems Manager Parameter Store\.
+ [`secretsmanager`](#dynamic-references-secretsmanager), for entire secrets or secret values stored in AWS Secrets Manager\.

## Considerations when using dynamic references<a name="dynamic-references-considerations"></a>

Below are considerations you should take into account when using dynamic references:

**Important**  
We strongly recommend against including dynamic references, or any sensitive data, in resource properties that are part of a resource's primary identifier\.  
When a dynamic reference parameter is included in a property that forms a primary resource identifier, CloudFormation may use the *actual plaintext value* in the primary resource identifier\. This resource ID may appear in any derived outputs or destinations\.  
To determine which resource properties comprise a resource type's primary identifier, refer to the [resource reference documentation](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-template-resource-type-ref.html) for that resource\. In the **Return values** section, the `Ref` function return value represents the resource properties that comprise the resource type's primary identifier\.
+ You can include up to 60 dynamic references in a stack template\.
+ For transforms, such as `AWS::Include` and `AWS::Serverless`, AWS CloudFormation doesn't resolve dynamic references before invoking any transforms\. Rather, AWS CloudFormation passes the literal string of the dynamic reference to the transform\. Dynamic references \(including those inserted into the processed template as the result of a transform\) are resolved when you execute the change set using the template\.
+ Dynamic references for secure values, such as `ssm-secure` and `secretsmanager`, aren't currently supported in [custom resources](template-custom-resources.md)\.

**Note**  
Do not create a dynamic reference that has a backslash \(\\\) as the final value\. AWS CloudFormation cannot resolve those references, which results in a resource failure\.

## Specifying dynamic references in stack templates<a name="dynamic-references-pattern"></a>

Dynamic references adhere to the following pattern:

`'{{resolve:service-name:reference-key}}'` or `'{{resolve:ssm:[a-zA-Z0-9_.\-/]+(:\d+)?}}'`\.

**service\-name**  
Specifies the service in which the value is stored and managed\.  
Required\.  
Currently, valid values include:  
+ `ssm`: Systems Manager Parameter Store plaintext parameter\.
+ `ssm-secure`: Systems Manager Parameter Store secure string parameter\.
**Note**  
Currently, SecureString parameters aren't supported by Systems Manager in the `cn-north-1` and `cn-northwest-1` regions\.

  For more information, see [AWS Systems Manager Parameter Store](https://docs.aws.amazon.com/systems-manager/latest/userguide/systems-manager-paramstore.html) in the *AWS Systems Manager User Guide*\.
+ `secretsmanager`: Secrets Manager secret\.

**reference\-key**  
The reference key\. Depending on the type of dynamic reference, the reference key may be comprised of multiple segments\.  
Required\.

## SSM parameters<a name="dynamic-references-ssm"></a>

Use the `ssm` dynamic reference to include values stored in the Systems Manager Parameter Store of type `String` or `StringList` in your templates\.

### Reference pattern<a name="dynamic-references-ssm-pattern"></a>

For SSM Parameters, the `reference-key` segment is composed of the parameter name and version number\. Use the following pattern:

`'{{resolve:ssm:parameter-name:version}}'`

Your reference must adhere to the following regular expression pattern for parameter\-name and version:

`'{{resolve:ssm:[a-zA-Z0-9_.-/]+:\\d+}}'`

**parameter\-name**  
The name of the parameter in the Systems Manager Parameter Store\. The parameter name is case\-sensitive\.  
Required\.

**version**  
An integer that specifies the version of the parameter to use\. If you don't specify the exact version, CloudFormation uses the latest version of the parameter whenever you create or update the stack\. For more information, see [Working with parameter versions](https://docs.aws.amazon.com/systems-manager/latest/userguide/sysman-paramstore-versions.html) in the *AWS Systems Manager User Guide*  
Optional\.

### Example<a name="dynamic-references-ssm-example"></a>

The following example uses an `ssm` dynamic reference to set the access control for an S3 bucket to a parameter value stored in Systems Manager Parameter Store\. As specified, CloudFormation will use version 2 of the `S3AccessControl` parameter for stack and change set operations\.

#### JSON<a name="dynamic-references-ssm-example.json"></a>

```
  "MyS3Bucket": {
    "Type": "AWS::S3::Bucket",
    "Properties": {
      "AccessControl": "{{resolve:ssm:S3AccessControl:2}}"
    }
  }
```

#### YAML<a name="dynamic-references-ssm-example.yaml"></a>

```
  MyS3Bucket:
    Type: 'AWS::S3::Bucket'
    Properties:
      AccessControl: '{{resolve:ssm:S3AccessControl:2}}'
```

To specify a parameter stored in the Systems Manager Parameter Store, you must have access to call `[GetParameters](https://docs.aws.amazon.com/systems-manager/latest/APIReference/API_GetParameter.html)` for the specified parameter\. For more information, see [Controlling access to Systems Manager parameters](https://docs.aws.amazon.com/systems-manager/latest/userguide/sysman-paramstore-access.html) in the *AWS Systems Manager User Guide*\.

Additional considerations to note when using the `ssm` dynamic reference pattern:
+ Currently, CloudFormation doesn't support cross\-account SSM parameter access\.
+ For custom resources, CloudFormation resolves `ssm` dynamic references prior to sending the request to the custom resource\. For more information, see [Custom resources](template-custom-resources.md)\.
+ CloudFormation doesn't support using parameter labels or public parameters in dynamic references\.

  A parameter label is a user\-defined alias to help you manage different versions of a parameter\. For more information, see [Labeling parameters](https://docs.aws.amazon.com/systems-manager/latest/userguide/sysman-paramstore-labels.html) in the *AWS Systems Manager User Guide*\.

  A public parameter is a parameter provided by an AWS service for use with that service, and stored in AWS Systems Manager Parameter Store\. For an example of public parameters, see [Retrieving the Amazon ECS\-optimized AMI metadata](https://docs.aws.amazon.com/AmazonECS/latest/developerguide/retrieve-ecs-optimized_AMI.html) in the *Amazon Elastic Container Service Developer Guide*\.
+ CloudFormation doesn't currently support drift detection on dynamic references\. For `ssm` dynamic references where you haven't specified the parameter version, we recommend that, if you update the parameter version in SSM, you also perform a stack update operation on any stacks that include the `ssm` dynamic reference, in order to fetch the latest parameter version\.
+ To verify which version of an the `ssm` dynamic reference will be used in a stack operation, [create a change set](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-changesets-create.html) for the stack operation\. Then [review the processed template](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-changesets-view.html) on the **Template** tab\.
+ SSM parameters without a version isn't supported in the [Parameters block](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/parameters-section-structure.html), use [SSM parameter types](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/parameters-section-structure.html#aws-ssm-parameter-types) instead\. If you do use SSM parameters, you must specify a version of the Systems Manager parameter for AWS CloudFormation to use\.

## SSM secure string parameters<a name="dynamic-references-ssm-secure-strings"></a>

Use the `ssm-secure` dynamic reference pattern to specify AWS Systems Manager `SecureString` type parameters in your templates\. For `ssm-secure` dynamic references, AWS CloudFormation never stores the actual parameter value\. AWS CloudFormation accesses the parameter value during create and update operations for stacks and change sets\. Currently, secure string parameters can only be used for [resource properties that support](#template-parameters-dynamic-patterns-resources) the `ssm-secure` dynamic reference pattern\.

A *secure string parameter* is any sensitive data that needs to be stored and referenced in a secure manner\. That is, data that you don't want users to alter or reference in clear text, such as passwords or license keys\. For more information on secure strings, see [Use secure string parameters](https://docs.aws.amazon.com/systems-manager/latest/userguide/sysman-paramstore-about.html#sysman-paramstore-securestring) in the *AWS Systems Manager User Guide*\.

Secure string parameters values aren't stored in CloudFormation, nor are they returned in any API call results\.

### Reference pattern<a name="dynamic-references-ssm-secure-pattern"></a>

For `ssm-secure` dynamic references, the `reference-key` segment is composed of the parameter name and version number\. Use the following pattern:

`'{{resolve:ssm-secure:parameter-name:version}}'`

Your reference must adhere to the following regular expression pattern for parameter\-name and version:

`'{{resolve:ssm-secure:[a-zA-Z0-9_.-/]+:\\d+}}'`

**parameter\-name**  
The name of the parameter in the Systems Manager Parameter Store\. The parameter name is case\-sensitive\.  
Required\.

**version**  
An integer that specifies the version of the parameter to use\. If you don't specify the exact version, AWS CloudFormation uses the latest version of the parameter whenever you create or update the stack\. For more information, see [Working with parameter versions](https://docs.aws.amazon.com/systems-manager/latest/userguide/sysman-paramstore-versions.html) in the *AWS Systems Manager User Guide*  
Optional\.

### Example<a name="dynamic-references-ssm-secure-example"></a>

The following example uses an `ssm-secure` dynamic reference to set the password for an IAM user to a secure string stored in Systems Manager Parameter Store\. As specified, CloudFormation will use version 10 of the `IAMUserPassword` parameter for stack and change set operations\.

#### JSON<a name="dynamic-references-ssm-secure-example.json"></a>

```
  "MyIAMUser": {
    "Type": "AWS::IAM::User",
    "Properties": {
      "UserName": "MyUserName",
      "LoginProfile": {
        "Password": "{{resolve:ssm-secure:IAMUserPassword:10}}"
      }
    }
  }
```

#### YAML<a name="dynamic-references-ssm-secure-example.yaml"></a>

```
  MyIAMUser:
    Type: AWS::IAM::User
    Properties:
      UserName: 'MyUserName'
      LoginProfile:
        Password: '{{resolve:ssm-secure:IAMUserPassword:10}}'
```

Additional considerations to note when using the `ssm-secure` dynamic reference pattern:
+ CloudFormation doesn't return the actual parameter value for secure strings in any API calls, but rather returns the literal dynamic reference\.
+ CloudFormation does store the literal dynamic reference, which contains the plain text parameter name of the secure string\.
+ For change sets, CloudFormation compares the literal dynamic reference string\. It doesn't resolve and compare the actual values of `ssm-secure` references\.
+ Dynamic references for secure values, such as `ssm-secure` and `secretsmanager`, aren't currently supported in [custom resources](template-custom-resources.md)\.
+ In cases where CloudFormation must rollback a stack update, that update rollback operation will fail if the previously specified version of a secure string parameter is no longer available\. In such cases, do one of the following:
  + Use `CONTINUE_UPDATE_ROLLBACK` to skip the resource\.
  + Recreate the secure string parameter in the Systems Manager Parameter Store, and update it until the parameter version reaches the version used in the template\. Then use `CONTINUE_UPDATE_ROLLBACK` without skipping the resource\.
+ Currently, AWS CloudFormation doesn't support cross\-account SSM parameter access\.
+ CloudFormation doesn't support using parameter labels or public parameters in dynamic references\.

  A parameter label is a user\-defined alias to help you manage different versions of a parameter\. For more information, see [Labeling parameters](https://docs.aws.amazon.com/systems-manager/latest/userguide/sysman-paramstore-labels.html) in the *AWS Systems Manager User Guide*\.

  A public parameter is a parameter provided by an AWS service for use with that service, and stored in AWS Systems Manager Parameter Store\. For an example of public parameters, see [Retrieving the Amazon ECS\-optimized AMI metadata](https://docs.aws.amazon.com/AmazonECS/latest/developerguide/retrieve-ecs-optimized_AMI.html) in the *Amazon Elastic Container Service Developer Guide*\.

### Resources that support dynamic parameter patterns for secure strings<a name="template-parameters-dynamic-patterns-resources"></a>

Resources that support the `ssm-secure` dynamic reference pattern currently include:


| Resource | Property type | Properties | 
| --- | --- | --- | 
| [AWS::DirectoryService::MicrosoftAD](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-directoryservice-microsoftad.html) |  | `Password` | 
| [AWS::DirectoryService::SimpleAD](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-directoryservice-simplead.html) |  | `Password` | 
| [AWS::ElastiCache::ReplicationGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-elasticache-replicationgroup.html) |  | `AuthToken` | 
| [AWS::IAM::User](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-iam-user.html) | [LoginProfile](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-iam-user-loginprofile.html) | `Password` | 
| [AWS::KinesisFirehose::DeliveryStream](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-kinesisfirehose-deliverystream.html) | [RedshiftDestinationConfiguration](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-kinesisfirehose-deliverystream-redshiftdestinationconfiguration.html) | `Password` | 
| [AWS::OpsWorks::App](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-opsworks-app.html) | [Source](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-opsworks-stack-source-1.html) | `Password` | 
| [AWS::OpsWorks::Stack](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-opsworks-stack.html) | [CustomCookbooksSource](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-opsworks-stack-source.html) | `Password` | 
| [AWS::OpsWorks::Stack](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-opsworks-stack.html) | [RdsDbInstances](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-opsworks-stack-rdsdbinstance.html) | `DbPassword` | 
| [AWS::RDS::DBCluster](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-rds-dbcluster.html) |  | `MasterUserPassword` | 
| [AWS::RDS::DBInstance](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-rds-database-instance.html) |  | `MasterUserPassword`  | 
| [AWS::Redshift::Cluster](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-redshift-cluster.html) |  | `MasterUserPassword` | 

## Secrets Manager secrets<a name="dynamic-references-secretsmanager"></a>

Use the `secretsmanager` dynamic reference to retrieve entire secrets or secret values that are stored in Secrets Manager for use in your templates\. *Secrets* can be database credentials, passwords, third\-party API keys, or arbitrary text\. Using Secrets Manager, you can store and control access to these secrets centrally, so that you can replace hardcoded credentials in your code \(including passwords\), with an API call to Secrets Manager to retrieve the secret programmatically\. For more information, see [What is AWS Secrets Manager?](https://docs.aws.amazon.com/secretsmanager/latest/userguide/intro.html) in the *AWS Secrets Manager User Guide*\.

### Important considerations when using dynamic references for Secrets Manager secrets<a name="dynamic-references-secretsmanager-considerations"></a>

You should take the following important security considerations into account when using dynamic references to specify Secrets Manager secrets in your stack templates:
+ The `secretsmanager` dynamic reference can be used in all resource properties\. Using the `secretsmanager` dynamic reference indicates that neither Secrets Manager nor CloudFormation logs should persist any resolved secret value\. However, the secret value may show up in the service whose resource it's being used in\. Review your usage to avoid leaking secret data\.
+ Updating a secret in Secrets Manager doesn't automatically update the secret in CloudFormation\. In order for CloudFormation to update a `secretsmanager` dynamic reference, you must perform a stack update that updates the resource containing the dynamic reference, either by updating the resource property that contains the `secretsmanager` dynamic reference, or updating another of the resource's properties\.

  For example, suppose in your template you specify the `MasterPassword` property of an `[AWS::RDS::DBInstance](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-rds-database-instance.html)` resource to be a `secretsmanager` dynamic reference, and then create a stack from the template\. You later update that secret's value in Secrets Manager, but don't update the `AWS::RDS::DBInstance` resource in your template\. In this case, even if you perform a stack update, the secret value in the `MasterPassword` property isn't updated, and remains the previous secret value\.

  Also, consider using Secrets Manager to automatically rotate the secret for a secured service or database\. For more information, see [Rotate AWS Secrets Manager secrets](https://docs.aws.amazon.com/secretsmanager/latest/userguide/rotating-secrets.html)\.
+ Dynamic references for secure values, such as `secretsmanager`, aren't currently supported in [custom resources](template-custom-resources.md)\.

### Permissions required<a name="dynamic-references-secretsmanager-permissions"></a>

To specify a secret stored in Secrets Manager, you must have access to call `[GetSecretValue](https://docs.aws.amazon.com/secretsmanager/latest/apireference/API_GetSecretValue.html)` for the secret\.

### Reference pattern<a name="dynamic-references-secretsmanager-pattern"></a>

For Secrets Manager secrets, the `reference-key` segment is composed of several segments, including the secret id, secret value key, version stage, and version id\. Use the following pattern:

`{{resolve:secretsmanager:secret-id:secret-string:json-key:version-stage:version-id}}`

**secret\-id**  
The name or ARN of the secret\.  
To access a secret in your AWS account, you need only specify the secret name\. To access a secret in a different AWS account, specify the complete ARN of the secret\.  
Required\.

**secret\-string**  
Currently, the only supported value is `SecretString`\. The default is `SecretString`\.

**json\-key**  
The key name of the key\-value pair whose value you want to retrieve\. If you don't specify a `json-key`, CloudFormation retrieves the entire secret text\.  
This segment may not include the colon character \( `:`\)\.

**version\-stage**  
The staging label of the version of the secret to use\. Secrets Manager uses staging labels to keep track of different versions during the rotation process\. If you use `version-stage` then don't specify `version-id`\. If you don't specify either `version-stage` or `version-id`, then the default is the `AWSCURRENT` version\.  
This segment may not include the colon character \( `:`\)\.

**version\-id**  
The unique identifier of the version of the secret to use\. If you specify `version-id`, then don't specify `version-stage`\. If you don't specify either `version-stage` or `version-id`, then the default is the `AWSCURRENT` version\.  
This segment may not include the colon character \( `:`\)\.

### Examples<a name="dynamic-references-secretsmanager-example"></a>

The following example uses the `secret-name` and `json-key` segments to retrieve the user name and password values stored in the MyRDSSecret secret\. By default, the secret version retrieved is the version with the version stage value of `AWSCURRENT`\.

#### JSON<a name="dynamic-references-secretsmanager-example.json"></a>

```
{
    "MyRDSInstance": {
        "Type": "AWS::RDS::DBInstance",
        "Properties": {
            "DBName": "MyRDSInstance",
            "AllocatedStorage": "20",
            "DBInstanceClass": "db.t2.micro",
            "Engine": "mysql",
            "MasterUsername": "{{resolve:secretsmanager:MyRDSSecret:SecretString:username}}",
            "MasterUserPassword": "{{resolve:secretsmanager:MyRDSSecret:SecretString:password}}"
        }
    }
}
```

#### YAML<a name="dynamic-references-secretsmanager-example.yaml"></a>

```
  MyRDSInstance:
    Type: 'AWS::RDS::DBInstance'
    Properties:
      DBName: MyRDSInstance
      AllocatedStorage: '20'
      DBInstanceClass: db.t2.micro
      Engine: mysql
      MasterUsername: '{{resolve:secretsmanager:MyRDSSecret:SecretString:username}}'
      MasterUserPassword: '{{resolve:secretsmanager:MyRDSSecret:SecretString:password}}'
```

Specifying the following segments would retrieve the `SecretString` for MySecret\.

```
  '{{resolve:secretsmanager:MySecret}}' or '{{resolve:secretsmanager:MySecret::::}}'
```

Specifying the following segments would retrieve the `password` value for MySecret\.

```
  '{{resolve:secretsmanager:MySecret:SecretString:password}}'
```

Specifying the following segments would retrieve the `SecretString` for MySecret that is in another AWS account\. You must specify the complete secret ARN to access secrets in another AWS account\.

```
  '{{resolve:secretsmanager:arn:aws:secretsmanager:us-west-2:123456789012:secret:MySecret-a1b2c3}}'
```

Specifying the following segments would retrieve the `password` value for MySecret that is in another AWS account\. You must specify the complete secret ARN to access secrets in another AWS account\.

```
  '{{resolve:secretsmanager:arn:aws:secretsmanager:us-west-2:123456789012:secret:MySecret-a1b2c3:SecretString:password}}'
```

Specifying the following segments would retrieve the `password` value for the `AWSPREVIOUS` version of MySecret\.

```
  '{{resolve:secretsmanager:MySecret:SecretString:password:AWSPREVIOUS}}'
```