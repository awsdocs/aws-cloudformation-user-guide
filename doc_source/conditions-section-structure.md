# Conditions<a name="conditions-section-structure"></a>

The optional [https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-condition.html](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-condition.html) section contains statements that define the circumstances under which entities are created or configured\. For example, you can create a condition and then associate it with a resource or output so that AWS CloudFormation only creates the resource or output if the condition is true\. Similarly, you can associate the condition with a property so that AWS CloudFormation only sets the property to a specific value if the condition is true\. If the condition is false, AWS CloudFormation sets the property to a different value that you specify\.

You might use conditions when you want to reuse a template that can create resources in different contexts, such as a test environment versus a production environment\. In your template, you can add an `EnvironmentType` input parameter, which accepts either **prod** or **test** as inputs\. For the production environment, you might include Amazon EC2 instances with certain capabilities; however, for the test environment, you want to use reduced capabilities to save money\. With conditions, you can define which resources are created and how they're configured for each environment type\.

Conditions are evaluated based on predefined pseudo parameters or input parameter values that you specify when you create or update a stack\. Within each condition, you can reference another condition, a parameter value, or a mapping\. After you define all your conditions, you can associate them with resources and resource properties in the `Resources` and `Outputs` sections of a template\.

At stack creation or stack update, AWS CloudFormation evaluates all the conditions in your template before creating any resources\. Resources that are associated with a true condition are created\. Resources that are associated with a false condition are ignored\. AWS CloudFormation also re\-evaluates these conditions at each stack update before updating any resources\. Resources that are still associated with a true condition are updated\. Resources that are now associated with a false condition are deleted\.

**Important**  
During a stack update, you cannot update conditions by themselves\. You can update conditions only when you include changes that add, modify, or delete resources\.

## How to use conditions overview<a name="conditions-section-structure-overview"></a>

Depending on the entity you want to conditionally create or configure, you must include statements in the following template sections:

`Parameters` section  
Define the inputs that you want your conditions to evaluate\. The conditions evaluate to true or false based on the values of these input parameters\. If you want your conditions to evaluate pseudo parameters, you don't need to define the pseudo parameters in this section; pseudo parameters are predefined by AWS CloudFormation\.

`Conditions` section  
Define conditions by using the intrinsic condition functions\. These conditions determine when AWS CloudFormation creates the associated resources\.

`Resources` and `Outputs` sections  
Associate conditions with the resources or outputs that you want to conditionally create\. AWS CloudFormation creates entities that are associated with a true condition and ignores entities that are associated with a false condition\. Use the `Condition` key and a condition's logical ID to associate it with a resource or output\. To conditionally specify a property, use the `Fn::If` function\. For more information, see [Condition functions](intrinsic-function-reference-conditions.md)\.

## Syntax<a name="conditions-section-structure-syntax"></a>

The `Conditions` section consists of the key name `Conditions`\. Each condition declaration includes a logical ID and intrinsic functions that are evaluated when you create or update a stack\. The following pseudo template outlines the `Conditions` section:

### JSON<a name="conditions-section-structure-syntax.json"></a>

```
"Conditions" : {

  "Logical ID" : {Intrinsic function}
}
```

### YAML<a name="conditions-section-structure-syntax.yaml"></a>

```
Conditions:
  Logical ID:
    Intrinsic function
```

#### Condition intrinsic functions<a name="conditions-section-structure-functions"></a>

You can use the following intrinsic functions to define conditions:
+ `Fn::And`
+ `Fn::Equals`
+ `Fn::If`
+ `Fn::Not`
+ `Fn::Or`

For the syntax and information about each function, see [Condition functions](intrinsic-function-reference-conditions.md)\. 

**Note**  
`Fn::If` is only supported in the metadata attribute, update policy attribute, and property values in the `Resources` section and `Outputs` sections of a template\.

## Examples<a name="conditions-section-structure-examples"></a>

### Simple condition<a name="w7739ab1c27c15c23c17b3"></a>

The following sample template includes an `EnvType` input parameter, where you can specify `prod` to create a stack for production or `test` to create a stack for testing\. For a production environment, AWS CloudFormation creates an Amazon EC2 instance and attaches a volume to the instance\. For a test environment, AWS CloudFormation creates only the Amazon EC2 instance\.

The `CreateProdResources` condition evaluates to `true` if the `EnvType` parameter is equal to `prod`\. In the sample template, the `NewVolume` and `MountPoint` resources are associated with the `CreateProdResources` condition\. Therefore, the resources are created only if the `EnvType` parameter is equal to `prod`\.

#### JSON<a name="conditions-section-structure-example.json"></a>

```
{
    "AWSTemplateFormatVersion": "2010-09-09",
    "Parameters": {
        "EnvType": {
            "Description": "Environment type.",
            "Default": "test",
            "Type": "String",
            "AllowedValues": [
                "prod",
                "test"
            ],
            "ConstraintDescription": "must specify prod or test."
        }
    },
    "Conditions": {
        "CreateProdResources": {
            "Fn::Equals": [
                {
                    "Ref": "EnvType"
                },
                "prod"
            ]
        }
    },
    "Resources": {
        "EC2Instance": {
            "Type": "AWS::EC2::Instance",
            "Properties": {
                "ImageId": "ami-0ff8a91507f77f867"
            }
        },
        "MountPoint": {
            "Type": "AWS::EC2::VolumeAttachment",
            "Condition": "CreateProdResources",
            "Properties": {
                "InstanceId": {
                    "Ref": "EC2Instance"
                },
                "VolumeId": {
                    "Ref": "NewVolume"
                },
                "Device": "/dev/sdh"
            }
        },
        "NewVolume": {
            "Type": "AWS::EC2::Volume",
            "Condition": "CreateProdResources",
            "Properties": {
                "Size": 100,
                "AvailabilityZone": {
                    "Fn::GetAtt": [
                        "EC2Instance",
                        "AvailabilityZone"
                    ]
                }
            }
        }
    }
}
```

#### YAML<a name="conditions-section-structure-example.yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Parameters:
  EnvType:
    Description: Environment type.
    Default: test
    Type: String
    AllowedValues:
      - prod
      - test
    ConstraintDescription: must specify prod or test.
Conditions:
  CreateProdResources: !Equals 
    - !Ref EnvType
    - prod
Resources:
  EC2Instance:
    Type: 'AWS::EC2::Instance'
    Properties:
      ImageId: ami-0ff8a91507f77f867
  MountPoint:
    Type: 'AWS::EC2::VolumeAttachment'
    Condition: CreateProdResources
    Properties:
      InstanceId: !Ref EC2Instance
      VolumeId: !Ref NewVolume
      Device: /dev/sdh
  NewVolume:
    Type: 'AWS::EC2::Volume'
    Condition: CreateProdResources
    Properties:
      Size: 100
      AvailabilityZone: !GetAtt 
        - EC2Instance
        - AvailabilityZone
```

#### Nested condition<a name="w7739ab1c27c15c23c17b3c11"></a>

The following sample template references a condition within another condition\. You can create a stack that creates an s3 bucket\. For a stack deployed in a production environment, AWS CloudFormation creates a policy for the S3 bucket\.

##### JSON<a name="conditions-section-structure-example-nested.json"></a>

```
{
    "Parameters": {
        "EnvType": {
            "Type": "String",
            "AllowedValues": [
                "prod",
                "test"
            ]
        },
        "BucketName": {
            "Default": "",
            "Type": "String"
        }
    },
    "Conditions": {
        "IsProduction": {
            "Fn::Equals": [
                {
                    "Ref": "EnvType"
                },
                "prod"
            ]
        },
        "CreateBucket": {
            "Fn::Not": [
                {
                    "Fn::Equals": [
                        {
                            "Ref": "BucketName"
                        },
                        ""
                    ]
                }
            ]
        },
        "CreateBucketPolicy": {
            "Fn::And": [
                {
                    "Condition": "IsProduction"
                },
                {
                    "Condition": "CreateBucket"
                }
            ]
        }
    },
    "Resources": {
        "Bucket": {
            "Type": "AWS::S3::Bucket",
            "Condition": "CreateBucket"
        },
        "Policy": {
            "Type": "AWS::S3::BucketPolicy",
            "Condition": "CreateBucketPolicy",
            "Properties": {
                "Bucket": {
                    "Ref": "Bucket"
                },
                "PolicyDocument": "..."
            }
        }
    }
}
```

##### YAML<a name="conditions-section-structure-example-nested.yaml"></a>

```
Parameters:
  EnvType:
    Type: String
    AllowedValues:
      - prod
      - test
  BucketName:
    Default: ''
    Type: String
Conditions:
  IsProduction: !Equals 
    - !Ref EnvType
    - prod
  CreateBucket: !Not 
    - !Equals 
      - !Ref BucketName
      - ''
  CreateBucketPolicy: !And 
    - !Condition IsProduction
    - !Condition CreateBucket
Resources:
  Bucket:
    Type: 'AWS::S3::Bucket'
    Condition: CreateBucket
  Policy:
    Type: 'AWS::S3::BucketPolicy'
    Condition: CreateBucketPolicy
    Properties:
      Bucket: !Ref Bucket
      PolicyDocument: ...
```