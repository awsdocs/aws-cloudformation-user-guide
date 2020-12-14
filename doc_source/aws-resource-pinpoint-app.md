# AWS::Pinpoint::App<a name="aws-resource-pinpoint-app"></a>

The AWS::Pinpoint::App resource is an Amazon Pinpoint application, also referred to as a *project* or *app*\. An application is a collection of related settings, customer information, segments, campaigns, and other types of Amazon Pinpoint resources\.

## Syntax<a name="aws-resource-pinpoint-app-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-pinpoint-app-syntax.json"></a>

```
{
  "Type" : "AWS::Pinpoint::App",
  "Properties" : {
      "[Name](#cfn-pinpoint-app-name)" : String,
      "[Tags](#cfn-pinpoint-app-tags)" : Json
    }
}
```

### YAML<a name="aws-resource-pinpoint-app-syntax.yaml"></a>

```
Type: AWS::Pinpoint::App
Properties: 
  [Name](#cfn-pinpoint-app-name): String
  [Tags](#cfn-pinpoint-app-tags): Json
```

## Properties<a name="aws-resource-pinpoint-app-properties"></a>

`Name`  <a name="cfn-pinpoint-app-name"></a>
The display name of the application\. This name is displayed as the **Project name** on the Amazon Pinpoint console\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-pinpoint-app-tags"></a>
A string\-to\-string map of key\-value pairs that defines the tags to associate with the application\. Each tag consists of a required tag key and an associated tag value\.  
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-pinpoint-app-return-values"></a>

### Ref<a name="aws-resource-pinpoint-app-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the unique identifier \(`ApplicationId`\) for the Amazon Pinpoint application\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-pinpoint-app-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-pinpoint-app-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the application\.