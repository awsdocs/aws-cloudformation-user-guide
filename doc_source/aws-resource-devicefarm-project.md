# AWS::DeviceFarm::Project<a name="aws-resource-devicefarm-project"></a>

Creates a project\.

## Syntax<a name="aws-resource-devicefarm-project-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-devicefarm-project-syntax.json"></a>

```
{
  "Type" : "AWS::DeviceFarm::Project",
  "Properties" : {
      "[DefaultJobTimeoutMinutes](#cfn-devicefarm-project-defaultjobtimeoutminutes)" : Integer,
      "[Name](#cfn-devicefarm-project-name)" : String,
      "[Tags](#cfn-devicefarm-project-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-devicefarm-project-syntax.yaml"></a>

```
Type: AWS::DeviceFarm::Project
Properties: 
  [DefaultJobTimeoutMinutes](#cfn-devicefarm-project-defaultjobtimeoutminutes): Integer
  [Name](#cfn-devicefarm-project-name): String
  [Tags](#cfn-devicefarm-project-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-devicefarm-project-properties"></a>

`DefaultJobTimeoutMinutes`  <a name="cfn-devicefarm-project-defaultjobtimeoutminutes"></a>
Sets the execution timeout value \(in minutes\) for a project\. All test runs in this project use the specified execution timeout value unless overridden when scheduling a run\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-devicefarm-project-name"></a>
The project's name\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `256`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-devicefarm-project-tags"></a>
The tags to add to the resource\. A tag is an array of key\-value pairs\. Tag keys can have a maximum character length of 128 characters\. Tag values can have a maximum length of 256 characters\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-devicefarm-project-return-values"></a>

### Ref<a name="aws-resource-devicefarm-project-return-values-ref"></a>

Not supported for this resource\.

### Fn::GetAtt<a name="aws-resource-devicefarm-project-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-devicefarm-project-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the project\. See [Amazon resource names](https://docs.aws.amazon.com/general/latest/gr/aws-arns-and-namespaces.html) in the *General Reference guide*\.