# AWS::APS::RuleGroupsNamespace<a name="aws-resource-aps-rulegroupsnamespace"></a>

The `AWS::APS::RuleGroupsNamespace` resource creates or updates a rule groups namespace within a Amazon Managed Service for Prometheus workspace\. For more information, see [ Recording rules and alerting rules](https://docs.aws.amazon.com/prometheus/latest/userguide/AMP-Ruler.html)\.

## Syntax<a name="aws-resource-aps-rulegroupsnamespace-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-aps-rulegroupsnamespace-syntax.json"></a>

```
{
  "Type" : "AWS::APS::RuleGroupsNamespace",
  "Properties" : {
      "[Data](#cfn-aps-rulegroupsnamespace-data)" : String,
      "[Name](#cfn-aps-rulegroupsnamespace-name)" : String,
      "[Tags](#cfn-aps-rulegroupsnamespace-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[Workspace](#cfn-aps-rulegroupsnamespace-workspace)" : String
    }
}
```

### YAML<a name="aws-resource-aps-rulegroupsnamespace-syntax.yaml"></a>

```
Type: AWS::APS::RuleGroupsNamespace
Properties: 
  [Data](#cfn-aps-rulegroupsnamespace-data): String
  [Name](#cfn-aps-rulegroupsnamespace-name): String
  [Tags](#cfn-aps-rulegroupsnamespace-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [Workspace](#cfn-aps-rulegroupsnamespace-workspace): String
```

## Properties<a name="aws-resource-aps-rulegroupsnamespace-properties"></a>

`Data`  <a name="cfn-aps-rulegroupsnamespace-data"></a>
The rules definition file for this namespace\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-aps-rulegroupsnamespace-name"></a>
The name of the rule groups namespace\. This property is required\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-aps-rulegroupsnamespace-tags"></a>
A list of key and value pairs for the workspace resources\.   
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Workspace`  <a name="cfn-aps-rulegroupsnamespace-workspace"></a>
The ARN of the workspace that contains this rule groups namespace\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-aps-rulegroupsnamespace-return-values"></a>

### Ref<a name="aws-resource-aps-rulegroupsnamespace-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the ARN of the rules group namespace\. For example, `arn:aws:aps:us-west-2:123456789012:rulegroupsnamespace/ws-EXAMPLE-3687-4ac9-853c-EXAMPLEe8f/amp-rules`\. 

### Fn::GetAtt<a name="aws-resource-aps-rulegroupsnamespace-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-aps-rulegroupsnamespace-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The ARN of the rules group namespace\. For example, `arn:aws:aps:us-west-2:123456789012:rulegroupsnamespace/ws-EXAMPLE-3687-4ac9-853c-EXAMPLEe8f/amp=rules`