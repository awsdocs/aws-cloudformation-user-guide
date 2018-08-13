# AWS OpsWorks Recipes Type<a name="aws-properties-opsworks-layer-recipes"></a>

Describes custom event recipes for the [AWS::OpsWorks::Layer](aws-resource-opsworks-layer.md) resource type that AWS OpsWorks runs after the standard event recipes\. For more information, see [AWS OpsWorks Lifecycle Events](http://docs.aws.amazon.com/opsworks/latest/userguide/workingcookbook-events.html) in the *AWS OpsWorks User Guide*\.

## Syntax<a name="w3ab2c21c14e1585b5"></a>

### JSON<a name="aws-properties-opsworks-layer-recipes-syntax.json"></a>

```
{
  "[Configure](#cfn-opsworks-layer-customrecipes-configure)" : [ String, ... ],
  "[Deploy](#cfn-opsworks-layer-customrecipes-deploy)" : [ String, ... ],
  "[Setup](#cfn-opsworks-layer-customrecipes-setup)" : [ String, ... ],
  "[Shutdown](#cfn-opsworks-layer-customrecipes-shutdown)" : [ String, ... ],
  "[Undeploy](#cfn-opsworks-layer-customrecipes-undeploy)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-opsworks-layer-recipes-syntax.yaml"></a>

```
[Configure](#cfn-opsworks-layer-customrecipes-configure):
  - String
[Deploy](#cfn-opsworks-layer-customrecipes-deploy):
  - String
[Setup](#cfn-opsworks-layer-customrecipes-setup):
  - String
[Shutdown](#cfn-opsworks-layer-customrecipes-shutdown):
  - String
[Undeploy](#cfn-opsworks-layer-customrecipes-undeploy):
  - String
```

## Properties<a name="w3ab2c21c14e1585b7"></a>

`Configure`  <a name="cfn-opsworks-layer-customrecipes-configure"></a>
Custom recipe names to be run following a Configure event\. The event occurs on all of the stack's instances when an instance enters or leaves the online state\.  
*Required*: No  
*Type*: List of String values

`Deploy`  <a name="cfn-opsworks-layer-customrecipes-deploy"></a>
Custom recipe names to be run following a Deploy event\. The event occurs when you run a `deploy` command, typically to deploy an application to a set of application server instances\.  
*Required*: No  
*Type*: List of String values

`Setup`  <a name="cfn-opsworks-layer-customrecipes-setup"></a>
Custom recipe names to be run following a Setup event\. This event occurs on a new instance after it successfully boots\.  
*Required*: No  
*Type*: List of String values

`Shutdown`  <a name="cfn-opsworks-layer-customrecipes-shutdown"></a>
Custom recipe names to be run following a Shutdown event\. This event occurs after you direct AWS OpsWorks to shut an instance down before the associated Amazon EC2 instance is actually terminated\.   
*Required*: No  
*Type*: List of String values

`Undeploy`  <a name="cfn-opsworks-layer-customrecipes-undeploy"></a>
Custom recipe names to be run following a Undeploy event\. This event occurs when you delete an app or run an `undeploy` command to remove an app from a set of application server instances\.  
*Required*: No  
*Type*: List of String values