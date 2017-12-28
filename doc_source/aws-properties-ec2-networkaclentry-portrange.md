# EC2 NetworkAclEntry PortRange<a name="aws-properties-ec2-networkaclentry-portrange"></a>

The `PortRange` property is an embedded property of the AWS::EC2::NetworkAclEntry type\.

## Syntax<a name="w3ab2c21c14d585b5"></a>

### JSON<a name="aws-properties-ec2-networkaclentry-portrange-syntax.json"></a>

```
{
   "[[ERROR] BAD/MISSING LINK TEXT](#cfn-ec2-networkaclentry-portrange-from)" : Integer,
   "[[ERROR] BAD/MISSING LINK TEXT](#cfn-ec2-networkaclentry-portrange-to)" : Integer
}
```

### YAML<a name="aws-properties-ec2-networkaclentry-portrange-syntax.yaml"></a>

```
[[ERROR] BAD/MISSING LINK TEXT](#cfn-ec2-networkaclentry-portrange-from): Integer
[[ERROR] BAD/MISSING LINK TEXT](#cfn-ec2-networkaclentry-portrange-to): Integer
```

## Properties<a name="w3ab2c21c14d585b7"></a>

`From`  
The first port in the range\.  
*Required: *Conditional\. Required if you specify 6 \(TCP\) or 17 \(UDP\) for the protocol parameter\.  
*Type*: Integer

`To`  
The last port in the range\.  
*Required: *Conditional\. Required if you specify 6 \(TCP\) or 17 \(UDP\) for the protocol parameter\.  
*Type*: Integer