# AWS::Connect::TaskTemplate Constraints<a name="aws-properties-connect-tasktemplate-constraints"></a>

Describes constraints that apply to the template fields\.

## Syntax<a name="aws-properties-connect-tasktemplate-constraints-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-connect-tasktemplate-constraints-syntax.json"></a>

```
{
  "[InvisibleFields](#cfn-connect-tasktemplate-constraints-invisiblefields)" : [ InvisibleFieldInfo, ... ],
  "[ReadOnlyFields](#cfn-connect-tasktemplate-constraints-readonlyfields)" : [ ReadOnlyFieldInfo, ... ],
  "[RequiredFields](#cfn-connect-tasktemplate-constraints-requiredfields)" : [ RequiredFieldInfo, ... ]
}
```

### YAML<a name="aws-properties-connect-tasktemplate-constraints-syntax.yaml"></a>

```
  [InvisibleFields](#cfn-connect-tasktemplate-constraints-invisiblefields): 
    - InvisibleFieldInfo
  [ReadOnlyFields](#cfn-connect-tasktemplate-constraints-readonlyfields): 
    - ReadOnlyFieldInfo
  [RequiredFields](#cfn-connect-tasktemplate-constraints-requiredfields): 
    - RequiredFieldInfo
```

## Properties<a name="aws-properties-connect-tasktemplate-constraints-properties"></a>

`InvisibleFields`  <a name="cfn-connect-tasktemplate-constraints-invisiblefields"></a>
Lists the fields that are invisible to agents\.  
*Required*: No  
*Type*: List of [InvisibleFieldInfo](aws-properties-connect-tasktemplate-invisiblefieldinfo.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ReadOnlyFields`  <a name="cfn-connect-tasktemplate-constraints-readonlyfields"></a>
Lists the fields that are read\-only to agents, and cannot be edited\.  
*Required*: No  
*Type*: List of [ReadOnlyFieldInfo](aws-properties-connect-tasktemplate-readonlyfieldinfo.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RequiredFields`  <a name="cfn-connect-tasktemplate-constraints-requiredfields"></a>
Lists the fields that are required to be filled by agents\.  
*Required*: No  
*Type*: List of [RequiredFieldInfo](aws-properties-connect-tasktemplate-requiredfieldinfo.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)