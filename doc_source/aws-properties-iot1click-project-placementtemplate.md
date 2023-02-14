# AWS::IoT1Click::Project PlacementTemplate<a name="aws-properties-iot1click-project-placementtemplate"></a>

In AWS CloudFormation, use the `PlacementTemplate` property type to define the template for an AWS IoT 1\-Click project\.

`PlacementTemplate` is a property of the `AWS::IoT1Click::Project` resource\. 

## Syntax<a name="aws-properties-iot1click-project-placementtemplate-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iot1click-project-placementtemplate-syntax.json"></a>

```
{
  "[DefaultAttributes](#cfn-iot1click-project-placementtemplate-defaultattributes)" : Json,
  "[DeviceTemplates](#cfn-iot1click-project-placementtemplate-devicetemplates)" : Json
}
```

### YAML<a name="aws-properties-iot1click-project-placementtemplate-syntax.yaml"></a>

```
  [DefaultAttributes](#cfn-iot1click-project-placementtemplate-defaultattributes): Json
  [DeviceTemplates](#cfn-iot1click-project-placementtemplate-devicetemplates): Json
```

## Properties<a name="aws-properties-iot1click-project-placementtemplate-properties"></a>

`DefaultAttributes`  <a name="cfn-iot1click-project-placementtemplate-defaultattributes"></a>
The default attributes \(key\-value pairs\) to be applied to all placements using this template\.  
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DeviceTemplates`  <a name="cfn-iot1click-project-placementtemplate-devicetemplates"></a>
An object specifying the [DeviceTemplate](https://docs.aws.amazon.com/iot-1-click/latest/projects-apireference/API_DeviceTemplate.html) for all placements using this \([PlacementTemplate](https://docs.aws.amazon.com/iot-1-click/latest/projects-apireference/API_PlacementTemplate.html)\) template\.  
*Required*: No  
*Type*: Json  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## See also<a name="aws-properties-iot1click-project-placementtemplate--seealso"></a>
+ [Projects, Templates, and Placements](https://docs.aws.amazon.com/iot-1-click/latest/developerguide/1click-PTP.html)
+ [AWS IoT 1\-Click Programming Model](https://docs.aws.amazon.com/iot-1-click/latest/developerguide/1click-programming.html)