# AWS::S3Outposts::Endpoint<a name="aws-resource-s3outposts-endpoint"></a>

This AWS::S3Outposts::Endpoint resource specifies an endpoint and associates it with the specified Outpost\.

Amazon S3 on Outposts access points simplify managing data access at scale for shared datasets in S3 on Outposts\. S3 on Outposts uses endpoints to connect to S3 on Outposts buckets so that you can perform actions within your virtual private cloud \(VPC\)\. For more information, see [ Accessing S3 on Outposts using VPC\-only access points](https://docs.aws.amazon.com/AmazonS3/latest/userguide/AccessingS3Outposts.html)\.

**Note**  
It can take up to 5 minutes for this resource to be created\.



## Syntax<a name="aws-resource-s3outposts-endpoint-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-s3outposts-endpoint-syntax.json"></a>

```
{
  "Type" : "AWS::S3Outposts::Endpoint",
  "Properties" : {
      "[AccessType](#cfn-s3outposts-endpoint-accesstype)" : String,
      "[CustomerOwnedIpv4Pool](#cfn-s3outposts-endpoint-customerownedipv4pool)" : String,
      "[OutpostId](#cfn-s3outposts-endpoint-outpostid)" : String,
      "[SecurityGroupId](#cfn-s3outposts-endpoint-securitygroupid)" : String,
      "[SubnetId](#cfn-s3outposts-endpoint-subnetid)" : String
    }
}
```

### YAML<a name="aws-resource-s3outposts-endpoint-syntax.yaml"></a>

```
Type: AWS::S3Outposts::Endpoint
Properties: 
  [AccessType](#cfn-s3outposts-endpoint-accesstype): String
  [CustomerOwnedIpv4Pool](#cfn-s3outposts-endpoint-customerownedipv4pool): String
  [OutpostId](#cfn-s3outposts-endpoint-outpostid): String
  [SecurityGroupId](#cfn-s3outposts-endpoint-securitygroupid): String
  [SubnetId](#cfn-s3outposts-endpoint-subnetid): String
```

## Properties<a name="aws-resource-s3outposts-endpoint-properties"></a>

`AccessType`  <a name="cfn-s3outposts-endpoint-accesstype"></a>
The container for the type of connectivity used to access the Amazon S3 on Outposts endpoint\. To use the Amazon VPC, choose `Private`\. To use the endpoint with an on\-premises network, choose `CustomerOwnedIp`\. If you choose `CustomerOwnedIp`, you must also provide the customer\-owned IP address pool \(CoIP pool\)\.  
`Private` is the default access type value\.
*Required*: No  
*Type*: String  
*Allowed values*: `CustomerOwnedIp | Private`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`CustomerOwnedIpv4Pool`  <a name="cfn-s3outposts-endpoint-customerownedipv4pool"></a>
The ID of the customer\-owned IPv4 address pool \(CoIP pool\) for the endpoint\. IP addresses are allocated from this pool for the endpoint\.  
*Required*: No  
*Type*: String  
*Pattern*: `^ipv4pool-coip-([0-9a-f]{17})$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`OutpostId`  <a name="cfn-s3outposts-endpoint-outpostid"></a>
The ID of the Outpost\.   
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SecurityGroupId`  <a name="cfn-s3outposts-endpoint-securitygroupid"></a>
The ID of the security group to use with the endpoint\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SubnetId`  <a name="cfn-s3outposts-endpoint-subnetid"></a>
The ID of the subnet\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-s3outposts-endpoint-return-values"></a>

### Ref<a name="aws-resource-s3outposts-endpoint-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the Amazon Resource Name \(ARN\) for the endpoint\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-s3outposts-endpoint-return-values-fn--getatt"></a>

#### <a name="aws-resource-s3outposts-endpoint-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The ARN of the endpoint\.

`CidrBlock`  <a name="CidrBlock-fn::getatt"></a>
The VPC CIDR block committed by this endpoint\.

`CreationTime`  <a name="CreationTime-fn::getatt"></a>
The time the endpoint was created\.

`Id`  <a name="Id-fn::getatt"></a>
The ID of the endpoint\. 

`NetworkInterfaces`  <a name="NetworkInterfaces-fn::getatt"></a>
The network interface of the endpoint\.

`Status`  <a name="Status-fn::getatt"></a>
The status of the endpoint\.

## Examples<a name="aws-resource-s3outposts-endpoint--examples"></a>

### Creating an endpoint for your Outpost using CloudFormation<a name="aws-resource-s3outposts-endpoint--examples--Creating_an_endpoint_for_your_Outpost_using_CloudFormation"></a>

This example creates an endpoint for an Outpost\.

#### JSON<a name="aws-resource-s3outposts-endpoint--examples--Creating_an_endpoint_for_your_Outpost_using_CloudFormation--json"></a>

```
{
    "AWSTemplateFormatVersion": "2010-09-09",
    "Description": "Endpoint",
    "Resources": {
        "ExampleS3OutpostsEndpoint": {
            "Type": "AWS::S3Outposts::Endpoint",
            "Properties": {
                "OutpostID": "op-01ac5d28a6a232977",
                "SecurityGroupID": "sg-0eada697f44597077",
                "SubnetID": "subnet-0e866e469c4ec9b77"
            }
        }
    },
    "Outputs": {
        "ExampleS3OutpostsEndpointARN": {
            "Description": "The ARN of ExampleS3OutpostsEndpoint",
            "Value": {
                "Ref": "ExampleS3OutpostsEndpoint"
            }
        },
        "ExampleS3OutpostsEndpointID": {
            "Description": "The ID of ExampleS3OutpostsEndpoint",
            "Value": {
                "Fn::GetAtt": [
                    "ExampleS3OutpostsEndpoint",
                    "ID"
                ]
            }
        },
        "ExampleS3OutpostsEndpointStackID": {
            "Description": "The stack ID",
            "Value": {
                "Ref": "AWS::StackID"
            },
            "Export": {
                "Name": {
                    "Fn::Sub": "${AWS::StackName}-StackID"
                }
            }
        }
    }
}
```

#### YAML<a name="aws-resource-s3outposts-endpoint--examples--Creating_an_endpoint_for_your_Outpost_using_CloudFormation--yaml"></a>

```
AWSTemplateFormatVersion: '2010-09-09'
Description: Endpoint
Resources:
  ExampleS3OutpostsEndpoint:
    Type: AWS::S3Outposts::Endpoint
    Properties:
      OutpostID: op-01ac5d28a6a232977
      SecurityGroupID: sg-0eada697f44597077
      SubnetID: subnet-0e866e469c4ec9b77
Outputs:
  ExampleS3OutpostsEndpointARN:
    Description: The ARN of ExampleS3OutpostsEndpoint
    Value:
      Ref: ExampleS3OutpostsEndpoint
  ExampleS3OutpostsEndpointID:
    Description: The ID of ExampleS3OutpostsEndpoint
    Value:
      Fn::GetAtt:
      - ExampleS3OutpostsEndpoint
      - ID
  ExampleS3OutpostsEndpointStackID:
    Description: The stack ID
    Value:
      Ref: AWS::StackID
    Export:
      Name:
        Fn::Sub: "${AWS::StackName}-StackID"
```

### Creating an on\-premises endpoint for your Outpost using CloudFormation<a name="aws-resource-s3outposts-endpoint--examples--Creating_an_on-premises_endpoint_for_your_Outpost_using_CloudFormation"></a>

This example creates an on\-premises endpoint for an Outpost using customer\-owner IP \(CoIP\) addresses\.

#### JSON<a name="aws-resource-s3outposts-endpoint--examples--Creating_an_on-premises_endpoint_for_your_Outpost_using_CloudFormation--json"></a>

```
{
    "AWSTemplateFormatVersion": "2010-09-09",
    "Description": "Endpoint",
    "Resources": {
        "ExampleS3OutpostsEndpoint": {
            "Type": "AWS::S3Outposts::Endpoint",
            "Properties": {
                "OutpostID": "op-01ac5d28a6a232977",
                "SecurityGroupID": "sg-0eada697f44597077",
                "SubnetID": "subnet-0e866e469c4ec9b77",
                "AccessType": "CustomerOwnedIp",
                "CustomerOwnedIpv4Pool": "ipv4pool-coip-12345678901234567"
            }
        }
    },
    "Outputs": {
        "ExampleS3OutpostsEndpointARN": {
            "Description": "The ARN of ExampleS3OutpostsEndpoint",
            "Value": {
                "Ref": "ExampleS3OutpostsEndpoint"
            }
        },
        "ExampleS3OutpostsEndpointID": {
            "Description": "The ID of ExampleS3OutpostsEndpoint",
            "Value": {
                "Fn::GetAtt": [
                    "ExampleS3OutpostsEndpoint",
                    "ID"
                ]
            }
        },
        "ExampleS3OutpostsEndpointStackID": {
            "Description": "The stack ID",
            "Value": {
                "Ref": "AWS::StackID"
            },
            "Export": {
                "Name": {
                    "Fn::Sub": "${AWS::StackName}-StackID"
                }
            }
        }
    }
}
```

#### YAML<a name="aws-resource-s3outposts-endpoint--examples--Creating_an_on-premises_endpoint_for_your_Outpost_using_CloudFormation--yaml"></a>

```
AWSTemplateFormatVersion: '2010-09-09'
Description: Endpoint
Resources:
  ExampleS3OutpostsEndpoint:
    Type: AWS::S3Outposts::Endpoint
    Properties:
      OutpostID: op-01ac5d28a6a232977
      SecurityGroupID: sg-0eada697f44597077
      SubnetID: subnet-0e866e469c4ec9b77
      AccessType: CustomerOwnedIp
      CustomerOwnedIpv4Pool: ipv4pool-coip-12345678901234567
Outputs:
  ExampleS3OutpostsEndpointARN:
    Description: The ARN of ExampleS3OutpostsEndpoint
    Value:
      Ref: ExampleS3OutpostsEndpoint
  ExampleS3OutpostsEndpointID:
    Description: The ID of ExampleS3OutpostsEndpoint
    Value:
      Fn::GetAtt:
      - ExampleS3OutpostsEndpoint
      - ID
  ExampleS3OutpostsEndpointStackID:
    Description: The stack ID
    Value:
      Ref: AWS::StackID
    Export:
      Name:
        Fn::Sub: "${AWS::StackName}-StackID"
```