# EC2 NetworkAclEntry Icmp<a name="aws-properties-ec2-networkaclentry-icmp"></a>

The `Icmp` property is an embedded property of the [AWS::EC2::NetworkAclEntry](aws-resource-ec2-network-acl-entry.md) type\.

## Syntax<a name="w3ab2c21c14d740b5"></a>

### JSON<a name="aws-properties-ec2-networkaclentry-icmp-syntax.json"></a>

```
{
   "[Code](#cfn-ec2-networkaclentry-icmp-code)" : Integer,
   "[Type](#cfn-ec2-networkaclentry-icmp-type)" : Integer
}
```

### YAML<a name="aws-properties-ec2-networkaclentry-icmp-syntax.yaml"></a>

```
[Code](#cfn-ec2-networkaclentry-icmp-code): Integer
[Type](#cfn-ec2-networkaclentry-icmp-type): Integer
```

## Properties<a name="w3ab2c21c14d740b7"></a>

`Code`  <a name="cfn-ec2-networkaclentry-icmp-code"></a>
The Internet Control Message Protocol \(ICMP\) code\. You can use \-1 to specify all ICMP codes for the given ICMP type\.  
*Required*: Conditional\. Required if you specify `1` \(ICMP\) for the CreateNetworkAclEntry protocol parameter\.  
*Type*: Integer

`Type`  <a name="cfn-ec2-networkaclentry-icmp-type"></a>
The Internet Control Message Protocol \(ICMP\) type\. You can use \-1 to specify all ICMP types\.  
*Required*: Conditional\. Required if you specify `1` \(ICMP\) for the CreateNetworkAclEntry protocol parameter\.  
*Type*: Integer