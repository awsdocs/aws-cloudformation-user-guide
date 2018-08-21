# EC2 NetworkAclEntry PortRange<a name="aws-properties-ec2-networkaclentry-portrange"></a>

The `PortRange` property is an embedded property of the [AWS::EC2::NetworkAclEntry](aws-resource-ec2-network-acl-entry.md) type\.

## Syntax<a name="w3ab2c21c14d745b5"></a>

### JSON<a name="aws-properties-ec2-networkaclentry-portrange-syntax.json"></a>

```
{
   "[From](#cfn-ec2-networkaclentry-portrange-from)" : Integer,
   "[To](#cfn-ec2-networkaclentry-portrange-to)" : Integer
}
```

### YAML<a name="aws-properties-ec2-networkaclentry-portrange-syntax.yaml"></a>

```
[From](#cfn-ec2-networkaclentry-portrange-from): Integer
[To](#cfn-ec2-networkaclentry-portrange-to): Integer
```

## Properties<a name="w3ab2c21c14d745b7"></a>

`From`  <a name="cfn-ec2-networkaclentry-portrange-from"></a>
The first port in the range\.  
*Required*: Conditional\. Required if you specify 6 \(TCP\) or 17 \(UDP\) for the protocol parameter\.  
*Type*: Integer

`To`  <a name="cfn-ec2-networkaclentry-portrange-to"></a>
The last port in the range\.  
*Required*: Conditional\. Required if you specify 6 \(TCP\) or 17 \(UDP\) for the protocol parameter\.  
*Type*: Integer