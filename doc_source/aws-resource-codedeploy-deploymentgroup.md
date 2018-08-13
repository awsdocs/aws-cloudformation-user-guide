# AWS::CodeDeploy::DeploymentGroup<a name="aws-resource-codedeploy-deploymentgroup"></a>

The `AWS::CodeDeploy::DeploymentGroup` resource creates an AWS CodeDeploy deployment group that specifies which instances your application revisions are deployed to, along with other deployment options\. For more information, see [CreateDeploymentGroup](http://docs.aws.amazon.com//codedeploy/latest/APIReference/API_CreateDeploymentGroup.html) in the *AWS CodeDeploy API Reference*\.

**Topics**
+ [Syntax](#aws-resource-codedeploy-deploymentgroup-syntax)
+ [Properties](#w3ab2c21c10d258b9)
+ [Return Value](#w3ab2c21c10d258c11)
+ [Examples](#w3ab2c21c10d258c13)

## Syntax<a name="aws-resource-codedeploy-deploymentgroup-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-codedeploy-deploymentgroup-syntax.json"></a>

```
{
  "Type" : "AWS::CodeDeploy::DeploymentGroup",
  "Properties" : {
    "[AlarmConfiguration](#cfn-codedeploy-deploymentgroup-alarmconfiguration)" : [*AlarmConfiguration*](aws-properties-codedeploy-deploymentgroup-alarmconfiguration.md),
    "[ApplicationName](#cfn-codedeploy-deploymentgroup-applicationname)" : String,
    "[AutoRollbackConfiguration](#cfn-codedeploy-deploymentgroup-autorollbackconfiguration)" : [*AutoRollbackConfiguration*](aws-properties-codedeploy-deploymentgroup-autorollbackconfiguration.md),
    "[AutoScalingGroups](#cfn-codedeploy-deploymentgroup-autoscalinggroups)" : [ String, ... ],
    "[Deployment](#cfn-codedeploy-deploymentgroup-deployment)" : [*Deployment*](aws-properties-codedeploy-deploymentgroup-deployment.md),
    "[DeploymentConfigName](#cfn-codedeploy-deploymentgroup-deploymentconfigname)" : String,
    "[DeploymentGroupName](#cfn-codedeploy-deploymentgroup-deploymentgroupname)" : String,
    "[DeploymentStyle](#cfn-codedeploy-deploymentgroup-deploymentstyle)" : [*DeploymentStyle*](aws-properties-codedeploy-deploymentgroup-deploymentstyle.md),
    "[Ec2TagFilters](#cfn-codedeploy-deploymentgroup-ec2tagfilters)" : [ [*Ec2TagFilter, \.\.\.*](aws-properties-codedeploy-deploymentgroup-ec2tagfilters.md) ],
    "[LoadBalancerInfo](#cfn-codedeploy-deploymentgroup-loadbalancerinfo)" : [*LoadBalancerInfo*](aws-properties-codedeploy-deploymentgroup-loadbalancerinfo.md),
    "[OnPremisesInstanceTagFilters](#cfn-codedeploy-deploymentgroup-onpremisesinstancetagfilters)" : [ [*OnPremisesInstanceTagFilter, \.\.\.*](aws-properties-codedeploy-deploymentgroup-onpremisesinstancetagfilters.md) ],
    "[ServiceRoleArn](#cfn-codedeploy-deploymentgroup-servicerolearn)" : String,
    "[TriggerConfigurations](#cfn-codedeploy-deploymentgroup-triggerconfigurations)" : [ [*TriggerConfig, \.\.\.*](aws-properties-codedeploy-deploymentgroup-triggerconfig.md) ]
  }
}
```

### YAML<a name="aws-resource-codedeploy-deploymentgroup-syntax.yaml"></a>

```
Type: "AWS::CodeDeploy::DeploymentGroup"
Properties:
  [AlarmConfiguration](#cfn-codedeploy-deploymentgroup-alarmconfiguration):
    [*AlarmConfiguration*](aws-properties-codedeploy-deploymentgroup-alarmconfiguration.md)
  [ApplicationName](#cfn-codedeploy-deploymentgroup-applicationname): String
  [AutoRollbackConfiguration](#cfn-codedeploy-deploymentgroup-autorollbackconfiguration): 
    [*AutoRollbackConfiguration*](aws-properties-codedeploy-deploymentgroup-autorollbackconfiguration.md)
  [AutoScalingGroups](#cfn-codedeploy-deploymentgroup-autoscalinggroups):
    - String
  [Deployment](#cfn-codedeploy-deploymentgroup-deployment):
    [*Deployment*](aws-properties-codedeploy-deploymentgroup-deployment.md)
  [DeploymentConfigName](#cfn-codedeploy-deploymentgroup-deploymentconfigname): String
  [DeploymentGroupName](#cfn-codedeploy-deploymentgroup-deploymentgroupname): String
  [DeploymentStyle](#cfn-codedeploy-deploymentgroup-deploymentstyle): 
    [*DeploymentStyle*](aws-properties-codedeploy-deploymentgroup-deploymentstyle.md)
  [Ec2TagFilters](#cfn-codedeploy-deploymentgroup-ec2tagfilters):
    - [*Ec2TagFilters*](aws-properties-codedeploy-deploymentgroup-ec2tagfilters.md)
  [LoadBalancerInfo](#cfn-codedeploy-deploymentgroup-loadbalancerinfo): 
    [*LoadBalancerInfo*](aws-properties-codedeploy-deploymentgroup-loadbalancerinfo.md)
  [OnPremisesInstanceTagFilters](#cfn-codedeploy-deploymentgroup-onpremisesinstancetagfilters):
    - [*OnPremisesInstanceTagFilters*](aws-properties-codedeploy-deploymentgroup-onpremisesinstancetagfilters.md)
  [ServiceRoleArn](#cfn-codedeploy-deploymentgroup-servicerolearn): String
  [TriggerConfigurations](#cfn-codedeploy-deploymentgroup-triggerconfigurations):
    - [*TriggerConfig*](aws-properties-codedeploy-deploymentgroup-triggerconfig.md)
```

## Properties<a name="w3ab2c21c10d258b9"></a>

`AlarmConfiguration`  <a name="cfn-codedeploy-deploymentgroup-alarmconfiguration"></a>
Information about the Amazon CloudWatch alarms that are associated with the deployment group\.  
*Required*: No  
*Type*: [AWS CodeDeploy DeploymentGroup AlarmConfiguration](aws-properties-codedeploy-deploymentgroup-alarmconfiguration.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`ApplicationName`  <a name="cfn-codedeploy-deploymentgroup-applicationname"></a>
The name of an existing AWS CodeDeploy application to associate this deployment group with\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`AutoRollbackConfiguration`  <a name="cfn-codedeploy-deploymentgroup-autorollbackconfiguration"></a>
Information about the automatic rollback configuration that is associated with the deployment group\. If you specify this property, don't specify the `Deployment` property\.  
 *Required*: No  
 *Type*: [AWS CodeDeploy DeploymentGroup AutoRollbackConfiguration](aws-properties-codedeploy-deploymentgroup-autorollbackconfiguration.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`AutoScalingGroups`  <a name="cfn-codedeploy-deploymentgroup-autoscalinggroups"></a>
A list of associated Auto Scaling groups that AWS CodeDeploy automatically deploys revisions to when new instances are created\. Duplicates are not allowed\.  
*Required*: No  
*Type*: List of String values  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Deployment`  <a name="cfn-codedeploy-deploymentgroup-deployment"></a>
The application revision to deploy to this deployment group\. If you specify this property, your target application revision will be deployed as soon as the provisioning process is complete\. If you specify this property, don't specify the `AutoRollbackConfiguration` property\.  
*Required*: No  
*Type*: [AWS CodeDeploy DeploymentGroup Deployment](aws-properties-codedeploy-deploymentgroup-deployment.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`DeploymentConfigName`  <a name="cfn-codedeploy-deploymentgroup-deploymentconfigname"></a>
A deployment configuration name or a predefined configuration name\. With predefined configurations, you can deploy application revisions to one instance at a time, half of the instances at a time, or all the instances at once\. For more information and valid values, see [Working with Deployment Configurations](http://docs.aws.amazon.com/codedeploy/latest/userguide/deployment-configurations.html) in the *AWS CodeDeploy User Guide*\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`DeploymentGroupName`  <a name="cfn-codedeploy-deploymentgroup-deploymentgroupname"></a>
A name for the deployment group\. If you don't specify a name, AWS CloudFormation generates a unique physical ID and uses that ID for the deployment group name\. For more information, see [Name Type](aws-properties-name.md)\.  
If you specify a name, you cannot perform updates that require replacement of this resource\. You can perform updates that require no or some interruption\. If you must replace the resource, specify a new name\.
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`DeploymentStyle`  <a name="cfn-codedeploy-deploymentgroup-deploymentstyle"></a>
Attributes that determine the type of deployment to run and whether to route deployment traffic behind a load balancer\.  
If you specify this property with a blue/green deployment type, don't specify the `AutoScalingGroups`, `LoadBalancerInfo`, or `Deployment` properties\.  
For blue/green deployments, AWS CloudFormation supports deployments on AWS Lambda compute platforms only\.
 *Required*: No  
 *Type*: [AWS CodeDeploy DeploymentGroup DeploymentStyle](aws-properties-codedeploy-deploymentgroup-deploymentstyle.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Ec2TagFilters`  <a name="cfn-codedeploy-deploymentgroup-ec2tagfilters"></a>
The EC2 tags that are already applied to EC2 instances that you want to include in the deployment group\. AWS CodeDeploy includes all EC2 instances identified by any of the tags you specify in this deployment group\. Duplicates are not allowed\.  
*Required*: No  
*Type*: List of [AWS CodeDeploy DeploymentGroup Ec2TagFilters](aws-properties-codedeploy-deploymentgroup-ec2tagfilters.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`LoadBalancerInfo`  <a name="cfn-codedeploy-deploymentgroup-loadbalancerinfo"></a>
Information about the load balancer used in the deployment\. For more information, see [ Integrating AWS CodeDeploy with Elastic Load Balancing](http://docs.aws.amazon.com/codedeploy/latest/userguide/integrations-aws-elastic-load-balancing.html) in the *AWS CodeDeploy User Guide*\.  
 *Required*: No  
 *Type*: [AWS CodeDeploy DeploymentGroup LoadBalancerInfo](aws-properties-codedeploy-deploymentgroup-loadbalancerinfo.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`OnPremisesInstanceTagFilters`  <a name="cfn-codedeploy-deploymentgroup-onpremisesinstancetagfilters"></a>
The on\-premises instance tags already applied to on\-premises instances that you want to include in the deployment group\. AWS CodeDeploy includes all on\-premises instances identified by any of the tags you specify in this deployment group\. To register on\-premises instances with AWS CodeDeploy, see [Working with On\-Premises Instances for AWS CodeDeploy](http://docs.aws.amazon.com/codedeploy/latest/userguide/instances-on-premises.html) in the *AWS CodeDeploy User Guide*\. Duplicates are not allowed\.  
*Required*: No  
*Type*: List of [AWS CodeDeploy DeploymentGroup OnPremisesInstanceTagFilters](aws-properties-codedeploy-deploymentgroup-onpremisesinstancetagfilters.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`ServiceRoleArn`  <a name="cfn-codedeploy-deploymentgroup-servicerolearn"></a>
A service role Amazon Resource Name \(ARN\) that grants AWS CodeDeploy permission to make calls to AWS services on your behalf\. For more information, see [Create a Service Role for AWS CodeDeploy](http://docs.aws.amazon.com/codedeploy/latest/userguide/how-to-create-service-role.html) in the *AWS CodeDeploy User Guide\.*  
In some cases, you might need to add a dependency on the service role's policy\. For more information, see IAM role policy in [DependsOn Attribute](aws-attribute-dependson.md)\.
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`TriggerConfigurations`  <a name="cfn-codedeploy-deploymentgroup-triggerconfigurations"></a>
Information about the notification triggers for the deployment group\. Duplicates are not allowed\.  
*Required*: No  
*Type*: List of [AWS CodeDeploy DeploymentGroup TriggerConfig](aws-properties-codedeploy-deploymentgroup-triggerconfig.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

## Return Value<a name="w3ab2c21c10d258c11"></a>

### Ref<a name="w3ab2c21c10d258c11b2"></a>

When you pass the logical ID of an `AWS::CodeDeploy::DeploymentGroup` resource to the intrinsic `Ref` function, the function returns the deployment group name, such as `mydeploymentgroup-a123d0d1`\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.

## Examples<a name="w3ab2c21c10d258c13"></a>

### Revision in GitHub<a name="w3ab2c21c10d258c13b2"></a>

The following example creates a deployment group that is associated with Auto Scaling groups and uses an application revision that is stored in a GitHub repository\. You specify the repository information as input parameters\.

#### JSON<a name="aws-resource-codedeploy-deploymentgroup-example1.json"></a>

```
"DeploymentGroup" : {
  "Type" : "AWS::CodeDeploy::DeploymentGroup",
  "Properties" : {
    "ApplicationName" : {"Ref" : "ApplicationName"},
    "AutoScalingGroups" : [ {"Ref" : "CodeDeployAutoScalingGroups" } ],
    "Deployment" : {
      "Description" : "A sample deployment",
      "IgnoreApplicationStopFailures" : "true",
      "Revision" : {
        "RevisionType" : "GitHub",
        "GitHubLocation" : {
          "CommitId" : {"Ref" : "CommitId"},
          "Repository" : {"Ref" : "Repository"}
        }
      }
    },
    "ServiceRoleArn" : {"Ref" : "RoleArn"}
  }
}
```

#### YAML<a name="aws-resource-codedeploy-deploymentgroup-example1.yaml"></a>

```
DeploymentGroup: 
  Type: "AWS::CodeDeploy::DeploymentGroup"
  Properties: 
    ApplicationName: 
      Ref: "ApplicationName"
    AutoScalingGroups: 
      - Ref: CodeDeployAutoScalingGroups
    Deployment: 
      Description: "A sample deployment"
      IgnoreApplicationStopFailures: true
      Revision: 
        RevisionType: GitHub
        GitHubLocation: 
          CommitId: 
            Ref: CommitId
          Repository: 
            Ref: Repository
    ServiceRoleArn: 
      Ref: RoleArn
```

### Associate EC2 Instances<a name="w3ab2c21c10d258c13b4"></a>

The following example creates a deployment group that uses instance tags to associate EC2 instances with the deployment group\. The deployment group uses an application revision that is stored in an S3 bucket\.

#### JSON<a name="aws-resource-codedeploy-deploymentgroup-example2.json"></a>

```
"DeploymentGroup" : {
  "Type" : "AWS::CodeDeploy::DeploymentGroup",
  "Properties" : {
    "ApplicationName" : {"Ref" : "Application"},
    "Deployment" : {
      "Description" : "First time",
      "IgnoreApplicationStopFailures" : "true",
      "Revision" : {
        "RevisionType" : "S3",
        "S3Location" : {
          "Bucket" : {"Ref" : "Bucket"},
          "Key" : {"Ref" : "Key"},
          "BundleType" : "Zip",
          "ETag" : {"Ref" : "ETag"},
          "Version" : {"Ref" : "Version"}
        }
      }
    },
    "Ec2TagFilters" : [{
      "Key" : {"Ref" : "TagKey"},
      "Value" : {"Ref" : "TagValue"},
      "Type" : "KEY_AND_VALUE"
    }],
    "ServiceRoleArn" : {"Ref" : "RoleArn"}
  }
}
```

#### YAML<a name="aws-resource-codedeploy-deploymentgroup-example2.yaml"></a>

```
DeploymentGroup: 
  Type: "AWS::CodeDeploy::DeploymentGroup"
  Properties: 
    ApplicationName: 
      Ref: "Application"
    Deployment: 
      Description: "First time"
      IgnoreApplicationStopFailures: true
      Revision:
        RevisionType: S3
        S3Location: 
          Bucket: 
            Ref: Bucket
          Key: 
            Ref: Key
          BundleType: Zip
          ETag: 
            Ref: ETag
          Version: 
            Ref: Version
    Ec2TagFilters: 
      - 
        Key: 
          Ref: TagKey
        Value: 
          Ref: TagValue
        Type: "KEY_AND_VALUE"
    ServiceRoleArn: 
      Ref: RoleArn
```

### Alarm and Trigger<a name="w3ab2c21c10d258c13b6"></a>

The following example configures a billing alarm and a notification trigger for the deployment group\.

#### JSON<a name="aws-resource-codedeploy-deploymentgroup-example3.json"></a>

```
{
  "AWSTemplateFormatVersion": "2010-09-09",
  "Parameters": {
    "EC2TagKey0": {
      "Type": "String",
      "Default": "ec2TagKey0"
    },
    "EC2TagValue0": {
      "Type": "String",
      "Default": "ec2TagValue0"
    },
    "EC2TagKey1": {
      "Type": "String",
      "Default": "ec2TagKey1"
    },
    "EC2TagValue1": {
      "Type": "String",
      "Default": "ec2TagValue1"
    },
    "CodeDeployServiceRole": {
      "Type": "String"
    },
    "DeploymentGroupName": {
      "Type": "String"
    }
  },
  "Resources": {
    "myAlarm": {
      "Type": "AWS::CloudWatch::Alarm",
      "Properties": {
        "Namespace": "AWS/Billing",
        "MetricName": "EstimatedCharges",
        "Statistic": "Maximum",
        "Period": "21600",
        "EvaluationPeriods": "1",
        "Threshold": 1000,
        "ComparisonOperator": "GreaterThanThreshold"
      }
    },
    "mySNSTopic": {
      "Type": "AWS::SNS::Topic",
      "Properties": {}
    },
    "Application": {
      "Type": "AWS::CodeDeploy::Application"
    },
    "DeploymentConfig": {
      "Type": "AWS::CodeDeploy::DeploymentConfig",
      "Properties": {
        "MinimumHealthyHosts": {
          "Type": "FLEET_PERCENT",
          "Value": "25"
        }
      }
    },
    "DeploymentGroup": {
      "Type": "AWS::CodeDeploy::DeploymentGroup",
      "Properties": {
        "AlarmConfiguration": {
          "Alarms": [
            {
              "Name": {
                "Ref": "myAlarm"
              }
            }
          ]
        },
        "ApplicationName": {
          "Ref": "Application"
        },
        "DeploymentConfigName": {
          "Ref": "DeploymentConfig"
        },
        "DeploymentGroupName": {
          "Ref": "DeploymentGroupName"
        },
        "Ec2TagFilters": [
          {
            "Key": {
              "Ref": "EC2TagKey0"
            },
            "Value": {
              "Ref": "EC2TagValue0"
            },
            "Type": "KEY_AND_VALUE"
          },
          {
            "Key": {
              "Ref": "EC2TagKey1"
            },
            "Type": "KEY_ONLY"
          },
          {
            "Value": {
              "Ref": "EC2TagValue1"
            },
            "Type": "VALUE_ONLY"
          }
        ],
        "ServiceRoleArn": {
          "Ref": "CodeDeployServiceRole"
        },
        "TriggerConfigurations": [
          {
            "TriggerEvents": [
              "DeploymentSuccess",
              "DeploymentRollback"
            ],
            "TriggerName": "MyTarget",
            "TriggerTargetArn": {
              "Ref": "mySNSTopic"
            }
          }
        ]
      }
    }
  }
}
```

#### YAML<a name="aws-resource-codedeploy-deploymentgroup-example3.yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Parameters:
  EC2TagKey0:
    Type: String
    Default: ec2TagKey0
  EC2TagValue0:
    Type: String
    Default: ec2TagValue0
  EC2TagKey1:
    Type: String
    Default: ec2TagKey1
  EC2TagValue1:
    Type: String
    Default: ec2TagValue1
  CodeDeployServiceRole:
    Type: String
  DeploymentGroupName:
    Type: String
Resources:
  myAlarm:
    Type: 'AWS::CloudWatch::Alarm'
    Properties:
      Namespace: AWS/Billing
      MetricName: EstimatedCharges
      Statistic: Maximum
      Period: '21600'
      EvaluationPeriods: '1'
      Threshold: 1000
      ComparisonOperator: GreaterThanThreshold
  mySNSTopic:
    Type: 'AWS::SNS::Topic'
    Properties: {}
  Application:
    Type: 'AWS::CodeDeploy::Application'
  DeploymentConfig:
    Type: 'AWS::CodeDeploy::DeploymentConfig'
    Properties:
      MinimumHealthyHosts:
        Type: FLEET_PERCENT
        Value: '25'
  DeploymentGroup:
    Type: 'AWS::CodeDeploy::DeploymentGroup'
    Properties:
      AlarmConfiguration:
        Alarms:
          - Name: !Ref myAlarm
      ApplicationName: !Ref Application
      DeploymentConfigName: !Ref DeploymentConfig
      DeploymentGroupName: !Ref DeploymentGroupName
      Ec2TagFilters:
        - Key: !Ref EC2TagKey0
          Value: !Ref EC2TagValue0
          Type: KEY_AND_VALUE
        - Key: !Ref EC2TagKey1
          Type: KEY_ONLY
        - Value: !Ref EC2TagValue1
          Type: VALUE_ONLY
      ServiceRoleArn: !Ref CodeDeployServiceRole
      TriggerConfigurations:
        - TriggerEvents:
            - DeploymentSuccess
            - DeploymentRollback
          TriggerName: MyTarget
          TriggerTargetArn: !Ref mySNSTopic
```

### Automatic Rollback Configuration<a name="w3ab2c21c10d258c13b8"></a>

The following example configures automatic rollback for the deployment group\.

#### JSON<a name="aws-resource-codedeploy-deploymentgroup-example4.json"></a>

```
{
  "Parameters": {
    "EC2TagKey0": {
      "Type": "String",
      "Default": "ec2TagKey0"
    },
    "EC2TagValue0": {
      "Type": "String",
      "Default": "ec2TagValue0"
    },
    "EC2TagKey1": {
      "Type": "String",
      "Default": "ec2TagKey1"
    },
    "EC2TagValue1": {
      "Type": "String",
      "Default": "ec2TagValue1"
    },
    "CodeDeployServiceRole": {
      "Type": "String"
    },
    "DeploymentGroupName": {
      "Type": "String"
    }
  },
  "Resources": {
    "myAlarm": {
      "Type": "AWS::CloudWatch::Alarm",
      "Properties": {
        "Namespace": "AWS/Billing",
        "MetricName": "EstimatedCharges",
        "Statistic": "Maximum",
        "Period": "21600",
        "EvaluationPeriods": "1",
        "Threshold": 1000,
        "ComparisonOperator": "GreaterThanThreshold"
      }
    },
    "mySNSTopic": {
      "Type": "AWS::SNS::Topic",
      "Properties": {}
    },
    "Application": {
      "Type": "AWS::CodeDeploy::Application"
    },
    "DeploymentConfig": {
      "Type": "AWS::CodeDeploy::DeploymentConfig",
      "Properties": {
        "MinimumHealthyHosts": {
          "Type": "FLEET_PERCENT",
          "Value": "25"
        }
      }
    },
    "DeploymentGroup": {
      "Type": "AWS::CodeDeploy::DeploymentGroup",
      "Properties": {
        "AlarmConfiguration": {
          "Alarms": [
            {
              "Name": { "Ref": "myAlarm" }
            }
          ]
        },
        "ApplicationName": {
          "Ref": "Application"
        },
        "AutoRollbackConfiguration": {
          "Enabled": "true",
          "Events": [ "DEPLOYMENT_FAILURE" ]
        },
        "DeploymentConfigName": {
          "Ref": "DeploymentConfig"
        },
        "DeploymentGroupName": {
          "Ref": "DeploymentGroupName"
        },
        "Ec2TagFilters": [
          {
            "Key": {
              "Ref": "EC2TagKey0"
            },
            "Value": {
              "Ref": "EC2TagValue0"
            },
            "Type": "KEY_AND_VALUE"
          },
          {
            "Key": {
              "Ref": "EC2TagKey1"
            },
            "Type": "KEY_ONLY"
          },
          {
            "Value": {
              "Ref": "EC2TagValue1"
            },
            "Type": "VALUE_ONLY"
          }
        ],
        "ServiceRoleArn": {
          "Ref": "CodeDeployServiceRole"
        },
        "TriggerConfigurations": [
          {
            "TriggerEvents": [ "DeploymentSuccess", "DeploymentRollback" ],
            "TriggerName": "MyTarget",
            "TriggerTargetArn": { "Ref": "mySNSTopic" }
          }
        ]
      }
    }
  }
}
```

#### YAML<a name="aws-resource-codedeploy-deploymentgroup-example4.yaml"></a>

```
Parameters:
  EC2TagKey0:
    Type: String
    Default: ec2TagKey0
  EC2TagValue0:
    Type: String
    Default: ec2TagValue0
  EC2TagKey1:
    Type: String
    Default: ec2TagKey1
  EC2TagValue1:
    Type: String
    Default: ec2TagValue1
  CodeDeployServiceRole:
    Type: String
  DeploymentGroupName:
    Type: String
Resources:
  myAlarm:
    Type: 'AWS::CloudWatch::Alarm'
    Properties:
      Namespace: AWS/Billing
      MetricName: EstimatedCharges
      Statistic: Maximum
      Period: '21600'
      EvaluationPeriods: '1'
      Threshold: 1000
      ComparisonOperator: GreaterThanThreshold
  mySNSTopic:
    Type: 'AWS::SNS::Topic'
    Properties: {}
  Application:
    Type: 'AWS::CodeDeploy::Application'
  DeploymentConfig:
    Type: 'AWS::CodeDeploy::DeploymentConfig'
    Properties:
      MinimumHealthyHosts:
        Type: FLEET_PERCENT
        Value: '25'
  DeploymentGroup:
    Type: 'AWS::CodeDeploy::DeploymentGroup'
    Properties:
      AlarmConfiguration:
        Alarms:
          - Name: !Ref myAlarm
      ApplicationName: !Ref Application
      AutoRollbackConfiguration:
        Enabled: 'true'
        Events:
          - DEPLOYMENT_FAILURE
      DeploymentConfigName: !Ref DeploymentConfig
      DeploymentGroupName: !Ref DeploymentGroupName
      Ec2TagFilters:
        - Key: !Ref EC2TagKey0
          Value: !Ref EC2TagValue0
          Type: KEY_AND_VALUE
        - Key: !Ref EC2TagKey1
          Type: KEY_ONLY
        - Value: !Ref EC2TagValue1
          Type: VALUE_ONLY
      ServiceRoleArn: !Ref CodeDeployServiceRole
      TriggerConfigurations:
        - TriggerEvents:
            - DeploymentSuccess
            - DeploymentRollback
          TriggerName: MyTarget
          TriggerTargetArn: !Ref mySNSTopic
```

### Load Balancer<a name="w3ab2c21c10d258c13c10"></a>

The following example configures an Elastic Load Balancing load balancer for the deployment group\.

#### JSON<a name="aws-resource-codedeploy-deploymentgroup-example5.json"></a>

```
{
  "Parameters": {
    "EC2TagKey0": {
      "Type": "String",
      "Default": "ec2TagKey0"
    },
    "EC2TagValue0": {
      "Type": "String",
      "Default": "ec2TagValue0"
    },
    "EC2TagKey1": {
      "Type": "String",
      "Default": "ec2TagKey1"
    },
    "EC2TagValue1": {
      "Type": "String",
      "Default": "ec2TagValue1"
    },
    "CodeDeployServiceRole": {
      "Type": "String"
    },
    "DeploymentGroupName": {
      "Type": "String"
    },
    "VpcCidr": {
      "Type": "String"
    },
    "SubnetCidr": {
      "Type": "String"
    }
  },
  "Resources": {
    "myVpc": {
      "Type": "AWS::EC2::VPC",
      "Properties": {
        "CidrBlock": { "Ref": "VpcCidr" }
      }
    },
    "mySubnet" : {
      "Type" : "AWS::EC2::Subnet",
      "Properties" : {
        "VpcId" : { "Ref" : "myVpc" },
        "CidrBlock" : { "Ref": "SubnetCidr" }
      }
    },
    "InternetGateway" : {
      "Type" : "AWS::EC2::InternetGateway"
    },
    "AttachGateway" : {
      "Type" : "AWS::EC2::VPCGatewayAttachment",
      "Properties" : {
        "VpcId" : { "Ref" : "myVpc" },
        "InternetGatewayId" : { "Ref" : "InternetGateway" }
      }
    },
    "myELB": {
      "Type": "AWS::ElasticLoadBalancing::LoadBalancer",
      "Properties": {
        "Listeners": [{
          "InstancePort": "8000",
          "LoadBalancerPort": "80",
          "Protocol": "HTTP"
        }],
        "Subnets": [ { "Ref" : "mySubnet" } ]
      }
    },
    "mySNSTopic": {
      "Type": "AWS::SNS::Topic",
      "Properties": {}
    },
    "Application": {
      "Type": "AWS::CodeDeploy::Application"
    },
    "DeploymentConfig": {
      "Type": "AWS::CodeDeploy::DeploymentConfig",
      "Properties": {
        "MinimumHealthyHosts": {
          "Type": "FLEET_PERCENT",
          "Value": "25"
        }
      }
    },
    "DeploymentGroup": {
      "Type": "AWS::CodeDeploy::DeploymentGroup",
      "Properties": {
        "ApplicationName": {
          "Ref": "Application"
        },
        "DeploymentConfigName": {
          "Ref": "DeploymentConfig"
        },
        "DeploymentGroupName": {
          "Ref": "DeploymentGroupName"
        },
        "Ec2TagFilters": [
          {
            "Key": {
              "Ref": "EC2TagKey0"
            },
            "Value": {
              "Ref": "EC2TagValue0"
            },
            "Type": "KEY_AND_VALUE"
          },
          {
            "Key": {
              "Ref": "EC2TagKey1"
            },
            "Type": "KEY_ONLY"
          }
        ],
        "LoadBalancerInfo": {
          "ElbInfoList": [{
            "Name": { "Ref" : "myELB" }
          }]
        },
        "DeploymentStyle": {
          "DeploymentOption": "WITH_TRAFFIC_CONTROL"
        },
        "ServiceRoleArn": {
          "Ref": "CodeDeployServiceRole"
        },
        "TriggerConfigurations": [
          {
            "TriggerEvents": [ "DeploymentSuccess", "DeploymentFailure" ],
            "TriggerName": "MyTarget",
            "TriggerTargetArn": { "Ref": "mySNSTopic" }
          }
        ]
      }
    }
  },
  "Outputs": {
    "ELB": {
      "Description": "ELB for DeploymentGroup",
      "Value" : { "Ref" : "myELB" }
    }
  }
}
```

#### YAML<a name="aws-resource-codedeploy-deploymentgroup-example5.yaml"></a>

```
Parameters:
  EC2TagKey0:
    Type: String
    Default: ec2TagKey0
  EC2TagValue0:
    Type: String
    Default: ec2TagValue0
  EC2TagKey1:
    Type: String
    Default: ec2TagKey1
  EC2TagValue1:
    Type: String
    Default: ec2TagValue1
  CodeDeployServiceRole:
    Type: String
  DeploymentGroupName:
    Type: String
  VpcCidr:
    Type: String
  SubnetCidr:
    Type: String
Resources:
  myVpc:
    Type: 'AWS::EC2::VPC'
    Properties:
      CidrBlock: !Ref VpcCidr
  mySubnet:
    Type: 'AWS::EC2::Subnet'
    Properties:
      VpcId: !Ref myVpc
      CidrBlock: !Ref SubnetCidr
  InternetGateway:
    Type: 'AWS::EC2::InternetGateway'
  AttachGateway:
    Type: 'AWS::EC2::VPCGatewayAttachment'
    Properties:
      VpcId: !Ref myVpc
      InternetGatewayId: !Ref InternetGateway
  myELB:
    Type: 'AWS::ElasticLoadBalancing::LoadBalancer'
    Properties:
      Listeners:
        - InstancePort: '8000'
          LoadBalancerPort: '80'
          Protocol: HTTP
      Subnets:
        - !Ref mySubnet
  mySNSTopic:
    Type: 'AWS::SNS::Topic'
    Properties: {}
  Application:
    Type: 'AWS::CodeDeploy::Application'
  DeploymentConfig:
    Type: 'AWS::CodeDeploy::DeploymentConfig'
    Properties:
      MinimumHealthyHosts:
        Type: FLEET_PERCENT
        Value: '25'
  DeploymentGroup:
    Type: 'AWS::CodeDeploy::DeploymentGroup'
    Properties:
      ApplicationName: !Ref Application
      DeploymentConfigName: !Ref DeploymentConfig
      DeploymentGroupName: !Ref DeploymentGroupName
      Ec2TagFilters:
        - Key: !Ref EC2TagKey0
          Value: !Ref EC2TagValue0
          Type: KEY_AND_VALUE
        - Key: !Ref EC2TagKey1
          Type: KEY_ONLY
      LoadBalancerInfo:
        ElbInfoList:
          - Name: !Ref myELB
      DeploymentStyle:
        DeploymentOption: WITH_TRAFFIC_CONTROL
      ServiceRoleArn: !Ref CodeDeployServiceRole
      TriggerConfigurations:
        - TriggerEvents:
            - DeploymentSuccess
            - DeploymentFailure
          TriggerName: MyTarget
          TriggerTargetArn: !Ref mySNSTopic
Outputs:
  ELB:
    Description: ELB for DeploymentGroup
    Value: !Ref myELB
```

### Target Group Info<a name="w3ab2c21c10d258c13c12"></a>

The following example specifies the target group to use in a deployment\. Instances are registered as targets in a target group, and traffic is routed to the target group\.

#### JSON<a name="aws-resource-codedeploy-deploymentgroup-example6.json"></a>

```
{
    "AWSTemplateFormatVersion": "2010-09-09",
    "Resources": {
        "AppDeploymentGroup": {
            "Type": "AWS::CodeDeploy::DeploymentGroup",
            "Properties": {
                "ApplicationName": "MyApp",
                "DeploymentStyle": {
                    "DeploymentOption": "WITH_TRAFFIC_CONTROL"
                },
                "LoadBalancerInfo": {
                    "TargetGroupInfoList": [
                        {
                            "Name": { "Fn::GetAtt": ["MyTargetGroup", "TargetGroupName"] }
                        }
                    ]
                },
                "ServiceRoleArn": "arn:aws:iam::12345678:role/CodeDeployServiceRole"
            }
        }
    }
}
```

#### YAML<a name="aws-resource-codedeploy-deploymentgroup-example6.yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Resources:
  AppDeploymentGroup:
    Type: 'AWS::CodeDeploy::DeploymentGroup'
    Properties:
      ApplicationName: MyApp
      DeploymentStyle:
        DeploymentOption: WITH_TRAFFIC_CONTROL
      LoadBalancerInfo:
        TargetGroupInfoList:
          - Name: !GetAtt MyTargetGroup.TargetGroupName
      ServiceRoleArn: 'arn:aws:iam::12345678:role/CodeDeployServiceRole'
```