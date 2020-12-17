# AWS::RoboMaker::Fleet<a name="aws-resource-robomaker-fleet"></a>

The `AWS::RoboMaker::Fleet` resource creates an AWS RoboMaker fleet\. Fleets contain robots and can receive deployments\.

## Syntax<a name="aws-resource-robomaker-fleet-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-robomaker-fleet-syntax.json"></a>

```
{
  "Type" : "AWS::RoboMaker::Fleet",
  "Properties" : {
      "[Name](#cfn-robomaker-fleet-name)" : String,
      "[Tags](#cfn-robomaker-fleet-tags)" : Json
    }
}
```

### YAML<a name="aws-resource-robomaker-fleet-syntax.yaml"></a>

```
Type: AWS::RoboMaker::Fleet
Properties: 
  [Name](#cfn-robomaker-fleet-name): String
  [Tags](#cfn-robomaker-fleet-tags): Json
```

## Properties<a name="aws-resource-robomaker-fleet-properties"></a>

`Name`  <a name="cfn-robomaker-fleet-name"></a>
The name of the fleet\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `255`  
*Pattern*: `[a-zA-Z0-9_\-]*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-robomaker-fleet-tags"></a>
The list of all tags added to the fleet\.  
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-robomaker-fleet-return-values"></a>

### Ref<a name="aws-resource-robomaker-fleet-return-values-ref"></a>

When you pass the logical ID of an `AWS::RoboMaker::Fleet` resource to the intrinsic `Ref` function, the function returns the Amazon Resource Name \(ARN\) of the fleet, such as `arn:aws:robomaker:us-west-2:123456789012:deployment-fleet/MyFleet/1539894765711`\. 

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-robomaker-fleet-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-robomaker-fleet-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the fleet, such as `arn:aws:robomaker:us-west-2:123456789012:deployment-fleet/MyFleet/1539894765711`\.

## Examples<a name="aws-resource-robomaker-fleet--examples"></a>



### Specifies an AWS RoboMaker Fleet<a name="aws-resource-robomaker-fleet--examples--Specifies_an_AWS_RoboMaker_Fleet"></a>

The following example creates a fleet\.

#### JSON<a name="aws-resource-robomaker-fleet--examples--Specifies_an_AWS_RoboMaker_Fleet--json"></a>

```
{
  "Description": "RoboMaker Fleet example",
  "Resources": {
    "BasicFleet": {
      "Type": "AWS::RoboMaker::Fleet",
      "Properties": {
        "Name": "MyFleet",
        "Tags": {
          "Name": "BasicFleet",
          "Type": "CFN"
        }
      }
    }
  },
  "Outputs": {
    "Fleet": {
      "Value": "BasicFleet"
    }
  }
}
```

#### YAML<a name="aws-resource-robomaker-fleet--examples--Specifies_an_AWS_RoboMaker_Fleet--yaml"></a>

```
---
Description: "RoboMaker Fleet example"
Resources:
  BasicFleet:
    Type: "AWS::RoboMaker::Fleet"
    Properties:
      Name: "MyFleet"
      Tags:
        "Name" : "BasicFleet"
        "Type" : "CFN"
Outputs:
  Fleet:
    Value: !Ref BasicFleet
```