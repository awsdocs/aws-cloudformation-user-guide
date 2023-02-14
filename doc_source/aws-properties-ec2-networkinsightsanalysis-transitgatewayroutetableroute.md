# AWS::EC2::NetworkInsightsAnalysis TransitGatewayRouteTableRoute<a name="aws-properties-ec2-networkinsightsanalysis-transitgatewayroutetableroute"></a>

Describes a route in a transit gateway route table\.

## Syntax<a name="aws-properties-ec2-networkinsightsanalysis-transitgatewayroutetableroute-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ec2-networkinsightsanalysis-transitgatewayroutetableroute-syntax.json"></a>

```
{
  "[AttachmentId](#cfn-ec2-networkinsightsanalysis-transitgatewayroutetableroute-attachmentid)" : String,
  "[DestinationCidr](#cfn-ec2-networkinsightsanalysis-transitgatewayroutetableroute-destinationcidr)" : String,
  "[PrefixListId](#cfn-ec2-networkinsightsanalysis-transitgatewayroutetableroute-prefixlistid)" : String,
  "[ResourceId](#cfn-ec2-networkinsightsanalysis-transitgatewayroutetableroute-resourceid)" : String,
  "[ResourceType](#cfn-ec2-networkinsightsanalysis-transitgatewayroutetableroute-resourcetype)" : String,
  "[RouteOrigin](#cfn-ec2-networkinsightsanalysis-transitgatewayroutetableroute-routeorigin)" : String,
  "[State](#cfn-ec2-networkinsightsanalysis-transitgatewayroutetableroute-state)" : String
}
```

### YAML<a name="aws-properties-ec2-networkinsightsanalysis-transitgatewayroutetableroute-syntax.yaml"></a>

```
  [AttachmentId](#cfn-ec2-networkinsightsanalysis-transitgatewayroutetableroute-attachmentid): String
  [DestinationCidr](#cfn-ec2-networkinsightsanalysis-transitgatewayroutetableroute-destinationcidr): String
  [PrefixListId](#cfn-ec2-networkinsightsanalysis-transitgatewayroutetableroute-prefixlistid): String
  [ResourceId](#cfn-ec2-networkinsightsanalysis-transitgatewayroutetableroute-resourceid): String
  [ResourceType](#cfn-ec2-networkinsightsanalysis-transitgatewayroutetableroute-resourcetype): String
  [RouteOrigin](#cfn-ec2-networkinsightsanalysis-transitgatewayroutetableroute-routeorigin): String
  [State](#cfn-ec2-networkinsightsanalysis-transitgatewayroutetableroute-state): String
```

## Properties<a name="aws-properties-ec2-networkinsightsanalysis-transitgatewayroutetableroute-properties"></a>

`AttachmentId`  <a name="cfn-ec2-networkinsightsanalysis-transitgatewayroutetableroute-attachmentid"></a>
The ID of the route attachment\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DestinationCidr`  <a name="cfn-ec2-networkinsightsanalysis-transitgatewayroutetableroute-destinationcidr"></a>
The CIDR block used for destination matches\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PrefixListId`  <a name="cfn-ec2-networkinsightsanalysis-transitgatewayroutetableroute-prefixlistid"></a>
The ID of the prefix list\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ResourceId`  <a name="cfn-ec2-networkinsightsanalysis-transitgatewayroutetableroute-resourceid"></a>
The ID of the resource for the route attachment\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ResourceType`  <a name="cfn-ec2-networkinsightsanalysis-transitgatewayroutetableroute-resourcetype"></a>
The resource type for the route attachment\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RouteOrigin`  <a name="cfn-ec2-networkinsightsanalysis-transitgatewayroutetableroute-routeorigin"></a>
The route origin\. The following are the possible values:  
+ static
+ propagated
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`State`  <a name="cfn-ec2-networkinsightsanalysis-transitgatewayroutetableroute-state"></a>
The state of the route\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)