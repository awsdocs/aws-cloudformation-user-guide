# AWS::CloudWatch::Dashboard<a name="aws-properties-cw-dashboard"></a>

The `AWS::CloudWatch::Dashboard` resource creates an Amazon CloudWatch dashboard\. A dashboard is a customizable home page in the CloudWatch console that you can use to monitor your AWS resources in a single view\. Each metric, graph, alarm, or text block on a dashboard is called a widget\.

This resource supports updates\. For more information about updating this resource, see [PutDashboard](http://docs.aws.amazon.com/AmazonCloudWatch/latest/APIReference/API_PutDashboard.html) in the *Amazon CloudWatch API Reference*\. For more information about updating stacks, see [AWS CloudFormation Stacks Updates](using-cfn-updating-stacks.md)\.

**Topics**
+ [Syntax](#aws-resource-cw-dashboard-syntax)
+ [Properties](#aws-properties-cw-dashboard-prop)
+ [Return Values](#aws-properties-cw-dashboard-ref)
+ [Examples](#w3ab2c21c10d238c15)

## Syntax<a name="aws-resource-cw-dashboard-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-cw-dashboard-syntax.json"></a>

```
{
  "Type" : "AWS::CloudWatch::Dashboard",
  "Properties" : {
      "[DashboardName](#cfn-cloudwatch-dashboard-name)" : String,
      "[DashboardBody](#cfn-cloudwatch-dashboard-body)" : String,
  }
}
```

### YAML<a name="aws-resource-cw-dashboard-syntax.yaml"></a>

```
Type: "AWS::CloudWatch::Dashboard"
Properties:
      [DashboardName](#cfn-cloudwatch-dashboard-name): String
      [DashboardBody](#cfn-cloudwatch-dashboard-body): String
```

## Properties<a name="aws-properties-cw-dashboard-prop"></a>

`DashboardName`  <a name="cfn-cloudwatch-dashboard-name"></a>
A name for the dashboard\. The name must be between 1 and 255 characters\. If you do not specify a name, one will be generated automatically\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`DashboardBody`  <a name="cfn-cloudwatch-dashboard-body"></a>
A JSON string that defines the widgets contained in the dashboard and their location\. For information about how to format this string, see [Dashboard Body Structure and Syntax](http://docs.aws.amazon.com/AmazonCloudWatch/latest/APIReference/CloudWatch-Dashboard-Body-Structure.html)\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

## Return Values<a name="aws-properties-cw-dashboard-ref"></a>

### Ref<a name="w3ab2c21c10d238c13b2"></a>

When you specify an `AWS::CloudWatch::Dashboard` resource as an argument to the `Ref` function, AWS CloudFormation returns the value of the `Name`\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.

## Examples<a name="w3ab2c21c10d238c15"></a>

For examples, see [Amazon CloudWatch Template Snippets](quickref-cloudwatch.md)\.