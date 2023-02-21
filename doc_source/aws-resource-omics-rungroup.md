# AWS::Omics::RunGroup<a name="aws-resource-omics-rungroup"></a>

Creates a run group\.

## Syntax<a name="aws-resource-omics-rungroup-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-omics-rungroup-syntax.json"></a>

```
{
  "Type" : "AWS::Omics::RunGroup",
  "Properties" : {
      "[MaxCpus](#cfn-omics-rungroup-maxcpus)" : Double,
      "[MaxDuration](#cfn-omics-rungroup-maxduration)" : Double,
      "[MaxRuns](#cfn-omics-rungroup-maxruns)" : Double,
      "[Name](#cfn-omics-rungroup-name)" : String,
      "[Tags](#cfn-omics-rungroup-tags)" : {Key : Value, ...}
    }
}
```

### YAML<a name="aws-resource-omics-rungroup-syntax.yaml"></a>

```
Type: AWS::Omics::RunGroup
Properties: 
  [MaxCpus](#cfn-omics-rungroup-maxcpus): Double
  [MaxDuration](#cfn-omics-rungroup-maxduration): Double
  [MaxRuns](#cfn-omics-rungroup-maxruns): Double
  [Name](#cfn-omics-rungroup-name): String
  [Tags](#cfn-omics-rungroup-tags): 
    Key : Value
```

## Properties<a name="aws-resource-omics-rungroup-properties"></a>

`MaxCpus`  <a name="cfn-omics-rungroup-maxcpus"></a>
The group's maximum CPU count setting\.  
*Required*: No  
*Type*: Double  
*Minimum*: `1`  
*Maximum*: `100000`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MaxDuration`  <a name="cfn-omics-rungroup-maxduration"></a>
The group's maximum duration setting in minutes\.  
*Required*: No  
*Type*: Double  
*Minimum*: `1`  
*Maximum*: `100000`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MaxRuns`  <a name="cfn-omics-rungroup-maxruns"></a>
The group's maximum concurrent run setting\.  
*Required*: No  
*Type*: Double  
*Minimum*: `1`  
*Maximum*: `100000`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-omics-rungroup-name"></a>
The group's name\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Pattern*: `[\p{L}||\p{M}||\p{Z}||\p{S}||\p{N}||\p{P}]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-omics-rungroup-tags"></a>
Tags for the group\.  
*Required*: No  
*Type*: Map of String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-omics-rungroup-return-values"></a>

### Ref<a name="aws-resource-omics-rungroup-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the details of this resource\. For example:

 `{ "Ref": "RunGroup.CreationTime" }` `Ref` returns the timestamp for a run group\. 

### Fn::GetAtt<a name="aws-resource-omics-rungroup-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-omics-rungroup-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The run group's ARN\.

`CreationTime`  <a name="CreationTime-fn::getatt"></a>
When the run group was created\.

`Id`  <a name="Id-fn::getatt"></a>
The run group's ID\.