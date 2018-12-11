# AWS::EC2::VPCEndpoint<a name="aws-resource-ec2-vpcendpoint"></a>

Creates a VPC endpoint that you can use to establish a private connection between your VPC and another AWS service without requiring access over the Internet, a VPN connection, or AWS Direct Connect\. For more information, see [CreateVpcEndpoint](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_CreateVpcEndpoint.html)\.

**Topics**
+ [Syntax](#aws-resource-ec2-vpcendpoint-syntax)
+ [Properties](#aws-resource-ec2-vpcendpoint-properties)
+ [Return Value](#aws-resource-ec2-vpcendpoint-return-values)
+ [Example](#aws-resource-ec2-vpcendpoint-examples)

## Syntax<a name="aws-resource-ec2-vpcendpoint-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ec2-vpcendpoint-syntax.json"></a>

```
{
  "Type" : "AWS::EC2::VPCEndpoint",
  "Properties" : {
    "[VpcId](#cfn-ec2-vpcendpoint-vpcid)" : String,
    "[RouteTableIds](#cfn-ec2-vpcendpoint-routetableids)" : [ String, ... ],
    "[ServiceName](#cfn-ec2-vpcendpoint-servicename)" : String,
    "[PolicyDocument](#cfn-ec2-vpcendpoint-policydocument)" : String,
    "[VpcEndpointType](#cfn-ec2-vpcendpoint-vpcendpointtype)" : String,
    "[PrivateDnsEnabled](#cfn-ec2-vpcendpoint-privatednsenabled)" : Boolean,
    "[SubnetIds](#cfn-ec2-vpcendpoint-subnetids)" : [ String, ... ],
    "[SecurityGroupIds](#cfn-ec2-vpcendpoint-securitygroupids)" : [ String, ... ]
  }
}
```

### YAML<a name="aws-resource-ec2-vpcendpoint-syntax.yaml"></a>

```
Type: AWS::EC2::VPCEndpoint
Properties: 
  [VpcId](#cfn-ec2-vpcendpoint-vpcid): String
  [RouteTableIds](#cfn-ec2-vpcendpoint-routetableids): 
    - String
  [ServiceName](#cfn-ec2-vpcendpoint-servicename): String
  [PolicyDocument](#cfn-ec2-vpcendpoint-policydocument): String
  [VpcEndpointType](#cfn-ec2-vpcendpoint-vpcendpointtype): String
  [PrivateDnsEnabled](#cfn-ec2-vpcendpoint-privatednsenabled): Boolean
  [SubnetIds](#cfn-ec2-vpcendpoint-subnetids): 
    - String
  [SecurityGroupIds](#cfn-ec2-vpcendpoint-securitygroupids): 
    - String
```

## Properties<a name="aws-resource-ec2-vpcendpoint-properties"></a>

`PrivateDnsEnabled`  <a name="cfn-ec2-vpcendpoint-privatednsenabled"></a>
\[Interface endpoint\] Indicates whether to associate a private hosted zone with the specified VPC\.  
 *Required*: No  
 *Type*: Boolean  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`PolicyDocument`  <a name="cfn-ec2-vpcendpoint-policydocument"></a>
\[Gateway endpoint\] A policy to attach to the endpoint that controls access to the service\. The policy must be valid JSON\. The default policy allows full access to the AWS service\. For more information, see [Controlling Access to Services](https://docs.aws.amazon.com/vpc/latest/userguide/vpc-endpoints.html#vpc-endpoints-access) in the *Amazon VPC User Guide*\.  
*Required*: No  
*Type*: JSON object  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`RouteTableIds`  <a name="cfn-ec2-vpcendpoint-routetableids"></a>
\[Gateway endpoint\] One or more route table IDs that are used by the VPC to reach the endpoint\.  
*Required*: No  
*Type*: List of String values  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`SecurityGroupIds`  <a name="cfn-ec2-vpcendpoint-securitygroupids"></a>
\[Interface endpoint\] The ID of one or more security groups to associate with the endpoint network interface\.  
 *Required*: No  
 *Type*: List of String values  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`ServiceName`  <a name="cfn-ec2-vpcendpoint-servicename"></a>
The name of the service\. To get a list of available services, use [DescribeVpcEndpointServices](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_DescribeVpcEndpointServices.html) or get the name from the service provider\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`SubnetIds`  <a name="cfn-ec2-vpcendpoint-subnetids"></a>
\[Interface endpoint\] The ID of one or more subnets in which to create an endpoint network interface\.  
 *Required*: No  
 *Type*: List of String values  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`VpcEndpointType`  <a name="cfn-ec2-vpcendpoint-vpcendpointtype"></a>
The type of endpoint\. Valid values are `Interface` and `Gateway`\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`VpcId`  <a name="cfn-ec2-vpcendpoint-vpcid"></a>
The ID of the VPC in which the endpoint will be used\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

## Return Value<a name="aws-resource-ec2-vpcendpoint-return-values"></a>

### Ref<a name="aws-resource-ec2-vpcendpoint-ref"></a>

When you pass the logical ID of an `AWS::EC2::VPCEndpoint` resource to the intrinsic `Ref` function, the function returns the endpoint ID, such as `vpce-a123d0d1`\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.

### Fn::GetAtt<a name="aws-resource-ec2-vpcendpoint-getatt"></a>

`Fn::GetAtt` returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

`CreationTimestamp`  
*Returns*: The date and time the VPC endpoint was created\. For example: `Fri Sep 28 23:34:36 UTC 2018`

`DnsEntries`  
*Returns*: \(Interface endpoint\) The DNS entries for the endpoint\. Each entry is a combination of the hosted zone ID and the DNS name\. The entries are ordered as follows: regional public DNS, zonal public DNS, private DNS, and wildcard DNS\. This order is not enforced for AWS Marketplace services\.  
The following is an example\. In the first entry, the hosted zone ID is Z1HUB23UULQXV and the DNS name is vpce\-01abc23456de78f9g\-12abccd3\.ec2\.us\-east\-1\.vpce\.amazonaws\.com\.  
\["Z1HUB23UULQXV:vpce\-01abc23456de78f9g\-12abccd3\.ec2\.us\-east\-1\.vpce\.amazonaws\.com", "Z1HUB23UULQXV:vpce\-01abc23456de78f9g\-12abccd3\-us\-east\-1a\.ec2\.us\-east\-1\.vpce\.amazonaws\.com", "Z1C12344VYDITB0:ec2\.us\-east\-1\.amazonaws\.com"\]  
If you update the `PrivateDnsEnabled` or `SubnetIds` properties, the DNS entries in the list will change\.

`NetworkInterfaceIds`  
*Returns*: \(Interface endpoint\) One or more network interfaces for the endpoint\. For example:  
`["eni-12345ab6789c10d1e", "eni-012345678ab9c10d1"]`  
If you update the `PrivateDnsEnabled` or `SubnetIds` properties, the items in this list might change\.

For more information about using `Fn::GetAtt`, see [Fn::GetAtt](intrinsic-function-reference-getatt.md)\.

## Example<a name="aws-resource-ec2-vpcendpoint-examples"></a>

The following example creates a VPC endpoint that allows only the `s3:GetObject` action on the `examplebucket` bucket\. Traffic to S3 within subnets that are associated with the `routetableA` and `routetableB` route tables is automatically routed through the VPC endpoint\.

### JSON<a name="aws-resource-ec2-vpcendpoint-example.json"></a>

```
"S3Endpoint" : {
  "Type" : "AWS::EC2::VPCEndpoint",
  "Properties" : {
    "PolicyDocument" : {
      "Version":"2012-10-17",
      "Statement":[{
        "Effect":"Allow",
        "Principal": "*",
        "Action":["s3:GetObject"],
        "Resource":["arn:aws:s3:::examplebucket/*"]
      }]
    },
    "RouteTableIds" : [ {"Ref" : "routetableA"}, {"Ref" : "routetableB"} ],
    "ServiceName" : { "Fn::Join": [ "", [ "com.amazonaws.", { "Ref": "AWS::Region" }, ".s3" ] ] },
    "VpcId" : {"Ref" : "VPCID"}
  }
}
```

### YAML<a name="aws-resource-ec2-vpcendpoint-example.yaml"></a>

```
S3Endpoint:
  Type: AWS::EC2::VPCEndpoint
  Properties:
    PolicyDocument:
      Version: 2012-10-17
      Statement:
        - Effect: Allow
          Principal: '*'
          Action:
            - 's3:GetObject'
          Resource:
            - 'arn:aws:s3:::examplebucket/*'
    RouteTableIds:
      - !Ref routetableA
      - !Ref routetableB
    ServiceName: !Join 
      - ''
      - - com.amazonaws.
        - !Ref 'AWS::Region'
        - .s3
    VpcId: !Ref VPCID
```