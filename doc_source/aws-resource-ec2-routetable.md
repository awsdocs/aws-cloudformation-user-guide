# AWS::EC2::RouteTable<a name="aws-resource-ec2-routetable"></a>

Specifies a route table for the specified VPC\. After you create a route table, you can add routes and associate the table with a subnet\.

For more information, see [Route Tables](https://docs.aws.amazon.com/AmazonVPC/latest/UserGuide/VPC_Route_Tables.html) in the *Amazon VPC User Guide*\.

## Syntax<a name="aws-resource-ec2-routetable-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ec2-routetable-syntax.json"></a>

```
{
  "Type" : "AWS::EC2::RouteTable",
  "Properties" : {
      "[Tags](#cfn-ec2-routetable-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[VpcId](#cfn-ec2-routetable-vpcid)" : String
    }
}
```

### YAML<a name="aws-resource-ec2-routetable-syntax.yaml"></a>

```
Type: AWS::EC2::RouteTable
Properties: 
  [Tags](#cfn-ec2-routetable-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [VpcId](#cfn-ec2-routetable-vpcid): String
```

## Properties<a name="aws-resource-ec2-routetable-properties"></a>

`Tags`  <a name="cfn-ec2-routetable-tags"></a>
Any tags assigned to the route table\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VpcId`  <a name="cfn-ec2-routetable-vpcid"></a>
The ID of the VPC\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-ec2-routetable-return-values"></a>

### Ref<a name="aws-resource-ec2-routetable-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the ID of the route table\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-ec2-routetable-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-ec2-routetable-return-values-fn--getatt-fn--getatt"></a>

`RouteTableId`  <a name="RouteTableId-fn::getatt"></a>
The ID of the route table\.

## Examples<a name="aws-resource-ec2-routetable--examples"></a>



### Route table<a name="aws-resource-ec2-routetable--examples--Route_table"></a>

The following example uses the VPC ID from a VPC named myVPC that was declared elsewhere in the same template\.

#### JSON<a name="aws-resource-ec2-routetable--examples--Route_table--json"></a>

```
"myRouteTable" : {
   "Type" : "AWS::EC2::RouteTable",
   "Properties" : {
      "VpcId" : { "Ref" : "myVPC" },
      "Tags" : [ { "Key" : "stack", "Value" : "production" } ]
   }
}
```

#### YAML<a name="aws-resource-ec2-routetable--examples--Route_table--yaml"></a>

```
  myRouteTable:
    Type: AWS::EC2::RouteTable
    Properties:
      VpcId:  
        Ref: myVPC
      Tags:
      - Key: stack
        Value: production
```

## See also<a name="aws-resource-ec2-routetable--seealso"></a>
+  [AWS::EC2::Route](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-route.html)
+  [CreateRouteTable](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_CreateRouteTable.html) in the *Amazon EC2 API Reference*
+  [Route tables](https://docs.aws.amazon.com/vpc/latest/userguide/VPC_Route_Tables.html) in the *Amazon VPC User Guide*
+  [Tag your Amazon EC2 resources](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/Using_Tags.html) in the *Amazon EC2 User Guide*

