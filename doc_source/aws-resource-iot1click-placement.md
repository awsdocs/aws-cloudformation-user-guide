# AWS::IoT1Click::Placement<a name="aws-resource-iot1click-placement"></a>

The `AWS::IoT1Click::Placement` resource creates a placement to be associated with an AWS IoT 1\-Click project\. A placement is an instance of a device in a location\. For more information, see [Projects, Templates, and Placements](https://docs.aws.amazon.com/iot-1-click/latest/developerguide/1click-PTP.html) in the *AWS IoT 1\-Click Developer Guide*\. 

## Syntax<a name="aws-resource-iot1click-placement-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-iot1click-placement-syntax.json"></a>

```
{
  "Type" : "AWS::IoT1Click::Placement",
  "Properties" : {
      "[AssociatedDevices](#cfn-iot1click-placement-associateddevices)" : Json,
      "[Attributes](#cfn-iot1click-placement-attributes)" : Json,
      "[PlacementName](#cfn-iot1click-placement-placementname)" : String,
      "[ProjectName](#cfn-iot1click-placement-projectname)" : String
    }
}
```

### YAML<a name="aws-resource-iot1click-placement-syntax.yaml"></a>

```
Type: AWS::IoT1Click::Placement
Properties: 
  [AssociatedDevices](#cfn-iot1click-placement-associateddevices): Json
  [Attributes](#cfn-iot1click-placement-attributes): Json
  [PlacementName](#cfn-iot1click-placement-placementname): String
  [ProjectName](#cfn-iot1click-placement-projectname): String
```

## Properties<a name="aws-resource-iot1click-placement-properties"></a>

`AssociatedDevices`  <a name="cfn-iot1click-placement-associateddevices"></a>
The devices to associate with the placement, as defined by a mapping of zero or more key\-value pairs wherein the key is a template name and the value is a device ID\.  
*Required*: No  
*Type*: Json  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Attributes`  <a name="cfn-iot1click-placement-attributes"></a>
The user\-defined attributes associated with the placement\.  
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PlacementName`  <a name="cfn-iot1click-placement-placementname"></a>
The name of the placement\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ProjectName`  <a name="cfn-iot1click-placement-projectname"></a>
The name of the project containing the placement\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-iot1click-placement-return-values"></a>

### Ref<a name="aws-resource-iot1click-placement-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns a string of the form `projects/A/placements/B`, where A is the name of the project and B is the name of the placement\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-iot1click-placement-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-iot1click-placement-return-values-fn--getatt-fn--getatt"></a>

`PlacementName`  <a name="PlacementName-fn::getatt"></a>
The name of the placement, such as `floor17`\.

`ProjectName`  <a name="ProjectName-fn::getatt"></a>
The name of the project containing the placement, such as `conference-rooms`\.

## Examples<a name="aws-resource-iot1click-placement--examples"></a>

### Declare a Project and Placement<a name="aws-resource-iot1click-placement--examples--Declare_a_Project_and_Placement"></a>

#### JSON<a name="aws-resource-iot1click-placement--examples--Declare_a_Project_and_Placement--json"></a>

```
{
    "BasicProjectWithPlacement": {
        "Type": "AWS::IoT1Click::Project",
        "Properties": {
            "ProjectName": "project-with-placements",
            "Description": "description",
            "PlacementTemplate": {
                "DefaultAttributes": {
                    "Attribute": "Value",
                    "Foo": "Bar"
                },
                "DeviceTemplates": {
                    "testButton": {
                        "DeviceType": "button",
                        "CallbackOverrides": {
                            "onClickCallback": ""
                        }
                    }
                }
            }
        }
    },

    "BasicPlacement": {
        "Type": "AWS::IoT1Click::Placement",
        "Properties": {
            "ProjectName": {
                "Ref": "BasicProjectWithPlacement"
            },
            "PlacementName": "placement"
        }
    }
}
```

#### YAML<a name="aws-resource-iot1click-placement--examples--Declare_a_Project_and_Placement--yaml"></a>

```
BasicProjectWithPlacement:
  Type: "AWS::IoT1Click::Project"
  Properties:
    ProjectName: "project-with-placements"
    Description: "description"
    PlacementTemplate:
      DefaultAttributes:
        Attribute: Value
        Foo: Bar
      DeviceTemplates:
        testButton:
          DeviceType: "button"
          CallbackOverrides:
            onClickCallback: ""

BasicPlacement:
  Type: "AWS::IoT1Click::Placement"
  Properties:
    ProjectName: !Ref BasicProjectWithPlacement
    PlacementName: "placement"
```

## See also<a name="aws-resource-iot1click-placement--seealso"></a>
+ [CreatePlacement](https://docs.aws.amazon.com/iot-1-click/latest/projects-apireference/API_CreatePlacement.html)
+ [Projects, Templates, and Placements](https://docs.aws.amazon.com/iot-1-click/latest/developerguide/1click-PTP.html)
+ [AWS IoT 1\-Click Programming Model](https://docs.aws.amazon.com/iot-1-click/latest/developerguide/1click-programming.html)