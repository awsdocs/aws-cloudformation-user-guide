# AWS::IoT1Click::Project DeviceTemplate<a name="aws-properties-iot1click-project-devicetemplate"></a>

In AWS CloudFormation, use the `DeviceTemplate` property type to define the template for an AWS IoT 1\-Click project\.

`DeviceTemplate` is a property of the `AWS::IoT1Click::Project` resource\.

## Syntax<a name="aws-properties-iot1click-project-devicetemplate-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iot1click-project-devicetemplate-syntax.json"></a>

```
{
  "[CallbackOverrides](#cfn-iot1click-project-devicetemplate-callbackoverrides)" : Json,
  "[DeviceType](#cfn-iot1click-project-devicetemplate-devicetype)" : String
}
```

### YAML<a name="aws-properties-iot1click-project-devicetemplate-syntax.yaml"></a>

```
  [CallbackOverrides](#cfn-iot1click-project-devicetemplate-callbackoverrides): Json
  [DeviceType](#cfn-iot1click-project-devicetemplate-devicetype): String
```

## Properties<a name="aws-properties-iot1click-project-devicetemplate-properties"></a>

`CallbackOverrides`  <a name="cfn-iot1click-project-devicetemplate-callbackoverrides"></a>
An optional AWS Lambda function to invoke instead of the default AWS Lambda function provided by the placement template\.  
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DeviceType`  <a name="cfn-iot1click-project-devicetemplate-devicetype"></a>
The device type, which currently must be `"button"`\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-iot1click-project-devicetemplate--seealso"></a>
+ [Projects, Templates, and Placements](https://docs.aws.amazon.com/iot-1-click/latest/developerguide/1click-PTP.html)
+ [AWS IoT 1\-Click Programming Model](https://docs.aws.amazon.com/iot-1-click/latest/developerguide/1click-programming.html)