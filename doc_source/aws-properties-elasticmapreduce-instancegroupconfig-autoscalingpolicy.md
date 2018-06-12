# Amazon EMR InstanceGroupConfig AutoScalingPolicy<a name="aws-properties-elasticmapreduce-instancegroupconfig-autoscalingpolicy"></a>

`AutoScalingPolicy` is a property of the [AWS::EMR::InstanceGroupConfig](aws-resource-emr-instancegroupconfig.md) resource that specifies the constraints and rules for an Auto Scaling group policy\. For more information, see [PutAutoScalingPolicy](http://docs.aws.amazon.com//ElasticMapReduce/latest/API/API_PutAutoScalingPolicy.html) in the Amazon EMR API Reference\.

## Syntax<a name="w3ab2c21c14e1180b5"></a>

### JSON<a name="aws-properties-elasticmapreduce-instancegroupconfig-autoscalingpolicy-syntax.json"></a>

```
{
  "[Constraints](#cfn-elasticmapreduce-instancegroupconfig-autoscalingpolicy-constraints)" : ScalingConstraints,
  "[Rules](#cfn-elasticmapreduce-instancegroupconfig-autoscalingpolicy-rules)" : [ ScalingRule ]
}
```

### YAML<a name="aws-properties-elasticmapreduce-instancegroupconfig-autoscalingpolicy-syntax.yaml"></a>

```
[Constraints](#cfn-elasticmapreduce-instancegroupconfig-autoscalingpolicy-constraints): 
  ScalingConstraints
[Rules](#cfn-elasticmapreduce-instancegroupconfig-autoscalingpolicy-rules): 
  - ScalingRule
```

## Properties<a name="w3ab2c21c14e1180b7"></a>

`Constraints`  <a name="cfn-elasticmapreduce-instancegroupconfig-autoscalingpolicy-constraints"></a>
The upper and lower Amazon EC2 instance limits for an automatic scaling policy\. Automatic scaling activity doesn't cause an instance group to grow above or below these limits\.   
*Required*: Yes  
*Type*: [Amazon EMR InstanceGroupConfig ScalingConstraints](aws-properties-elasticmapreduce-instancegroupconfig-scalingconstraints.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Rules`  <a name="cfn-elasticmapreduce-instancegroupconfig-autoscalingpolicy-rules"></a>
The scale\-in and scale\-out rules that compose the automatic scaling policy\.  
*Required*: Yes  
*Type*: List of [Amazon EMR InstanceGroupConfig ScalingRule](aws-properties-elasticmapreduce-instancegroupconfig-scalingrule.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

## Example<a name="w3ab2c21c14e1180b9"></a>

The following example defines an `AutoScalingPolicy` for an `InstanceGroupConfig` resource\.

### JSON<a name="w3ab2c21c14e1180b9b4"></a>

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

### YAML<a name="w3ab2c21c14e1180b9b6"></a>

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