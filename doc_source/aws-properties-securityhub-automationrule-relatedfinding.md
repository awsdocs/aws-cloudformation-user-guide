# AWS::SecurityHub::AutomationRule RelatedFinding<a name="aws-properties-securityhub-automationrule-relatedfinding"></a>

 Provides details about a list of findings that the current finding relates to\. 

## Syntax<a name="aws-properties-securityhub-automationrule-relatedfinding-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-securityhub-automationrule-relatedfinding-syntax.json"></a>

```
{
  "[Id](#cfn-securityhub-automationrule-relatedfinding-id)" : Json,
  "[ProductArn](#cfn-securityhub-automationrule-relatedfinding-productarn)" : String
}
```

### YAML<a name="aws-properties-securityhub-automationrule-relatedfinding-syntax.yaml"></a>

```
  [Id](#cfn-securityhub-automationrule-relatedfinding-id): Json
  [ProductArn](#cfn-securityhub-automationrule-relatedfinding-productarn): String
```

## Properties<a name="aws-properties-securityhub-automationrule-relatedfinding-properties"></a>

`Id`  <a name="cfn-securityhub-automationrule-relatedfinding-id"></a>
 The product\-generated identifier for a related finding\.   
 Array Members: Minimum number of 1 item\. Maximum number of 20 items\.   
*Required*: Yes  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ProductArn`  <a name="cfn-securityhub-automationrule-relatedfinding-productarn"></a>
 The Amazon Resource Name \(ARN\) for the product that generated a related finding\.   
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)