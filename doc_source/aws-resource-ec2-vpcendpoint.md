# AWS::EC2::VPCEndpoint<a name="aws-resource-ec2-vpcendpoint"></a>

The `AWS::EC2::VPCEndpoint` resource creates a VPC endpoint that you can use to establish a private connection between your VPC and another AWS service without requiring access over the Internet, a VPN connection, or AWS Direct Connect\.

**Topics**
+ [Syntax](#aws-resource-ec2-vpcendpoint-syntax)
+ [Properties](#w3ab2c21c10d523b9)
+ [Return Value](#w3ab2c21c10d523c11)
+ [Example](#w3ab2c21c10d523c13)

## Syntax<a name="aws-resource-ec2-vpcendpoint-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ec2-vpcendpoint-syntax.json"></a>

```
{
  "Type" : "AWS::EC2::VPCEndpoint",
  "Properties" : {
    "[PolicyDocument](#cfn-ec2-vpcendpoint-policydocument)" : JSON object,
    "[RouteTableIds](#cfn-ec2-vpcendpoint-routetableids)" : [ String, ... ],
    "[ServiceName](#cfn-ec2-vpcendpoint-servicename)" : String,
    "[VpcId](#cfn-ec2-vpcendpoint-vpcid)" : String
  }
}
```

### YAML<a name="aws-resource-ec2-vpcendpoint-syntax.yaml"></a>

```
Type: "AWS::EC2::VPCEndpoint"
Properties: 
  [PolicyDocument](#cfn-ec2-vpcendpoint-policydocument): JSON object
  [RouteTableIds](#cfn-ec2-vpcendpoint-routetableids):
    - String
  [ServiceName](#cfn-ec2-vpcendpoint-servicename): String
  [VpcId](#cfn-ec2-vpcendpoint-vpcid): String
```

## Properties<a name="w3ab2c21c10d523b9"></a>

`PolicyDocument`  <a name="cfn-ec2-vpcendpoint-policydocument"></a>
A policy to attach to the endpoint that controls access to the service\. The policy must be valid JSON\. The default policy allows full access to the AWS service\. For more information, see [Controlling Access to Services](http://docs.aws.amazon.com/AmazonVPC/latest/UserGuide/vpc-endpoints.html#vpc-endpoints-access) in the *Amazon VPC User Guide*\.  
*Required*: No  
*Type*: JSON object  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`RouteTableIds`  <a name="cfn-ec2-vpcendpoint-routetableids"></a>
One or more route table IDs that are used by the VPC to reach the endpoint\.  
*Required*: No  
*Type*: List of String values  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`ServiceName`  <a name="cfn-ec2-vpcendpoint-servicename"></a>
The AWS service to which you want to establish a connection\. Specify the service name in the form of `com.amazonaws.region.service`\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`VpcId`  <a name="cfn-ec2-vpcendpoint-vpcid"></a>
The ID of the VPC in which the endpoint is used\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

## Return Value<a name="w3ab2c21c10d523c11"></a>

### Ref<a name="w3ab2c21c10d523c11b1"></a>

When you pass the logical ID of an `AWS::EC2::VPCEndpoint` resource to the intrinsic `Ref` function, the function returns the endpoint ID, such as `vpce-a123d0d1`\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.

## Example<a name="w3ab2c21c10d523c13"></a>

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
  Type: 'AWS::EC2::VPCEndpoint'
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