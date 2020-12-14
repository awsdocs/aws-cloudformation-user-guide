# AWS::Greengrass::SubscriptionDefinition<a name="aws-resource-greengrass-subscriptiondefinition"></a>

The `AWS::Greengrass::SubscriptionDefinition` resource represents a subscription definition for AWS IoT Greengrass\. Subscription definitions are used to organize your subscription definition versions\.

Subscription definitions can reference multiple subscription definition versions\. All subscription definition versions must be associated with a subscription definition\. Each subscription definition version can contain one or more subscriptions\.

**Note**  
When you create a subscription definition, you can optionally include an initial subscription definition version\. To associate a subscription definition version later, create an [https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrass-subscriptiondefinitionversion.html](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrass-subscriptiondefinitionversion.html) resource and specify the ID of this subscription definition\.  
After you create the subscription definition version that contains the subscriptions you want to deploy, you must add it to your group version\. For more information, see [https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrass-group.html](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrass-group.html)\.

## Syntax<a name="aws-resource-greengrass-subscriptiondefinition-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-greengrass-subscriptiondefinition-syntax.json"></a>

```
{
  "Type" : "AWS::Greengrass::SubscriptionDefinition",
  "Properties" : {
      "[InitialVersion](#cfn-greengrass-subscriptiondefinition-initialversion)" : SubscriptionDefinitionVersion,
      "[Name](#cfn-greengrass-subscriptiondefinition-name)" : String,
      "[Tags](#cfn-greengrass-subscriptiondefinition-tags)" : Json
    }
}
```

### YAML<a name="aws-resource-greengrass-subscriptiondefinition-syntax.yaml"></a>

```
Type: AWS::Greengrass::SubscriptionDefinition
Properties: 
  [InitialVersion](#cfn-greengrass-subscriptiondefinition-initialversion): 
    SubscriptionDefinitionVersion
  [Name](#cfn-greengrass-subscriptiondefinition-name): String
  [Tags](#cfn-greengrass-subscriptiondefinition-tags): Json
```

## Properties<a name="aws-resource-greengrass-subscriptiondefinition-properties"></a>

`InitialVersion`  <a name="cfn-greengrass-subscriptiondefinition-initialversion"></a>
The subscription definition version to include when the subscription definition is created\. A subscription definition version contains a list of [ `subscription` ](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-greengrass-subscriptiondefinition-subscription.html) property types\.  
To associate a subscription definition version after the subscription definition is created, create an [ `AWS::Greengrass::SubscriptionDefinitionVersion` ](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrass-subscriptiondefinitionversion.html) resource and specify the ID of this subscription definition\.
*Required*: No  
*Type*: [SubscriptionDefinitionVersion](aws-properties-greengrass-subscriptiondefinition-subscriptiondefinitionversion.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Name`  <a name="cfn-greengrass-subscriptiondefinition-name"></a>
The name of the subscription definition\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-greengrass-subscriptiondefinition-tags"></a>
Application\-specific metadata to attach to the subscription definition\. You can use tags in IAM policies to control access to AWS IoT Greengrass resources\. You can also use tags to categorize your resources\. For more information, see [Tagging Your AWS IoT Greengrass Resources](https://docs.aws.amazon.com/greengrass/latest/developerguide/tagging.html) in the *AWS IoT Greengrass Developer Guide*\.  
This `Json` property type is processed as a map of key\-value pairs\. It uses the following format, which is different from most `Tags` implementations in AWS CloudFormation templates\.  

```
"Tags": {
    "KeyName0": "value",
    "KeyName1": "value",
    "KeyName2": "value"
}
```
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-greengrass-subscriptiondefinition-return-values"></a>

### Ref<a name="aws-resource-greengrass-subscriptiondefinition-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the ID of the subscription definition, such as `1234a5b6-78cd-901e-2fgh-3i45j6k178l9`\. 

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-greengrass-subscriptiondefinition-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-greengrass-subscriptiondefinition-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the `SubscriptionDefinition`, such as `arn:aws:greengrass:us-east-1:123456789012:/greengrass/definition/subscriptions/1234a5b6-78cd-901e-2fgh-3i45j6k178l9`\. 

`Id`  <a name="Id-fn::getatt"></a>
The ID of the `SubscriptionDefinition`, such as `1234a5b6-78cd-901e-2fgh-3i45j6k178l9`\. 

`LatestVersionArn`  <a name="LatestVersionArn-fn::getatt"></a>
The ARN of the last `SubscriptionDefinitionVersion` that was added to the `SubscriptionDefinition`, such as `arn:aws:greengrass:us-east-1:123456789012:/greengrass/definition/subscriptions/1234a5b6-78cd-901e-2fgh-3i45j6k178l9/versions/9876ac30-4bdb-4f9d-95af-b5fdb66be1a2`\. 

`Name`  <a name="Name-fn::getatt"></a>
The name of the `SubscriptionDefinition`, such as `MySubscriptionDefinition`\. 

## Examples<a name="aws-resource-greengrass-subscriptiondefinition--examples"></a>



### Subscription Definition Snippet<a name="aws-resource-greengrass-subscriptiondefinition--examples--Subscription_Definition_Snippet"></a>

The following snippet defines a subscription definition subscription with an initial version that contains a subscription\. In this example, the subscription source is an existing device in the group\. The target is a function in the group that was created in another stack and is referenced using the `ImportValue` function\.

For an example of a complete template, see the [https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-subscription-greengrass-group.html](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-subscription-greengrass-group.html) subscription\.

#### JSON<a name="aws-resource-greengrass-subscriptiondefinition--examples--Subscription_Definition_Snippet--json"></a>

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

#### YAML<a name="aws-resource-greengrass-subscriptiondefinition--examples--Subscription_Definition_Snippet--yaml"></a>

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

## See also<a name="aws-resource-greengrass-subscriptiondefinition--seealso"></a>
+  [CreateSubscriptionDefinition](https://docs.aws.amazon.com/greengrass/latest/apireference/createsubscriptiondefinition-post.html) in the * AWS IoT Greengrass API Reference * 
+  [AWS IoT Greengrass Developer Guide](https://docs.aws.amazon.com/greengrass/latest/developerguide/) 