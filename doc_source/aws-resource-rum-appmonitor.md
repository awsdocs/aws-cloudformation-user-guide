# AWS::RUM::AppMonitor<a name="aws-resource-rum-appmonitor"></a>

Creates a CloudWatch RUM app monitor, which you can use to collect telemetry data from your application and send it to CloudWatch RUM\. The data includes performance and reliability information such as page load time, client\-side errors, and user behavior\.

After you create an app monitor, sign in to the CloudWatch RUM console to get the JavaScript code snippet to add to your web application\. For more information, see [How do I find a code snippet that I've already generated?](https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/CloudWatch-RUM-find-code-snippet.html)

## Syntax<a name="aws-resource-rum-appmonitor-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-rum-appmonitor-syntax.json"></a>

```
{
  "Type" : "AWS::RUM::AppMonitor",
  "Properties" : {
      "[AppMonitorConfiguration](#cfn-rum-appmonitor-appmonitorconfiguration)" : AppMonitorConfiguration,
      "[CustomEvents](#cfn-rum-appmonitor-customevents)" : CustomEvents,
      "[CwLogEnabled](#cfn-rum-appmonitor-cwlogenabled)" : Boolean,
      "[Domain](#cfn-rum-appmonitor-domain)" : String,
      "[Name](#cfn-rum-appmonitor-name)" : String,
      "[Tags](#cfn-rum-appmonitor-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-rum-appmonitor-syntax.yaml"></a>

```
Type: AWS::RUM::AppMonitor
Properties: 
  [AppMonitorConfiguration](#cfn-rum-appmonitor-appmonitorconfiguration): 
    AppMonitorConfiguration
  [CustomEvents](#cfn-rum-appmonitor-customevents): 
    CustomEvents
  [CwLogEnabled](#cfn-rum-appmonitor-cwlogenabled): Boolean
  [Domain](#cfn-rum-appmonitor-domain): String
  [Name](#cfn-rum-appmonitor-name): String
  [Tags](#cfn-rum-appmonitor-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-rum-appmonitor-properties"></a>

`AppMonitorConfiguration`  <a name="cfn-rum-appmonitor-appmonitorconfiguration"></a>
A structure that contains much of the configuration data for the app monitor\. If you are using Amazon Cognito for authorization, you must include this structure in your request, and it must include the ID of the Amazon Cognito identity pool to use for authorization\. If you don't include `AppMonitorConfiguration`, you must set up your own authorization method\. For more information, see [Authorize your application to send data to AWS](https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/CloudWatch-RUM-get-started-authorization.html)\.  
If you omit this argument, the sample rate used for CloudWatch RUM is set to 10% of the user sessions\.  
*Required*: No  
*Type*: [AppMonitorConfiguration](aws-properties-rum-appmonitor-appmonitorconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CustomEvents`  <a name="cfn-rum-appmonitor-customevents"></a>
Specifies whether this app monitor allows the web client to define and send custom events\. If you omit this parameter, custom events are `DISABLED`\.  
*Required*: No  
*Type*: [CustomEvents](aws-properties-rum-appmonitor-customevents.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CwLogEnabled`  <a name="cfn-rum-appmonitor-cwlogenabled"></a>
Data collected by CloudWatch RUM is kept by RUM for 30 days and then deleted\. This parameter specifies whether CloudWatch RUM sends a copy of this telemetry data to Amazon CloudWatch Logs in your account\. This enables you to keep the telemetry data for more than 30 days, but it does incur Amazon CloudWatch Logs charges\.  
If you omit this parameter, the default is `false`\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Domain`  <a name="cfn-rum-appmonitor-domain"></a>
The top\-level internet domain name for which your application has administrative authority\. This parameter is required\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-rum-appmonitor-name"></a>
A name for the app monitor\. This parameter is required\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-rum-appmonitor-tags"></a>
Assigns one or more tags \(key\-value pairs\) to the app monitor\.  
Tags can help you organize and categorize your resources\. You can also use them to scope user permissions by granting a user permission to access or change only resources with certain tag values\.  
Tags don't have any semantic meaning to AWS and are interpreted strictly as strings of characters\.  
You can associate as many as 50 tags with an app monitor\.  
For more information, see [Tagging AWS resources](https://docs.aws.amazon.com/general/latest/gr/aws_tagging.html)\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-rum-appmonitor-return-values"></a>

### Ref<a name="aws-resource-rum-appmonitor-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the name of the app monitor\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.