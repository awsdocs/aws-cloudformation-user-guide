# AWS::LookoutVision::Project<a name="aws-resource-lookoutvision-project"></a>

The `AWS::LookoutVision::Project` type creates an Amazon Lookout for Vision project\. A project is a grouping of the resources needed to create and manage an Amazon Lookout for Vision model\.

## Syntax<a name="aws-resource-lookoutvision-project-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-lookoutvision-project-syntax.json"></a>

```
{
  "Type" : "AWS::LookoutVision::Project",
  "Properties" : {
      "[ProjectName](#cfn-lookoutvision-project-projectname)" : String
    }
}
```

### YAML<a name="aws-resource-lookoutvision-project-syntax.yaml"></a>

```
Type: AWS::LookoutVision::Project
Properties: 
  [ProjectName](#cfn-lookoutvision-project-projectname): String
```

## Properties<a name="aws-resource-lookoutvision-project-properties"></a>

`ProjectName`  <a name="cfn-lookoutvision-project-projectname"></a>
The name of the project\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `255`  
*Pattern*: `[a-zA-Z0-9][a-zA-Z0-9_\-]*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-lookoutvision-project-return-values"></a>

### Ref<a name="aws-resource-lookoutvision-project-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the resource name\. For example:

 `{ "Ref": "CircuitBoardProject" }` 

For the Amazon Lookout for Vision `CircuitBoardProject`, Ref returns the name of the project\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-lookoutvision-project-return-values-fn--getatt"></a>

`Fn::GetAtt` returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\. For more information about using `Fn::GetAtt`, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\. 

#### <a name="aws-resource-lookoutvision-project-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
Returns the Amazon Resource Name of the project\.