# AWS::IoTSiteWise::Portal<a name="aws-resource-iotsitewise-portal"></a>

Creates a portal, which can contain projects and dashboards\. Before you can create a portal, you must enable IAM Identity Center\. AWS IoT SiteWise Monitor uses IAM Identity Center to manage user permissions\. For more information, see [Enabling IAM Identity Center](https://docs.aws.amazon.com/iot-sitewise/latest/userguide/monitor-get-started.html#mon-gs-sso) in the *AWS IoT SiteWise User Guide*\.

**Note**  
Before you can sign in to a new portal, you must add at least one IAM Identity Center user or group to that portal\. For more information, see [Adding or removing portal administrators](https://docs.aws.amazon.com/iot-sitewise/latest/userguide/administer-portals.html#portal-change-admins) in the *AWS IoT SiteWise User Guide*\.

## Syntax<a name="aws-resource-iotsitewise-portal-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-iotsitewise-portal-syntax.json"></a>

```
{
  "Type" : "AWS::IoTSiteWise::Portal",
  "Properties" : {
      "[Alarms](#cfn-iotsitewise-portal-alarms)" : Alarms,
      "[NotificationSenderEmail](#cfn-iotsitewise-portal-notificationsenderemail)" : String,
      "[PortalAuthMode](#cfn-iotsitewise-portal-portalauthmode)" : String,
      "[PortalContactEmail](#cfn-iotsitewise-portal-portalcontactemail)" : String,
      "[PortalDescription](#cfn-iotsitewise-portal-portaldescription)" : String,
      "[PortalName](#cfn-iotsitewise-portal-portalname)" : String,
      "[RoleArn](#cfn-iotsitewise-portal-rolearn)" : String,
      "[Tags](#cfn-iotsitewise-portal-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-iotsitewise-portal-syntax.yaml"></a>

```
Type: AWS::IoTSiteWise::Portal
Properties: 
  [Alarms](#cfn-iotsitewise-portal-alarms): 
    Alarms
  [NotificationSenderEmail](#cfn-iotsitewise-portal-notificationsenderemail): String
  [PortalAuthMode](#cfn-iotsitewise-portal-portalauthmode): String
  [PortalContactEmail](#cfn-iotsitewise-portal-portalcontactemail): String
  [PortalDescription](#cfn-iotsitewise-portal-portaldescription): String
  [PortalName](#cfn-iotsitewise-portal-portalname): String
  [RoleArn](#cfn-iotsitewise-portal-rolearn): String
  [Tags](#cfn-iotsitewise-portal-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-iotsitewise-portal-properties"></a>

`Alarms`  <a name="cfn-iotsitewise-portal-alarms"></a>
Contains the configuration information of an alarm created in an AWS IoT SiteWise Monitor portal\. You can use the alarm to monitor an asset property and get notified when the asset property value is outside a specified range\. For more information, see [Monitoring with alarms](https://docs.aws.amazon.com/iot-sitewise/latest/appguide/monitor-alarms.html) in the * AWS IoT SiteWise Application Guide*\.  
*Required*: No  
*Type*: [Alarms](aws-properties-iotsitewise-portal-alarms.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NotificationSenderEmail`  <a name="cfn-iotsitewise-portal-notificationsenderemail"></a>
The email address that sends alarm notifications\.  
If you use the [AWS IoT Events managed Lambda function](https://docs.aws.amazon.com/iotevents/latest/developerguide/lambda-support.html) to manage your emails, you must [verify the sender email address in Amazon SES](https://docs.aws.amazon.com/ses/latest/DeveloperGuide/verify-email-addresses.html)\.
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PortalAuthMode`  <a name="cfn-iotsitewise-portal-portalauthmode"></a>
The service to use to authenticate users to the portal\. Choose from the following options:  
+  `SSO` – The portal uses AWS IAM Identity Center \(successor to AWS Single Sign\-On\) to authenticate users and manage user permissions\. Before you can create a portal that uses IAM Identity Center, you must enable IAM Identity Center\. For more information, see [Enabling IAM Identity Center](https://docs.aws.amazon.com/iot-sitewise/latest/userguide/monitor-get-started.html#mon-gs-sso) in the *AWS IoT SiteWise User Guide*\. This option is only available in AWS Regions other than the China Regions\.
+  `IAM` – The portal uses AWS Identity and Access Management \(IAM\) to authenticate users and manage user permissions\.
You can't change this value after you create a portal\.  
Default: `SSO`   
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`PortalContactEmail`  <a name="cfn-iotsitewise-portal-portalcontactemail"></a>
The AWS administrator's contact email address\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PortalDescription`  <a name="cfn-iotsitewise-portal-portaldescription"></a>
A description for the portal\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PortalName`  <a name="cfn-iotsitewise-portal-portalname"></a>
A friendly name for the portal\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RoleArn`  <a name="cfn-iotsitewise-portal-rolearn"></a>
The [ARN](https://docs.aws.amazon.com/general/latest/gr/aws-arns-and-namespaces.html) of a service role that allows the portal's users to access your AWS IoT SiteWise resources on your behalf\. For more information, see [Using service roles for AWS IoT SiteWise Monitor](https://docs.aws.amazon.com/iot-sitewise/latest/userguide/monitor-service-role.html) in the *AWS IoT SiteWise User Guide*\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-iotsitewise-portal-tags"></a>
A list of key\-value pairs that contain metadata for the portal\. For more information, see [Tagging your AWS IoT SiteWise resources](https://docs.aws.amazon.com/iot-sitewise/latest/userguide/tag-resources.html) in the *AWS IoT SiteWise User Guide*\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-iotsitewise-portal-return-values"></a>

### Ref<a name="aws-resource-iotsitewise-portal-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the `PortalId`\.

### Fn::GetAtt<a name="aws-resource-iotsitewise-portal-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-iotsitewise-portal-return-values-fn--getatt-fn--getatt"></a>

`PortalArn`  <a name="PortalArn-fn::getatt"></a>
The [ARN](https://docs.aws.amazon.com/general/latest/gr/aws-arns-and-namespaces.html) of the portal, which has the following format\.  
`arn:${Partition}:iotsitewise:${Region}:${Account}:portal/${PortalId}`  
For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

`PortalClientId`  <a name="PortalClientId-fn::getatt"></a>
The IAM Identity Center application generated client ID \(used with IAM Identity Center APIs\)\.  
For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

`PortalId`  <a name="PortalId-fn::getatt"></a>
The ID of the created portal\.  
For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

`PortalStartUrl`  <a name="PortalStartUrl-fn::getatt"></a>
The public URL for the AWS IoT SiteWise Monitor portal\.  
For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.