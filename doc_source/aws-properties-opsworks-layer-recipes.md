# AWS OpsWorks Recipes Type<a name="aws-properties-opsworks-layer-recipes"></a>

Describes custom event recipes for the [AWS::OpsWorks::Layer](aws-resource-opsworks-layer.md) resource type that AWS OpsWorks runs after the standard event recipes\. For more information, see [AWS OpsWorks Lifecycle Events](http://docs.aws.amazon.com/opsworks/latest/userguide/workingcookbook-events.html) in the *AWS OpsWorks User Guide*\.

## Syntax<a name="w3ab2c21c14e1379b5"></a>

### JSON<a name="aws-properties-opsworks-layer-recipes-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-opsworks-layer-customrecipes-configure)" : [ String, ... ],
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-opsworks-layer-customrecipes-deploy)" : [ String, ... ],
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-opsworks-layer-customrecipes-setup)" : [ String, ... ],
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-opsworks-layer-customrecipes-shutdown)" : [ String, ... ],
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-opsworks-layer-customrecipes-undeploy)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-opsworks-layer-recipes-syntax.yaml"></a>

```
[[ERROR] BAD/MISSING LINK TEXT](#cfn-opsworks-layer-customrecipes-configure):
  - String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-opsworks-layer-customrecipes-deploy):
  - String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-opsworks-layer-customrecipes-setup):
  - String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-opsworks-layer-customrecipes-shutdown):
  - String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-opsworks-layer-customrecipes-undeploy):
  - String
```

## Properties<a name="w3ab2c21c14e1379b7"></a>

`Configure`  
Custom recipe names to be run following a Configure event\. The event occurs on all of the stack's instances when an instance enters or leaves the online state\.  
*Required: *No  
*Type*: List of String values

`Deploy`  
Custom recipe names to be run following a Deploy event\. The event occurs when you run a `deploy` command, typically to deploy an application to a set of application server instances\.  
*Required: *No  
*Type*: List of String values

`Setup`  
Custom recipe names to be run following a Setup event\. This event occurs on a new instance after it successfully boots\.  
*Required: *No  
*Type*: List of String values

`Shutdown`  
Custom recipe names to be run following a Shutdown event\. This event occurs after you direct AWS OpsWorks to shut an instance down before the associated Amazon EC2 instance is actually terminated\.   
*Required: *No  
*Type*: List of String values

`Undeploy`  
Custom recipe names to be run following a Undeploy event\. This event occurs when you delete an app or run an `undeploy` command to remove an app from a set of application server instances\.  
*Required: *No  
*Type*: List of String values