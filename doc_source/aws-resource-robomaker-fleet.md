# AWS::RoboMaker::Fleet<a name="aws-resource-robomaker-fleet"></a>

The `AWS::RoboMaker::Fleet` resource creates an AWS RoboMaker fleet\. Fleets contain robots and can receive deployments\. For more information, see [API\_CreateFleet](https://docs.aws.amazon.com/robomaker/latest/dg/API_CreateFleet) in the *RoboMaker Developer Guide*\. 

## Syntax<a name="aws-resource-robomaker-fleet-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-robomaker-fleet-syntax.json"></a>

```
{
  "Type" : "AWS::RoboMaker::Fleet",
  "Properties" : {
    "[Name](#cfn-robomaker-fleet-name)" : String,
    "[Tags](#cfn-robomaker-fleet-tags)" : JSON object
  }
}
```

### YAML<a name="aws-resource-robomaker-fleet-syntax.yaml"></a>

```
Type: "AWS::RoboMaker::Fleet"
Properties:
  [Name](#cfn-robomaker-fleet-name): String
  [Tags](#cfn-robomaker-fleet-tags): JSON object
```

## Properties<a name="aws-resource-robomaker-fleet-properties"></a>

`Name`  <a name="cfn-robomaker-fleet-name"></a>
The name of the fleet\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`Tags`  <a name="cfn-robomaker-fleet-tags"></a>
An array of key\-value pairs\. For more information, see [Using Cost Allocation Tags](https://docs.aws.amazon.com/awsaccountbilling/latest/aboutv2/cost-alloc-tags.html) in the *AWS Billing and Cost Management User Guide*\.  
 *Required*: No  
 *Type*: JSON object  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## Return Values<a name="aws-resource-robomaker-fleet-returnvalues"></a>

### Ref<a name="aws-resource-robomaker-fleet-ref"></a>

When you pass the logical ID of an `AWS::RoboMaker::Fleet` resource to the intrinsic `Ref` function, the function returns the Amazon Resource Name \(ARN\) of the fleet, such as `arn:aws:robomaker:us-west-2:123456789012:deployment-fleet/MyFleet/1539894765711`\. 

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\. 

### Fn::GetAtt<a name="aws-resource-robomaker-fleet-getatt"></a>

 `Fn::GetAtt` returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\. 

`Arn`  
The Amazon Resource Name \(ARN\) of the fleet, such as `arn:aws:robomaker:us-west-2:123456789012:deployment-fleet/MyFleet/1539894765711`\. 

For more information about using `Fn::GetAtt`, see [Fn::GetAtt](intrinsic-function-reference-getatt.md)\. 

## Examples<a name="aws-resource-robomaker-fleet-examples"></a>

### Create an AWS RoboMaker Fleet<a name="aws-resource-robomaker-fleet-example1"></a>

The following example creates a fleet\.

#### JSON<a name="aws-resource-robomaker-fleet-example1.json"></a>

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

#### YAML<a name="aws-resource-robomaker-fleet-example1.yaml"></a>

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