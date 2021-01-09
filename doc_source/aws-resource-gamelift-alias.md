# AWS::GameLift::Alias<a name="aws-resource-gamelift-alias"></a>

The `AWS::GameLift::Alias` resource creates an alias for an Amazon GameLift \(GameLift\) fleet destination\. There are two types of routing strategies for aliases: simple and terminal\. A simple alias points to an active fleet\. A terminal alias displays a message instead of routing players to an active fleet\. For example, a terminal alias might display a URL link that directs players to an upgrade site\. You can use aliases to define destinations in a game session queue or when requesting new game sessions\. 

## Syntax<a name="aws-resource-gamelift-alias-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-gamelift-alias-syntax.json"></a>

```
{
  "Type" : "AWS::GameLift::Alias",
  "Properties" : {
      "[Description](#cfn-gamelift-alias-description)" : String,
      "[Name](#cfn-gamelift-alias-name)" : String,
      "[RoutingStrategy](#cfn-gamelift-alias-routingstrategy)" : RoutingStrategy
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
    RoutingStrategy
```

## Properties<a name="aws-resource-gamelift-alias-properties"></a>

`Description`  <a name="cfn-gamelift-alias-description"></a>
A human\-readable description of the alias\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1024`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-gamelift-alias-name"></a>
A descriptive label that is associated with an alias\. Alias names do not need to be unique\.  
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

## Return values<a name="aws-resource-gamelift-alias-return-values"></a>

### Ref<a name="aws-resource-gamelift-alias-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the alias ID, such as `alias-1111aaaa-22bb-33cc-44dd-5555eeee66ff`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-gamelift-alias-return-values-fn--getatt"></a>

#### <a name="aws-resource-gamelift-alias-return-values-fn--getatt-fn--getatt"></a>

`AliasId`  <a name="AliasId-fn::getatt"></a>
Not currently supported by AWS CloudFormation\.

## Examples<a name="aws-resource-gamelift-alias--examples"></a>



### Create a Simple Alias<a name="aws-resource-gamelift-alias--examples--Create_a_Simple_Alias"></a>

The following example creates a simple alias for a fleet\. The template uses `!Ref` to reference a fleet resource, which can be declared elsewhere in the same template\.

#### JSON<a name="aws-resource-gamelift-alias--examples--Create_a_Simple_Alias--json"></a>

```
{
    "Resources": {
        "AliasResource": {
            "Properties": {
                "Name": "MyAlias",
                "Description": "My Alias Description",
                "RoutingStrategy": {
                    "Type": "SIMPLE",
                    "FleetId": {
                        "Ref": "FleetResource"
                    }
                }
            },
            "Type": "AWS::GameLift::Alias"
        }
    }
}
```

#### YAML<a name="aws-resource-gamelift-alias--examples--Create_a_Simple_Alias--yaml"></a>

```
Resources:  
  AliasResource:
    Properties:
      Name: MyAlias
      Description: My Alias Description
      RoutingStrategy:
        Type: SIMPLE
        FleetId: !Ref FleetResource
    Type: AWS::GameLift::Alias
```

### Create terminal alias<a name="aws-resource-gamelift-alias--examples--Create_terminal_alias"></a>

The following example creates a terminal alias with a generic terminal message\.

#### JSON<a name="aws-resource-gamelift-alias--examples--Create_terminal_alias--json"></a>

```
{
    "Resources": {
        "AliasResource": {
            "Type": "AWS::GameLift::Alias",
            "Properties": {
                "Name": "MyTerminalAlias",
                "Description": "A terminal alias",
                "RoutingStrategy": {
                    "Type": "TERMINAL",
                    "Message": "Terminal routing strategy message"
                }
            }
        }
    }
}
```

#### YAML<a name="aws-resource-gamelift-alias--examples--Create_terminal_alias--yaml"></a>

```
Resources:
  AliasResource:
    Type: AWS::GameLift::Alias
    Properties:
      Name: MyTerminalAlias
      Description: A terminal alias
      RoutingStrategy:
        Type: TERMINAL
        Message: Terminal routing strategy message
```

## See also<a name="aws-resource-gamelift-alias--seealso"></a>
+ [ Create GameLift Resources Using AWS CloudFormation](https://docs.aws.amazon.com/gamelift/latest/developerguide/resources-cloudformation.html) in the *Amazon GameLift Developer Guide*
+  [Add an Alias to a GameLift Fleet](https://docs.aws.amazon.com/gamelift/latest/developerguide/aliases-creating.html) in the *Amazon GameLift Developer Guide* 
+  [CreateAlias](https://docs.aws.amazon.com/gamelift/latest/apireference/API_CreateAlias.html) in the *Amazon GameLift API Reference* 