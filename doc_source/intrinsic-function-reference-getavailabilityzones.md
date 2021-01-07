# `Fn::GetAZs`<a name="intrinsic-function-reference-getavailabilityzones"></a>

The intrinsic function `Fn::GetAZs` returns an array that lists Availability Zones for a specified region in alphabetical order\. Because customers have access to different Availability Zones, the intrinsic function `Fn::GetAZs` enables template authors to write templates that adapt to the calling user's access\. That way you don't have to hard\-code a full list of Availability Zones for a specified region\.

**Important**  
For the EC2\-Classic platform, the `Fn::GetAZs` function returns all Availability Zones for a region\. For the [EC2\-VPC](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ec2-supported-platforms.html) platform, the `Fn::GetAZs` function returns only Availability Zones that have a default subnet unless none of the Availability Zones has a default subnet; in that case, all Availability Zones are returned\.  
Similarly to the response from the `describe-availability-zones` AWS CLI command, the order of the results from the `Fn::GetAZs` function is not guaranteed and can change when new Availability Zones are added\.

IAM permissions

The permissions that you need in order to use the `Fn::GetAZs` function depend on the platform in which you're launching Amazon EC2 instances\. For both platforms, you need permissions to the Amazon EC2 `DescribeAvailabilityZones` and `DescribeAccountAttributes` actions\. For EC2\-VPC, you also need permissions to the Amazon EC2 `DescribeSubnets` action\.

## Declaration<a name="w7739ab1c33c28c36c11"></a>

### JSON<a name="intrinsic-function-reference-getazs-syntax.json"></a>

```
{ "Fn::GetAZs" : "region" }
```

### YAML<a name="intrinsic-function-reference-getazs-syntax.yaml"></a>

Syntax for the full function name:

```
Fn::GetAZs: region
```

Syntax for the short form:

```
!GetAZs region
```

## Parameters<a name="w7739ab1c33c28c36c13"></a>

region  
The name of the region for which you want to get the Availability Zones\.  
You can use the `AWS::Region` pseudo parameter to specify the region in which the stack is created\. Specifying an empty string is equivalent to specifying `AWS::Region`\.

## Return value<a name="w7739ab1c33c28c36c15"></a>

The list of Availability Zones for the region\.

## Examples<a name="w7739ab1c33c28c36c17"></a>

### Evaluate a Region<a name="w7739ab1c33c28c36c17b2"></a>

For these examples, AWS CloudFormation evaluates `Fn::GetAZs` to the following array—assuming that the user has created the stack in the `us-east-1` region:

`[ "us-east-1a", "us-east-1b", "us-east-1c", "us-east-1d" ]`

#### JSON<a name="intrinsic-function-reference-getazs-example1.json"></a>

```
1. { "Fn::GetAZs" : "" }
2. { "Fn::GetAZs" : { "Ref" : "AWS::Region" } }
3. { "Fn::GetAZs" : "us-east-1" }
```

#### YAML<a name="intrinsic-function-reference-getazs-example1.yaml"></a>

```
1. Fn::GetAZs: ""
2. Fn::GetAZs:
3.   Ref: "AWS::Region"
4. Fn::GetAZs: us-east-1
```

 

### Specify a subnet's Availability Zone<a name="w7739ab1c33c28c36c17b4"></a>

The following example uses `Fn::GetAZs` to specify a subnet's Availability Zone:

#### JSON<a name="intrinsic-function-reference-getazs-example.json"></a>

```
"mySubnet" : {
  "Type" : "AWS::EC2::Subnet",
  "Properties" : {
    "VpcId" : { 
      "Ref" : "VPC"   
    },
    "CidrBlock" : "10.0.0.0/24",
    "AvailabilityZone" : {
      "Fn::Select" : [ 
        "0", 
        { 
          "Fn::GetAZs" : "" 
        } 
      ]
    }
  }
}
```

#### YAML<a name="intrinsic-function-reference-getazs-example.yaml"></a>

```
mySubnet: 
  Type: "AWS::EC2::Subnet"
  Properties: 
    VpcId: 
      !Ref VPC
    CidrBlock: 10.0.0.0/24
    AvailabilityZone: 
      Fn::Select: 
        - 0
        - Fn::GetAZs: ""
```

 

### Nested functions with short form YAML<a name="w7739ab1c33c28c36c17b8"></a>

The following examples show valid patterns for using nested intrinsic functions using short form YAML\. You can't nest short form functions consecutively, so a pattern like `!GetAZs !Ref` is invalid\.

#### YAML<a name="intrinsic-function-reference-select-example3.yaml"></a>

```
1. AvailabilityZone: !Select 
2.   - 0
3.   - !GetAZs 
4.     Ref: 'AWS::Region'
```

#### YAML<a name="intrinsic-function-reference-select-example4.yaml"></a>

```
1. AvailabilityZone: !Select 
2.   - 0
3.   - Fn::GetAZs: !Ref 'AWS::Region'
```

## Supported functions<a name="w7739ab1c33c28c36c19"></a>

You can use the `Ref` function in the `Fn::GetAZs` function\.