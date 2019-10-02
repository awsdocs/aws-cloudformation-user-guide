# AWS::Pinpoint::App<a name="aws-resource-pinpoint-app"></a>

Specifies an app\. In Amazon Pinpoint, an *app* \(also referred to as a *project*\) is a collection of settings, customer information, segments, and campaigns\.

You can use the App resource to retrieve information about or delete an existing application\. To create a new application, use the Apps resource and send a POST request to the `/apps` URI\.

## Syntax<a name="aws-resource-pinpoint-app-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-pinpoint-app-syntax.json"></a>

```
{
  "Type" : "AWS::Pinpoint::App",
  "Properties" : {
      "[Name](#cfn-pinpoint-app-name)" : String
    }
}
```

### YAML<a name="aws-resource-pinpoint-app-syntax.yaml"></a>

```
Type: AWS::Pinpoint::App
Properties: 
  [Name](#cfn-pinpoint-app-name): String
```

## Properties<a name="aws-resource-pinpoint-app-properties"></a>

`Name`  <a name="cfn-pinpoint-app-name"></a>
The display name of the application\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return Values<a name="aws-resource-pinpoint-app-return-values"></a>

### Ref<a name="aws-resource-pinpoint-app-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the unique ID of the Amazon Pinpoint app\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Supported Regions

This ResourceType is supported by the following regions:

- `ap-south-1`
- `ap-southeast-2`
- `eu-central-1`
- `eu-west-1`
- `us-east-1`
- `us-west-2`
