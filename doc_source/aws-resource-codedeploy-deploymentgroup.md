# AWS::CodeDeploy::DeploymentGroup<a name="aws-resource-codedeploy-deploymentgroup"></a>

 The `AWS::CodeDeploy::DeploymentGroup` resource creates an AWS CodeDeploy deployment group that specifies which instances your application revisions are deployed to, along with other deployment options\. For more information, see [CreateDeploymentGroup](https://docs.aws.amazon.com/codedeploy/latest/APIReference/API_CreateDeploymentGroup.html) in the *CodeDeploy API Reference*\. 

**Note**  
 ECS blue/green deployments through CodeDeploy do not use the `AWS::CodeDeploy::DeploymentGroup` resource\. To perform ECS blue/green deployments, use the `AWS::CodeDeploy::BlueGreen` hook\. See [Perform ECS blue/green deployments through CodeDeploy using AWS CloudFormation](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/blue-green.html) for more information\. 

## Syntax<a name="aws-resource-codedeploy-deploymentgroup-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-codedeploy-deploymentgroup-syntax.json"></a>

```
{
  "Type" : "AWS::CodeDeploy::DeploymentGroup",
  "Properties" : {
      "[AlarmConfiguration](#cfn-codedeploy-deploymentgroup-alarmconfiguration)" : AlarmConfiguration,
      "[ApplicationName](#cfn-codedeploy-deploymentgroup-applicationname)" : String,
      "[AutoRollbackConfiguration](#cfn-codedeploy-deploymentgroup-autorollbackconfiguration)" : AutoRollbackConfiguration,
      "[AutoScalingGroups](#cfn-codedeploy-deploymentgroup-autoscalinggroups)" : [ String, ... ],
      "[Deployment](#cfn-codedeploy-deploymentgroup-deployment)" : Deployment,
      "[DeploymentConfigName](#cfn-codedeploy-deploymentgroup-deploymentconfigname)" : String,
      "[DeploymentGroupName](#cfn-codedeploy-deploymentgroup-deploymentgroupname)" : String,
      "[DeploymentStyle](#cfn-codedeploy-deploymentgroup-deploymentstyle)" : DeploymentStyle,
      "[Ec2TagFilters](#cfn-codedeploy-deploymentgroup-ec2tagfilters)" : [ EC2TagFilter, ... ],
      "[Ec2TagSet](#cfn-codedeploy-deploymentgroup-ec2tagset)" : EC2TagSet,
      "[LoadBalancerInfo](#cfn-codedeploy-deploymentgroup-loadbalancerinfo)" : LoadBalancerInfo,
      "[OnPremisesInstanceTagFilters](#cfn-codedeploy-deploymentgroup-onpremisesinstancetagfilters)" : [ TagFilter, ... ],
      "[OnPremisesTagSet](#cfn-codedeploy-deploymentgroup-onpremisestagset)" : OnPremisesTagSet,
      "[ServiceRoleArn](#cfn-codedeploy-deploymentgroup-servicerolearn)" : String,
      "[TriggerConfigurations](#cfn-codedeploy-deploymentgroup-triggerconfigurations)" : [ TriggerConfig, ... ]
    }
}
```

### YAML<a name="aws-resource-codedeploy-deploymentgroup-syntax.yaml"></a>

```
Type: AWS::CodeDeploy::DeploymentGroup
Properties: 
  [AlarmConfiguration](#cfn-codedeploy-deploymentgroup-alarmconfiguration): 
    AlarmConfiguration
  [ApplicationName](#cfn-codedeploy-deploymentgroup-applicationname): String
  [AutoRollbackConfiguration](#cfn-codedeploy-deploymentgroup-autorollbackconfiguration): 
    AutoRollbackConfiguration
  [AutoScalingGroups](#cfn-codedeploy-deploymentgroup-autoscalinggroups): 
    - String
  [Deployment](#cfn-codedeploy-deploymentgroup-deployment): 
    Deployment
  [DeploymentConfigName](#cfn-codedeploy-deploymentgroup-deploymentconfigname): String
  [DeploymentGroupName](#cfn-codedeploy-deploymentgroup-deploymentgroupname): String
  [DeploymentStyle](#cfn-codedeploy-deploymentgroup-deploymentstyle): 
    DeploymentStyle
  [Ec2TagFilters](#cfn-codedeploy-deploymentgroup-ec2tagfilters): 
    - EC2TagFilter
  [Ec2TagSet](#cfn-codedeploy-deploymentgroup-ec2tagset): 
    EC2TagSet
  [LoadBalancerInfo](#cfn-codedeploy-deploymentgroup-loadbalancerinfo): 
    LoadBalancerInfo
  [OnPremisesInstanceTagFilters](#cfn-codedeploy-deploymentgroup-onpremisesinstancetagfilters): 
    - TagFilter
  [OnPremisesTagSet](#cfn-codedeploy-deploymentgroup-onpremisestagset): 
    OnPremisesTagSet
  [ServiceRoleArn](#cfn-codedeploy-deploymentgroup-servicerolearn): String
  [TriggerConfigurations](#cfn-codedeploy-deploymentgroup-triggerconfigurations): 
    - TriggerConfig
```

## Properties<a name="aws-resource-codedeploy-deploymentgroup-properties"></a>

`AlarmConfiguration`  <a name="cfn-codedeploy-deploymentgroup-alarmconfiguration"></a>
Information about the Amazon CloudWatch alarms that are associated with the deployment group\.  
*Required*: No  
*Type*: [AlarmConfiguration](aws-properties-codedeploy-deploymentgroup-alarmconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ApplicationName`  <a name="cfn-codedeploy-deploymentgroup-applicationname"></a>
 The name of an existing CodeDeploy application to associate this deployment group with\.   
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `100`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`AutoRollbackConfiguration`  <a name="cfn-codedeploy-deploymentgroup-autorollbackconfiguration"></a>
 Information about the automatic rollback configuration that is associated with the deployment group\. If you specify this property, don't specify the `Deployment` property\.   
*Required*: No  
*Type*: [AutoRollbackConfiguration](aws-properties-codedeploy-deploymentgroup-autorollbackconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AutoScalingGroups`  <a name="cfn-codedeploy-deploymentgroup-autoscalinggroups"></a>
 A list of associated Auto Scaling groups that CodeDeploy automatically deploys revisions to when new instances are created\. Duplicates are not allowed\.   
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Deployment`  <a name="cfn-codedeploy-deploymentgroup-deployment"></a>
 The application revision to deploy to this deployment group\. If you specify this property, your target application revision is deployed as soon as the provisioning process is complete\. If you specify this property, don't specify the `AutoRollbackConfiguration` property\.   
*Required*: No  
*Type*: [Deployment](aws-properties-codedeploy-deploymentgroup-deployment.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DeploymentConfigName`  <a name="cfn-codedeploy-deploymentgroup-deploymentconfigname"></a>
 A deployment configuration name or a predefined configuration name\. With predefined configurations, you can deploy application revisions to one instance at a time \(`CodeDeployDefault.OneAtATime`\), half of the instances at a time \(`CodeDeployDefault.HalfAtATime`\), or all the instances at once \(`CodeDeployDefault.AllAtOnce`\)\. For more information and valid values, see [Working with Deployment Configurations](https://docs.aws.amazon.com/codedeploy/latest/userguide/deployment-configurations.html) in the *AWS CodeDeploy User Guide*\.   
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `100`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DeploymentGroupName`  <a name="cfn-codedeploy-deploymentgroup-deploymentgroupname"></a>
 A name for the deployment group\. If you don't specify a name, AWS CloudFormation generates a unique physical ID and uses that ID for the deployment group name\. For more information, see [Name Type](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-name.html)\.  
 If you specify a name, you cannot perform updates that require replacement of this resource\. You can perform updates that require no or some interruption\. If you must replace the resource, specify a new name\. 
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `100`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`DeploymentStyle`  <a name="cfn-codedeploy-deploymentgroup-deploymentstyle"></a>
 Attributes that determine the type of deployment to run and whether to route deployment traffic behind a load balancer\.   
 If you specify this property with a blue/green deployment type, don't specify the `AutoScalingGroups`, `LoadBalancerInfo`, or `Deployment` properties\.   
 For blue/green deployments, AWS CloudFormation supports deployments on Lambda compute platforms only\. You can perform ECS blue/green deployments using `AWS::CodeDeploy::BlueGreen ` hook\. See [Perform ECS blue/green deployments through CodeDeploy using AWS CloudFormation](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/blue-green.html) for more information\. 
*Required*: No  
*Type*: [DeploymentStyle](aws-properties-codedeploy-deploymentgroup-deploymentstyle.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Ec2TagFilters`  <a name="cfn-codedeploy-deploymentgroup-ec2tagfilters"></a>
 The EC2 tags that are already applied to EC2 instances that you want to include in the deployment group\. CodeDeploy includes all EC2 instances identified by any of the tags you specify in this deployment group\. Duplicates are not allowed\.   
 You can specify `EC2TagFilters` or `Ec2TagSet`, but not both\.   
*Required*: No  
*Type*: List of [EC2TagFilter](aws-properties-codedeploy-deploymentgroup-ec2tagfilter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Ec2TagSet`  <a name="cfn-codedeploy-deploymentgroup-ec2tagset"></a>
Information about groups of tags applied to EC2 instances\. The deployment group includes only EC2 instances identified by all the tag groups\. Cannot be used in the same call as `ec2TagFilter`\.  
*Required*: No  
*Type*: [EC2TagSet](aws-properties-codedeploy-deploymentgroup-ec2tagset.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LoadBalancerInfo`  <a name="cfn-codedeploy-deploymentgroup-loadbalancerinfo"></a>
Information about the load balancer to use in a deployment\. For more information, see [ Integrating CodeDeploy with Elastic Load Balancing ](https://docs.aws.amazon.com/codedeploy/latest/userguide/integrations-aws-elastic-load-balancing.html) in the *AWS CodeDeploy User Guide*\.  
*Required*: No  
*Type*: [LoadBalancerInfo](aws-properties-codedeploy-deploymentgroup-loadbalancerinfo.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OnPremisesInstanceTagFilters`  <a name="cfn-codedeploy-deploymentgroup-onpremisesinstancetagfilters"></a>
 The on\-premises instance tags already applied to on\-premises instances that you want to include in the deployment group\. CodeDeploy includes all on\-premises instances identified by any of the tags you specify in this deployment group\. To register on\-premises instances with CodeDeploy, see [Working with On\-Premises Instances for CodeDeploy](https://docs.aws.amazon.com/codedeploy/latest/userguide/instances-on-premises.html) in the *AWS CodeDeploy User Guide*\. Duplicates are not allowed\.   
 You can specify `OnPremisesInstanceTagFilters` or `OnPremisesInstanceTagSet`, but not both\.   
*Required*: No  
*Type*: List of [TagFilter](aws-properties-codedeploy-deploymentgroup-tagfilter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OnPremisesTagSet`  <a name="cfn-codedeploy-deploymentgroup-onpremisestagset"></a>
Information about groups of tags applied to on\-premises instances\. The deployment group includes only on\-premises instances identified by all the tag groups\.  
 You can specify `OnPremisesInstanceTagFilters` or `OnPremisesInstanceTagSet`, but not both\.   
*Required*: No  
*Type*: [OnPremisesTagSet](aws-properties-codedeploy-deploymentgroup-onpremisestagset.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ServiceRoleArn`  <a name="cfn-codedeploy-deploymentgroup-servicerolearn"></a>
A service role Amazon Resource Name \(ARN\) that grants CodeDeploy permission to make calls to AWS services on your behalf\. For more information, see [Create a Service Role for AWS CodeDeploy](https://docs.aws.amazon.com/codedeploy/latest/userguide/getting-started-create-service-role.html) in the *AWS CodeDeploy User Guide*\.   
 In some cases, you might need to add a dependency on the service role's policy\. For more information, see IAM role policy in [DependsOn Attribute](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-attribute-dependson.html)\.
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TriggerConfigurations`  <a name="cfn-codedeploy-deploymentgroup-triggerconfigurations"></a>
Information about triggers associated with the deployment group\. Duplicates are not allowed  
*Required*: No  
*Type*: List of [TriggerConfig](aws-properties-codedeploy-deploymentgroup-triggerconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-codedeploy-deploymentgroup-return-values"></a>

### Ref<a name="aws-resource-codedeploy-deploymentgroup-return-values-ref"></a>

When you pass the logical ID of an `AWS::CodeDeploy::DeploymentGroup` resource to the intrinsic `Ref` function, the function returns the deployment group name, such as `mydeploymentgroup-a123d0d1`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-codedeploy-deploymentgroup--examples"></a>



### Revision in GitHub<a name="aws-resource-codedeploy-deploymentgroup--examples--Revision_in_GitHub"></a>

The following example creates a deployment group that is associated with Auto Scaling groups and uses an application revision that is stored in a GitHub repository\. You specify the repository information as input parameters\.

#### JSON<a name="aws-resource-codedeploy-deploymentgroup--examples--Revision_in_GitHub--json"></a>

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
    "ServiceRoleArn" : {
      "Fn::GetAtt" : [
        "RoleArn", 
        "Arn"
      ]
    }
  }
}
```

#### YAML<a name="aws-resource-codedeploy-deploymentgroup--examples--Revision_in_GitHub--yaml"></a>

```
DeploymentGroup: 
  Type: AWS::CodeDeploy::DeploymentGroup
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
      Fn::GetAtt: [ RoleArn, Arn ]
```

### Associate EC2 Instances<a name="aws-resource-codedeploy-deploymentgroup--examples--Associate_EC2_Instances"></a>

The following example creates a deployment group that uses instance tags to associate EC2 instances with the deployment group\. The deployment group uses an application revision that is stored in an S3 bucket\.

#### JSON<a name="aws-resource-codedeploy-deploymentgroup--examples--Associate_EC2_Instances--json"></a>

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
    "ServiceRoleArn" : { 
      "Fn::GetAtt" : [ 
        "RoleArn", 
        "Arn" 
      ] 
    } 
  }
}
```

#### YAML<a name="aws-resource-codedeploy-deploymentgroup--examples--Associate_EC2_Instances--yaml"></a>

```
DeploymentGroup: 
  Type: AWS::CodeDeploy::DeploymentGroup
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
      Fn::GetAtt: [ RoleArn, Arn ]
```

### Deployment Style<a name="aws-resource-codedeploy-deploymentgroup--examples--Deployment_Style"></a>

The following example creates deployment group with a `BLUE_GREEN` deployment type\.

#### JSON<a name="aws-resource-codedeploy-deploymentgroup--examples--Deployment_Style--json"></a>

```
"CodeDeployDeploymentGroup": {
  "Type": "AWS::CodeDeploy::DeploymentGroup",
  "Properties": {
    "ApplicationName": {
      "Ref": "CodeDeployApplication"
    },
    "DeploymentConfigName": "CodeDeployDefault.LambdaCanary10Percent5Minutes",
    "DeploymentStyle": {
      "DeploymentType": "BLUE_GREEN",
      "DeploymentOption": "WITH_TRAFFIC_CONTROL"
    },
    "ServiceRoleArn": {
      "Fn::GetAtt": [
        "CodeDeployServiceRole",
          "Arn"
      ]
    }
  }
}
```

#### YAML<a name="aws-resource-codedeploy-deploymentgroup--examples--Deployment_Style--yaml"></a>

```
CodeDeployDeploymentGroup:
  Type: 'AWS::CodeDeploy::DeploymentGroup'
  Properties:
    ApplicationName: !Ref CodeDeployApplication
    DeploymentConfigName: CodeDeployDefault.LambdaCanary10Percent5Minutes
    DeploymentStyle:
      DeploymentType: BLUE_GREEN
      DeploymentOption: WITH_TRAFFIC_CONTROL
    ServiceRoleArn: !GetAtt CodeDeployServiceRole.Arn
```

### Alarm and Trigger<a name="aws-resource-codedeploy-deploymentgroup--examples--Alarm_and_Trigger"></a>

The following example configures a billing alarm and a notification trigger for the deployment group\.

#### JSON<a name="aws-resource-codedeploy-deploymentgroup--examples--Alarm_and_Trigger--json"></a>

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
          "Fn::GetAtt": [
            "CodeDeployServiceRole", 
            "Arn"
          ]
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

#### YAML<a name="aws-resource-codedeploy-deploymentgroup--examples--Alarm_and_Trigger--yaml"></a>

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
    Type: AWS::CloudWatch::Alarm
    Properties:
      Namespace: AWS/Billing
      MetricName: EstimatedCharges
      Statistic: Maximum
      Period: '21600'
      EvaluationPeriods: '1'
      Threshold: 1000
      ComparisonOperator: GreaterThanThreshold
  mySNSTopic:
    Type: AWS::SNS::Topic
    Properties: {}
  Application:
    Type: AWS::CodeDeploy::Application
  DeploymentConfig:
    Type: AWS::CodeDeploy::DeploymentConfig
    Properties:
      MinimumHealthyHosts:
        Type: FLEET_PERCENT
        Value: '25'
  DeploymentGroup:
    Type: AWS::CodeDeploy::DeploymentGroup
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
        ServiceRoleArn: !GetAtt CodeDeployServiceRole.Arn
        TriggerConfigurations:
          - TriggerEvents:
          - DeploymentSuccess
          - DeploymentRollback
        TriggerName: MyTarget
        TriggerTargetArn: !Ref mySNSTopic
```

### Automatic Rollback Configuration<a name="aws-resource-codedeploy-deploymentgroup--examples--Automatic_Rollback_Configuration"></a>

The following example configures automatic rollback for the deployment group\.

#### YAML<a name="aws-resource-codedeploy-deploymentgroup--examples--Automatic_Rollback_Configuration--yaml"></a>

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
    Type: AWS::CloudWatch::Alarm
    Properties:
      Namespace: AWS/Billing
      MetricName: EstimatedCharges
      Statistic: Maximum
      Period: '21600'
      EvaluationPeriods: '1'
      Threshold: 1000
      ComparisonOperator: GreaterThanThreshold
  mySNSTopic:
    Type: AWS::SNS::Topic
    Properties: {}
  Application:
    Type: AWS::CodeDeploy::Application
  DeploymentConfig:
    Type: AWS::CodeDeploy::DeploymentConfig
    Properties:
      MinimumHealthyHosts:
        Type: FLEET_PERCENT
        Value: '25'
  DeploymentGroup:
    Type: AWS::CodeDeploy::DeploymentGroup
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
      ServiceRoleArn: !GetAtt CodeDeployServiceRole.Arn
      TriggerConfigurations:
        - TriggerEvents:
            - DeploymentSuccess
            - DeploymentRollback
          TriggerName: MyTarget
          TriggerTargetArn: !Ref mySNSTopic
```

#### JSON<a name="aws-resource-codedeploy-deploymentgroup--examples--Automatic_Rollback_Configuration--json"></a>

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
          "Fn::GetAtt": [
            "CodeDeployServiceRole",
            "Arn"
          ]
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

### Load Balancer<a name="aws-resource-codedeploy-deploymentgroup--examples--Load_Balancer"></a>

The following example configures an Elastic Load Balancing load balancer for the deployment group\.

#### YAML<a name="aws-resource-codedeploy-deploymentgroup--examples--Load_Balancer--yaml"></a>

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
    Type: AWS::EC2::VPC
    Properties:
      CidrBlock: !Ref VpcCidr
  mySubnet:
    Type: AWS::EC2::Subnet
    Properties:
      VpcId: !Ref myVpc
      CidrBlock: !Ref SubnetCidr
  InternetGateway:
    Type: AWS::EC2::InternetGateway
  AttachGateway:
    Type: AWS::EC2::VPCGatewayAttachment
    Properties:
      VpcId: !Ref myVpc
      InternetGatewayId: !Ref InternetGateway
  myELB:
    Type: AWS::ElasticLoadBalancing::LoadBalancer
    Properties:
      Listeners:
        - InstancePort: '8000'
          LoadBalancerPort: '80'
          Protocol: HTTP
      Subnets:
        - !Ref mySubnet
  mySNSTopic:
    Type: AWS::SNS::Topic
    Properties: {}
  Application:
    Type: AWS::CodeDeploy::Application
  DeploymentConfig:
    Type: AWS::CodeDeploy::DeploymentConfig
    Properties:
      MinimumHealthyHosts:
        Type: FLEET_PERCENT
        Value: '25'
  DeploymentGroup:
    Type: AWS::CodeDeploy::DeploymentGroup
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
      ServiceRoleArn: !GetAtt CodeDeployServiceRole.Arn
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

#### JSON<a name="aws-resource-codedeploy-deploymentgroup--examples--Load_Balancer--json"></a>

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
          "Fn::GetAtt": [
            "CodeDeployServiceRole", 
            "Arn"
          ]
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

### Target Group Info<a name="aws-resource-codedeploy-deploymentgroup--examples--Target_Group_Info"></a>

The following example specifies the target group to use in a deployment\. Instances are registered as targets in a target group, and traffic is routed to the target group\.

#### YAML<a name="aws-resource-codedeploy-deploymentgroup--examples--Target_Group_Info--yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Resources:
  AppDeploymentGroup:
    Type: AWS::CodeDeploy::DeploymentGroup
    Properties:
      ApplicationName: MyApp
      DeploymentStyle:
        DeploymentOption: WITH_TRAFFIC_CONTROL
      LoadBalancerInfo:
        TargetGroupInfoList:
          - Name: !GetAtt MyTargetGroup.TargetGroupName
      ServiceRoleArn: 'arn:aws:iam::12345678:role/CodeDeployServiceRole'
```

#### JSON<a name="aws-resource-codedeploy-deploymentgroup--examples--Target_Group_Info--json"></a>

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