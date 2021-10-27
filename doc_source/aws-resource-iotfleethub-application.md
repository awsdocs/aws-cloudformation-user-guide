# AWS::IoTFleetHub::Application<a name="aws-resource-iotfleethub-application"></a>

Represents a Fleet Hub for AWS IoT Device Management web application\.

## Syntax<a name="aws-resource-iotfleethub-application-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-iotfleethub-application-syntax.json"></a>

```
{
  "Type" : "AWS::IoTFleetHub::Application",
  "Properties" : {
      "[ApplicationDescription](#cfn-iotfleethub-application-applicationdescription)" : String,
      "[ApplicationName](#cfn-iotfleethub-application-applicationname)" : String,
      "[RoleArn](#cfn-iotfleethub-application-rolearn)" : String,
      "[Tags](#cfn-iotfleethub-application-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-iotfleethub-application-syntax.yaml"></a>

```
Type: AWS::IoTFleetHub::Application
Properties: 
  [ApplicationDescription](#cfn-iotfleethub-application-applicationdescription): String
  [ApplicationName](#cfn-iotfleethub-application-applicationname): String
  [RoleArn](#cfn-iotfleethub-application-rolearn): String
  [Tags](#cfn-iotfleethub-application-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-iotfleethub-application-properties"></a>

`ApplicationDescription`  <a name="cfn-iotfleethub-application-applicationdescription"></a>
An optional description of the web application\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `2048`  
*Pattern*: `^[ -~]*$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ApplicationName`  <a name="cfn-iotfleethub-application-applicationname"></a>
The name of the web application\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `100`  
*Pattern*: `^[ -~]*$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RoleArn`  <a name="cfn-iotfleethub-application-rolearn"></a>
The ARN of the role that the web application assumes when it interacts with AWS IoT Core\.  
The name of the role must be in the form `FleetHub_random_string`\.
Pattern: `^arn:[!-~]+$`  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-iotfleethub-application-tags"></a>
A set of key/value pairs that you can use to manage the web application resource\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-iotfleethub-application-return-values"></a>

### Ref<a name="aws-resource-iotfleethub-application-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic Ref function, Ref returns the application ID\. 

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-iotfleethub-application-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-iotfleethub-application-return-values-fn--getatt-fn--getatt"></a>

`ApplicationArn`  <a name="ApplicationArn-fn::getatt"></a>
The ARN of the web application\.

`ApplicationCreationDate`  <a name="ApplicationCreationDate-fn::getatt"></a>
The date \(in Unix epoch time\) when the web application was created\.

`ApplicationId`  <a name="ApplicationId-fn::getatt"></a>
The unique Id of the web application\.

`ApplicationLastUpdateDate`  <a name="ApplicationLastUpdateDate-fn::getatt"></a>
The date \(in Unix epoch time\) when the web application was last updated\.

`ApplicationState`  <a name="ApplicationState-fn::getatt"></a>
The current state of the web application\.

`ApplicationUrl`  <a name="ApplicationUrl-fn::getatt"></a>
The URL of the web application\.

`ErrorMessage`  <a name="ErrorMessage-fn::getatt"></a>
A message that explains any failures included in the applicationState response field\. This message explains failures in the `CreateApplication` and `DeleteApplication` actions\.

`SsoClientId`  <a name="SsoClientId-fn::getatt"></a>
The Id of the single sign\-on client that you use to authenticate and authorize users on the web application\.