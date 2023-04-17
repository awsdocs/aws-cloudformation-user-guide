# AWS::QuickSight::Dashboard CustomActionNavigationOperation<a name="aws-properties-quicksight-dashboard-customactionnavigationoperation"></a>

The navigation operation that navigates between different sheets in the same analysis\.

This is a union type structure\. For this structure to be valid, only one of the attributes can be defined\.

## Syntax<a name="aws-properties-quicksight-dashboard-customactionnavigationoperation-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dashboard-customactionnavigationoperation-syntax.json"></a>

```
{
  "[LocalNavigationConfiguration](#cfn-quicksight-dashboard-customactionnavigationoperation-localnavigationconfiguration)" : LocalNavigationConfiguration
}
```

### YAML<a name="aws-properties-quicksight-dashboard-customactionnavigationoperation-syntax.yaml"></a>

```
  [LocalNavigationConfiguration](#cfn-quicksight-dashboard-customactionnavigationoperation-localnavigationconfiguration): 
    LocalNavigationConfiguration
```

## Properties<a name="aws-properties-quicksight-dashboard-customactionnavigationoperation-properties"></a>

`LocalNavigationConfiguration`  <a name="cfn-quicksight-dashboard-customactionnavigationoperation-localnavigationconfiguration"></a>
The configuration that chooses the navigation target\.  
*Required*: No  
*Type*: [LocalNavigationConfiguration](aws-properties-quicksight-dashboard-localnavigationconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)