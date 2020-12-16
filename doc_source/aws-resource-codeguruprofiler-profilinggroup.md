# AWS::CodeGuruProfiler::ProfilingGroup<a name="aws-resource-codeguruprofiler-profilinggroup"></a>

Creates a profiling group\.

## Syntax<a name="aws-resource-codeguruprofiler-profilinggroup-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-codeguruprofiler-profilinggroup-syntax.json"></a>

```
{
  "Type" : "AWS::CodeGuruProfiler::ProfilingGroup",
  "Properties" : {
      "[AgentPermissions](#cfn-codeguruprofiler-profilinggroup-agentpermissions)" : Json,
      "[AnomalyDetectionNotificationConfiguration](#cfn-codeguruprofiler-profilinggroup-anomalydetectionnotificationconfiguration)" : [ Channel, ... ],
      "[ComputePlatform](#cfn-codeguruprofiler-profilinggroup-computeplatform)" : String,
      "[ProfilingGroupName](#cfn-codeguruprofiler-profilinggroup-profilinggroupname)" : String,
      "[Tags](#cfn-codeguruprofiler-profilinggroup-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-codeguruprofiler-profilinggroup-syntax.yaml"></a>

```
Type: AWS::CodeGuruProfiler::ProfilingGroup
Properties: 
  [AgentPermissions](#cfn-codeguruprofiler-profilinggroup-agentpermissions): Json
  [AnomalyDetectionNotificationConfiguration](#cfn-codeguruprofiler-profilinggroup-anomalydetectionnotificationconfiguration): 
    - Channel
  [ComputePlatform](#cfn-codeguruprofiler-profilinggroup-computeplatform): String
  [ProfilingGroupName](#cfn-codeguruprofiler-profilinggroup-profilinggroupname): String
  [Tags](#cfn-codeguruprofiler-profilinggroup-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-codeguruprofiler-profilinggroup-properties"></a>

`AgentPermissions`  <a name="cfn-codeguruprofiler-profilinggroup-agentpermissions"></a>
The agent permissions attached to this profiling group\. This action group grants `ConfigureAgent` and `PostAgentProfile` permissions to perform actions required by the profiling agent\. The Json consists of key `Principals`\.  
*Principals*: A list of string ARNs for the roles and users you want to grant access to the profiling group\. Wildcards are not supported in the ARNs\. You are allowed to provide up to 50 ARNs\. An empty list is not permitted\. This is a required key\.   
For more information, see [Resource\-based policies in CodeGuru Profiler](https://docs.aws.amazon.com/codeguru/latest/profiler-ug/resource-based-policies.html) in the *Amazon CodeGuru Profiler user guide*, [ConfigureAgent](https://docs.aws.amazon.com/codeguru/latest/profiler-api/API_ConfigureAgent.html), and [PostAgentProfile](https://docs.aws.amazon.com/codeguru/latest/profiler-api/API_PostAgentProfile.html)\.  
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AnomalyDetectionNotificationConfiguration`  <a name="cfn-codeguruprofiler-profilinggroup-anomalydetectionnotificationconfiguration"></a>
Adds anomaly notifications for a profiling group\.  
*Required*: No  
*Type*: List of [Channel](aws-properties-codeguruprofiler-profilinggroup-channel.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ComputePlatform`  <a name="cfn-codeguruprofiler-profilinggroup-computeplatform"></a>
 The compute platform of the profiling group\. Use `AWSLambda` if your application runs on AWS Lambda\. Use `Default` if your application runs on a compute platform that is not AWS Lambda, such an Amazon EC2 instance, an on\-premises server, or a different platform\. If not specified, `Default` is used\. This property is immutable\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ProfilingGroupName`  <a name="cfn-codeguruprofiler-profilinggroup-profilinggroupname"></a>
The name of the profiling group\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-codeguruprofiler-profilinggroup-tags"></a>
 A list of tags to add to the created profiling group\.   
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-codeguruprofiler-profilinggroup-return-values"></a>

### Ref<a name="aws-resource-codeguruprofiler-profilinggroup-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the name of the profiling group\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-codeguruprofiler-profilinggroup-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-codeguruprofiler-profilinggroup-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The full Amazon Resource Name \(ARN\) for that profiling group\.

## Examples<a name="aws-resource-codeguruprofiler-profilinggroup--examples"></a>



### CodeGuru Profiler profiling group resource configuration<a name="aws-resource-codeguruprofiler-profilinggroup--examples--CodeGuru_Profiler_profiling_group_resource_configuration"></a>

The following is an example of the profiling group resource with the profiling group name and agent permissions properties\.

#### JSON<a name="aws-resource-codeguruprofiler-profilinggroup--examples--CodeGuru_Profiler_profiling_group_resource_configuration--json"></a>

```
"MyProfilingGroupWithAgentPermissions": {
  "Type": "AWS::CodeGuruProfiler::ProfilingGroup",
  "Properties": {
    "ProfilingGroupName": "MyProfilingGroup",
    "AgentPermissions": {
      "Principals": [
          "arn:aws:iam::1233456789012:role/agent-permissions-role-1", 
          "arn:aws:iam::1233456789012:role/agent-permissions-role-2"
      ]
    }
  }
}
```

#### YAML<a name="aws-resource-codeguruprofiler-profilinggroup--examples--CodeGuru_Profiler_profiling_group_resource_configuration--yaml"></a>

```
MyProfilingGroupWithAgentPermissions:
  Type: AWS::CodeGuruProfiler::ProfilingGroup
  Properties:
    ProfilingGroupName: "MyProfilingGroup"
    AgentPermissions:
      Principals:
        - "arn:aws:iam::1233456789012:role/agent-permissions-role-1"
        - "arn:aws:iam::1233456789012:role/agent-permissions-role-2"
```

### CodeGuru Profiler profiling group resource with compute platform<a name="aws-resource-codeguruprofiler-profilinggroup--examples--CodeGuru_Profiler_profiling_group_resource_with_compute_platform"></a>

The following is an example of the profiling group resource that runs on AWS Lambda\.

#### JSON<a name="aws-resource-codeguruprofiler-profilinggroup--examples--CodeGuru_Profiler_profiling_group_resource_with_compute_platform--json"></a>

```
"MyProfilingGroupWithComputePlatform": {
  "Type": "AWS::CodeGuruProfiler::ProfilingGroup",
  "Properties": {
    "ProfilingGroupName": "MyProfilingGroup",
    "ComputePlatform": "AWSLambda"
  }
}
```

#### YAML<a name="aws-resource-codeguruprofiler-profilinggroup--examples--CodeGuru_Profiler_profiling_group_resource_with_compute_platform--yaml"></a>

```
MyProfilingGroupWithComputePlatform:
  Type: AWS::CodeGuruProfiler::ProfilingGroup
  Properties:
    ProfilingGroupName: "MyProfilingGroup"
    ComputePlatform: "AWSLambda"
```

### CodeGuru Profiler profiling group resource with notifications<a name="aws-resource-codeguruprofiler-profilinggroup--examples--CodeGuru_Profiler_profiling_group_resource_with_notifications"></a>

The following is an example of the a notification configuration for a profiling group\.

#### JSON<a name="aws-resource-codeguruprofiler-profilinggroup--examples--CodeGuru_Profiler_profiling_group_resource_with_notifications--json"></a>

```
"MyProfilingGroupWithNotificationChannelConfiguration": {
  "Type": "AWS::CodeGuruProfiler::ProfilingGroup",
  "Properties": {
    "ProfilingGroupName": "MyProfilingGroup",
    "AnomalyDetectionNotificationConfiguration": [
        {
            "channelUri": "SOME_SNS_TOPIC_ARN",
            "channelId": "aaaaaaaa-bbbb-cccc-dddd-eeeeeeeeeeee"
        }
    ]
  }
}
```

#### YAML<a name="aws-resource-codeguruprofiler-profilinggroup--examples--CodeGuru_Profiler_profiling_group_resource_with_notifications--yaml"></a>

```
MyProfilingGroupWithNotificationChannelConfiguration:
  Type: AWS::CodeGuruProfiler::ProfilingGroup
  Properties:
    ProfilingGroupName: MyProfilingGroup
    AnomalyDetectionNotificationConfiguration:
    - channelUri: SOME_SNS_TOPIC_ARN
      channelId: aaaaaaaa-bbbb-cccc-dddd-eeeeeeeeeeee
```

### CodeGuru Profiler profiling group configuration<a name="aws-resource-codeguruprofiler-profilinggroup--examples--CodeGuru_Profiler_profiling_group_configuration"></a>

The following is an example of a profiling group that runs on AWS Lambda\. This profiling group has enabled agent permissions\. Notifications have also been configured with `AnomalyDetectionConfiguration`\.

#### JSON<a name="aws-resource-codeguruprofiler-profilinggroup--examples--CodeGuru_Profiler_profiling_group_configuration--json"></a>

```
"MyProfilingGroupWithAgentPermissions": {
  "Type": "AWS::CodeGuruProfiler::ProfilingGroup",
  "Properties": {
    "ProfilingGroupName": "MyProfilingGroup",
    "ComputePlatform": "AWSLambda",
    "AgentPermissions": {
      "Principals": [
          "arn:aws:iam::1233456789012:role/agent-permissions-role-1", 
          "arn:aws:iam::1233456789012:role/agent-permissions-role-2"
      ]
    },
    "AnomalyDetectionNotificationConfiguration": [
        {
            "channelUri": "SOME_SNS_TOPIC_ARN",
            "channelId": "aaaaaaaa-bbbb-cccc-dddd-eeeeeeeeeeee"
        }
    ]
  }
}
```

#### YAML<a name="aws-resource-codeguruprofiler-profilinggroup--examples--CodeGuru_Profiler_profiling_group_configuration--yaml"></a>

```
MyProfilingGroup:
  Type: AWS::CodeGuruProfiler::ProfilingGroup
  Properties:
    ProfilingGroupName: "MyProfilingGroup"
    ComputePlatform: "AWSLambda"
    AgentPermissions:
      Principals:
        - "arn:aws:iam::1233456789012:role/agent-permissions-role-1"
        - "arn:aws:iam::1233456789012:role/agent-permissions-role-2"
    AnomalyDetectionNotificationConfiguration:
    - channelUri: SOME_SNS_TOPIC_ARN
      channelId: aaaaaaaa-bbbb-cccc-dddd-eeeeeeeeeeee
```