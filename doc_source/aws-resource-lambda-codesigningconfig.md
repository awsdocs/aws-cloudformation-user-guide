# AWS::Lambda::CodeSigningConfig<a name="aws-resource-lambda-codesigningconfig"></a>

Details about a Code signing configuration\. 

## Syntax<a name="aws-resource-lambda-codesigningconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-lambda-codesigningconfig-syntax.json"></a>

```
{
  "Type" : "AWS::Lambda::CodeSigningConfig",
  "Properties" : {
      "[AllowedPublishers](#cfn-lambda-codesigningconfig-allowedpublishers)" : AllowedPublishers,
      "[CodeSigningPolicies](#cfn-lambda-codesigningconfig-codesigningpolicies)" : CodeSigningPolicies,
      "[Description](#cfn-lambda-codesigningconfig-description)" : String
    }
}
```

### YAML<a name="aws-resource-lambda-codesigningconfig-syntax.yaml"></a>

```
Type: AWS::Lambda::CodeSigningConfig
Properties: 
  [AllowedPublishers](#cfn-lambda-codesigningconfig-allowedpublishers): 
    AllowedPublishers
  [CodeSigningPolicies](#cfn-lambda-codesigningconfig-codesigningpolicies): 
    CodeSigningPolicies
  [Description](#cfn-lambda-codesigningconfig-description): String
```

## Properties<a name="aws-resource-lambda-codesigningconfig-properties"></a>

`AllowedPublishers`  <a name="cfn-lambda-codesigningconfig-allowedpublishers"></a>
List of allowed publishers\.  
*Required*: Yes  
*Type*: [AllowedPublishers](aws-properties-lambda-codesigningconfig-allowedpublishers.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CodeSigningPolicies`  <a name="cfn-lambda-codesigningconfig-codesigningpolicies"></a>
The code signing policy controls the validation failure action for signature mismatch or expiry\.  
*Required*: No  
*Type*: [CodeSigningPolicies](aws-properties-lambda-codesigningconfig-codesigningpolicies.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Description`  <a name="cfn-lambda-codesigningconfig-description"></a>
Code signing configuration description\.  
*Required*: No  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `256`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-lambda-codesigningconfig-return-values"></a>

### Ref<a name="aws-resource-lambda-codesigningconfig-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the resource name\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-lambda-codesigningconfig-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-lambda-codesigningconfig-return-values-fn--getatt-fn--getatt"></a>

`CodeSigningConfigArn`  <a name="CodeSigningConfigArn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the code signing configuration\.

`CodeSigningConfigId`  <a name="CodeSigningConfigId-fn::getatt"></a>
The code signing configuration ID\.