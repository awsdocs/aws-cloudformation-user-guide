# Using Dynamic References to Specify Template Values<a name="dynamic-references"></a>

*Dynamic references* provide a compact, powerful way for you to specify external values that are stored and managed in other services, such as the Systems Manager Parameter Store, in your stack templates\. When you use a dynamic reference, CloudFormation retrieves the value of the specified reference when necessary during stack and change set operations\. 

CloudFormation currently supports two dynamic reference patterns:
+ `ssm`, for plaintext values stored in AWS Systems Manager Parameter Store
+ `ssm-secure`, for secure strings stored in AWS Systems Manager Parameter Store

You can include up to 60 dynamic references in a stack template\.

## Specifying Dynamic References in Stack Templates<a name="dynamic-references-pattern"></a>

Dynamic references adhere to the following pattern:

`{{resolve:service-name:reference-key}}`

All segments of the pattern are required\.

**service\-name**: 

Specifies the service in which the value is stored and managed\. Currently, valid values include:
+ `ssm`: Systems Manager Parameter Store plaintext parameter\.
+ `ssm-secure`: Systems Manager Parameter Store secure string parameter\.
**Note**  
Currently, SecureString parameters are not supported by Systems Manager in the `cn-north-1` and `cn-northwest-1` regions\. 

  For more information, see [AWS Systems Manager Parameter Store](https://docs.aws.amazon.com/systems-manager/latest/userguide/systems-manager-paramstore.html) in the *AWS Systems Manager User Guide*\.

**reference\-key**: The reference key\.

For transforms, such as AWS::Include and AWS::Serverless, AWS CloudFormation does not resolve dynamic references prior to invoking any transforms\. Rather, AWS CloudFormation passes the literal string of the dynamic reference to the transform\. Dynamic references \(including those inserted into the processed template as the result of a transform\) are resolved when you execute the change set using the template\.

## Dynamic References Supported in CloudFormation<a name="dynamic-references-supported"></a>

The following dynamic reference patterns are supported for use in stack templates\.

### SSM Parameters<a name="dynamic-references-ssm"></a>

Use the `ssm` dynamic reference to include values stored in the Systems Manager Parameter Store of type `String` or `StringList` in your templates\. 

#### Reference Pattern<a name="dynamic-references-ssm-pattern"></a>

For SSM Parameters, the `reference-key` segment is composed of the parameter name and version number\. Use the following pattern:

`{{resolve:ssm:parameter-name:version}}`

Your reference must adhere to the following regular expression pattern for parameter\-name and version:

`'{{resolve:ssm:[a-zA-Z0-9_.-/]+:\\d+}}'`

The parameter name is case\-sensitive\.

The **version** segment is an integer that specifies the version of the parameter to use, and is required\. For more information, see [Working with Parameter Versions](https://docs.aws.amazon.com/systems-manager/latest/userguide/sysman-paramstore-versions.html) in the *AWS Systems Manager User Guide*

**Note**  
Specifying the exact version is required\. You cannot currently specify that AWS CloudFormation use the latest version of a parameter\.

#### Example<a name="dynamic-references-ssm-example"></a>

The following example uses an `ssm` dynamic reference to set the access control for an S3 bucket to a parameter value stored in Systems Manager Parameter Store\. As specified, CloudFormation will use version 2 of the `S3AccessControl` parameter for stack and change set operations\.

**Example JSON Syntax**  

```
  "MyS3Bucket": {
    "Type": "AWS::S3::Bucket",
    "Properties": {
      "AccessControl": "{{resolve:ssm:S3AccessControl:2}}""
    }
  }
```

**Example YAML Syntax**  

```
  MyS3Bucket:
    Type: 'AWS::S3::Bucket'
    Properties:
      AccessControl: '{{resolve:ssm:S3AccessControl:2}}'
```

To specify a parameter stored in the Systems Manager Parameter Store, you must have access to call `[GetParameters](https://docs.aws.amazon.com/systems-manager/latest/APIReference/API_GetParameter.html)` for the specified parameter\. For more information, see [Controlling Access to Systems Manager Parameters](https://docs.aws.amazon.com/systems-manager/latest/userguide/sysman-paramstore-access.html) in the *AWS Systems Manager User Guide*\.

Additional considerations to note when using the `ssm` dynamic reference pattern:
+ Currently, CloudFormation does not support cross\-account SSM parameter access\.
+ For custom resources, CloudFormation resolves `ssm` dynamic references prior to sending the request to the custom resource\. For more information, see [Custom Resources](template-custom-resources.md)\.
+ CloudFormation does not support using parameter labels or public parameters in dynamic references\. 

  A parameter label is a user\-defined alias to help you manage different versions of a parameter\. For more information, see [Labeling Parameters](https://docs.aws.amazon.com/systems-manager/latest/userguide/sysman-paramstore-labels.html) in the *AWS Systems Manager User Guide*\.

  A public parameter is a parameter provided by an AWS service for use with that service, and stored in AWS Systems Manager Parameter Store\. For an example of public parameters, see [Retrieving the Amazon ECS\-optimized AMI Metadata](https://docs.aws.amazon.com/AmazonECS/latest/developerguide/retrieve-ecs-optimized_AMI.html) in the *Amazon Elastic Container Service Developer Guide*\.

### SSM Secure String Parameters<a name="dynamic-references-ssm-secure-strings"></a>

Use the `ssm-secure` dynamic reference pattern to specify AWS Systems Manager SecureString type parameters in your templates\. For `ssm-secure` dynamic references, AWS CloudFormation never stores the actual parameter value\. AWS CloudFormation accesses the parameter value during create and update operations for stacks and change sets\. Currently, secure string parameters can only be used for [resource properties that support](#template-parameters-dynamic-patterns-resources) the `ssm-secure` dynamic reference pattern\. 

A *secure string parameter* is any sensitive data that needs to be stored and referenced in a secure manner\. That is, data that you don't want users to alter or reference in clear text, such as passwords or license keys\. For more information on secure strings, see [Use Secure String Parameters](https://docs.aws.amazon.com/systems-manager/latest/userguide/sysman-paramstore-about.html#sysman-paramstore-securestring) in the *AWS Systems Manager User Guide*\.

Secure string parameters values are not stored in CloudFormation, nor are they returned as part of in any API call results\. 

#### Reference Pattern<a name="dynamic-references-ssm-secure-pattern"></a>

For `ssm-secure` dynamic references, the `reference-key` segment is composed of the parameter name and version number\. Use the following pattern:

`{{resolve:ssm-secure:parameter-name:version}}`

Your reference must adhere to the following regular expression pattern for parameter\-name and version:

`'{{resolve:ssm-secure:[a-zA-Z0-9_.-/]+:\\d+}}'`

The parameter name is case\-sensitive\.

The **version** segment is an integer that specifies the version of the parameter to use, and is required\. For more information, see [Working with Parameter Versions](https://docs.aws.amazon.com/systems-manager/latest/userguide/sysman-paramstore-versions.html) in the *AWS Systems Manager User Guide*\.

**Note**  
Specifying the exact version is required\. You cannot currently specify that AWS CloudFormation use the latest version of a parameter\.

#### Example<a name="dynamic-references-ssm-secure-example"></a>

The following example uses an `ssm-secure` dynamic reference to set the password for an IAM user to a secure string stored in Systems Manager Parameter Store\. As specified, CloudFormation will use version 10 of the `IAMUserPassword` parameter for stack and change set operations\.

**Example JSON Syntax**  

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

**Example YAML Syntax**  

```
  MyIAMUser:
    Type: AWS::IAM::User
    Properties:
      UserName: 'MyUserName'
      LoginProfile:
        Password: '{{resolve:ssm-secure:IAMUserPassword:10}}'
```

Additional considerations to note when using the `ssm-secure` dynamic reference pattern:
+ CloudFormation does not return the actual parameter value for secure strings in any API calls, but rather returns the literal dynamic reference\. 
+ CloudFormation does store the literal dynamic reference, which contains the plaintext parameter name of the secure string\.
+ For change sets, CloudFormation compares the literal dynamic reference string\. It does not resolve and compare the actual values of `ssm-secure` references\. 
+ In cases where CloudFormation must rollback a stack update, that update rollback operation will fail if the previously\-specified version of a secure string parameter is no longer available\. in such cases, do one of the following: 
  + Use `CONTINUE_UPDATE_ROLLBACK` to skip the resource\. 
  + Recreate the secure string parameter in the Systems Manager Parameter Store, and update it until the parameter version reaches the version used in the template\. Then use `CONTINUE_UPDATE_ROLLBACK` without skipping the resource\. 
+ Currently, AWS CloudFormation does not support cross\-account SSM parameter access\.
+ CloudFormation does not support using parameter labels or public parameters in dynamic references\. 

  A parameter label is a user\-defined alias to help you manage different versions of a parameter\. For more information, see [Labeling Parameters](https://docs.aws.amazon.com/systems-manager/latest/userguide/sysman-paramstore-labels.html) in the *AWS Systems Manager User Guide*\.

  A public parameter is a parameter provided by an AWS service for use with that service, and stored in AWS Systems Manager Parameter Store\. For an example of public parameters, see [Retrieving the Amazon ECS\-optimized AMI Metadata](https://docs.aws.amazon.com/AmazonECS/latest/developerguide/retrieve-ecs-optimized_AMI.html) in the *Amazon Elastic Container Service Developer Guide*\.

#### Resources that Support Dynamic Parameter Patterns for Secure Strings<a name="template-parameters-dynamic-patterns-resources"></a>

Resources that support the `ssm-secure` dynamic reference pattern currently include:


| Resource | Property Type | Properties | 
| --- | --- | --- | 
| [AWS::DirectoryService::MicrosoftAD](aws-resource-directoryservice-microsoftad.md) |  | `Password` | 
| [AWS::DirectoryService::SimpleAD](aws-resource-directoryservice-simplead.md) |  | `Password` | 
| [AWS::ElastiCache::ReplicationGroup](aws-resource-elasticache-replicationgroup.md) |  | `AuthToken` | 
| [AWS::IAM::User](aws-properties-iam-user.md) | [LoginProfile](aws-properties-iam-user-loginprofile.md) | `Password` | 
| [AWS::KinesisFirehose::DeliveryStream](aws-resource-kinesisfirehose-deliverystream.md) | [RedshiftDestinationConfiguration](aws-properties-kinesisfirehose-deliverystream-redshiftdestinationconfiguration.md) | `Password` | 
| [AWS::OpsWorks::App](aws-resource-opsworks-app.md) | [AppSource](aws-properties-opsworks-stack-source.md) | `Password` | 
| [AWS::OpsWorks::Stack](aws-resource-opsworks-stack.md) | [CustomCookbooksSource](aws-properties-opsworks-stack-source.md) | `Password` | 
| [AWS::OpsWorks::Stack](aws-resource-opsworks-stack.md) | [RdsDbInstances](aws-properties-opsworks-stack-rdsdbinstance.md) | `DbPassword` | 
| [AWS::RDS::DBCluster](aws-resource-rds-dbcluster.md) |  | `MasterUserPassword` | 
| [AWS::RDS::DBInstance](aws-properties-rds-database-instance.md) |  | `MasterUserPassword`  | 
| [AWS::Redshift::Cluster](aws-resource-redshift-cluster.md) |  | `MasterUserPassword` | 