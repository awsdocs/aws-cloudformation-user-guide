# AWS::Connect::Prompt<a name="aws-resource-connect-prompt"></a>

Creates a prompt for the specified Amazon Connect instance\.

## Syntax<a name="aws-resource-connect-prompt-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-connect-prompt-syntax.json"></a>

```
{
  "Type" : "AWS::Connect::Prompt",
  "Properties" : {
      "[Description](#cfn-connect-prompt-description)" : String,
      "[InstanceArn](#cfn-connect-prompt-instancearn)" : String,
      "[Name](#cfn-connect-prompt-name)" : String,
      "[S3Uri](#cfn-connect-prompt-s3uri)" : String,
      "[Tags](#cfn-connect-prompt-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-connect-prompt-syntax.yaml"></a>

```
Type: AWS::Connect::Prompt
Properties: 
  [Description](#cfn-connect-prompt-description): String
  [InstanceArn](#cfn-connect-prompt-instancearn): String
  [Name](#cfn-connect-prompt-name): String
  [S3Uri](#cfn-connect-prompt-s3uri): String
  [Tags](#cfn-connect-prompt-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-connect-prompt-properties"></a>

`Description`  <a name="cfn-connect-prompt-description"></a>
The description of the prompt\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`InstanceArn`  <a name="cfn-connect-prompt-instancearn"></a>
The identifier of the Amazon Connect instance\.   
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-connect-prompt-name"></a>
The name of the prompt\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`S3Uri`  <a name="cfn-connect-prompt-s3uri"></a>
The URI for the S3 bucket where the prompt is stored\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-connect-prompt-tags"></a>
The tags used to organize, track, or control access for this resource\. For example, \{ "tags": \{"key1":"value1", "key2":"value2"\} \}\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-connect-prompt-return-values"></a>

### Ref<a name="aws-resource-connect-prompt-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref`function, `Ref`returns the quick rule name\. For example:

`{ "Ref": "myPromptName" }`

For more information about using the `Ref`function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-connect-prompt-return-values-fn--getatt"></a>

The `Fn::GetAtt`intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt`intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-connect-prompt-return-values-fn--getatt-fn--getatt"></a>

`PromptArn`  <a name="PromptArn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the prompt\.