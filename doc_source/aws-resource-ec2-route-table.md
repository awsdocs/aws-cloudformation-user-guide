# AWS::EC2::RouteTable<a name="aws-resource-ec2-route-table"></a>

Specifies a route table for a specified VPC\. After you create a route table, you can add routes and associate the table with a subnet\.

For more information, see [Route Tables](https://docs.aws.amazon.com/AmazonVPC/latest/UserGuide/VPC_Route_Tables.html) in the *Amazon Virtual Private Cloud User Guide*\.

## Syntax<a name="aws-resource-ec2-route-table-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ec2-route-table-syntax.json"></a>

```
{
  "Type" : "AWS::EC2::RouteTable",
  "Properties" : {
      "[Tags](#cfn-ec2-routetable-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[VpcId](#cfn-ec2-routetable-vpcid)" : String
    }
}
```

### YAML<a name="aws-resource-ec2-route-table-syntax.yaml"></a>

```
Type: AWS::EC2::RouteTable
Properties: 
  [Tags](#cfn-ec2-routetable-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [VpcId](#cfn-ec2-routetable-vpcid): String
```

## Properties<a name="aws-resource-ec2-route-table-properties"></a>

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

## Return values<a name="aws-resource-ec2-route-table-return-values"></a>

### Ref<a name="aws-resource-ec2-route-table-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the ID of the route table\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-ec2-route-table--examples"></a>



### Route Table<a name="aws-resource-ec2-route-table--examples--Route_Table"></a>

The following example uses the VPC ID from a VPC named myVPC that was declared elsewhere in the same template\.

#### JSON<a name="aws-resource-ec2-route-table--examples--Route_Table--json"></a>

```
"myRouteTable" : {
   "Type" : "AWS::EC2::RouteTable",
   "Properties" : {
      "VpcId" : { "Ref" : "myVPC" },
      "Tags" : [ { "Key" : "foo", "Value" : "bar" } ]
   }
}
```

#### YAML<a name="aws-resource-ec2-route-table--examples--Route_Table--yaml"></a>

```
  myRouteTable:
    Type: AWS::EC2::RouteTable
    Properties:
      VpcId:  
        Ref: myVPC
      Tags:
      - Key: foo
        Value: bar
```

## See also<a name="aws-resource-ec2-route-table--seealso"></a>
+  [AWS::EC2::Route](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-route.html)
+  [CreateRouteTable](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_CreateRouteTable.html) in the *Amazon EC2 API Reference*
+  [Route Tables](https://docs.aws.amazon.com/vpc/latest/userguide/VPC_Route_Tables.html) in the *Amazon VPC User Guide*
+  [Using Tags](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/Using_Tags.html) in the *Amazon Elastic Compute Cloud User Guide*

