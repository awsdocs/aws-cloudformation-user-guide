# AWS::VpcLattice::Rule<a name="aws-resource-vpclattice-rule"></a>

Creates a listener rule\. Each listener has a default rule for checking connection requests, but you can define additional rules\. Each rule consists of a priority, one or more actions, and one or more conditions\. For more information, see [Listener rules](https://docs.aws.amazon.com/vpc-lattice/latest/ug/listeners.html#listener-rules) in the *Amazon VPC Lattice User Guide*\.

## Syntax<a name="aws-resource-vpclattice-rule-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-vpclattice-rule-syntax.json"></a>

```
{
  "Type" : "AWS::VpcLattice::Rule",
  "Properties" : {
      "[Action](#cfn-vpclattice-rule-action)" : Action,
      "[ListenerIdentifier](#cfn-vpclattice-rule-listeneridentifier)" : String,
      "[Match](#cfn-vpclattice-rule-match)" : Match,
      "[Name](#cfn-vpclattice-rule-name)" : String,
      "[Priority](#cfn-vpclattice-rule-priority)" : Integer,
      "[ServiceIdentifier](#cfn-vpclattice-rule-serviceidentifier)" : String,
      "[Tags](#cfn-vpclattice-rule-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-vpclattice-rule-syntax.yaml"></a>

```
Type: AWS::VpcLattice::Rule
Properties: 
  [Action](#cfn-vpclattice-rule-action): 
    Action
  [ListenerIdentifier](#cfn-vpclattice-rule-listeneridentifier): String
  [Match](#cfn-vpclattice-rule-match): 
    Match
  [Name](#cfn-vpclattice-rule-name): String
  [Priority](#cfn-vpclattice-rule-priority): Integer
  [ServiceIdentifier](#cfn-vpclattice-rule-serviceidentifier): String
  [Tags](#cfn-vpclattice-rule-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-vpclattice-rule-properties"></a>

`Action`  <a name="cfn-vpclattice-rule-action"></a>
Describes the action for a rule\. Each rule must include exactly one of the following types of actions: `forward `or `fixed-response`, and it must be the last action to be performed\.  
*Required*: Yes  
*Type*: [Action](aws-properties-vpclattice-rule-action.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ListenerIdentifier`  <a name="cfn-vpclattice-rule-listeneridentifier"></a>
The ID or Amazon Resource Name \(ARN\) of the listener\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Match`  <a name="cfn-vpclattice-rule-match"></a>
The rule match\.  
*Required*: Yes  
*Type*: [Match](aws-properties-vpclattice-rule-match.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-vpclattice-rule-name"></a>
The name of the rule\. The name must be unique within the listener\. The valid characters are a\-z, 0\-9, and hyphens \(\-\)\. You can't use a hyphen as the first or last character, or immediately after another hyphen\.  
If you don't specify a name, CloudFormation generates one\. However, if you specify a name, and later want to replace the resource, you must specify a new name\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Priority`  <a name="cfn-vpclattice-rule-priority"></a>
The priority assigned to the rule\. Each rule for a specific listener must have a unique priority\. The lower the priority number the higher the priority\.  
*Required*: Yes  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ServiceIdentifier`  <a name="cfn-vpclattice-rule-serviceidentifier"></a>
The ID or Amazon Resource Name \(ARN\) of the service\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-vpclattice-rule-tags"></a>
The tags for the rule\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-vpclattice-rule-return-values"></a>

### Ref<a name="aws-resource-vpclattice-rule-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the Amazon Resource Name \(ARN\) of the rule\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-vpclattice-rule-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-vpclattice-rule-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the rule\.

`Id`  <a name="Id-fn::getatt"></a>
The ID of the listener\.