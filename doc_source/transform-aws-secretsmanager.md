# AWS::SecretsManager transform<a name="transform-aws-secretsmanager"></a>

Use the `AWS::SecretsManager` transform, which is a macro hosted by AWS CloudFormation, to specify a Lambda function to perform secrets rotation\. When [Creating a change set](using-cfn-updating-stacks-changesets-create.md) or [Updating stacks using change sets](using-cfn-updating-stacks-changesets.md), and the templates references `AWS::SecretsManager`, AWS CloudFormation generates a Lambda function to perform secrets rotation\. Use the `[HostedRotationLambda](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-secretsmanager-rotationschedule-hostedrotationlambda.html)` property type of the `[AWS::SecretsManager::RotationSchedule](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-secretsmanager-rotationschedule.html)` resource to specify the attributes of the desired Lambda function\. 

The Lambda function is included as a [nested stack](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-nested-stacks.html) \(that is, an [AWS::CloudFormation::Stack](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-stack.html) resource\) in the processed template\. This resource in turns links to the appropriate function template in the [AWS Secrets Manager Rotation Lambda Functions](https://github.com/aws-samples/aws-secrets-manager-rotation-lambdas) repository, based on the [RotationType](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-secretsmanager-rotationschedule-hostedrotationlambda.html#cfn-secretsmanager-rotationschedule-hostedrotationlambda-rotationtype) specified in the `[AWS::SecretsManager::RotationSchedule](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-secretsmanager-rotationschedule.html)` resource\.

## Usage<a name="aws-secretsmanager-usage"></a>

Use the `AWS::SecretsManager` transform at the top level of the template\. You cannot use `AWS::SecretsManager` as a transform embedded in any other template section\.

The value for the transform declaration must be a literal string\. You cannot use a parameter or function to specify a transform value\. 

### Syntax at the top level of a template<a name="aws-secretsmanager-syntax-top-level-overview"></a>

To include `AWS::SecretsManager` at the top level of a template, in the `Transform` section, use the following syntax\.

#### JSON<a name="aws-secretsmanager-syntax-top-level.json"></a>

```
1. {
2.   "Transform": "AWS::SecretsManager-2020-07-23",
3.     . . .
4. }
```

#### YAML<a name="aws-secretsmanager-syntax-top-level.yaml"></a>

```
1. Transform: AWS::SecretsManager-2020-07-23
```

## Parameters<a name="aws-secretsmanager-transform-parameters"></a>

The `AWS::SecretsManager` transform does not accept any parameters\. Instead, specify the properties of the secret rotation Lamdba function you want to create using the `[HostedRotationLambda](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-secretsmanager-rotationschedule-hostedrotationlambda.html)` property type of the `[AWS::SecretsManager::RotationSchedule](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-secretsmanager-rotationschedule.html)` resources in the stack template\.

## Remarks<a name="aws-secretsmanager-transform-remarks"></a>

For general considerations about using macros, see [Considerations when creating AWS CloudFormation macro definitions](template-macros.md#template-macros-considerations)

## Example<a name="aws-secretsmanager-transform-examples"></a>

The following partial template example shows how to use the `AWS::SecretsManager` transform to specify a Lambda function for secret rotation on a MySQL database for a single user, based on the properties specified in the `HostedRotationLambda` property type of the `AWS::SecretsManager::RotationSchedule` resource\.

For complete template examples illustrating secret rotations for RDS databases, Redshift clusters, and Document DB clusters, see the [Examples](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-secretsmanager-rotationschedule.html#aws-resource-secretsmanager-rotationschedule--examples) section of [AWS::SecretsManager::RotationSchedule](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-secretsmanager-rotationschedule.html)\.

### JSON<a name="aws-secretsmanager-example.json"></a>

```
 1. {
 2.         "AWSTemplateFormatVersion": "2010-09-09",
 3.         "Transform": "AWS::SecretsManager-2020-07-23",
 4.         "Resources": {
 5.             
 6.             . . . 
 7.             
 8.             "MySecretRotationSchedule": {
 9.                 "Type": "AWS::SecretsManager::RotationSchedule",
10.                 "DependsOn": "SecretRDSInstanceAttachment",
11.                 "Properties": {
12.                     "SecretId": {
13.                         "Ref": "MyRDSInstanceRotationSecret"
14.                     },
15.                     "HostedRotationLambda": {
16.                         "RotationType": "MySQLSingleUser",
17.                         "RotationLambdaName": "SecretsManagerRotation",
18.                         "VpcSecurityGroupIds": {
19.                             "Fn::GetAtt": [
20.                                 "TestVPC",
21.                                 "DefaultSecurityGroup"
22.                             ]
23.                         },
24.                         "VpcSubnetIds": {
25.                             "Fn::Join": [
26.                                 ",",
27.                                 [
28.                                     {
29.                                         "Ref": "TestSubnet01"
30.                                     },
31.                                     {
32.                                         "Ref": "TestSubnet02"
33.                                     }
34.                                 ]
35.                             ]
36.                         }
37.                     },
38.                     "RotationRules": {
39.                         "AutomaticallyAfterDays": 30
40.                     }
41.                 }
42.             }
43.         }
44.     }
```

### YAML<a name="aws-secretsmanager-example.yaml"></a>

```
 1.  AWSTemplateFormatVersion: 2010-09-09
 2.  Transform: AWS::SecretsManager-2020-07-23
 3.  Resources:
 4. 
 5.       . . . 
 6.            
 7.       MySecretRotationSchedule:
 8.         Type: AWS::SecretsManager::RotationSchedule
 9.         DependsOn: SecretRDSInstanceAttachment 
10.         Properties:
11.           SecretId: !Ref MyRDSInstanceRotationSecret
12.           HostedRotationLambda:
13.             RotationType: MySQLSingleUser
14.             RotationLambdaName: SecretsManagerRotation
15.             VpcSecurityGroupIds: !GetAtt TestVPC.DefaultSecurityGroup
16.             VpcSubnetIds:
17.               Fn::Join:
18.                 - ","
19.                 - - Ref: TestSubnet01
20.                   - Ref: TestSubnet02
21.           RotationRules:
22.             AutomaticallyAfterDays: 30
```