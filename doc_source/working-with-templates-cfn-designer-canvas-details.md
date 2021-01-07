# Canvas pane<a name="working-with-templates-cfn-designer-canvas-details"></a>

Designer displays your template resources as a diagram in the **canvas** pane\. You can modify the diagram's layout, add or remove resources, and add or remove connections between resources in this pane\. For example, you can add an Auto Scaling group and a launch configuration from the **Resource types** pane to the **canvas** pane\. To connect these related resources, you simply drag a connection between them\.

## How does Designer model resources?<a name="w7739ab1c27c17c13c15b5"></a>

When you drag a resource from the **Resource types** pane to the **canvas** pane, Designer models it as a container or as a square object\.

Containers  
Container resources are resizable rectangles that can contain other resources\. For example, Designer models the `AWS::EC2::VPC` resource type as a container\. You can drag resources, such as a subnet, into the VPC\.  
**Container resource**  

![\[Example of a container resource.\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/images/designer-canvas-container.png)

Square objects  
Square objects resources can't be resized or contain other resources\. For example, Designer models the `AWS::EC2::Instance` resource type as a square object\.  
**Square object**  

![\[Example of a square object.\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/images/designer-canvas-square.png)

## Connecting resources<a name="w7739ab1c27c17c13c15b7"></a>

You connect resources to create associations between related resources\. For example, when you add an Internet gateway and a VPC to the **canvas** pane, they have no relationship\. To attach the gateway to the VPC, you must connect them\. The method for connecting resources depends on the resource type and how Designer models the resource\. The following descriptions and figures explain each method\.

Adding resources to containers  
When you drag valid resource into containers, Designer automatically creates associations between the resource and the container\. For example, VPCs are container resources; you can drag a subnet into a VPC, and Designer automatically associates the two resources\.  

![\[A subnet resource inside a VPC container.\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/images/designer-canvas-subnetinvpc.png)
These associations are represented in your template as a `Ref` intrinsic function, as shown in the following example:   
JSON  

```
"PublicSubnet": {
  "Type": "AWS::EC2::Subnet",
  "Properties": {
      "VpcId": {
          "Ref": "VPC"
      },
      "CidrBlock": "10.0.0.0/24"
  }
```
YAML  

```
PublicSubnet:
  Type: 'AWS::EC2::Subnet'
  Properties:
    VpcId: !Ref VPC
    CidrBlock: 10.0.0.0/24
```
In some cases, dropping a resource into a container doesn't create an association; you must drag a connection between the resources \(see the next method for information about dragging connections between resources\)\. To see if Designer associates resources, use the integrated JSON and YAML editor to look for a `Ref` from one resource to the other\. For example, when you add an Auto Scaling group in a subnet container, Designer doesn't specify the group's `VPCZoneIdentifier` \(subnet\) property\. To associate the two resources, you must drag a connection from the Auto Scaling group to the subnet\.

Dragging connections between resources  
The edge of each square and container resource has one or more dots, which represent the resources that you can create connections with\. To create a connection, drag a connector line from the dot to the corresponding resource type\. For example, to attach an Internet gateway to a VPC, drag a line from the VPC gateway attachment dot to anywhere on the VPC\.  

![\[Dragging a connector line to create a connection (shown as an arrow).\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/images/designer-canvas-vpcgateway.png)
These associations are represented in your template as a `Ref` intrinsic function or as a separate resource type\. For example, when you connect an Internet gateway with a VPC, Designer creates an `AWS::EC2::VPCGatewayAttachment` resource type in your template to associate them\. Resources like these are not listed in the **Resource types** pane\.  
JSON  

```
"VPCGatewayAttachment": {
  "Type": "AWS::EC2::VPCGatewayAttachment",
  "Properties": {
      "InternetGatewayId": {
          "Ref": "InternetGateway"
      },
      "VpcId": {
          "Ref": "VPC"
      }
  }
```
YAML  

```
VPCGatewayAttachment:
  Type: 'AWS::EC2::VPCGatewayAttachment'
  Properties:
    InternetGatewayId: !Ref InternetGateway
    VpcId: !Ref VPC
```

Coding connections between resources  
In some cases, you must edit the template's JSON or YAML to create connections, such as when you connect two security groups\. When you must edit the JSON or YAML to create connections, you create hard\-coded connections \(dashed\-line connections\)\. You cannot create or edit these connections in the **canvas** pane\.  

![\[Two resources connected with a dashed-line connection.\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/images/designer-canvas-hardcodedconnection.png)
Typically, when you embed references \(`Ref`\) within a resource's property, you create hard\-coded connections\. For example, you can define a connection between two security groups where one security group has an embedded ingress rule that permits traffic from the other\. The following `WebServerSecurityGroup` resource has an ingress rule with a reference to the `PublicLoadBalancerSecurityGroup` resource\.  
JSON  

```
"WebServerSecurityGroup": {
  "Type": "AWS::EC2::SecurityGroup",
  "Properties": {
      "VpcId": {
          "Ref": "VPC"
      },
      "GroupDescription": "Allow access from HTTP and SSH traffic",
      "SecurityGroupIngress": [
          {
              "IpProtocol": "tcp",
              "FromPort": "80",
              "ToPort": "80",
              "CidrIp": "0.0.0.0/0"
          },
          {
              "IpProtocol": "tcp",
              "FromPort": "22",
              "ToPort": "22",
              "CidrIp": {
                  "Ref": "SSHLocation"
              }
          }
      ]
  }
...
```
YAML  

```
WebServerSecurityGroup:
  Type: 'AWS::EC2::SecurityGroup'
  Properties:
    VpcId: !Ref VPC
    GroupDescription: Allow access from HTTP and SSH traffic
    SecurityGroupIngress:
      - IpProtocol: tcp
        FromPort: '80'
        ToPort: '80'
        CidrIp: 0.0.0.0/0
      - IpProtocol: tcp
        FromPort: '22'
        ToPort: '22'
        CidrIp: !Ref SSHLocation
```

## Accessing common resource actions with the resource menu<a name="w7739ab1c27c17c13c15b9"></a>

The **Resource** menu provides easy access to common resource actions: editing resource properties, duplicating a resource, deleting a resource, or viewing the documentation for the resource\. To view the **Resource** menu, right\-click on a resource in the **canvas** pane\. The documentation link goes to the [template reference](aws-template-resource-type-ref.md), which describes the properties and syntax for that resource\.

**Resource menu**

![\[The resource menu with its four buttons.\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/images/designer-canvas-resourcemenu.png)

## Defining explicit dependencies<a name="w7739ab1c27c17c13c15c11"></a>

To specify the order in which AWS CloudFormation creates and deletes resources, you can create explicit dependencies\. Explicit dependencies are useful for overriding parallel resource creation and deletion\. AWS CloudFormation automatically determines which resources in a template can be processed in parallel and which cannot\. When you specify a property that references an attribute from another source \(using the `Ref` intrinsic function\) or gets an attribute from another resource \(with the `Fn::GetAtt` intrinsic function\) in the same template, this implies a dependency and AWS CloudFormation builds them in the correct order\.

However, in some cases, you must explicitly define dependencies\. For example, a routing rule cannot use an Internet gateway until the gateway has been attached to the VPC\. Normally, AWS CloudFormation creates the routing rule immediately after it creates the Internet gateway due to an implicit dependency\. But, AWS CloudFormation might create the rule before the Internet gateway has attached to the VPC, which causes an error\. Therefore, you must explicitly define a dependency on the gateway\-VPC attachment\.

To create an explicit dependency, drag a line from the `DependsOn` \(**\***\) dot on the route to the gateway\-VPC attachment\.

![\[Dragging the DependsOn dot to create a dependency.\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/images/designer-canvas-routedependsonattachment.png)

For more information about when you might need to create an explicit dependency, see [DependsOn attribute](aws-attribute-dependson.md)\.

### JSON<a name="working-with-templates-cfn-designer-dependson.json"></a>

In JSON, these explicit dependencies are represented as a `DependsOn` attribute on a resource, as shown in the following example:

```
"PublicRoute": {
  "Type": "AWS::EC2::Route",
  "DependsOn": "VPCGatewayAttachment",
  "Properties": {
      "DestinationCidrBlock": "0.0.0.0/0",
      "RouteTableId": {
          "Ref": "PublicRouteTable"
      },
      "GatewayId": {
          "Ref": "InternetGateway"
      }
  }
```

### YAML<a name="working-with-templates-cfn-designer-dependson.yaml"></a>

In YAML, these explicit dependencies are represented as a `DependsOn` attribute on a resource, as shown in the following example:

```
PublicRoute:
  Type: 'AWS::EC2::Route'
  DependsOn:
    - VPCGatewayAttachment
  Properties:
    DestinationCidrBlock: 0.0.0.0/0
    RouteTableId: !Ref PublicRouteTable
    GatewayId: !Ref InternetGateway
```