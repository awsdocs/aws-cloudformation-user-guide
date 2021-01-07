# AWS::IoTSiteWise::Portal<a name="aws-resource-iotsitewise-portal"></a>

Creates a portal, which can contain projects and dashboards\. Before you can create a portal, you must enable AWS Single Sign\-On\. AWS IoT SiteWise Monitor uses AWS SSO to manage user permissions\. For more information, see [Enabling AWS SSO](https://docs.aws.amazon.com/iot-sitewise/latest/userguide/monitor-get-started.html#mon-gs-sso) in the *AWS IoT SiteWise User Guide*\.

**Note**  
Before you can sign in to a new portal, you must add at least one AWS SSO user or group to that portal\. For more information, see [Adding or removing portal administrators](https://docs.aws.amazon.com/iot-sitewise/latest/userguide/administer-portals.html#portal-change-admins) in the *AWS IoT SiteWise User Guide*\.

## Syntax<a name="aws-resource-iotsitewise-portal-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-iotsitewise-portal-syntax.json"></a>

```
{
  "Type" : "AWS::IoTSiteWise::Portal",
  "Properties" : {
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
  [PortalContactEmail](#cfn-iotsitewise-portal-portalcontactemail): String
  [PortalDescription](#cfn-iotsitewise-portal-portaldescription): String
  [PortalName](#cfn-iotsitewise-portal-portalname): String
  [RoleArn](#cfn-iotsitewise-portal-rolearn): String
  [Tags](#cfn-iotsitewise-portal-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-iotsitewise-portal-properties"></a>

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
The AWS SSO application generated client ID \(used with AWS SSO APIs\)\.  
For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

`PortalId`  <a name="PortalId-fn::getatt"></a>
The ID of the created portal\.  
For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

`PortalStartUrl`  <a name="PortalStartUrl-fn::getatt"></a>
The public URL for the AWS IoT SiteWise Monitor portal\.  
For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

`PortalStatus`  <a name="PortalStatus-fn::getatt"></a>
The status of the portal, which contains a state \(`CREATING` after successfully calling this operation\) and any error message\.  
For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.