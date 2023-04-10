# AWS::VpcLattice::Listener<a name="aws-resource-vpclattice-listener"></a>

Creates a listener for a service\. Before you start using your Amazon VPC Lattice service, you must add one or more listeners\. A listener is a process that checks for connection requests to your services\. For more information, see [Listeners](https://docs.aws.amazon.com/vpc-lattice/latest/ug/listeners.html) in the *Amazon VPC Lattice User Guide*\.

## Syntax<a name="aws-resource-vpclattice-listener-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-vpclattice-listener-syntax.json"></a>

```
{
  "Type" : "AWS::VpcLattice::Listener",
  "Properties" : {
      "[DefaultAction](#cfn-vpclattice-listener-defaultaction)" : DefaultAction,
      "[Name](#cfn-vpclattice-listener-name)" : String,
      "[Port](#cfn-vpclattice-listener-port)" : Integer,
      "[Protocol](#cfn-vpclattice-listener-protocol)" : String,
      "[ServiceIdentifier](#cfn-vpclattice-listener-serviceidentifier)" : String,
      "[Tags](#cfn-vpclattice-listener-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-vpclattice-listener-syntax.yaml"></a>

```
Type: AWS::VpcLattice::Listener
Properties: 
  [DefaultAction](#cfn-vpclattice-listener-defaultaction): 
    DefaultAction
  [Name](#cfn-vpclattice-listener-name): String
  [Port](#cfn-vpclattice-listener-port): Integer
  [Protocol](#cfn-vpclattice-listener-protocol): String
  [ServiceIdentifier](#cfn-vpclattice-listener-serviceidentifier): String
  [Tags](#cfn-vpclattice-listener-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-vpclattice-listener-properties"></a>

`DefaultAction`  <a name="cfn-vpclattice-listener-defaultaction"></a>
The action for the default rule\. Each listener has a default rule\. Each rule consists of a priority, one or more actions, and one or more conditions\. The default rule is the rule that's used if no other rules match\. Each rule must include exactly one of the following types of actions: `forward `or `fixed-response`, and it must be the last action to be performed\.   
*Required*: Yes  
*Type*: [DefaultAction](aws-properties-vpclattice-listener-defaultaction.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-vpclattice-listener-name"></a>
The name of the listener\. A listener name must be unique within a service\. The valid characters are a\-z, 0\-9, and hyphens \(\-\)\. You can't use a hyphen as the first or last character, or immediately after another hyphen\.  
If you don't specify a name, CloudFormation generates one\. However, if you specify a name, and later want to replace the resource, you must specify a new name\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Port`  <a name="cfn-vpclattice-listener-port"></a>
The listener port\. You can specify a value from `1` to `65535`\. For HTTP, the default is `80`\. For HTTPS, the default is `443`\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Protocol`  <a name="cfn-vpclattice-listener-protocol"></a>
The listener protocol HTTP or HTTPS\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ServiceIdentifier`  <a name="cfn-vpclattice-listener-serviceidentifier"></a>
The ID or Amazon Resource Name \(ARN\) of the service\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-vpclattice-listener-tags"></a>
The tags for the listener\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-vpclattice-listener-return-values"></a>

### Ref<a name="aws-resource-vpclattice-listener-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the Amazon Resource Name \(ARN\) of the listener\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-vpclattice-listener-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-vpclattice-listener-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the listener\.

`Id`  <a name="Id-fn::getatt"></a>
The ID of the listener\.

`ServiceArn`  <a name="ServiceArn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the service\.

`ServiceId`  <a name="ServiceId-fn::getatt"></a>
The ID of the service\.