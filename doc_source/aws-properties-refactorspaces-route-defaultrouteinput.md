# AWS::RefactorSpaces::Route DefaultRouteInput<a name="aws-properties-refactorspaces-route-defaultrouteinput"></a>

 The configuration for the default route type\. 

## Syntax<a name="aws-properties-refactorspaces-route-defaultrouteinput-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-refactorspaces-route-defaultrouteinput-syntax.json"></a>

```
{
  "[ActivationState](#cfn-refactorspaces-route-defaultrouteinput-activationstate)" : String
}
```

### YAML<a name="aws-properties-refactorspaces-route-defaultrouteinput-syntax.yaml"></a>

```
  [ActivationState](#cfn-refactorspaces-route-defaultrouteinput-activationstate): String
```

## Properties<a name="aws-properties-refactorspaces-route-defaultrouteinput-properties"></a>

`ActivationState`  <a name="cfn-refactorspaces-route-defaultrouteinput-activationstate"></a>
If set to `ACTIVE`, traffic is forwarded to this route’s service after the route is created\.   
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)