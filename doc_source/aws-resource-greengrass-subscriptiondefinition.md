# AWS::Greengrass::SubscriptionDefinition<a name="aws-resource-greengrass-subscriptiondefinition"></a>

The `AWS::Greengrass::SubscriptionDefinition` resource represents a subscription definition for AWS IoT Greengrass\. Subscription definitions are used to organize your subscription definition versions\.

Subscription definitions can reference multiple subscription definition versions\.

![\[A subscription definition hierarchy with associated subscription definition versions and subscriptions.\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/images/greengrass/gg-subscription.png)

All subscription definition versions must be associated with a subscription definition\. Each subscription definition version can contain one or more subscriptions\.

**Note**  
When you create a subscription definition, you can optionally include an initial subscription definition version\. To associate a subscription definition version later, create an [AWS::Greengrass::SubscriptionDefinitionVersion](aws-resource-greengrass-subscriptiondefinitionversion.md) resource and specify the ID of this subscription definition\.  
After you create the subscription definition version that contains the subscriptions you want to deploy, you must add it to your group version\. For more information, see [AWS::Greengrass::Group](aws-resource-greengrass-group.md)\.

## Syntax<a name="aws-resource-greengrass-subscriptiondefinition-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-greengrass-subscriptiondefinition-syntax.json"></a>

```
{
  "Type" : "AWS::Greengrass::SubscriptionDefinition",
  "Properties" : {
    "[InitialVersion](#cfn-greengrass-subscriptiondefinition-initialversion)" : [*SubscriptionDefinitionVersion*](aws-properties-greengrass-subscriptiondefinition-subscriptiondefinitionversion.md),
    "[Name](#cfn-greengrass-subscriptiondefinition-name)" : String
  }
}
```

### YAML<a name="aws-resource-greengrass-subscriptiondefinition-syntax.yaml"></a>

```
Type: "AWS::Greengrass::SubscriptionDefinition"
Properties:
  [InitialVersion](#cfn-greengrass-subscriptiondefinition-initialversion): 
    [*SubscriptionDefinitionVersion*](aws-properties-greengrass-subscriptiondefinition-subscriptiondefinitionversion.md)
  [Name](#cfn-greengrass-subscriptiondefinition-name): String
```

## Properties<a name="aws-resource-greengrass-subscriptiondefinition-properties"></a>

`InitialVersion`  <a name="cfn-greengrass-subscriptiondefinition-initialversion"></a>
The subscription definition version to include when the subscription definition is created\. A subscription definition version contains a list of [`subscription`](aws-properties-greengrass-subscriptiondefinition-subscription.md) property types\.  
To associate a subscription definition version after the subscription definition is created, create an [AWS::Greengrass::SubscriptionDefinitionVersion](aws-resource-greengrass-subscriptiondefinitionversion.md) resource and specify the ID of this subscription definition\.
 *Required*: No  
 *Type*: [SubscriptionDefinitionVersion](aws-properties-greengrass-subscriptiondefinition-subscriptiondefinitionversion.md)  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`Name`  <a name="cfn-greengrass-subscriptiondefinition-name"></a>
The name of the subscription definition\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## Return Values<a name="aws-resource-greengrass-subscriptiondefinition-returnvalues"></a>

### Ref<a name="aws-resource-greengrass-subscriptiondefinition-ref"></a>

When you pass the logical ID of an `AWS::Greengrass::SubscriptionDefinition` resource to the intrinsic `Ref` function, the function returns the ID of the subscription definition, such as `1234a5b6-78cd-901e-2fgh-3i45j6k178l9`\. 

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\. 

### Fn::GetAtt<a name="aws-resource-greengrass-subscriptiondefinition-getatt"></a>

 `Fn::GetAtt` returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\. 

`LatestVersionArn`  
The Amazon Resource Name \(ARN\) of the last `SubscriptionDefinitionVersion` that was added to the `SubscriptionDefinition`, such as `arn:aws:greengrass:us-east-1:123456789012:/greengrass/definition/subscriptions/1234a5b6-78cd-901e-2fgh-3i45j6k178l9/versions/9876ac30-4bdb-4f9d-95af-b5fdb66be1a2`\. 

`Id`  
The ID of the `SubscriptionDefinition`, such as `1234a5b6-78cd-901e-2fgh-3i45j6k178l9`\. 

`Arn`  
The ARN of the `SubscriptionDefinition`, such as `arn:aws:greengrass:us-east-1:123456789012:/greengrass/definition/subscriptions/1234a5b6-78cd-901e-2fgh-3i45j6k178l9`\. 

`Name`  
The name of the `SubscriptionDefinition`, such as `MySubscriptionDefinition`\. 

For more information about using `Fn::GetAtt`, see [Fn::GetAtt](intrinsic-function-reference-getatt.md)\. 

## Examples<a name="aws-resource-greengrass-subscriptiondefinition-examples"></a>

### Subscription Definition Snippet<a name="aws-resource-greengrass-subscriptiondefinition-example1"></a>

The following snippet defines a subscription definition resource with an initial version that contains a subscription\. In this example, the subscription source is an existing device in the group\. The target is a function in the group that was created in another stack \(and referenced using the `ImportValue` function\)\.

For an example of a complete template, see the [Group](aws-resource-greengrass-group.md#aws-resource-greengrass-group-examples) resource\.

#### JSON<a name="aws-resource-greengrass-subscriptiondefinition-example1.json"></a>

```
"TestSubscriptionDefinition": {
    "Type": "AWS::Greengrass::SubscriptionDefinition",
    "Properties": {
        "Name": "DemoTestSubscriptionDefinition",
        "InitialVersion": {
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
}
```

#### YAML<a name="aws-resource-greengrass-subscriptiondefinition-example1.yaml"></a>

```
TestSubscriptionDefinition:
  Type: 'AWS::Greengrass::SubscriptionDefinition'
  Properties:
    Name: DemoTestSubscriptionDefinition
    InitialVersion:
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

## See Also<a name="aws-resource-greengrass-subscriptiondefinition-seealso"></a>
+ [CreateSubscriptionDefinition](https://docs.aws.amazon.com/greengrass/latest/apireference/createsubscriptiondefinition-post.html) in the *AWS IoT Greengrass API Reference*
+ [AWS IoT Greengrass Developer Guide](https://docs.aws.amazon.com/greengrass/latest/developerguide/)