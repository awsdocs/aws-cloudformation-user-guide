# AWS::IoTSiteWise::Dashboard<a name="aws-resource-iotsitewise-dashboard"></a>

Creates a dashboard in an AWS IoT SiteWise Monitor project\.

## Syntax<a name="aws-resource-iotsitewise-dashboard-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-iotsitewise-dashboard-syntax.json"></a>

```
{
  "Type" : "AWS::IoTSiteWise::Dashboard",
  "Properties" : {
      "[DashboardDefinition](#cfn-iotsitewise-dashboard-dashboarddefinition)" : String,
      "[DashboardDescription](#cfn-iotsitewise-dashboard-dashboarddescription)" : String,
      "[DashboardName](#cfn-iotsitewise-dashboard-dashboardname)" : String,
      "[ProjectId](#cfn-iotsitewise-dashboard-projectid)" : String,
      "[Tags](#cfn-iotsitewise-dashboard-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-iotsitewise-dashboard-syntax.yaml"></a>

```
Type: AWS::IoTSiteWise::Dashboard
Properties: 
  [DashboardDefinition](#cfn-iotsitewise-dashboard-dashboarddefinition): String
  [DashboardDescription](#cfn-iotsitewise-dashboard-dashboarddescription): String
  [DashboardName](#cfn-iotsitewise-dashboard-dashboardname): String
  [ProjectId](#cfn-iotsitewise-dashboard-projectid): String
  [Tags](#cfn-iotsitewise-dashboard-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-iotsitewise-dashboard-properties"></a>

`DashboardDefinition`  <a name="cfn-iotsitewise-dashboard-dashboarddefinition"></a>
The dashboard definition specified in a JSON literal\. For detailed information, see [Creating dashboards \(CLI\)](https://docs.aws.amazon.com/iot-sitewise/latest/userguide/create-dashboards-using-aws-cli.html) in the *AWS IoT SiteWise User Guide*\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DashboardDescription`  <a name="cfn-iotsitewise-dashboard-dashboarddescription"></a>
A description for the dashboard\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DashboardName`  <a name="cfn-iotsitewise-dashboard-dashboardname"></a>
A friendly name for the dashboard\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ProjectId`  <a name="cfn-iotsitewise-dashboard-projectid"></a>
The ID of the project in which to create the dashboard\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-iotsitewise-dashboard-tags"></a>
A list of key\-value pairs that contain metadata for the dashboard\. For more information, see [Tagging your AWS IoT SiteWise resources](https://docs.aws.amazon.com/iot-sitewise/latest/userguide/tag-resources.html) in the *AWS IoT SiteWise User Guide*\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-iotsitewise-dashboard-return-values"></a>

### Ref<a name="aws-resource-iotsitewise-dashboard-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the `DashboardId`\.

### Fn::GetAtt<a name="aws-resource-iotsitewise-dashboard-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-iotsitewise-dashboard-return-values-fn--getatt-fn--getatt"></a>

`DashboardArn`  <a name="DashboardArn-fn::getatt"></a>
The [ARN](https://docs.aws.amazon.com/general/latest/gr/aws-arns-and-namespaces.html) of the dashboard, which has the following format\.  
`arn:${Partition}:iotsitewise:${Region}:${Account}:dashboard/${DashboardId}`  
For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

`DashboardId`  <a name="DashboardId-fn::getatt"></a>
The ID of the dashboard\.  
For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.