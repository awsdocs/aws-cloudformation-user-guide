# AWS::Lex::ResourcePolicy<a name="aws-resource-lex-resourcepolicy"></a>

**Note**  
Amazon Lex V2 is the only supported version in AWS CloudFormation\.

Specifies a new resource policy with the specified policy statements\.

## Syntax<a name="aws-resource-lex-resourcepolicy-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-lex-resourcepolicy-syntax.json"></a>

```
{
  "Type" : "AWS::Lex::ResourcePolicy",
  "Properties" : {
      "[Policy](#cfn-lex-resourcepolicy-policy)" : Json,
      "[ResourceArn](#cfn-lex-resourcepolicy-resourcearn)" : String
    }
}
```

### YAML<a name="aws-resource-lex-resourcepolicy-syntax.yaml"></a>

```
Type: AWS::Lex::ResourcePolicy
Properties: 
  [Policy](#cfn-lex-resourcepolicy-policy): Json
  [ResourceArn](#cfn-lex-resourcepolicy-resourcearn): String
```

## Properties<a name="aws-resource-lex-resourcepolicy-properties"></a>

`Policy`  <a name="cfn-lex-resourcepolicy-policy"></a>
A resource policy to add to the resource\. The policy is a JSON structure that contains one or more statements that define the policy\. The policy must follow IAM syntax\. If the policy isn't valid, Amazon Lex returns a validation exception\.  
*Required*: Yes  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ResourceArn`  <a name="cfn-lex-resourcepolicy-resourcearn"></a>
The Amazon Resource Name \(ARN\) of the bot or bot alias that the resource policy is attached to\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-lex-resourcepolicy-return-values"></a>

### Fn::GetAtt<a name="aws-resource-lex-resourcepolicy-return-values-fn--getatt"></a>

#### <a name="aws-resource-lex-resourcepolicy-return-values-fn--getatt-fn--getatt"></a>

`Id`  <a name="Id-fn::getatt"></a>
The identifier of the resource policy\.

`RevisionId`  <a name="RevisionId-fn::getatt"></a>
Specifies the current revision of a resource policy\. 