# Sample templates<a name="conditions-sample-templates"></a>

## Conditionally create resources for a production, development, or test stack<a name="w7739ab1c33c28c21c47b3"></a>

In some cases, you might want to create stacks that are similar but with minor tweaks\. For example, you might have a template that you use for production applications\. You want to create the same production stack so that you can use it for development or testing\. However, for development and testing, you might not require all the extra capacity that's included in a production\-level stack\. Instead, you can use an environment type input parameter in order to conditionally create stack resources that are specific to production, development, or testing, as shown in the following sample: 

**Example JSON**  

```
{
  "AWSTemplateFormatVersion" : "2010-09-09",

  "Mappings" : {
    "RegionMap" : {
      "us-east-1"      : { "AMI" : "ami-0ff8a91507f77f867"},
      "us-west-1"      : { "AMI" : "ami-0bdb828fd58c52235"},
      "us-west-2"      : { "AMI" : "ami-a0cfeed8"},
      "eu-west-1"      : { "AMI" : "ami-047bb4163c506cd98"},
      "sa-east-1"      : { "AMI" : "ami-07b14488da8ea02a0"},
      "ap-southeast-1" : { "AMI" : "ami-08569b978cc4dfa10"},
      "ap-southeast-2" : { "AMI" : "ami-09b42976632b27e9b"},
      "ap-northeast-1" : { "AMI" : "ami-06cd52961ce9f0d85"}
    }
  },
  
  "Parameters" : {
    "EnvType" : {
      "Description" : "Environment type.",
      "Default" : "test",
      "Type" : "String",
      "AllowedValues" : ["prod", "dev", "test"],
      "ConstraintDescription" : "must specify prod, dev, or test."
    }
  },
  
  "Conditions" : {
    "CreateProdResources" : {"Fn::Equals" : [{"Ref" : "EnvType"}, "prod"]},
    "CreateDevResources" : {"Fn::Equals" : [{"Ref" : "EnvType"}, "dev"]}
  },
  
  "Resources" : {
    "EC2Instance" : {
      "Type" : "AWS::EC2::Instance",
      "Properties" : {
        "ImageId" : { "Fn::FindInMap" : [ "RegionMap", { "Ref" : "AWS::Region" }, "AMI" ]},
        "InstanceType" : { "Fn::If" : [
          "CreateProdResources",
          "c1.xlarge",
          {"Fn::If" : [
            "CreateDevResources",
            "m1.large",
            "m1.small"
          ]}
        ]}
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
  }
}
```

**Example YAML**  

```
AWSTemplateFormatVersion: "2010-09-09"

Mappings:
  RegionMap:
    us-east-1:
      AMI: "ami-0ff8a91507f77f867"
    us-west-1:
      AMI: "ami-0bdb828fd58c52235"
    us-west-2:
      AMI: "ami-a0cfeed8"
    eu-west-1:
      AMI: "ami-047bb4163c506cd98"
    sa-east-1:
      AMI: "ami-07b14488da8ea02a0"
    ap-southeast-1:
      AMI: "ami-08569b978cc4dfa10"
    ap-southeast-2:
      AMI: "ami-09b42976632b27e9b"
    ap-northeast-1:
      AMI: "ami-06cd52961ce9f0d85"

Parameters:
  EnvType:
    Description: Environment type.
    Default: test
    Type: String
    AllowedValues: [prod, dev, test]
    ConstraintDescription: must specify prod, dev, or test.
  
Conditions:
  CreateProdResources: !Equals [!Ref EnvType, prod]
  CreateDevResources: !Equals [!Ref EnvType, "dev"]

Resources:
  EC2Instance:
    Type: "AWS::EC2::Instance"
    Properties:
      ImageId: !FindInMap [RegionMap, !Ref "AWS::Region", AMI]
      InstanceType: !If [CreateProdResources, c1.xlarge, !If [CreateDevResources, m1.large, m1.small]]    
  MountPoint:
    Type: "AWS::EC2::VolumeAttachment"
    Condition: CreateProdResources
    Properties:
      InstanceId: !Ref EC2Instance
      VolumeId: !Ref NewVolume
      Device: /dev/sdh
  NewVolume:
    Type: "AWS::EC2::Volume"
    Condition: CreateProdResources
    Properties:
      Size: 100
      AvailabilityZone: !GetAtt EC2Instance.AvailabilityZone
```

You can specify `prod`, `dev`, or `test` for the `EnvType` parameter\. For each environment type, the template specifies a different instance type\. The instance types can range from a large, compute\-optimized instance type to a small general purpose instance type\. In order to conditionally specify the instance type, the template defines two conditions in the Conditions section of the template: `CreateProdResources`, which evaluates to true if the `EnvType` parameter value is equal to `prod` and `CreateDevResources`, which evaluates to true if the parameter value is equal to `dev`\.

In the `InstanceType` property, the template nests two `Fn::If` intrinsic functions to determine which instance type to use\. If the `CreateProdResources` condition is true, the instance type is `c1.xlarge`\. If the condition is false, the `CreateDevResources` condition is evaluated\. If the `CreateDevResources` condition is true, the instance type is `m1.large` or else the instance type is `m1.small`\.

 In addition to the instance type, the production environment creates and attaches an Amazon EC2 volume to the instance\. The `MountPoint` and `NewVolume` resources are associated with the `CreateProdResources` condition so that the resources are created only if the condition evaluates to true\.

## Conditionally assign a resource property<a name="w7739ab1c33c28c21c47b5"></a>

In this example, you can create an Amazon RDS DB instance from a snapshot\. If you specify the `DBSnapshotName` parameter, AWS CloudFormation uses the parameter value as the snapshot name when creating the DB instance\. If you keep the default value \(empty string\), AWS CloudFormation removes the `DBSnapshotIdentifier` property and creates a DB instance from scratch\.

The example defines the `DBUser` and `DBPassword` parameters with their `NoEcho` property set to `true`\. If you set the `NoEcho` attribute to `true`, CloudFormation returns the parameter value masked as asterisks \(\*\*\*\*\*\) for any calls that describe the stack or stack events, except for information stored in the locations specified below\.

**Important**  
Using the `NoEcho` attribute does not mask any information stored in the following:  
The `Metadata` template section\. CloudFormation does not transform, modify, or redact any information you include in the `Metadata` section\. For more information, see [Metadata](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/metadata-section-structure.html)\.
The `Outputs` template section\. For more information, see [Outputs](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/outputs-section-structure.html)\.
The `Metadata` attribute of a resource definition\. For more information, [Metadata attribute](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-attribute-metadata.html)\.
We strongly recommend you do not use these mechanisms to include sensitive information, such as passwords or secrets\.

**Important**  
Rather than embedding sensitive information directly in your AWS CloudFormation templates, we recommend you use dynamic parameters in the stack template to reference sensitive information that is stored and managed outside of CloudFormation, such as in the AWS Systems Manager Parameter Store or AWS Secrets Manager\.  
For more information, see the [Do not embed credentials in your templates](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/best-practices.html#creds) best practice\.

**Example JSON**  

```
{
  "AWSTemplateFormatVersion" : "2010-09-09",

  "Parameters": {
    "DBUser": {
      "NoEcho": "true",
      "Description" : "The database admin account username",
      "Type": "String",
      "MinLength": "1",
      "MaxLength": "16",
      "AllowedPattern" : "[a-zA-Z][a-zA-Z0-9]*",
      "ConstraintDescription" : "must begin with a letter and contain only alphanumeric characters."
    },
    "DBPassword": {
      "NoEcho": "true",
      "Description" : "The database admin account password",
      "Type": "String",
      "MinLength": "1",
      "MaxLength": "41",
      "AllowedPattern" : "[a-zA-Z0-9]*",
      "ConstraintDescription" : "must contain only alphanumeric characters."
    },
    "DBSnapshotName": {
      "Description": "The name of a DB snapshot (optional)",
      "Default": "",
      "Type": "String"      
    }
  },
  
  "Conditions": {
    "UseDBSnapshot": {"Fn::Not": [{"Fn::Equals" : [{"Ref" : "DBSnapshotName"}, ""]}]}
  },

  "Resources" : {
    "MyDB" : {
      "Type" : "AWS::RDS::DBInstance",
      "Properties" : {
        "AllocatedStorage" : "5",
        "DBInstanceClass" : "db.t2.small",
        "Engine" : "MySQL",
        "EngineVersion" : "5.5",
        "MasterUsername" : { "Ref" : "DBUser" },
        "MasterUserPassword" : { "Ref" : "DBPassword" },
        "DBParameterGroupName" : { "Ref" : "MyRDSParamGroup" },
        "DBSnapshotIdentifier" : {
          "Fn::If" : [
            "UseDBSnapshot",
            {"Ref" : "DBSnapshotName"},
            {"Ref" : "AWS::NoValue"}
          ]
        }
      }
    },

    "MyRDSParamGroup" : {
      "Type": "AWS::RDS::DBParameterGroup",
      "Properties" : {
        "Family" : "MySQL5.5",
        "Description" : "CloudFormation Sample Database Parameter Group",
          "Parameters" : {
            "autocommit" : "1" ,
            "general_log" : "1",
            "old_passwords" : "0"
        }
      }
    }
  }
}
```

**Example YAML**  

```
AWSTemplateFormatVersion: "2010-09-09"
Parameters: 
  DBUser: 
    NoEcho: true
    Description: The database admin account username
    Type: String
    MinLength: 1
    MaxLength: 16
    AllowedPattern: "[a-zA-Z][a-zA-Z0-9]*"
    ConstraintDescription: must begin with a letter and contain only alphanumeric characters.
  DBPassword: 
    NoEcho: true
    Description: The database admin account password
    Type: String
    MinLength: 1
    MaxLength: 41
    AllowedPattern: "[a-zA-Z0-9]*"
    ConstraintDescription: must contain only alphanumeric characters.
  DBSnapshotName: 
    Description: The name of a DB snapshot (optional)
    Default: ""
    Type: String
Conditions: 
  UseDBSnapshot: !Not [!Equals [!Ref DBSnapshotName, ""]]
Resources: 
  MyDB: 
    Type: "AWS::RDS::DBInstance"
    Properties: 
      AllocatedStorage: 5
      DBInstanceClass: db.t2.small
      Engine: MySQL
      EngineVersion: 5.5
      MasterUsername: !Ref DBUser
      MasterUserPassword: !Ref DBPassword
      DBParameterGroupName: !Ref MyRDSParamGroup
      DBSnapshotIdentifier: !If [UseDBSnapshot, !Ref DBSnapshotName, !Ref "AWS::NoValue"]
  MyRDSParamGroup: 
    Type: "AWS::RDS::DBParameterGroup"
    Properties: 
      Family: MySQL5.5
      Description: CloudFormation Sample Database Parameter Group
      Parameters: 
        autocommit: 1
        general_log: 1
        old_passwords: 0
```

The `UseDBSnapshot` condition evaluates to true only if the `DBSnapshotName` is not an empty string\. If the `UseDBSnapshot` condition evaluates to true, AWS CloudFormation uses the `DBSnapshotName` parameter value for the `DBSnapshotIdentifier` property\. If the condition evaluates to false, AWS CloudFormation removes the `DBSnapshotIdentifier` property\. The `AWS::NoValue` pseudo parameter removes the corresponding resource property when it is used as a return value\.

## Conditionally use an existing resource<a name="w7739ab1c33c28c21c47b7"></a>

In this example, you can use an Amazon EC2 security group that has already been created or you can create a new security group, which is specified in the template\. For the `ExistingSecurityGroup` parameter, you can specify the `default` security group name or `NONE`\. If you specify `default`, AWS CloudFormation uses a security group that has already been created and is named `default`\. If you specify `NONE`, AWS CloudFormation creates the security group that's defined in the template\.

**Example JSON**  

```
{
  "Parameters" : {
    "ExistingSecurityGroup" : {
      "Description" : "An existing security group ID (optional).",
      "Default" : "NONE",
      "Type" : "String",
      "AllowedValues" : ["default", "NONE"]
    }
  },
 
  "Conditions" : {
    "CreateNewSecurityGroup" : {"Fn::Equals" : [{"Ref" : "ExistingSecurityGroup"}, "NONE"] }
  },

  "Resources" : {
    "MyInstance" : {
      "Type" : "AWS::EC2::Instance",
        "Properties" : {
          "ImageId" : "ami-0ff8a91507f77f867",
          "SecurityGroups" : [{
            "Fn::If" : [
              "CreateNewSecurityGroup",
              {"Ref" : "NewSecurityGroup"},
              {"Ref" : "ExistingSecurityGroup"}
            ]
          }]
        }
    },

    "NewSecurityGroup" : {
      "Type" : "AWS::EC2::SecurityGroup",
      "Condition" : "CreateNewSecurityGroup",
      "Properties" : {
        "GroupDescription" : "Enable HTTP access via port 80",
        "SecurityGroupIngress" : [ {
          "IpProtocol" : "tcp",
          "FromPort" : "80",
          "ToPort" : "80",
          "CidrIp" : "0.0.0.0/0"
        } ]
      }
    }
  },

  "Outputs" : {
    "SecurityGroupId" : {
      "Description" : "Group ID of the security group used.",
      "Value" : {
        "Fn::If" : [
          "CreateNewSecurityGroup",
          {"Ref" : "NewSecurityGroup"},
          {"Ref" : "ExistingSecurityGroup"}
        ]
      }
    }
  }
}
```

**Example YAML**  

```
Parameters: 
  ExistingSecurityGroup: 
    Description: An existing security group ID (optional).
    Default: NONE
    Type: String
    AllowedValues: 
      - default
      - NONE
Conditions: 
  CreateNewSecurityGroup: !Equals [!Ref ExistingSecurityGroup, NONE]
Resources: 
  MyInstance: 
    Type: "AWS::EC2::Instance"
    Properties: 
      ImageId: "ami-0ff8a91507f77f867"
      SecurityGroups: !If [CreateNewSecurityGroup, !Ref NewSecurityGroup, !Ref ExistingSecurityGroup]
  NewSecurityGroup: 
    Type: "AWS::EC2::SecurityGroup"
    Condition: CreateNewSecurityGroup
    Properties: 
      GroupDescription: Enable HTTP access via port 80
      SecurityGroupIngress: 
        - 
          IpProtocol: tcp
          FromPort: 80
          ToPort: 80
          CidrIp: 0.0.0.0/0
Outputs: 
  SecurityGroupId:
    Description: Group ID of the security group used.
    Value: !If [CreateNewSecurityGroup, !Ref NewSecurityGroup, !Ref ExistingSecurityGroup]
```

To determine whether to create the `NewSecurityGroup` resource, the resource is associated with the `CreateNewSecurityGroup` condition\. The resource is created only when the condition is true \(when the `ExistingSecurityGroup` parameter is equal to `NONE`\)\.

In the `SecurityGroups` property, the template uses the `Fn::If` intrinsic function to determine which security group to use\. If the `CreateNewSecurityGroup` condition evaluates to true, the security group property references the `NewSecurityGroup` resource\. If the `CreateNewSecurityGroup` condition evaluates to false, the security group property references the `ExistingSecurityGroup` parameter \(the `default` security group\)\.

Lastly, the template conditionally outputs the security group ID\. If the `CreateNewSecurityGroup` condition evaluates to true, AWS CloudFormation outputs the security group ID of the `NewSecurityGroup` resource\. If the condition is false, AWS CloudFormation outputs the security group ID of the `ExistingSecurityGroup` resource\.