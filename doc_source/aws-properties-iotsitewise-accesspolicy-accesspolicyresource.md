# AWS::IoTSiteWise::AccessPolicy AccessPolicyResource<a name="aws-properties-iotsitewise-accesspolicy-accesspolicyresource"></a>

The AWS IoT SiteWise Monitor resource for this access policy\. Choose either a portal or a project\.

## Syntax<a name="aws-properties-iotsitewise-accesspolicy-accesspolicyresource-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iotsitewise-accesspolicy-accesspolicyresource-syntax.json"></a>

```
{
  "[Portal](#cfn-iotsitewise-accesspolicy-accesspolicyresource-portal)" : Portal,
  "[Project](#cfn-iotsitewise-accesspolicy-accesspolicyresource-project)" : Project
}
```

### YAML<a name="aws-properties-iotsitewise-accesspolicy-accesspolicyresource-syntax.yaml"></a>

```
  [Portal](#cfn-iotsitewise-accesspolicy-accesspolicyresource-portal): 
    Portal
  [Project](#cfn-iotsitewise-accesspolicy-accesspolicyresource-project): 
    Project
```

## Properties<a name="aws-properties-iotsitewise-accesspolicy-accesspolicyresource-properties"></a>

`Portal`  <a name="cfn-iotsitewise-accesspolicy-accesspolicyresource-portal"></a>
The AWS IoT SiteWise Monitor portal for this access policy\.  
*Required*: No  
*Type*: [Portal](aws-properties-iotsitewise-accesspolicy-portal.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Project`  <a name="cfn-iotsitewise-accesspolicy-accesspolicyresource-project"></a>
The AWS IoT SiteWise Monitor project for this access policy\.  
*Required*: No  
*Type*: [Project](aws-properties-iotsitewise-accesspolicy-project.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)