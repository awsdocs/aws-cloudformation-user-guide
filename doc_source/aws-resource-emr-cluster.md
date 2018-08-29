# AWS::EMR::Cluster<a name="aws-resource-emr-cluster"></a>

The `AWS::EMR::Cluster` resource creates an Amazon EMR cluster\. This cluster is a collection of EC2 instances that you can run big data frameworks on to process and analyze vast amounts of data\. For more information, see [Plan an Amazon EMR Cluster](http://docs.aws.amazon.com//ElasticMapReduce/latest/ManagementGuide/emr-plan.html) in the *Amazon EMR Management Guide*\.

**Topics**
+ [Syntax](#aws-resource-emr-cluster-syntax)
+ [Properties](#w3ab2c21c10d660b9)
+ [Return Values](#aws-resource-emr-cluster-returnvalues)
+ [Examples](#aws-resource-emr-cluster-examples)

## Syntax<a name="aws-resource-emr-cluster-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-emr-cluster-syntax.json"></a>

```
{
  "Type" : "AWS::EMR::Cluster",
  "Properties" : {
    "[AdditionalInfo](#cfn-emr-cluster-additionalinfo)" : JSON object,
    "[Applications](#cfn-emr-cluster-applications)" : [ Applications, ... ],
    "[AutoScalingRole](#cfn-emr-cluster-autoscalingrole)" : String,
    "[BootstrapActions](#cfn-emr-cluster-bootstrapactions)" [ Bootstrap Actions, ... ],
    "[Configurations](#cfn-emr-cluster-configurations)" : [ Configurations, ... ],
    "[CustomAmiId](#cfn-elasticmapreduce-cluster-customamiid)" : String,
    "[EbsRootVolumeSize](#cfn-elasticmapreduce-cluster-ebsrootvolumesize)" : Integer,
    "[Instances](#cfn-emr-cluster-instances)" : JobFlowInstancesConfig,
    "[JobFlowRole](#cfn-emr-cluster-jobflowrole)" : String,
    "[LogUri](#cfn-emr-cluster-loguri)" : String,
    "[Name](#cfn-emr-cluster-name)" : String,
    "[ReleaseLabel](#cfn-emr-cluster-releaselabel)" : String,
    "[ScaleDownBehavior](#cfn-emr-cluster-scaledownbehavior)" : String,
    "[SecurityConfiguration](#cfn-emr-cluster-securityconfiguration)" : String,
    "[ServiceRole](#cfn-emr-cluster-servicerole)" : String,
    "[Tags](#cfn-emr-cluster-tags)" : [ Resource Tag, ... ],
    "[VisibleToAllUsers](#cfn-emr-cluster-visibletoallusers)" : Boolean
  }
}
```

### YAML<a name="aws-resource-emr-cluster-syntax.yaml"></a>

```
Type: "AWS::EMR::Cluster"
Properties: 
  [AdditionalInfo](#cfn-emr-cluster-additionalinfo): JSON object
  [Applications](#cfn-emr-cluster-applications):
    - Applications
  [AutoScalingRole](#cfn-emr-cluster-autoscalingrole): String      
  [BootstrapActions](#cfn-emr-cluster-bootstrapactions):
    - Bootstrap Actions
  [Configurations](#cfn-emr-cluster-configurations):
    - Configurations        
  [CustomAmiId](#cfn-elasticmapreduce-cluster-customamiid): String
  [EbsRootVolumeSize](#cfn-elasticmapreduce-cluster-ebsrootvolumesize): Integer
  [Instances](#cfn-emr-cluster-instances):
    JobFlowInstancesConfig
  [JobFlowRole](#cfn-emr-cluster-jobflowrole): String
  [LogUri](#cfn-emr-cluster-loguri): String
  [Name](#cfn-emr-cluster-name): String
  [ReleaseLabel](#cfn-emr-cluster-releaselabel): String
  [ScaleDownBehavior](#cfn-emr-cluster-scaledownbehavior): String
  [SecurityConfiguration](#cfn-emr-cluster-securityconfiguration): String
  [ServiceRole](#cfn-emr-cluster-servicerole): String
  [Tags](#cfn-emr-cluster-tags):
    - Resource Tag
  [VisibleToAllUsers](#cfn-emr-cluster-visibletoallusers): Boolean
```

## Properties<a name="w3ab2c21c10d660b9"></a>

**Note**  
For more information about the constraints and valid values of each property, see the [ Cluster](http://docs.aws.amazon.com/ElasticMapReduce/latest/API/API_Cluster.html) data type in the *Amazon EMR API Reference*\.

`AdditionalInfo`  <a name="cfn-emr-cluster-additionalinfo"></a>
\(Intended for advanced uses only\.\) Additional features that you want to select\. This is meta information about third\-party applications that third\-party vendors use for testing purposes\.  
*Required*: No  
*Type*: JSON object  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`Applications`  <a name="cfn-emr-cluster-applications"></a>
The software applications to deploy on the cluster, and the arguments that Amazon EMR passes to those applications\.  
*Required*: No  
*Type*: List of [Amazon EMR Cluster Application](aws-properties-emr-cluster-application.md) property types  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`AutoScalingRole`  <a name="cfn-emr-cluster-autoscalingrole"></a>
An AWS Identity and Access Management \(IAM\) role for automatic scaling policies\. The default role is `EMR_AutoScaling_DefaultRole`\. The IAM role provides permissions that the automatic scaling feature requires to launch and terminate Amazon EC2 instances in an instance group\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`BootstrapActions`  <a name="cfn-emr-cluster-bootstrapactions"></a>
A list of bootstrap actions that Amazon EMR runs before starting applications on the cluster\.  
*Required*: No  
*Type*: List of [Amazon EMR Cluster BootstrapActionConfig](aws-properties-emr-cluster-bootstrapactionconfig.md) property types  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`Configurations`  <a name="cfn-emr-cluster-configurations"></a>
The software configuration of the Amazon EMR cluster\.  
*Required*: No  
*Type*: List of [Amazon EMR Cluster Configurations](aws-properties-emr-cluster-configuration.md) property types  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`CustomAmiId`  <a name="cfn-elasticmapreduce-cluster-customamiid"></a>
A custom Amazon Linux AMI for the cluster \(instead of an EMR\-owned AMI\)\. For more information, see [Using a Custom AMI](http://docs.aws.amazon.com/emr/latest/ManagementGuide/emr-custom-ami.html) in the *Amazon EMR Management Guide*\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)  
*Example*: `"CustomAmiId" : "ami-7fb3bc69"`

`EbsRootVolumeSize`  <a name="cfn-elasticmapreduce-cluster-ebsrootvolumesize"></a>
The size, in GiB, of the EBS root device volume of the Linux AMI that's used for each EC2 instance\.  
Currently, AWS CloudFormation supports only Amazon EMR 4\.0 and later software releases\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`Instances`  <a name="cfn-emr-cluster-instances"></a>
Configures the EC2 instances that run jobs in the Amazon EMR cluster\.  
*Required*: Yes  
*Type*: [Amazon EMR Cluster JobFlowInstancesConfig](aws-properties-emr-cluster-jobflowinstancesconfig.md)  
*Update requires*: [Some interruptions](using-cfn-updating-stacks-update-behaviors.md#update-some-interrupt)

`JobFlowRole`  <a name="cfn-emr-cluster-jobflowrole"></a>
\(Also called *instance profile* and *EC2 role*\.\) Accepts an instance profile that's associated with the role that you want to use\. All EC2 instances in the cluster assume this role\. For more information, see [Create and Use IAM Roles for Amazon EMR](http://docs.aws.amazon.com/emr/latest/ManagementGuide/emr-iam-roles-creatingroles.html) in the *Amazon EMR Management Guide*\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`LogUri`  <a name="cfn-emr-cluster-loguri"></a>
An S3 bucket location that Amazon EMR writes logs files to from a job flow\. If you don't specify a value, Amazon EMR doesn't write any log files\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`Name`  <a name="cfn-emr-cluster-name"></a>
A name for the Amazon EMR cluster\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`ReleaseLabel`  <a name="cfn-emr-cluster-releaselabel"></a>
The Amazon EMR software release label\. A release is a set of software applications and components that you can install and configure on an Amazon EMR cluster\. For more information, see [About Amazon EMR Releases](http://docs.aws.amazon.com//ElasticMapReduce/latest/ReleaseGuide/emr-release-components.html) in the *Amazon EMR Release Guide*\.  
Currently, AWS CloudFormation supports only Amazon EMR 4\.0 and later software releases\.  
*Required*: Conditional\. If you specify the `Applications` property, you must specify this property\.  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`ScaleDownBehavior`  <a name="cfn-emr-cluster-scaledownbehavior"></a>
Indicates how individual EC2 instances terminate when an automatic scale\-in activity occurs or an instance group is resized\. For more information, see [Cluster](http://docs.aws.amazon.com//ElasticMapReduce/latest/API/API_Cluster.html) in the Amazon EMR API Reference\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`SecurityConfiguration`  <a name="cfn-emr-cluster-securityconfiguration"></a>
The name of the security configuration that's applied to the cluster\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`ServiceRole`  <a name="cfn-emr-cluster-servicerole"></a>
The IAM role that Amazon EMR assumes to access AWS resources on your behalf\. For more information, see [Configure IAM Roles for Amazon EMR](http://docs.aws.amazon.com//ElasticMapReduce/latest/ManagementGuide/emr-iam-roles.html) in the *Amazon EMR Management Guide*\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`Tags`  <a name="cfn-emr-cluster-tags"></a>
An arbitrary set of tags \(key–value pairs\) to help you identify the Amazon EMR cluster\.  
*Required*: No  
*Type*: [AWS CloudFormation Resource Tags](aws-properties-resource-tags.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`VisibleToAllUsers`  <a name="cfn-emr-cluster-visibletoallusers"></a>
Indicates whether the instances in the cluster are visible to all IAM users in the AWS account\. If you specify `true`, all IAM users can view and \(if they have permissions\) manage the instances\. If you specify `false`, only the IAM user that created the cluster can view and manage it\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)  
*Default value*: `false`

## Return Values<a name="aws-resource-emr-cluster-returnvalues"></a>

### Ref<a name="aws-resource-emr-cluster-ref"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the cluster ID, such as `j-1ABCD123AB1A`\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.

### Fn::GetAtt<a name="aws-resource-emr-cluster-getatt"></a>

`Fn::GetAtt` returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

`MasterPublicDNS`  
The public DNS name of the master node \(instance\), such as `ec2-12-123-123-123.us-west-2.compute.amazonaws.com`\.

For more information about using `Fn::GetAtt`, see [Fn::GetAtt](intrinsic-function-reference-getatt.md)\.

## Examples<a name="aws-resource-emr-cluster-examples"></a>

### Create a Cluster with Two Core Nodes<a name="aws-resource-emr-cluster-example1"></a>

The following example creates an Amazon EMR cluster with one master node and two core nodes\. The specified IAM roles are the default roles provided by Amazon EMR\. The example also assumes that the cluster is launched in an AWS Region with a default VPC and subnet\. If you don't have these, use the [`Ec2SubnetId`](aws-properties-emr-cluster-jobflowinstancesconfig.md) property to specify the VPC and subnet for the cluster\. Otherwise, AWS CloudFormation can't launch the cluster and returns the following status message: `ElasticMapReduce Cluster failed to stabilize`\. 

#### JSON<a name="aws-resource-emr-cluster-example1.json"></a>

```
"TestCluster": {
  "Type": "AWS::EMR::Cluster",
  "Properties": {
    "Instances": {
      "MasterInstanceGroup": {
        "InstanceCount": 1,
        "InstanceType": "m3.xlarge",
        "Market": "ON_DEMAND",
        "Name": "Master"
      },
      "CoreInstanceGroup": {
        "InstanceCount": 2,
        "InstanceType": "m3.xlarge",
        "Market": "ON_DEMAND",
        "Name": "Core"
      },
      "TerminationProtected" : true
    },
    "Name": "TestCluster",
    "JobFlowRole": "EMR_EC2_DefaultRole",
    "ServiceRole": "EMR_DefaultRole",
    "ReleaseLabel": "emr-4.2.0",
    "Tags": [
      {
        "Key": "IsTest",
        "Value": "True"
      }
    ]
  }
}
```

#### YAML<a name="aws-resource-emr-cluster-example1.yaml"></a>

```
TestCluster: 
  Type: "AWS::EMR::Cluster"
  Properties: 
    Instances: 
      MasterInstanceGroup: 
        InstanceCount: 1
        InstanceType: "m3.xlarge"
        Market: "ON_DEMAND"
        Name: "Master"
      CoreInstanceGroup: 
        InstanceCount: 2
        InstanceType: "m3.xlarge"
        Market: "ON_DEMAND"
        Name: "Core"
      TerminationProtected: true
    Name: "TestCluster"
    JobFlowRole: "EMR_EC2_DefaultRole"
    ServiceRole: "EMR_DefaultRole"
    ReleaseLabel: "emr-4.2.0"
    Tags: 
      - 
        Key: "IsTest"
        Value: "True"
```

### Create a Cluster with a Bootstrap Action<a name="aws-resource-emr-cluster-example2"></a>

The following example creates an Amazon EMR cluster with a bootstrap action\.

#### JSON<a name="aws-resource-emr-cluster-example2.json"></a>

```
"TestCluster": {
  "Type": "AWS::EMR::Cluster",
  "Properties": {
    "BootstrapActions": [{
      "Name": "SomeBootStrapAction",
      "ScriptBootstrapAction": {
        "Path": "/path/to/s3"
      }
    }],
    "Instances": {
      "MasterInstanceGroup": {
        "InstanceCount": 1,
        "InstanceType": "m3.xlarge",
        "Market": "ON_DEMAND",
        "Name": "Master"
      },
      "CoreInstanceGroup": {
        "InstanceCount": 2,
        "InstanceType": "m3.xlarge",
        "Market": "ON_DEMAND",
        "Name": "Core"
      },
      "TerminationProtected": true
    },
    "Name": "TestCluster",
    "JobFlowRole": "EMR_EC2_DefaultRole",
    "ScaleDownBehavior": "TERMINATE_AT_TASK_COMPLETION",
    "ServiceRole": "EMR_DefaultRole",
    "ReleaseLabel": "emr-4.2.0",
    "Tags": [
      {
        "Key": "IsTest",
        "Value": "True"
      }
    ]
  }
}
```

#### YAML<a name="aws-resource-emr-cluster-example2.yaml"></a>

```
TestCluster: 
  Type: "AWS::EMR::Cluster"
  Properties: 
    BootstrapActions: 
      - 
        Name: "SomeBootStrapAction"
        ScriptBootstrapAction: 
          Path: "/path/to/s3"
    Instances: 
      MasterInstanceGroup: 
        InstanceCount: 1
        InstanceType: "m3.xlarge"
        Market: "ON_DEMAND"
        Name: "Master"
      CoreInstanceGroup: 
        InstanceCount: 2
        InstanceType: "m3.xlarge"
        Market: "ON_DEMAND"
        Name: "Core"
      TerminationProtected: true
    Name: "TestCluster"
    JobFlowRole: "EMR_EC2_DefaultRole"
    ScaleDownBehavior: "TERMINATE_AT_TASK_COMPLETION"
    ServiceRole: "EMR_DefaultRole"
    ReleaseLabel: "emr-4.2.0"
    Tags: 
      - 
        Key: "IsTest"
        Value: "True"
```

### Create a Cluster with a Custom AMI<a name="aws-resource-emr-cluster-example3"></a>

The following example template enables you to specify a custom Amazon Linux AMI when creating an Amazon EMR cluster\.

#### JSON<a name="aws-resource-emr-cluster-example3.json"></a>

```
{
  "AWSTemplateFormatVersion": "2010-09-09",
  "Parameters" : {
    "CustomAmiId" : {
      "Type" : "String"
    },
    "InstanceType" : {
      "Type" : "String"
    },
    "ReleaseLabel" : {
      "Type" : "String"
    },
    "SubnetId" : {
      "Type" : "String"
    },
    "TerminationProtected" : {
      "Type" : "String",
      "Default" : "false"
    },
    "ElasticMapReducePrincipal" : {
      "Type" : "String"
    },
    "Ec2Principal" : {
      "Type" : "String"
    }
  },
  "Resources": {
    "cluster": {
      "Type": "AWS::EMR::Cluster",
      "Properties": {
        "CustomAmiId" : {"Ref" : "CustomAmiId"},
        "Instances": {
          "MasterInstanceGroup": {
            "InstanceCount": 1,
            "InstanceType": {"Ref" : "InstanceType"},
            "Market": "ON_DEMAND",
            "Name": "cfnMaster"
          },
          "CoreInstanceGroup": {
            "InstanceCount": 1,
            "InstanceType": {"Ref" : "InstanceType"},
            "Market": "ON_DEMAND",
            "Name": "cfnCore"
          },
          "TerminationProtected" : {"Ref" : "TerminationProtected"},
          "Ec2SubnetId" : {"Ref" : "SubnetId"}
        },
        "Name": "CFNtest",
        "JobFlowRole" : {"Ref": "emrEc2InstanceProfile"},
        "ServiceRole" : {"Ref": "emrRole"},
        "ReleaseLabel" : {"Ref" : "ReleaseLabel"},
        "VisibleToAllUsers" : true,
        "Tags": [
          {
            "Key": "key1",
            "Value": "value1"
          }
        ]
      }
    },
    "emrRole": {
      "Type": "AWS::IAM::Role",
      "Properties": {
        "AssumeRolePolicyDocument": {
          "Version": "2008-10-17",
          "Statement": [
            {
              "Sid": "",
              "Effect": "Allow",
              "Principal": {
                "Service": {"Ref" : "ElasticMapReducePrincipal"}
              },
              "Action": "sts:AssumeRole"
            }
          ]
        },
        "Path": "/",
        "ManagedPolicyArns": ["arn:aws:iam::aws:policy/service-role/AmazonElasticMapReduceRole"]
      }
    },
    "emrEc2Role": {
      "Type": "AWS::IAM::Role",
      "Properties": {
        "AssumeRolePolicyDocument": {
          "Version": "2008-10-17",
          "Statement": [
            {
              "Sid": "",
              "Effect": "Allow",
              "Principal": {
                "Service": {"Ref" : "Ec2Principal"}
              },
              "Action": "sts:AssumeRole"
            }
          ]
        },
        "Path": "/",
        "ManagedPolicyArns": ["arn:aws:iam::aws:policy/service-role/AmazonElasticMapReduceforEC2Role"]
      }
    },
    "emrEc2InstanceProfile": {
      "Type": "AWS::IAM::InstanceProfile",
      "Properties": {
        "Path": "/",
        "Roles": [ {
          "Ref": "emrEc2Role"
        } ]
      }
    }
  }
}
```

#### YAML<a name="aws-resource-emr-cluster-example3.yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Parameters:
  CustomAmiId:
    Type: String
  InstanceType:
    Type: String
  ReleaseLabel:
    Type: String
  SubnetId:
    Type: String
  TerminationProtected:
    Type: String
    Default: 'false'
  ElasticMapReducePrincipal:
    Type: String
  Ec2Principal:
    Type: String
Resources:
  cluster:
    Type: 'AWS::EMR::Cluster'
    Properties:
      CustomAmiId: !Ref CustomAmiId
      Instances:
        MasterInstanceGroup:
          InstanceCount: 1
          InstanceType: !Ref InstanceType
          Market: ON_DEMAND
          Name: cfnMaster
        CoreInstanceGroup:
          InstanceCount: 1
          InstanceType: !Ref InstanceType
          Market: ON_DEMAND
          Name: cfnCore
        TerminationProtected: !Ref TerminationProtected
        Ec2SubnetId: !Ref SubnetId
      Name: CFNtest
      JobFlowRole: !Ref emrEc2InstanceProfile
      ServiceRole: !Ref emrRole
      ReleaseLabel: !Ref ReleaseLabel
      VisibleToAllUsers: true
      Tags:
        - Key: key1
          Value: value1
  emrRole:
    Type: 'AWS::IAM::Role'
    Properties:
      AssumeRolePolicyDocument:
        Version: 2008-10-17
        Statement:
          - Sid: ''
            Effect: Allow
            Principal:
              Service: !Ref ElasticMapReducePrincipal
            Action: 'sts:AssumeRole'
      Path: /
      ManagedPolicyArns:
        - 'arn:aws:iam::aws:policy/service-role/AmazonElasticMapReduceRole'
  emrEc2Role:
    Type: 'AWS::IAM::Role'
    Properties:
      AssumeRolePolicyDocument:
        Version: 2008-10-17
        Statement:
          - Sid: ''
            Effect: Allow
            Principal:
              Service: !Ref Ec2Principal
            Action: 'sts:AssumeRole'
      Path: /
      ManagedPolicyArns:
        - 'arn:aws:iam::aws:policy/service-role/AmazonElasticMapReduceforEC2Role'
  emrEc2InstanceProfile:
    Type: 'AWS::IAM::InstanceProfile'
    Properties:
      Path: /
      Roles:
        - !Ref emrEc2Role
```

### Specify Root Volume Size<a name="aws-resource-emr-cluster-example4"></a>

The following example template enables you to specify the size of the EBS root volume for an Amazon EMR cluster\.

#### JSON<a name="aws-resource-emr-cluster-example3.json"></a>

```
{
  "AWSTemplateFormatVersion": "2010-09-09",
  "Parameters" : {
    "InstanceType" : {
      "Type" : "String"
    },
    "ReleaseLabel" : {
      "Type" : "String"
    },
    "SubnetId" : {
      "Type" : "String"
    },
    "TerminationProtected" : {
      "Type" : "String",
      "Default" : "false"
    },
    "EbsRootVolumeSize" : {
      "Type" : "String"
    }
  },
  "Resources": {
    "cluster": {
      "Type": "AWS::EMR::Cluster",
      "Properties": {
        "EbsRootVolumeSize" : {"Ref" : "EbsRootVolumeSize"},
        "Instances": {
          "MasterInstanceGroup": {
            "InstanceCount": 1,
            "InstanceType": {"Ref" : "InstanceType"},
            "Market": "ON_DEMAND",
            "Name": "cfnMaster"
          },
          "CoreInstanceGroup": {
            "InstanceCount": 1,
            "InstanceType": {"Ref" : "InstanceType"},
            "Market": "ON_DEMAND",
            "Name": "cfnCore"
          },
          "TerminationProtected" : {"Ref" : "TerminationProtected"},
          "Ec2SubnetId" : {"Ref" : "SubnetId"}
        },
        "Name": "CFNtest",
        "JobFlowRole" : {"Ref": "emrEc2InstanceProfile"},
        "ServiceRole" : {"Ref": "emrRole"},
        "ReleaseLabel" : {"Ref" : "ReleaseLabel"},
        "VisibleToAllUsers" : true,
        "Tags": [
          {
            "Key": "key1",
            "Value": "value1"
          }
        ]
      }
    },
    "emrRole": {
      "Type": "AWS::IAM::Role",
      "Properties": {
        "AssumeRolePolicyDocument": {
          "Version": "2008-10-17",
          "Statement": [
            {
              "Sid": "",
              "Effect": "Allow",
              "Principal": {
                "Service": "elasticmapreduce.amazonaws.com"
              },
              "Action": "sts:AssumeRole"
            }
          ]
        },
        "Path": "/",
        "ManagedPolicyArns": ["arn:aws:iam::aws:policy/service-role/AmazonElasticMapReduceRole"]
      }
    },
    "emrEc2Role": {
      "Type": "AWS::IAM::Role",
      "Properties": {
        "AssumeRolePolicyDocument": {
          "Version": "2008-10-17",
          "Statement": [
            {
              "Sid": "",
              "Effect": "Allow",
              "Principal": {
                "Service": "ec2.amazonaws.com"
              },
              "Action": "sts:AssumeRole"
            }
          ]
        },
        "Path": "/",
        "ManagedPolicyArns": ["arn:aws:iam::aws:policy/service-role/AmazonElasticMapReduceforEC2Role"]
      }
    },
    "emrEc2InstanceProfile": {
      "Type": "AWS::IAM::InstanceProfile",
      "Properties": {
        "Path": "/",
        "Roles": [ {
          "Ref": "emrEc2Role"
        } ]
      }
    }
  }
}
```

#### YAML<a name="aws-resource-emr-cluster-example3.yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Parameters:
  InstanceType:
    Type: String
  ReleaseLabel:
    Type: String
  SubnetId:
    Type: String
  TerminationProtected:
    Type: String
    Default: 'false'
  EbsRootVolumeSize:
    Type: String
Resources:
  cluster:
    Type: 'AWS::EMR::Cluster'
    Properties:
      EbsRootVolumeSize: !Ref EbsRootVolumeSize
      Instances:
        MasterInstanceGroup:
          InstanceCount: 1
          InstanceType: !Ref InstanceType
          Market: ON_DEMAND
          Name: cfnMaster
        CoreInstanceGroup:
          InstanceCount: 1
          InstanceType: !Ref InstanceType
          Market: ON_DEMAND
          Name: cfnCore
        TerminationProtected: !Ref TerminationProtected
        Ec2SubnetId: !Ref SubnetId
      Name: CFNtest
      JobFlowRole: !Ref emrEc2InstanceProfile
      ServiceRole: !Ref emrRole
      ReleaseLabel: !Ref ReleaseLabel
      VisibleToAllUsers: true
      Tags:
        - Key: key1
          Value: value1
  emrRole:
    Type: 'AWS::IAM::Role'
    Properties:
      AssumeRolePolicyDocument:
        Version: 2008-10-17
        Statement:
          - Sid: ''
            Effect: Allow
            Principal:
              Service: elasticmapreduce.amazonaws.com
            Action: 'sts:AssumeRole'
      Path: /
      ManagedPolicyArns:
        - 'arn:aws:iam::aws:policy/service-role/AmazonElasticMapReduceRole'
  emrEc2Role:
    Type: 'AWS::IAM::Role'
    Properties:
      AssumeRolePolicyDocument:
        Version: 2008-10-17
        Statement:
          - Sid: ''
            Effect: Allow
            Principal:
              Service: ec2.amazonaws.com
            Action: 'sts:AssumeRole'
      Path: /
      ManagedPolicyArns:
        - 'arn:aws:iam::aws:policy/service-role/AmazonElasticMapReduceforEC2Role'
  emrEc2InstanceProfile:
    Type: 'AWS::IAM::InstanceProfile'
    Properties:
      Path: /
      Roles:
        - !Ref emrEc2Role
```