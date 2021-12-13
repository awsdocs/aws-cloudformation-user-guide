# AWS::EC2::SubnetRouteTableAssociation<a name="aws-resource-ec2-subnetroutetableassociation"></a>

Associates a subnet with a route table\. The subnet and route table must be in the same VPC\. This association causes traffic originating from the subnet to be routed according to the routes in the route table\. A route table can be associated with multiple subnets\. If you want to associate a route table with a VPC, see [ AWS::EC2::RouteTable](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-route-table.html)\.

## Syntax<a name="aws-resource-ec2-subnetroutetableassociation-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ec2-subnetroutetableassociation-syntax.json"></a>

```
{
  "Type" : "AWS::EC2::SubnetRouteTableAssociation",
  "Properties" : {
      "[RouteTableId](#cfn-ec2-subnetroutetableassociation-routetableid)" : String,
      "[SubnetId](#cfn-ec2-subnetroutetableassociation-subnetid)" : String
    }
}
```

### YAML<a name="aws-resource-ec2-subnetroutetableassociation-syntax.yaml"></a>

```
Type: AWS::EC2::SubnetRouteTableAssociation
Properties: 
  [RouteTableId](#cfn-ec2-subnetroutetableassociation-routetableid): String
  [SubnetId](#cfn-ec2-subnetroutetableassociation-subnetid): String
```

## Properties<a name="aws-resource-ec2-subnetroutetableassociation-properties"></a>

`RouteTableId`  <a name="cfn-ec2-subnetroutetableassociation-routetableid"></a>
The ID of the route table\.  
The physical ID changes when the route table ID is changed\.   
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SubnetId`  <a name="cfn-ec2-subnetroutetableassociation-subnetid"></a>
The ID of the subnet\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-ec2-subnetroutetableassociation-return-values"></a>

### Ref<a name="aws-resource-ec2-subnetroutetableassociation-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the ID of the subnet route table association\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-ec2-subnetroutetableassociation-return-values-fn--getatt"></a>

#### <a name="aws-resource-ec2-subnetroutetableassociation-return-values-fn--getatt-fn--getatt"></a>

`Id`  <a name="Id-fn::getatt"></a>
Not currently supported by AWS CloudFormation\.

## Examples<a name="aws-resource-ec2-subnetroutetableassociation--examples"></a>



### Subnet route table association<a name="aws-resource-ec2-subnetroutetableassociation--examples--Subnet_route_table_association"></a>

The following example associates a subnet with a route table\.

#### JSON<a name="aws-resource-ec2-subnetroutetableassociation--examples--Subnet_route_table_association--json"></a>

```
"mySubnetRouteTableAssociation" : {
   "Type" : "AWS::EC2::SubnetRouteTableAssociation",
   "Properties" : {
      "SubnetId" : { "Ref" : "mySubnet" },
      "RouteTableId" : { "Ref" : "myRouteTable" }
   }
}
```

#### YAML<a name="aws-resource-ec2-subnetroutetableassociation--examples--Subnet_route_table_association--yaml"></a>

```
  mySubnetRouteTableAssociation:
    Type: AWS::EC2::SubnetRouteTableAssociation
    Properties:
      SubnetId:
        Ref: mySubnet
      RouteTableId:
        Ref: myRouteTable
```

## See also<a name="aws-resource-ec2-subnetroutetableassociation--seealso"></a>
+  [AssociateRouteTable](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_AssociateRouteTable.html) in the *Amazon EC2 API Reference*
+ [Route tables](https://docs.aws.amazon.com/vpc/latest/userguide/VPC_Route_Tables.html) in the *Amazon VPC User Guide*

