# AWS::IoTSiteWise::Portal PortalStatus<a name="aws-properties-iotsitewise-portal-portalstatus"></a>

Contains information about the current status of a portal\.

## Syntax<a name="aws-properties-iotsitewise-portal-portalstatus-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iotsitewise-portal-portalstatus-syntax.json"></a>

```
{
  "[error](#cfn-iotsitewise-portal-portalstatus-error)" : MonitorErrorDetails,
  "[state](#cfn-iotsitewise-portal-portalstatus-state)" : String
}
```

### YAML<a name="aws-properties-iotsitewise-portal-portalstatus-syntax.yaml"></a>

```
  [error](#cfn-iotsitewise-portal-portalstatus-error): 
    MonitorErrorDetails
  [state](#cfn-iotsitewise-portal-portalstatus-state): String
```

## Properties<a name="aws-properties-iotsitewise-portal-portalstatus-properties"></a>

`error`  <a name="cfn-iotsitewise-portal-portalstatus-error"></a>
Contains associated error information, if any\.  
*Required*: No  
*Type*: [MonitorErrorDetails](aws-properties-iotsitewise-portal-monitorerrordetails.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`state`  <a name="cfn-iotsitewise-portal-portalstatus-state"></a>
The current state of the portal\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)