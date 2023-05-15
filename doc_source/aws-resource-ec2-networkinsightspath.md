# AWS::EC2::NetworkInsightsPath<a name="aws-resource-ec2-networkinsightspath"></a>

Specifies a path to analyze for reachability\.

VPC Reachability Analyzer enables you to analyze and debug network reachability between two resources in your virtual private cloud \(VPC\)\. For more information, see the [Reachability Analyzer User Guide](https://docs.aws.amazon.com/vpc/latest/reachability/what-is-reachability-analyzer.html)\.

## Syntax<a name="aws-resource-ec2-networkinsightspath-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ec2-networkinsightspath-syntax.json"></a>

```
{
  "Type" : "AWS::EC2::NetworkInsightsPath",
  "Properties" : {
      "[Destination](#cfn-ec2-networkinsightspath-destination)" : String,
      "[DestinationIp](#cfn-ec2-networkinsightspath-destinationip)" : String,
      "[DestinationPort](#cfn-ec2-networkinsightspath-destinationport)" : Integer,
      "[FilterAtDestination](#cfn-ec2-networkinsightspath-filteratdestination)" : PathFilter,
      "[FilterAtSource](#cfn-ec2-networkinsightspath-filteratsource)" : PathFilter,
      "[Protocol](#cfn-ec2-networkinsightspath-protocol)" : String,
      "[Source](#cfn-ec2-networkinsightspath-source)" : String,
      "[SourceIp](#cfn-ec2-networkinsightspath-sourceip)" : String,
      "[Tags](#cfn-ec2-networkinsightspath-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-ec2-networkinsightspath-syntax.yaml"></a>

```
Type: AWS::EC2::NetworkInsightsPath
Properties: 
  [Destination](#cfn-ec2-networkinsightspath-destination): String
  [DestinationIp](#cfn-ec2-networkinsightspath-destinationip): String
  [DestinationPort](#cfn-ec2-networkinsightspath-destinationport): Integer
  [FilterAtDestination](#cfn-ec2-networkinsightspath-filteratdestination): 
    PathFilter
  [FilterAtSource](#cfn-ec2-networkinsightspath-filteratsource): 
    PathFilter
  [Protocol](#cfn-ec2-networkinsightspath-protocol): String
  [Source](#cfn-ec2-networkinsightspath-source): String
  [SourceIp](#cfn-ec2-networkinsightspath-sourceip): String
  [Tags](#cfn-ec2-networkinsightspath-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-ec2-networkinsightspath-properties"></a>

`Destination`  <a name="cfn-ec2-networkinsightspath-destination"></a>
The ID or ARN of the destination\. If the resource is in another account, you must specify an ARN\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`DestinationIp`  <a name="cfn-ec2-networkinsightspath-destinationip"></a>
The IP address of the destination\.  
*Required*: No  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `15`  
*Pattern*: `^([0-9]{1,3}.){3}[0-9]{1,3}$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`DestinationPort`  <a name="cfn-ec2-networkinsightspath-destinationport"></a>
The destination port\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `0`  
*Maximum*: `65535`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`FilterAtDestination`  <a name="cfn-ec2-networkinsightspath-filteratdestination"></a>
Scopes the analysis to network paths that match specific filters at the destination\. If you specify this parameter, you can't specify the parameter for the destination IP address\.  
*Required*: No  
*Type*: [PathFilter](aws-properties-ec2-networkinsightspath-pathfilter.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`FilterAtSource`  <a name="cfn-ec2-networkinsightspath-filteratsource"></a>
Scopes the analysis to network paths that match specific filters at the source\. If you specify this parameter, you can't specify the parameters for the source IP address or the destination port\.  
*Required*: No  
*Type*: [PathFilter](aws-properties-ec2-networkinsightspath-pathfilter.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Protocol`  <a name="cfn-ec2-networkinsightspath-protocol"></a>
The protocol\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `tcp | udp`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Source`  <a name="cfn-ec2-networkinsightspath-source"></a>
The ID or ARN of the source\. If the resource is in another account, you must specify an ARN\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SourceIp`  <a name="cfn-ec2-networkinsightspath-sourceip"></a>
The IP address of the source\.  
*Required*: No  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `15`  
*Pattern*: `^([0-9]{1,3}.){3}[0-9]{1,3}$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-ec2-networkinsightspath-tags"></a>
The tags to add to the path\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-ec2-networkinsightspath-return-values"></a>

### Ref<a name="aws-resource-ec2-networkinsightspath-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref`function, `Ref`returns the ID of the path\.

For more information about using the `Ref`function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-ec2-networkinsightspath-return-values-fn--getatt"></a>

The `Fn::GetAtt`intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt`intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-ec2-networkinsightspath-return-values-fn--getatt-fn--getatt"></a>

`CreatedDate`  <a name="CreatedDate-fn::getatt"></a>
The time stamp when the path was created\.

`DestinationArn`  <a name="DestinationArn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the destination\.

`NetworkInsightsPathArn`  <a name="NetworkInsightsPathArn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the path\.

`NetworkInsightsPathId`  <a name="NetworkInsightsPathId-fn::getatt"></a>
The ID of the path\.

`SourceArn`  <a name="SourceArn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the source\.