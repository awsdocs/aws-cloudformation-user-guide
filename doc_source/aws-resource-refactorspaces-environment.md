# AWS::RefactorSpaces::Environment<a name="aws-resource-refactorspaces-environment"></a>

Creates an AWS Migration Hub Refactor Spaces environment\. The caller owns the environment resource, and all Refactor Spaces applications, services, and routes created within the environment\. They are referred to as the *environment owner*\. The environment owner has cross\-account visibility and control of Refactor Spaces resources that are added to the environment by other accounts that the environment is shared with\. When creating an environment, Refactor Spaces provisions a transit gateway in your account\.

## Syntax<a name="aws-resource-refactorspaces-environment-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-refactorspaces-environment-syntax.json"></a>

```
{
  "Type" : "AWS::RefactorSpaces::Environment",
  "Properties" : {
      "[Description](#cfn-refactorspaces-environment-description)" : String,
      "[Name](#cfn-refactorspaces-environment-name)" : String,
      "[NetworkFabricType](#cfn-refactorspaces-environment-networkfabrictype)" : String,
      "[Tags](#cfn-refactorspaces-environment-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-refactorspaces-environment-syntax.yaml"></a>

```
Type: AWS::RefactorSpaces::Environment
Properties: 
  [Description](#cfn-refactorspaces-environment-description): String
  [Name](#cfn-refactorspaces-environment-name): String
  [NetworkFabricType](#cfn-refactorspaces-environment-networkfabrictype): String
  [Tags](#cfn-refactorspaces-environment-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-refactorspaces-environment-properties"></a>

`Description`  <a name="cfn-refactorspaces-environment-description"></a>
A description of the environment\.   
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Name`  <a name="cfn-refactorspaces-environment-name"></a>
The name of the environment\.   
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`NetworkFabricType`  <a name="cfn-refactorspaces-environment-networkfabrictype"></a>
The network fabric type of the environment\.   
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-refactorspaces-environment-tags"></a>
The tags assigned to the environment\.   
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-refactorspaces-environment-return-values"></a>

### Ref<a name="aws-resource-refactorspaces-environment-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the ID of the environment, for example, `env-1234654123`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-refactorspaces-environment-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-refactorspaces-environment-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the environment\.

`EnvironmentIdentifier`  <a name="EnvironmentIdentifier-fn::getatt"></a>
The unique identifier of the environment\.

`TransitGatewayId`  <a name="TransitGatewayId-fn::getatt"></a>
The ID of the AWS Transit Gateway set up by the environment\.