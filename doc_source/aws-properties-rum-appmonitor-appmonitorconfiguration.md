# AWS::RUM::AppMonitor AppMonitorConfiguration<a name="aws-properties-rum-appmonitor-appmonitorconfiguration"></a>

This structure contains much of the configuration data for the app monitor\.

## Syntax<a name="aws-properties-rum-appmonitor-appmonitorconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-rum-appmonitor-appmonitorconfiguration-syntax.json"></a>

```
{
  "[AllowCookies](#cfn-rum-appmonitor-appmonitorconfiguration-allowcookies)" : Boolean,
  "[EnableXRay](#cfn-rum-appmonitor-appmonitorconfiguration-enablexray)" : Boolean,
  "[ExcludedPages](#cfn-rum-appmonitor-appmonitorconfiguration-excludedpages)" : [ String, ... ],
  "[FavoritePages](#cfn-rum-appmonitor-appmonitorconfiguration-favoritepages)" : [ String, ... ],
  "[GuestRoleArn](#cfn-rum-appmonitor-appmonitorconfiguration-guestrolearn)" : String,
  "[IdentityPoolId](#cfn-rum-appmonitor-appmonitorconfiguration-identitypoolid)" : String,
  "[IncludedPages](#cfn-rum-appmonitor-appmonitorconfiguration-includedpages)" : [ String, ... ],
  "[MetricDestinations](#cfn-rum-appmonitor-appmonitorconfiguration-metricdestinations)" : [ MetricDestination, ... ],
  "[SessionSampleRate](#cfn-rum-appmonitor-appmonitorconfiguration-sessionsamplerate)" : Double,
  "[Telemetries](#cfn-rum-appmonitor-appmonitorconfiguration-telemetries)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-rum-appmonitor-appmonitorconfiguration-syntax.yaml"></a>

```
  [AllowCookies](#cfn-rum-appmonitor-appmonitorconfiguration-allowcookies): Boolean
  [EnableXRay](#cfn-rum-appmonitor-appmonitorconfiguration-enablexray): Boolean
  [ExcludedPages](#cfn-rum-appmonitor-appmonitorconfiguration-excludedpages): 
    - String
  [FavoritePages](#cfn-rum-appmonitor-appmonitorconfiguration-favoritepages): 
    - String
  [GuestRoleArn](#cfn-rum-appmonitor-appmonitorconfiguration-guestrolearn): String
  [IdentityPoolId](#cfn-rum-appmonitor-appmonitorconfiguration-identitypoolid): String
  [IncludedPages](#cfn-rum-appmonitor-appmonitorconfiguration-includedpages): 
    - String
  [MetricDestinations](#cfn-rum-appmonitor-appmonitorconfiguration-metricdestinations): 
    - MetricDestination
  [SessionSampleRate](#cfn-rum-appmonitor-appmonitorconfiguration-sessionsamplerate): Double
  [Telemetries](#cfn-rum-appmonitor-appmonitorconfiguration-telemetries): 
    - String
```

## Properties<a name="aws-properties-rum-appmonitor-appmonitorconfiguration-properties"></a>

`AllowCookies`  <a name="cfn-rum-appmonitor-appmonitorconfiguration-allowcookies"></a>
If you set this to `true`, the CloudWatch RUM web client sets two cookies, a session cookie and a user cookie\. The cookies allow the CloudWatch RUM web client to collect data relating to the number of users an application has and the behavior of the application across a sequence of events\. Cookies are stored in the top\-level domain of the current page\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EnableXRay`  <a name="cfn-rum-appmonitor-appmonitorconfiguration-enablexray"></a>
If you set this to `true`, CloudWatch RUM sends client\-side traces to X\-Ray for each sampled session\. You can then see traces and segments from these user sessions in the RUM dashboard and the CloudWatch ServiceLens console\. For more information, see [What is AWS X\-Ray?](https://docs.aws.amazon.com/xray/latest/devguide/aws-xray.html)  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ExcludedPages`  <a name="cfn-rum-appmonitor-appmonitorconfiguration-excludedpages"></a>
A list of URLs in your website or application to exclude from RUM data collection\.  
You can't include both `ExcludedPages` and `IncludedPages` in the same app monitor\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FavoritePages`  <a name="cfn-rum-appmonitor-appmonitorconfiguration-favoritepages"></a>
A list of pages in your application that are to be displayed with a "favorite" icon in the CloudWatch RUM console\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`GuestRoleArn`  <a name="cfn-rum-appmonitor-appmonitorconfiguration-guestrolearn"></a>
The ARN of the guest IAM role that is attached to the Amazon Cognito identity pool that is used to authorize the sending of data to CloudWatch RUM\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IdentityPoolId`  <a name="cfn-rum-appmonitor-appmonitorconfiguration-identitypoolid"></a>
The ID of the Amazon Cognito identity pool that is used to authorize the sending of data to CloudWatch RUM\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IncludedPages`  <a name="cfn-rum-appmonitor-appmonitorconfiguration-includedpages"></a>
If this app monitor is to collect data from only certain pages in your application, this structure lists those pages\.   
You can't include both `ExcludedPages` and `IncludedPages` in the same app monitor\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MetricDestinations`  <a name="cfn-rum-appmonitor-appmonitorconfiguration-metricdestinations"></a>
An array of structures that each define a destination that this app monitor will send extended metrics to\.  
*Required*: No  
*Type*: List of [MetricDestination](aws-properties-rum-appmonitor-metricdestination.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SessionSampleRate`  <a name="cfn-rum-appmonitor-appmonitorconfiguration-sessionsamplerate"></a>
Specifies the portion of user sessions to use for CloudWatch RUM data collection\. Choosing a higher portion gives you more data but also incurs more costs\.  
The range for this value is 0 to 1 inclusive\. Setting this to 1 means that 100% of user sessions are sampled, and setting it to 0\.1 means that 10% of user sessions are sampled\.  
If you omit this parameter, the default of 0\.1 is used, and 10% of sessions will be sampled\.  
*Required*: No  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Telemetries`  <a name="cfn-rum-appmonitor-appmonitorconfiguration-telemetries"></a>
An array that lists the types of telemetry data that this app monitor is to collect\.  
+ `errors` indicates that RUM collects data about unhandled JavaScript errors raised by your application\.
+ `performance` indicates that RUM collects performance data about how your application and its resources are loaded and rendered\. This includes Core Web Vitals\.
+ `http` indicates that RUM collects data about HTTP errors thrown by your application\.
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)