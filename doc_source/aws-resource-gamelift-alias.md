# AWS::GameLift::Alias<a name="aws-resource-gamelift-alias"></a>

The `AWS::GameLift::Alias` resource creates an alias for an Amazon GameLift \(GameLift\) fleet, which you can use to anonymize your fleet\. You can reference the alias instead of a specific fleet when you create game sessions\. For more information, see the [CreateAlias](https://docs.aws.amazon.com/gamelift/latest/apireference/API_CreateAlias.html) action in the *Amazon GameLift API Reference*\.

## Syntax<a name="aws-resource-gamelift-alias-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-gamelift-alias-syntax.json"></a>

```
{
  "Type" : "AWS::GameLift::Alias",
  "Properties" : {
      "[Description](#cfn-gamelift-alias-description)" : String,
      "[Name](#cfn-gamelift-alias-name)" : String,
      "[RoutingStrategy](#cfn-gamelift-alias-routingstrategy)" : [RoutingStrategy](aws-properties-gamelift-alias-routingstrategy.md)
    }
}
```

### YAML<a name="aws-resource-gamelift-alias-syntax.yaml"></a>

```
Type: AWS::GameLift::Alias
Properties: 
  [Description](#cfn-gamelift-alias-description): String
  [Name](#cfn-gamelift-alias-name): String
  [RoutingStrategy](#cfn-gamelift-alias-routingstrategy): 
    [RoutingStrategy](aws-properties-gamelift-alias-routingstrategy.md)
```

## Properties<a name="aws-resource-gamelift-alias-properties"></a>

`Description`  <a name="cfn-gamelift-alias-description"></a>
Human\-readable description of an alias\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1024`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-gamelift-alias-name"></a>
Descriptive label that is associated with an alias\. Alias names do not need to be unique\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1024`  
*Pattern*: `.*\S.*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RoutingStrategy`  <a name="cfn-gamelift-alias-routingstrategy"></a>
A routing configuration that specifies where traffic is directed for this alias, such as to a fleet or to a message\.  
*Required*: Yes  
*Type*: [RoutingStrategy](aws-properties-gamelift-alias-routingstrategy.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return Values<a name="aws-resource-gamelift-alias-return-values"></a>

### Ref<a name="aws-resource-gamelift-alias-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the alias ID, such as `myalias-a01234b56-7890-1de2-f345-g67h8i901j2k`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-gamelift-alias--examples"></a>

### Create terminal alias<a name="aws-resource-gamelift-alias--examples--Create_terminal_alias"></a>

The following example creates a terminal alias named `TerminalAlias` with a generic terminal message\.

#### JSON<a name="aws-resource-gamelift-alias--examples--Create_terminal_alias--json"></a>

```
"AliasResource": {
  "Type": "AWS::GameLift::Alias",
  "Properties": {
    "Name": "TerminalAlias",
    "Description": "A terminal alias",
    "RoutingStrategy": {
      "Type": "TERMINAL",
      "Message": "Terminal routing strategy message"
    }
  }
}
```

#### YAML<a name="aws-resource-gamelift-alias--examples--Create_terminal_alias--yaml"></a>

```
AliasResource: 
  Type: AWS::GameLift::Alias
  Properties: 
    Name: "TerminalAlias"
    Description: "A terminal alias"
    RoutingStrategy: 
      Type: "TERMINAL"
      Message: "Terminal routing strategy message"
```

## See Also<a name="aws-resource-gamelift-alias--seealso"></a>
+  [CreateAlias](https://docs.aws.amazon.com/gamelift/latest/apireference/API_CreateAlias.html) in the *Amazon GameLift API Reference* 

## Supported Regions

This ResourceType is supported by ***all*** regions.