# AWS::CloudWatch::Dashboard<a name="aws-resource-cloudwatch-dashboard"></a>

The `AWS::CloudWatch::Dashboard` resource specifies an Amazon CloudWatch dashboard\. A dashboard is a customizable home page in the CloudWatch console that you can use to monitor your AWS resources in a single view\.

All dashboards in your account are global, not region\-specific\.

## Syntax<a name="aws-resource-cloudwatch-dashboard-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-cloudwatch-dashboard-syntax.json"></a>

```
{
  "Type" : "AWS::CloudWatch::Dashboard",
  "Properties" : {
      "[DashboardBody](#cfn-cloudwatch-dashboard-dashboardbody)" : String,
      "[DashboardName](#cfn-cloudwatch-dashboard-dashboardname)" : String
    }
}
```

### YAML<a name="aws-resource-cloudwatch-dashboard-syntax.yaml"></a>

```
Type: AWS::CloudWatch::Dashboard
Properties: 
  [DashboardBody](#cfn-cloudwatch-dashboard-dashboardbody): String
  [DashboardName](#cfn-cloudwatch-dashboard-dashboardname): String
```

## Properties<a name="aws-resource-cloudwatch-dashboard-properties"></a>

`DashboardBody`  <a name="cfn-cloudwatch-dashboard-dashboardbody"></a>
The detailed information about the dashboard in JSON format, including the widgets to include and their location on the dashboard\. This parameter is required\.  
For more information about the syntax, see [Dashboard Body Structure and Syntax](https://docs.aws.amazon.com/AmazonCloudWatch/latest/APIReference/CloudWatch-Dashboard-Body-Structure.html)\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DashboardName`  <a name="cfn-cloudwatch-dashboard-dashboardname"></a>
The name of the dashboard\. The name must be between 1 and 255 characters\. If you do not specify a name, one will be generated automatically\.   
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-cloudwatch-dashboard-return-values"></a>

### Ref<a name="aws-resource-cloudwatch-dashboard-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the value of `DashboardName`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## See also<a name="aws-resource-cloudwatch-dashboard--seealso"></a>
+  [Amazon CloudWatch Template Snippets](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/quickref-cloudwatch.html) 

