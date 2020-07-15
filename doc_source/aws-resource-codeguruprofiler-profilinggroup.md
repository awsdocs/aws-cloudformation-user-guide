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
      "[ComputePlatform](#cfn-codeguruprofiler-profilinggroup-computeplatform)" : String,
      "[ProfilingGroupName](#cfn-codeguruprofiler-profilinggroup-profilinggroupname)" : String
    }
}
```

### YAML<a name="aws-resource-codeguruprofiler-profilinggroup-syntax.yaml"></a>

```
Type: AWS::CodeGuruProfiler::ProfilingGroup
Properties: 
  [AgentPermissions](#cfn-codeguruprofiler-profilinggroup-agentpermissions): Json
  [ComputePlatform](#cfn-codeguruprofiler-profilinggroup-computeplatform): String
  [ProfilingGroupName](#cfn-codeguruprofiler-profilinggroup-profilinggroupname): String
```

## Properties<a name="aws-resource-codeguruprofiler-profilinggroup-properties"></a>

`AgentPermissions`  <a name="cfn-codeguruprofiler-profilinggroup-agentpermissions"></a>
The agent permissions attached to this profiling group\.  
*Required*: No  
*Type*: Json  
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