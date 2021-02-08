# AWS::ApiGateway::VpcLink<a name="aws-resource-apigateway-vpclink"></a>

The `AWS::ApiGateway::VpcLink` resource creates an API Gateway VPC link for a REST API to access resources in an Amazon Virtual Private Cloud \(VPC\)\. For more information, see [vpclink:create](https://docs.aws.amazon.com/apigateway/api-reference/link-relation/vpclink-create/) in the `Amazon API Gateway REST API Reference`\.

## Syntax<a name="aws-resource-apigateway-vpclink-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-apigateway-vpclink-syntax.json"></a>

```
{
  "Type" : "AWS::ApiGateway::VpcLink",
  "Properties" : {
      "[Description](#cfn-apigateway-vpclink-description)" : String,
      "[Name](#cfn-apigateway-vpclink-name)" : String,
      "[TargetArns](#cfn-apigateway-vpclink-targetarns)" : [ String, ... ]
    }
}
```

### YAML<a name="aws-resource-apigateway-vpclink-syntax.yaml"></a>

```
Type: AWS::ApiGateway::VpcLink
Properties: 
  [Description](#cfn-apigateway-vpclink-description): String
  [Name](#cfn-apigateway-vpclink-name): String
  [TargetArns](#cfn-apigateway-vpclink-targetarns): 
    - String
```

## Properties<a name="aws-resource-apigateway-vpclink-properties"></a>

`Description`  <a name="cfn-apigateway-vpclink-description"></a>
A description of the VPC link\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-apigateway-vpclink-name"></a>
A name for the VPC link\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TargetArns`  <a name="cfn-apigateway-vpclink-targetarns"></a>
The ARN of network load balancer of the VPC targeted by the VPC link\. The network load balancer must be owned by the same AWS account of the API owner\.  
*Required*: Yes  
*Type*: List of String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-apigateway-vpclink-return-values"></a>

### Ref<a name="aws-resource-apigateway-vpclink-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the ID of the `VpcLink`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-apigateway-vpclink--examples"></a>



### Create VPC link<a name="aws-resource-apigateway-vpclink--examples--Create_VPC_link"></a>



#### JSON<a name="aws-resource-apigateway-vpclink--examples--Create_VPC_link--json"></a>

```
{
    "Parameters": {
        "description": {
            "Type": "String"
        },
        "name": {
            "Type": "String"
        }
    },
    "Resources": {
        "MyVpcLink": {
            "Type": "AWS::ApiGateway::VpcLink",
            "Properties": {
                "Description": {
                    "Ref": "description"
                },
                "Name": {
                    "Ref": "name"
                },
                "TargetArns": [
                    {
                        "Ref": "MyLoadBalancer"
                    }
                ]
            }
        },
        "MyLoadBalancer": {
            "Type": "AWS::ElasticLoadBalancingV2::LoadBalancer",
            "Properties": {
                "Type": "network",
                "Subnets": [
                    {
                        "Ref": "MySubnet"
                    }
                ]
            }
        },
        "MySubnet": {
            "Type": "AWS::EC2::Subnet",
            "Properties": {
                "VpcId": {
                    "Ref": "MyVPC"
                },
                "CidrBlock": "10.0.0.0/24"
            }
        },
        "MyVPC": {
            "Type": "AWS::EC2::VPC",
            "Properties": {
                "CidrBlock": "10.0.0.0/16"
            }
        },
        "MyInternetGateway": {
            "Type": "AWS::EC2::InternetGateway"
        },
        "MyInternetGatewayAttachment": {
            "Type": "AWS::EC2::VPCGatewayAttachment",
            "Properties": {
                "VpcId": {
                    "Ref": "MyVPC"
                },
                "InternetGatewayId": {
                    "Ref": "MyInternetGateway"
                }
            }
        }
    }
}
```

#### YAML<a name="aws-resource-apigateway-vpclink--examples--Create_VPC_link--yaml"></a>

```
Parameters:
    description:
        Type: String
    name:
        Type: String
Resources:
    MyVpcLink:
        Type: AWS::ApiGateway::VpcLink
        Properties:
            Description: !Ref description
            Name: !Ref name
            TargetArns:
               - !Ref MyLoadBalancer
    MyLoadBalancer:
            Type: AWS::ElasticLoadBalancingV2::LoadBalancer
            Properties:
                Type: network
                Subnets:
                   - !Ref MySubnet
    MySubnet:
        Type: AWS::EC2::Subnet
        Properties:
            VpcId: !Ref MyVPC
            CidrBlock: 10.0.0.0/24
    MyVPC:
        Type: AWS::EC2::VPC
        Properties:
            CidrBlock: 10.0.0.0/16
    MyInternetGateway:
        Type: AWS::EC2::InternetGateway
    MyInternetGatewayAttachment:
        Type: AWS::EC2::VPCGatewayAttachment
        Properties:
            VpcId: !Ref MyVPC
            InternetGatewayId: !Ref MyInternetGateway
```

## See also<a name="aws-resource-apigateway-vpclink--seealso"></a>
+ [vpclink:create](https://docs.aws.amazon.com/apigateway/api-reference/link-relation/vpclink-create/) in the *Amazon API Gateway REST API Reference*

