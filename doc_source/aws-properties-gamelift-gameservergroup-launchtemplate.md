# AWS::GameLift::GameServerGroup LaunchTemplate<a name="aws-properties-gamelift-gameservergroup-launchtemplate"></a>

 **This data type is used with the GameLift FleetIQ and game server groups\.** 

An Amazon EC2 launch template that contains configuration settings and game server code to be deployed to all instances in a game server group\. The launch template is specified when creating a new game server group with `GameServerGroup`\. 

## Syntax<a name="aws-properties-gamelift-gameservergroup-launchtemplate-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-gamelift-gameservergroup-launchtemplate-syntax.json"></a>

```
{
  "[LaunchTemplateId](#cfn-gamelift-gameservergroup-launchtemplate-launchtemplateid)" : String,
  "[LaunchTemplateName](#cfn-gamelift-gameservergroup-launchtemplate-launchtemplatename)" : String,
  "[Version](#cfn-gamelift-gameservergroup-launchtemplate-version)" : String
}
```

### YAML<a name="aws-properties-gamelift-gameservergroup-launchtemplate-syntax.yaml"></a>

```
  [LaunchTemplateId](#cfn-gamelift-gameservergroup-launchtemplate-launchtemplateid): String
  [LaunchTemplateName](#cfn-gamelift-gameservergroup-launchtemplate-launchtemplatename): String
  [Version](#cfn-gamelift-gameservergroup-launchtemplate-version): String
```

## Properties<a name="aws-properties-gamelift-gameservergroup-launchtemplate-properties"></a>

`LaunchTemplateId`  <a name="cfn-gamelift-gameservergroup-launchtemplate-launchtemplateid"></a>
A unique identifier for an existing Amazon EC2 launch template\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `255`  
*Pattern*: `[\u0020-\uD7FF\uE000-\uFFFD\uD800\uDC00-\uDBFF\uDFFF\r\n\t]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LaunchTemplateName`  <a name="cfn-gamelift-gameservergroup-launchtemplate-launchtemplatename"></a>
A readable identifier for an existing Amazon EC2 launch template\.   
*Required*: No  
*Type*: String  
*Minimum*: `3`  
*Maximum*: `128`  
*Pattern*: `[a-zA-Z0-9\(\)\.\-/_]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Version`  <a name="cfn-gamelift-gameservergroup-launchtemplate-version"></a>
The version of the Amazon EC2 launch template to use\. If no version is specified, the default version will be used\. With Amazon EC2, you can specify a default version for a launch template\. If none is set, the default is the first version created\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Pattern*: `[\u0020-\uD7FF\uE000-\uFFFD\uD800\uDC00-\uDBFF\uDFFF\r\n\t]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)