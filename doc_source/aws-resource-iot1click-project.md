# AWS::IoT1Click::Project<a name="aws-resource-iot1click-project"></a>

The `AWS::IoT1Click::Project` resource creates an empty project with a placement template\. A project contains zero or more placements that adhere to the placement template defined in the project\. For more information, see [CreateProject](https://docs.aws.amazon.com/iot-1-click/latest/projects-apireference/API_CreateProject.html) in the *AWS IoT 1\-Click Projects API Reference*\.

## Syntax<a name="aws-resource-iot1click-project-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-iot1click-project-syntax.json"></a>

```
{
  "Type" : "AWS::IoT1Click::Project",
  "Properties" : {
      "[Description](#cfn-iot1click-project-description)" : String,
      "[PlacementTemplate](#cfn-iot1click-project-placementtemplate)" : PlacementTemplate,
      "[ProjectName](#cfn-iot1click-project-projectname)" : String
    }
}
```

### YAML<a name="aws-resource-iot1click-project-syntax.yaml"></a>

```
Type: AWS::IoT1Click::Project
Properties: 
  [Description](#cfn-iot1click-project-description): String
  [PlacementTemplate](#cfn-iot1click-project-placementtemplate): 
    PlacementTemplate
  [ProjectName](#cfn-iot1click-project-projectname): String
```

## Properties<a name="aws-resource-iot1click-project-properties"></a>

`Description`  <a name="cfn-iot1click-project-description"></a>
The description of the project\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PlacementTemplate`  <a name="cfn-iot1click-project-placementtemplate"></a>
An object describing the project's placement specifications\.  
*Required*: Yes  
*Type*: [PlacementTemplate](aws-properties-iot1click-project-placementtemplate.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ProjectName`  <a name="cfn-iot1click-project-projectname"></a>
The name of the project from which to obtain information\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-iot1click-project-return-values"></a>

### Ref<a name="aws-resource-iot1click-project-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the project ARN, such as `arn:aws:iot1click:us-west-2:0123456789012:projects/test-project`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-iot1click-project-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-iot1click-project-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the project, such as `arn:aws:iot1click:us-east-1:123456789012:projects/project-a1bzhi`\.

`ProjectName`  <a name="ProjectName-fn::getatt"></a>
The name of the project, such as `project-a1bzhi`\.

## Examples<a name="aws-resource-iot1click-project--examples"></a>

### Declare an AWS IoT 1\-Click project<a name="aws-resource-iot1click-project--examples--Declare_an_AWS_IoT_1-Click_project"></a>

#### JSON<a name="aws-resource-iot1click-project--examples--Declare_an_AWS_IoT_1-Click_project--json"></a>

```
{
    "Description": "AWS IoT1Click Project test",
    "Resources": {
        "BasicProject": {
            "Type": "AWS::IoT1Click::Project",
            "Properties": {
                "ProjectName": "project",
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
        }
    },

    "Outputs": {
        "ProjectId": {
            "Value": {
                "Ref": "BasicProject"
            }
        }
    }
}
```

#### YAML<a name="aws-resource-iot1click-project--examples--Declare_an_AWS_IoT_1-Click_project--yaml"></a>

```
Description: "AWS IoT1Click Project test"
Resources:
  BasicProject:
    Type: "AWS::IoT1Click::Project"
    Properties:
      ProjectName: "project"
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

Outputs:
  ProjectId:
    Value: !Ref BasicProject
```

## See also<a name="aws-resource-iot1click-project--seealso"></a>
+ [CreateProject](https://docs.aws.amazon.com/iot-1-click/latest/projects-apireference/API_CreateProject.html)
+ [Projects, Templates, and Placements](https://docs.aws.amazon.com/iot-1-click/latest/developerguide/1click-PTP.html)
+ [AWS IoT 1\-Click Programming Model](https://docs.aws.amazon.com/iot-1-click/latest/developerguide/1click-programming.html)