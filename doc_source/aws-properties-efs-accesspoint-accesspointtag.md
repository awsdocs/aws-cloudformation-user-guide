# AWS::EFS::AccessPoint AccessPointTag<a name="aws-properties-efs-accesspoint-accesspointtag"></a>

A tag is a key\-value pair attached to a file system\. Allowed characters in the `Key` and `Value` properties are letters, white space, and numbers that can be represented in UTF\-8, and the following characters:` + - = . _ : /` 

## Syntax<a name="aws-properties-efs-accesspoint-accesspointtag-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-efs-accesspoint-accesspointtag-syntax.json"></a>

```
{
  "[Key](#cfn-efs-accesspoint-accesspointtag-key)" : String,
  "[Value](#cfn-efs-accesspoint-accesspointtag-value)" : String
}
```

### YAML<a name="aws-properties-efs-accesspoint-accesspointtag-syntax.yaml"></a>

```
  [Key](#cfn-efs-accesspoint-accesspointtag-key): String
  [Value](#cfn-efs-accesspoint-accesspointtag-value): String
```

## Properties<a name="aws-properties-efs-accesspoint-accesspointtag-properties"></a>

`Key`  <a name="cfn-efs-accesspoint-accesspointtag-key"></a>
The tag key \(String\)\. The key can't start with `aws:`\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Pattern*: `^(?![aA]{1}[wW]{1}[sS]{1}:)([\p{L}\p{Z}\p{N}_.:/=+\-@]+)$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Value`  <a name="cfn-efs-accesspoint-accesspointtag-value"></a>
The value of the tag key\.  
*Required*: No  
*Type*: String  
*Maximum*: `256`  
*Pattern*: `^([\p{L}\p{Z}\p{N}_.:/=+\-@]*)$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)