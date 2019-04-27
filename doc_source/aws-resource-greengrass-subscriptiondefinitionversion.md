# AWS::Greengrass::SubscriptionDefinitionVersion<a name="aws-resource-greengrass-subscriptiondefinitionversion"></a>

The `AWS::Greengrass::SubscriptionDefinitionVersion` resource represents a subscription definition version for AWS IoT Greengrass\. A subscription definition version contains a list of subscriptions\.

**Note**  
To create a subscription definition version, you must specify the ID of the subscription definition that you want to associate with the version\. For information about creating a subscription definition, see [AWS::Greengrass::SubscriptionDefinition](aws-resource-greengrass-subscriptiondefinition.md)\.  
After you create a subscription definition version that contains the subscriptions you want to deploy, you must add it to your group version\. For more information, see [AWS::Greengrass::Group](aws-resource-greengrass-group.md)\.

## Syntax<a name="aws-resource-greengrass-subscriptiondefinitionversion-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-greengrass-subscriptiondefinitionversion-syntax.json"></a>

```
{
  "Type" : "AWS::Greengrass::SubscriptionDefinitionVersion",
  "Properties" : {
    "[SubscriptionDefinitionId](#cfn-greengrass-subscriptiondefinitionversion-subscriptiondefinitionid)" : String,
    "[Subscriptions](#cfn-greengrass-subscriptiondefinitionversion-subscriptions)" : [ [*Subscription*](aws-properties-greengrass-subscriptiondefinitionversion-subscription.md), ... ]
  }
}
```

### YAML<a name="aws-resource-greengrass-subscriptiondefinitionversion-syntax.yaml"></a>

```
Type: "AWS::Greengrass::SubscriptionDefinitionVersion"
Properties:
  [SubscriptionDefinitionId](#cfn-greengrass-subscriptiondefinitionversion-subscriptiondefinitionid): String
  [Subscriptions](#cfn-greengrass-subscriptiondefinitionversion-subscriptions): 
    - [*Subscription*](aws-properties-greengrass-subscriptiondefinitionversion-subscription.md)
```

## Properties<a name="aws-resource-greengrass-subscriptiondefinitionversion-properties"></a>

`SubscriptionDefinitionId`  <a name="cfn-greengrass-subscriptiondefinitionversion-subscriptiondefinitionid"></a>
The ID of the subscription definition associated with this version\. This value is a GUID\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`Subscriptions`  <a name="cfn-greengrass-subscriptiondefinitionversion-subscriptions"></a>
The subscriptions in this version\.  
 *Required*: Yes  
 *Type*: List of [Subscription](aws-properties-greengrass-subscriptiondefinitionversion-subscription.md) property types  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

## Return Values<a name="aws-resource-greengrass-subscriptiondefinitionversion-returnvalues"></a>

### Ref<a name="aws-resource-greengrass-subscriptiondefinitionversion-ref"></a>

When you pass the logical ID of an `AWS::Greengrass::SubscriptionDefinitionVersion` resource to the intrinsic `Ref` function, the function returns the Amazon Resource Name \(ARN\) of the subscription definition version, such as `arn:aws:greengrass:us-east-1:123456789012:/greengrass/definition/subscriptions/1234a5b6-78cd-901e-2fgh-3i45j6k178l9/versions/9876ac30-4bdb-4f9d-95af-b5fdb66be1a2`\. 

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\. 

## Examples<a name="aws-resource-greengrass-subscriptiondefinitionversion-examples"></a>

### Subscription Definition Version<a name="aws-resource-greengrass-subscriptiondefinitionversion-example1"></a>

The following snippet defines subscription definition and subscription definition version resources\. The subscription definition version references the subscription definition and contains a subscription\. In this example, the subscription source is an existing device in the group\. The target is a function in the group that was created in another stack \(and referenced using the `ImportValue` function\)\.

For an example of a complete template, see the [Group](aws-resource-greengrass-group.md#aws-resource-greengrass-group-examples) resource\.

#### JSON<a name="aws-resource-greengrass-subscriptiondefinitionversion-example1.json"></a>

```
"TestSubscriptionDefinition": {
    "Type": "AWS::Greengrass::SubscriptionDefinition",
    "Properties": {
        "Name": "DemoTestSubscriptionDefinition"
    }
},
"TestSubscriptionDefinitionVersion": {
    "Type": "AWS::Greengrass::SubscriptionDefinitionVersion",
    "Properties": {
        "SubscriptionDefinitionId": {
            "Ref": "TestSubscriptionDefinition"
        },
        "Subscriptions": [
            {
                "Id": "TestSubscription1",
                "Source": {
                    "Fn::Join": [
                        ":",
                        [
                            "arn:aws:iot",
                            {
                                "Ref": "AWS::Region"
                            },
                            {
                                "Ref": "AWS::AccountId"
                            },
                            "thing/TestDevice1"
                        ]
                    ]
                },
                "Subject": "some/topic",
                "Target": {
                    "Fn::ImportValue": "TestCanaryLambdaVersionArn"
                }
            }
        ]
    }
}
```

#### YAML<a name="aws-resource-greengrass-subscriptiondefinitionversion-example1.yaml"></a>

```
TestSubscriptionDefinition:
  Type: 'AWS::Greengrass::SubscriptionDefinition'
  Properties:
    Name: DemoTestSubscriptionDefinition
TestSubscriptionDefinitionVersion:
  Type: 'AWS::Greengrass::SubscriptionDefinitionVersion'
  Properties:
    SubscriptionDefinitionId: !Ref TestSubscriptionDefinition
    Subscriptions:
      - Id: TestSubscription1
        Source: !Join 
          - ':'
          - - 'arn:aws:iot'
            - !Ref 'AWS::Region'
            - !Ref 'AWS::AccountId'
            - thing/TestDevice1
        Subject: some/topic
        Target: !ImportValue TestCanaryLambdaVersionArn
```

## See Also<a name="aws-resource-greengrass-subscriptiondefinitionversion-seealso"></a>
+ [SubscriptionDefinitionVersion](https://docs.aws.amazon.com/greengrass/latest/apireference/definitions-subscriptiondefinitionversion.html) in the *AWS IoT Greengrass API Reference*
+ [AWS IoT Greengrass Developer Guide](https://docs.aws.amazon.com/greengrass/latest/developerguide/)