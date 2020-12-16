# AWS::EMR::InstanceGroupConfig<a name="aws-resource-emr-instancegroupconfig"></a>

Use `InstanceGroupConfig` to define instance groups for an EMR cluster\. A cluster can not use both instance groups and instance fleets\. For more information, see [Create a Cluster with Instance Fleets or Uniform Instance Groups](https://docs.aws.amazon.com/emr/latest/ManagementGuide/emr-instance-group-configuration.html) in the *Amazon EMR Management Guide*\.

## Syntax<a name="aws-resource-emr-instancegroupconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-emr-instancegroupconfig-syntax.json"></a>

```
{
  "Type" : "AWS::EMR::InstanceGroupConfig",
  "Properties" : {
      "[AutoScalingPolicy](#cfn-elasticmapreduce-instancegroupconfig-autoscalingpolicy)" : AutoScalingPolicy,
      "[BidPrice](#cfn-emr-instancegroupconfig-bidprice)" : String,
      "[Configurations](#cfn-emr-instancegroupconfig-configurations)" : [ Configuration, ... ],
      "[EbsConfiguration](#cfn-emr-instancegroupconfig-ebsconfiguration)" : EbsConfiguration,
      "[InstanceCount](#cfn-emr-instancegroupconfiginstancecount-)" : Integer,
      "[InstanceRole](#cfn-emr-instancegroupconfig-instancerole)" : String,
      "[InstanceType](#cfn-emr-instancegroupconfig-instancetype)" : String,
      "[JobFlowId](#cfn-emr-instancegroupconfig-jobflowid)" : String,
      "[Market](#cfn-emr-instancegroupconfig-market)" : String,
      "[Name](#cfn-emr-instancegroupconfig-name)" : String
    }
}
```

### YAML<a name="aws-resource-emr-instancegroupconfig-syntax.yaml"></a>

```
Type: AWS::EMR::InstanceGroupConfig
Properties: 
  [AutoScalingPolicy](#cfn-elasticmapreduce-instancegroupconfig-autoscalingpolicy): 
    AutoScalingPolicy
  [BidPrice](#cfn-emr-instancegroupconfig-bidprice): String
  [Configurations](#cfn-emr-instancegroupconfig-configurations): 
    - Configuration
  [EbsConfiguration](#cfn-emr-instancegroupconfig-ebsconfiguration): 
    EbsConfiguration
  [InstanceCount](#cfn-emr-instancegroupconfiginstancecount-): Integer
  [InstanceRole](#cfn-emr-instancegroupconfig-instancerole): String
  [InstanceType](#cfn-emr-instancegroupconfig-instancetype): String
  [JobFlowId](#cfn-emr-instancegroupconfig-jobflowid): String
  [Market](#cfn-emr-instancegroupconfig-market): String
  [Name](#cfn-emr-instancegroupconfig-name): String
```

## Properties<a name="aws-resource-emr-instancegroupconfig-properties"></a>

`AutoScalingPolicy`  <a name="cfn-elasticmapreduce-instancegroupconfig-autoscalingpolicy"></a>
`AutoScalingPolicy` is a subproperty of `InstanceGroupConfig`\. `AutoScalingPolicy` defines how an instance group dynamically adds and terminates EC2 instances in response to the value of a CloudWatch metric\. For more information, see [Using Automatic Scaling in Amazon EMR](https://docs.aws.amazon.com/emr/latest/ManagementGuide/emr-automatic-scaling.html) in the *Amazon EMR Management Guide*\.  
*Required*: No  
*Type*: [AutoScalingPolicy](aws-properties-elasticmapreduce-instancegroupconfig-autoscalingpolicy.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`BidPrice`  <a name="cfn-emr-instancegroupconfig-bidprice"></a>
The bid price for each EC2 Spot Instance type as defined by `InstanceType`\. Expressed in USD\. If neither `BidPrice` nor `BidPriceAsPercentageOfOnDemandPrice` is provided, `BidPriceAsPercentageOfOnDemandPrice` defaults to 100%\.  
*Required*: No  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `256`  
*Pattern*: `[\u0020-\uD7FF\uE000-\uFFFD\uD800\uDC00-\uDBFF\uDFFF\r\n\t]*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Configurations`  <a name="cfn-emr-instancegroupconfig-configurations"></a>
Amazon EMR releases 4\.x or later\.
The list of configurations supplied for an EMR cluster instance group\. You can specify a separate configuration for each instance group \(master, core, and task\)\.  
*Required*: No  
*Type*: List of [Configuration](aws-properties-emr-cluster-configuration.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`EbsConfiguration`  <a name="cfn-emr-instancegroupconfig-ebsconfiguration"></a>
`EbsConfiguration` determines the EBS volumes to attach to EMR cluster instances\.  
*Required*: No  
*Type*: [EbsConfiguration](aws-properties-emr-ebsconfiguration.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`InstanceCount`  <a name="cfn-emr-instancegroupconfiginstancecount-"></a>
Target number of instances for the instance group\.  
*Required*: Yes  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`InstanceRole`  <a name="cfn-emr-instancegroupconfig-instancerole"></a>
The role of the instance group in the cluster\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `CORE | MASTER | TASK`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`InstanceType`  <a name="cfn-emr-instancegroupconfig-instancetype"></a>
The EC2 instance type for all instances in the instance group\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `256`  
*Pattern*: `[\u0020-\uD7FF\uE000-\uFFFD\uD800\uDC00-\uDBFF\uDFFF\r\n\t]*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`JobFlowId`  <a name="cfn-emr-instancegroupconfig-jobflowid"></a>
The ID of an Amazon EMR cluster that you want to associate this instance group with\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Market`  <a name="cfn-emr-instancegroupconfig-market"></a>
Market type of the EC2 instances used to create a cluster node\.  
*Required*: No  
*Type*: String  
*Allowed values*: `ON_DEMAND | SPOT`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Name`  <a name="cfn-emr-instancegroupconfig-name"></a>
Friendly name given to the instance group\.  
*Required*: No  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `256`  
*Pattern*: `[\u0020-\uD7FF\uE000-\uFFFD\uD800\uDC00-\uDBFF\uDFFF\r\n\t]*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-emr-instancegroupconfig-return-values"></a>

### Ref<a name="aws-resource-emr-instancegroupconfig-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns returns the ID of the instance group\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-emr-instancegroupconfig--examples"></a>

Example instance group configuration specifications\.

### Add a task instance group<a name="aws-resource-emr-instancegroupconfig--examples--Add_a_task_instance_group"></a>

The following example adds a task instance group to a cluster named `TestCluster`\.

#### JSON<a name="aws-resource-emr-instancegroupconfig--examples--Add_a_task_instance_group--json"></a>

```
"TestInstanceGroupConfig": {
    "Type": "AWS: : EMR: : InstanceGroupConfig",
    "Properties": {
        "InstanceCount": 2,
        "InstanceType": "m3.xlarge",
        "InstanceRole": "TASK",
        "Market": "ON_DEMAND",
        "Name": "cfnTask2",
        "JobFlowId": {
            "Ref": "cluster"
        }
    }
}
```

#### YAML<a name="aws-resource-emr-instancegroupconfig--examples--Add_a_task_instance_group--yaml"></a>

```
TestInstanceGroupConfig: 
  Properties: 
    InstanceCount: 2
    InstanceRole: TASK
    InstanceType: m3.xlarge
    JobFlowId: 
      Ref: cluster
    Market: ON_DEMAND
    Name: cfnTask2
  Type: "AWS::EMR::InstanceGroupConfig"
```

### Specify an Automatic Scaling Policy<a name="aws-resource-emr-instancegroupconfig--examples--Specify_an_Automatic_Scaling_Policy"></a>

The following example defines an `AutoScalingPolicy` for an `InstanceGroupConfig` resource\.

#### JSON<a name="aws-resource-emr-instancegroupconfig--examples--Specify_an_Automatic_Scaling_Policy--json"></a>

```
"MyInstanceGroupConfig": {
  "Type": "AWS::EMR::InstanceGroupConfig",
  "Properties": {
    "InstanceCount": 1,
    "InstanceType": {
      "Ref": "InstanceType"
    },
    "InstanceRole": "TASK",
    "Market": "ON_DEMAND",
    "Name": "cfnTask",
    "JobFlowId": {
      "Ref": "MyCluster"
    },
    "AutoScalingPolicy": {
      "Constraints": {
        "MinCapacity": {
          "Ref": "MinCapacity"
        },
        "MaxCapacity": {
          "Ref": "MaxCapacity"
        }
      },
      "Rules": [
        {
          "Name": "Scale-out",
          "Description": "Scale-out policy",
          "Action": {
            "SimpleScalingPolicyConfiguration": {
              "AdjustmentType": "CHANGE_IN_CAPACITY",
              "ScalingAdjustment": 1,
              "CoolDown": 300
            }
          },
          "Trigger": {
            "CloudWatchAlarmDefinition": {
              "Dimensions": [
                {
                  "Key": "JobFlowId",
                  "Value": "${emr.clusterId}"
                }
              ],
              "EvaluationPeriods": 1,
              "Namespace": "AWS/ElasticMapReduce",
              "Period": 300,
              "ComparisonOperator": "LESS_THAN",
              "Statistic": "AVERAGE",
              "Threshold": 15,
              "Unit": "PERCENT",
              "MetricName": "YARNMemoryAvailablePercentage"
            }
          }
        },
        {
          "Name": "Scale-in",
          "Description": "Scale-in policy",
          "Action": {
            "SimpleScalingPolicyConfiguration": {
              "AdjustmentType": "CHANGE_IN_CAPACITY",
              "ScalingAdjustment": -1,
              "CoolDown": 300
            }
          },
          "Trigger": {
            "CloudWatchAlarmDefinition": {
              "Dimensions": [
                {
                  "Key": "JobFlowId",
                  "Value": "${emr.clusterId}"
                }
              ],
              "EvaluationPeriods": 1,
              "Namespace": "AWS/ElasticMapReduce",
              "Period": 300,
              "ComparisonOperator": "GREATER_THAN",
              "Statistic": "AVERAGE",
              "Threshold": 75,
              "Unit": "PERCENT",
              "MetricName": "YARNMemoryAvailablePercentage"
            }
          }
        }
      ]
    }
  }
}
```

#### YAML<a name="aws-resource-emr-instancegroupconfig--examples--Specify_an_Automatic_Scaling_Policy--yaml"></a>

```
MyInstanceGroupConfig:
  Type: 'AWS::EMR::InstanceGroupConfig'
  Properties:
    InstanceCount: 1
    InstanceType: !Ref InstanceType
    InstanceRole: TASK
    Market: ON_DEMAND
    Name: cfnTask
    JobFlowId: !Ref MyCluster
    AutoScalingPolicy:
      Constraints:
        MinCapacity: !Ref MinCapacity
        MaxCapacity: !Ref MaxCapacity
      Rules:
        - Name: Scale-out
          Description: Scale-out policy
          Action:
            SimpleScalingPolicyConfiguration:
              AdjustmentType: CHANGE_IN_CAPACITY
              ScalingAdjustment: 1
              CoolDown: 300
          Trigger:
            CloudWatchAlarmDefinition:
              Dimensions:
                - Key: JobFlowId
                  Value: '${emr.clusterId}'
              EvaluationPeriods: 1
              Namespace: AWS/ElasticMapReduce
              Period: 300
              ComparisonOperator: LESS_THAN
              Statistic: AVERAGE
              Threshold: 15
              Unit: PERCENT
              MetricName: YARNMemoryAvailablePercentage
        - Name: Scale-in
          Description: Scale-in policy
          Action:
            SimpleScalingPolicyConfiguration:
              AdjustmentType: CHANGE_IN_CAPACITY
              ScalingAdjustment: -1
              CoolDown: 300
          Trigger:
            CloudWatchAlarmDefinition:
              Dimensions:
                - Key: JobFlowId
                  Value: '${emr.clusterId}'
              EvaluationPeriods: 1
              Namespace: AWS/ElasticMapReduce
              Period: 300
              ComparisonOperator: GREATER_THAN
              Statistic: AVERAGE
              Threshold: 75
              Unit: PERCENT
              MetricName: YARNMemoryAvailablePercentage
```