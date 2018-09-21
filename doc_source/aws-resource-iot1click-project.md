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
    "[PlacementTemplate](#cfn-iot1click-project-placementtemplate)" : [*PlacementTemplate*](aws-properties-iot1click-project-placementtemplate.md),
    "[ProjectName](#cfn-iot1click-project-projectname)" : String
  }
}
```

### YAML<a name="aws-resource-iot1click-project-syntax.yaml"></a>

```
Type: "AWS::IoT1Click::Project"
Properties:
  [Description](#cfn-iot1click-project-description): String
  [PlacementTemplate](#cfn-iot1click-project-placementtemplate):
    [*PlacementTemplate*](aws-properties-iot1click-project-placementtemplate.md)
  [ProjectName](#cfn-iot1click-project-projectname): String
```

## Properties<a name="aws-resource-iot1click-project-properties"></a>

`Description`  <a name="cfn-iot1click-project-description"></a>
An optional description for the project\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`PlacementTemplate`  <a name="cfn-iot1click-project-placementtemplate"></a>
The template defining the placement to be created\. A placement template defines placement default attributes and device templates\. You cannot add or remove device templates after the project has been created\. However, you can update `callbackOverrides` for the device templates using the `UpdateProject` API\.  
 *Required*: Yes  
 *Type*: [AWS IoT 1\-Click Project PlacementTemplate](aws-properties-iot1click-project-placementtemplate.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`ProjectName`  <a name="cfn-iot1click-project-projectname"></a>
The name of the project to create\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

## Return Values<a name="aws-resource-iot1click-project-returnvalues"></a>

### Ref<a name="aws-resource-iot1click-project-ref"></a>

When you pass the logical ID of an `AWS::IoT1Click::Project` resource to the intrinsic `Ref` function, the function returns the project ARN, such as `arn:aws:iot1click:us-west-2:0123456789012:projects/test-project`\. 

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\. 

### Fn::GetAtt<a name="aws-resource-iot1click-project-getatt"></a>

 `Fn::GetAtt` returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\. 

`Arn`  
The Amazon Resource Name \(ARN\) of the project, such as `arn:aws:iot1click:us-east-1:123456789012:projects/project-a1bzhi`\. 

`ProjectName`  
The name of the project, such as `project-a1bzhi`\. 

For more information about using `Fn::GetAtt`, see [Fn::GetAtt](intrinsic-function-reference-getatt.md)\. 

## Example<a name="aws-resource-iot1click-project-examples"></a>

The following example declares an AWS IoT 1\-Click project\.

### JSON<a name="aws-resource-iot1click-project-example1.json"></a>

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

### YAML<a name="aws-resource-iot1click-project-example1.yaml"></a>

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

## See Also<a name="aws-resource-iot1click-project-seealso"></a>
+ [CreateProject](https://docs.aws.amazon.com/iot-1-click/latest/projects-apireference/API_CreateProject.html)
+ [Projects, Templates, and Placements](https://docs.aws.amazon.com/iot-1-click/latest/developerguide/1click-PTP.html)
+ [AWS IoT 1\-Click Programming Model](https://docs.aws.amazon.com/iot-1-click/latest/developerguide/1click-programming.html)