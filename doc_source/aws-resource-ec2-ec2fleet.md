# AWS::EC2::EC2Fleet<a name="aws-resource-ec2-ec2fleet"></a>

Specifies the configuration information to launch a fleet\-\-or group\-\-of instances\. An EC2 Fleet can launch multiple instance types across multiple Availability Zones, using the On\-Demand Instance, Reserved Instance, and Spot Instance purchasing models together\. Using EC2 Fleet, you can define separate On\-Demand and Spot capacity targets, specify the instance types that work best for your applications, and specify how Amazon EC2 should distribute your fleet capacity within each purchasing model\. For more information, see [Launching an EC2 Fleet](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ec2-fleet.html) in the *Amazon EC2 User Guide for Linux Instances*\.

## Syntax<a name="aws-resource-ec2-ec2fleet-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ec2-ec2fleet-syntax.json"></a>

```
{
  "Type" : "AWS::EC2::EC2Fleet",
  "Properties" : {
      "[Context](#cfn-ec2-ec2fleet-context)" : String,
      "[ExcessCapacityTerminationPolicy](#cfn-ec2-ec2fleet-excesscapacityterminationpolicy)" : String,
      "[LaunchTemplateConfigs](#cfn-ec2-ec2fleet-launchtemplateconfigs)" : [ FleetLaunchTemplateConfigRequest, ... ],
      "[OnDemandOptions](#cfn-ec2-ec2fleet-ondemandoptions)" : OnDemandOptionsRequest,
      "[ReplaceUnhealthyInstances](#cfn-ec2-ec2fleet-replaceunhealthyinstances)" : Boolean,
      "[SpotOptions](#cfn-ec2-ec2fleet-spotoptions)" : SpotOptionsRequest,
      "[TagSpecifications](#cfn-ec2-ec2fleet-tagspecifications)" : [ TagSpecification, ... ],
      "[TargetCapacitySpecification](#cfn-ec2-ec2fleet-targetcapacityspecification)" : TargetCapacitySpecificationRequest,
      "[TerminateInstancesWithExpiration](#cfn-ec2-ec2fleet-terminateinstanceswithexpiration)" : Boolean,
      "[Type](#cfn-ec2-ec2fleet-type)" : String,
      "[ValidFrom](#cfn-ec2-ec2fleet-validfrom)" : String,
      "[ValidUntil](#cfn-ec2-ec2fleet-validuntil)" : String
    }
}
```

### YAML<a name="aws-resource-ec2-ec2fleet-syntax.yaml"></a>

```
Type: AWS::EC2::EC2Fleet
Properties: 
  [Context](#cfn-ec2-ec2fleet-context): String
  [ExcessCapacityTerminationPolicy](#cfn-ec2-ec2fleet-excesscapacityterminationpolicy): String
  [LaunchTemplateConfigs](#cfn-ec2-ec2fleet-launchtemplateconfigs): 
    - FleetLaunchTemplateConfigRequest
  [OnDemandOptions](#cfn-ec2-ec2fleet-ondemandoptions): 
    OnDemandOptionsRequest
  [ReplaceUnhealthyInstances](#cfn-ec2-ec2fleet-replaceunhealthyinstances): Boolean
  [SpotOptions](#cfn-ec2-ec2fleet-spotoptions): 
    SpotOptionsRequest
  [TagSpecifications](#cfn-ec2-ec2fleet-tagspecifications): 
    - TagSpecification
  [TargetCapacitySpecification](#cfn-ec2-ec2fleet-targetcapacityspecification): 
    TargetCapacitySpecificationRequest
  [TerminateInstancesWithExpiration](#cfn-ec2-ec2fleet-terminateinstanceswithexpiration): Boolean
  [Type](#cfn-ec2-ec2fleet-type): String
  [ValidFrom](#cfn-ec2-ec2fleet-validfrom): String
  [ValidUntil](#cfn-ec2-ec2fleet-validuntil): String
```

## Properties<a name="aws-resource-ec2-ec2fleet-properties"></a>

`Context`  <a name="cfn-ec2-ec2fleet-context"></a>
Reserved\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ExcessCapacityTerminationPolicy`  <a name="cfn-ec2-ec2fleet-excesscapacityterminationpolicy"></a>
Indicates whether running instances should be terminated if the total target capacity of the EC2 Fleet is decreased below the current size of the EC2 Fleet\.  
Supported only for fleets of type `maintain`\.  
*Required*: No  
*Type*: String  
*Allowed values*: `no-termination | termination`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LaunchTemplateConfigs`  <a name="cfn-ec2-ec2fleet-launchtemplateconfigs"></a>
The configuration for the EC2 Fleet\.  
*Required*: Yes  
*Type*: List of [FleetLaunchTemplateConfigRequest](aws-properties-ec2-ec2fleet-fleetlaunchtemplateconfigrequest.md)  
*Maximum*: `50`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`OnDemandOptions`  <a name="cfn-ec2-ec2fleet-ondemandoptions"></a>
Describes the configuration of On\-Demand Instances in an EC2 Fleet\.  
*Required*: No  
*Type*: [OnDemandOptionsRequest](aws-properties-ec2-ec2fleet-ondemandoptionsrequest.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ReplaceUnhealthyInstances`  <a name="cfn-ec2-ec2fleet-replaceunhealthyinstances"></a>
Indicates whether EC2 Fleet should replace unhealthy Spot Instances\. Supported only for fleets of type `maintain`\. For more information, see [EC2 Fleet health checks](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/manage-ec2-fleet.html#ec2-fleet-health-checks) in the *Amazon EC2 User Guide*\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SpotOptions`  <a name="cfn-ec2-ec2fleet-spotoptions"></a>
Describes the configuration of Spot Instances in an EC2 Fleet\.  
*Required*: No  
*Type*: [SpotOptionsRequest](aws-properties-ec2-ec2fleet-spotoptionsrequest.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`TagSpecifications`  <a name="cfn-ec2-ec2fleet-tagspecifications"></a>
The key\-value pair for tagging the EC2 Fleet request on creation\. For more information, see [Tagging your resources](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/Using_Tags.html#tag-resources)\.  
If the fleet type is `instant`, specify a resource type of `fleet` to tag the fleet or `instance` to tag the instances at launch\.  
If the fleet type is `maintain` or `request`, specify a resource type of `fleet` to tag the fleet\. You cannot specify a resource type of `instance`\. To tag instances at launch, specify the tags in a [launch template](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ec2-launch-templates.html#create-launch-template)\.  
*Required*: No  
*Type*: List of [TagSpecification](aws-properties-ec2-ec2fleet-tagspecification.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`TargetCapacitySpecification`  <a name="cfn-ec2-ec2fleet-targetcapacityspecification"></a>
The number of units to request\.  
*Required*: Yes  
*Type*: [TargetCapacitySpecificationRequest](aws-properties-ec2-ec2fleet-targetcapacityspecificationrequest.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TerminateInstancesWithExpiration`  <a name="cfn-ec2-ec2fleet-terminateinstanceswithexpiration"></a>
Indicates whether running instances should be terminated when the EC2 Fleet expires\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Type`  <a name="cfn-ec2-ec2fleet-type"></a>
The fleet type\. The default value is `maintain`\.  
+  `maintain` \- The EC2 Fleet places an asynchronous request for your desired capacity, and continues to maintain your desired Spot capacity by replenishing interrupted Spot Instances\.
+  `request` \- The EC2 Fleet places an asynchronous one\-time request for your desired capacity, but does submit Spot requests in alternative capacity pools if Spot capacity is unavailable, and does not maintain Spot capacity if Spot Instances are interrupted\.
+  `instant` \- The EC2 Fleet places a synchronous one\-time request for your desired capacity, and returns errors for any instances that could not be launched\.
For more information, see [EC2 Fleet request types](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ec2-fleet-request-type.html) in the *Amazon EC2 User Guide*\.  
*Required*: No  
*Type*: String  
*Allowed values*: `instant | maintain | request`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ValidFrom`  <a name="cfn-ec2-ec2fleet-validfrom"></a>
The start date and time of the request, in UTC format \(for example, *YYYY*\-*MM*\-*DD*T*HH*:*MM*:*SS*Z\)\. The default is to start fulfilling the request immediately\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ValidUntil`  <a name="cfn-ec2-ec2fleet-validuntil"></a>
The end date and time of the request, in UTC format \(for example, *YYYY*\-*MM*\-*DD*T*HH*:*MM*:*SS*Z\)\. At this point, no new EC2 Fleet requests are placed or able to fulfill the request\. If no value is specified, the request remains until you cancel it\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-ec2-ec2fleet-return-values"></a>

### Ref<a name="aws-resource-ec2-ec2fleet-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the fleet ID, such as `fleet-1fe24079-d272-4023-8e7c-70e10784cb0e`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-ec2-ec2fleet-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-ec2-ec2fleet-return-values-fn--getatt-fn--getatt"></a>

`FleetId`  <a name="FleetId-fn::getatt"></a>
The ID of the EC2 Fleet\.

## See also<a name="aws-resource-ec2-ec2fleet--seealso"></a>
+  [CreateFleet](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_CreateFleet.html) in the *Amazon EC2 API Reference* 