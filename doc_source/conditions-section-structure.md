# Conditions<a name="conditions-section-structure"></a>

The optional `Conditions` section includes statements that define when a resource is created or when a property is defined\. For example, you can compare whether a value is equal to another value\. Based on the result of that condition, you can conditionally create resources\. If you have multiple conditions, separate them with commas\.

You might use conditions when you want to reuse a template that can create resources in different contexts, such as a test environment versus a production environment\. In your template, you can add an `EnvironmentType` input parameter, which accepts either **prod** or **test** as inputs\. For the production environment, you might include Amazon EC2 instances with certain capabilities; however, for the test environment, you want to use reduced capabilities to save money\. With conditions, you can define which resources are created and how they're configured for each environment type\.

Conditions are evaluated based on input parameter values that you specify when you create or update a stack\. Within each condition, you can reference another condition, a parameter value, or a mapping\. After you define all your conditions, you can associate them with resources and resource properties in the `Resources` and `Outputs` sections of a template\.

At stack creation or stack update, AWS CloudFormation evaluates all the conditions in your template before creating any resources\. Any resources that are associated with a true condition are created\. Any resources that are associated with a false condition are ignored\.

**Important**  
During a stack update, you cannot update conditions by themselves\. You can update conditions only when you include changes that add, modify, or delete resources\.

## How to Use Conditions Overview<a name="w3ab2c17c15c21c13"></a>

To conditionally create resources, you must include statements in at least three different sections of a template:

`Parameters` section  
Define the input values that you want to evaluate in your conditions\. Conditions will result in true or false based on values from these input parameters\.

`Conditions` section  
Define conditions by using the intrinsic condition functions\. These conditions determine when AWS CloudFormation creates the associated resources\.

`Resources` and `Outputs` sections  
Associate conditions with the resources or outputs that you want to conditionally create\. AWS CloudFormation creates entities that are associated with a true condition and ignores entities that are associated with a false condition\. Use the `Condition` key and a condition's logical ID to associate it with a resource or output\. To conditionally specify a property, use the `Fn::If` function\. For more information, see [Condition Functions](intrinsic-function-reference-conditions.md)\.

## Syntax<a name="w3ab2c17c15c21c15"></a>

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

#### Condition Intrinsic Functions<a name="w3ab2c17c15c21c15b6b4"></a>

You can use the following intrinsic functions to define conditions:
+ `Fn::And`
+ `Fn::Equals`
+ `Fn::If`
+ `Fn::Not`
+ `Fn::Or`

For the syntax and information about each function, see [Condition Functions](intrinsic-function-reference-conditions.md)\. 

**Note**  
`Fn::If` is only supported in the metadata attribute, update policy attribute, and property values in the Resources section and Outputs sections of a template\.

## Examples<a name="w3ab2c17c15c21c17"></a>

The following sample template includes an `EnvType` input parameter, where you can specify `prod` to create a stack for production or `test` to create a stack for testing\. For a production environment, AWS CloudFormation creates an Amazon EC2 instance and attaches a volume to the instance\. For a test environment, AWS CloudFormation creates only the Amazon EC2 instance\.

The `CreateProdResources` condition evaluates to `true` if the `EnvType` parameter is equal to `prod`\. In the sample template, the `NewVolume` and `MountPoint` resources are associated with the `CreateProdResources` condition\. Therefore, the resources are created only if the `EnvType` parameter is equal to `prod`\.

### JSON<a name="conditions-section-structure-example.json"></a>

```
{
  "AWSTemplateFormatVersion" : "2010-09-09",

  "Mappings" : {
    "RegionMap" : {
      "us-east-1"      : { "AMI" : "ami-7f418316", "TestAz" : "us-east-1a" },
      "us-west-1"      : { "AMI" : "ami-951945d0", "TestAz" : "us-west-1a" },
      "us-west-2"      : { "AMI" : "ami-16fd7026", "TestAz" : "us-west-2a" },
      "eu-west-1"      : { "AMI" : "ami-24506250", "TestAz" : "eu-west-1a" },
      "sa-east-1"      : { "AMI" : "ami-3e3be423", "TestAz" : "sa-east-1a" },
      "ap-southeast-1" : { "AMI" : "ami-74dda626", "TestAz" : "ap-southeast-1a" },
      "ap-southeast-2" : { "AMI" : "ami-b3990e89", "TestAz" : "ap-southeast-2a" },
      "ap-northeast-1" : { "AMI" : "ami-dcfa4edd", "TestAz" : "ap-northeast-1a" }
    }
  },
    
  "Parameters" : {
    "EnvType" : {
      "Description" : "Environment type.",
      "Default" : "test",
      "Type" : "String",
      "AllowedValues" : ["prod", "test"],
      "ConstraintDescription" : "must specify prod or test."
    }
  },
  
  "Conditions" : {
    "CreateProdResources" : {"Fn::Equals" : [{"Ref" : "EnvType"}, "prod"]}
  },
  
  "Resources" : {
    "EC2Instance" : {
      "Type" : "AWS::EC2::Instance",
      "Properties" : {
        "ImageId" : { "Fn::FindInMap" : [ "RegionMap", { "Ref" : "AWS::Region" }, "AMI" ]}
      }
    },
    
    "MountPoint" : {
      "Type" : "AWS::EC2::VolumeAttachment",
      "Condition" : "CreateProdResources",
      "Properties" : {
        "InstanceId" : { "Ref" : "EC2Instance" },
        "VolumeId"  : { "Ref" : "NewVolume" },
        "Device" : "/dev/sdh"
      }
    },

    "NewVolume" : {
      "Type" : "AWS::EC2::Volume",
      "Condition" : "CreateProdResources",
      "Properties" : {
        "Size" : "100",
        "AvailabilityZone" : { "Fn::GetAtt" : [ "EC2Instance", "AvailabilityZone" ]}
      }
    }
  },
  
  "Outputs" : {
    "VolumeId" : {
      "Value" : { "Ref" : "NewVolume" }, 
      "Condition" : "CreateProdResources"
    }
  }  
}
```

### YAML<a name="conditions-section-structure-example.yaml"></a>

```
AWSTemplateFormatVersion: "2010-09-09"
Mappings: 
  RegionMap: 
    us-east-1: 
      AMI: "ami-7f418316"
      TestAz: "us-east-1a"
    us-west-1: 
      AMI: "ami-951945d0"
      TestAz: "us-west-1a"
    us-west-2: 
      AMI: "ami-16fd7026"
      TestAz: "us-west-2a"
    eu-west-1: 
      AMI: "ami-24506250"
      TestAz: "eu-west-1a"
    sa-east-1: 
      AMI: "ami-3e3be423"
      TestAz: "sa-east-1a"
    ap-southeast-1: 
      AMI: "ami-74dda626"
      TestAz: "ap-southeast-1a"
    ap-southeast-2: 
      AMI: "ami-b3990e89"
      TestAz: "ap-southeast-2a"
    ap-northeast-1: 
      AMI: "ami-dcfa4edd"
      TestAz: "ap-northeast-1a"
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
  CreateProdResources: !Equals [ !Ref EnvType, prod ]
Resources: 
  EC2Instance: 
    Type: "AWS::EC2::Instance"
    Properties: 
      ImageId: !FindInMap [RegionMap, !Ref "AWS::Region", AMI]
  MountPoint: 
    Type: "AWS::EC2::VolumeAttachment"
    Condition: CreateProdResources
    Properties: 
      InstanceId: 
        !Ref EC2Instance
      VolumeId: 
        !Ref NewVolume
      Device: /dev/sdh
  NewVolume: 
    Type: "AWS::EC2::Volume"
    Condition: CreateProdResources
    Properties: 
      Size: 100
      AvailabilityZone: 
        !GetAtt EC2Instance.AvailabilityZone
Outputs: 
  VolumeId: 
    Condition: CreateProdResources
    Value: 
      !Ref NewVolume
```