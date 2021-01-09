# AWS::SecurityHub::Hub<a name="aws-resource-securityhub-hub"></a>

The `AWS::SecurityHub::Hub` resource represents the implementation of the AWS Security Hub service in your account\. One hub resource is created for each Region in which you enable Security Hub\.

## Syntax<a name="aws-resource-securityhub-hub-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-securityhub-hub-syntax.json"></a>

```
{
  "Type" : "AWS::SecurityHub::Hub",
  "Properties" : {
      "[Tags](#cfn-securityhub-hub-tags)" : Json
    }
}
```

### YAML<a name="aws-resource-securityhub-hub-syntax.yaml"></a>

```
Type: AWS::SecurityHub::Hub
Properties: 
  [Tags](#cfn-securityhub-hub-tags): Json
```

## Properties<a name="aws-resource-securityhub-hub-properties"></a>

`Tags`  <a name="cfn-securityhub-hub-tags"></a>
The tags to add to the hub resource\.  
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-securityhub-hub-return-values"></a>

### Ref<a name="aws-resource-securityhub-hub-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the `HubArn` for the hub resource created, such as `arn:aws:securityhub:us-east-1:12345678910:hub/default`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-securityhub-hub--examples"></a>



### Declare a Hub Resource<a name="aws-resource-securityhub-hub--examples--Declare_a_Hub_Resource"></a>

The following example shows how to declare a Security Hub `Hub` resource:

#### JSON<a name="aws-resource-securityhub-hub--examples--Declare_a_Hub_Resource--json"></a>

```
{
    "Description": "Example Hub with Tags",
    "Resources": {
        "ExampleHubWithTags": {
            "Type": "AWS::SecurityHub::Hub",
            "Properties": {
                "Tags": {
                    "key1": "value1",
                    "key2": "value2"
                }
            }
        }
    },
    "Outputs": {
        "HubArn": {
            "Value": {
                "Ref": "ExampleHubWithTags"
            }
        }
    }
}
```

#### YAML<a name="aws-resource-securityhub-hub--examples--Declare_a_Hub_Resource--yaml"></a>

```
Description: Example Hub with Tags
Resources:
  ExampleHubWithTags:
    Type: 'AWS::SecurityHub::Hub'
    Properties:
      Tags:
        key1: value1
        key2: value2
Outputs:
  HubArn:
    Value: !Ref ExampleHubWithTags
```