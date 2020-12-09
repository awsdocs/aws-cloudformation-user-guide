# Walkthrough: Use AWS CloudFormation Designer to create a basic web server<a name="working-with-templates-cfn-designer-walkthrough-createbasicwebserver"></a>

AWS CloudFormation Designer graphically represents your templates to help you see the resources in the template and how they're connected\. The integrated JSON and YAML editor makes it easy to modify templates directly in the AWS CloudFormation console\. To demonstrate how to use both of these components, we'll use AWS CloudFormation Designer to build a basic web server in a VPC\. Then, we'll save the template and use it to create an AWS CloudFormation stack\. 

By the end of the walkthrough, you'll have a template similar to the following sample: [https://console\.aws\.amazon\.com/cloudformation/designer/home?templateUrl=https://s3\.amazonaws\.com/cloudformation\-examples/sample\-ec2\-vpc\.template&region=us\-east\-1](https://console.aws.amazon.com/cloudformation/designer/home?templateUrl=https://s3.amazonaws.com/cloudformation-examples/sample-ec2-vpc.template&region=us-east-1)\.

In the walkthrough, you will complete the following steps:

1. [Add and connect resources\.](#working-with-templates-cfn-designer-walkthrough-createbasicwebserver-addresources)

   When you first open AWS CloudFormation Designer, you start with a blank template\. We'll use AWS CloudFormation Designer to start populating the template by dragging resources, such as a VPC and an EC2 instance into your template\. We'll also create links between them\. For example, we'll use AWS CloudFormation Designer to create a connection between the Internet gateway and the VPC\.

1. [Add template parameters, mappings, and outputs\.](#working-with-templates-cfn-designer-walkthrough-createbasicwebserver-addother)

   We'll use the AWS CloudFormation Designer integrated editor to add other template components to make the template more useful\. For example, we'll add parameters to the template so that you can specify input values when you create a stack\. That way you don't have to constantly edit the template for property values that you might commonly change\.

1. [Specify resource properties\.](#working-with-templates-cfn-designer-walkthrough-createbasicwebserver-resourceproperties)

   We'll use the integrated editor again to specify configuration settings for our resources\.

1. [Provision resources](#working-with-templates-cfn-designer-walkthrough-createbasicwebserver-provision)

   None of your template resources are up and running until you create a stack\. We'll use the template that you just created to launch an AWS CloudFormation stack, which will provision all the resources that are defined in your template\.
**Note**  
AWS CloudFormation is a free service; however, you are charged for the AWS resources you include in your stacks at the current rate for each\. For more information about AWS pricing, see the detail page for each product on [http://aws\.amazon\.com](http://aws.amazon.com)\.

Prerequisites

This walkthrough assumes that you have a working knowledge of Amazon Virtual Private Cloud \(Amazon VPC\), Amazon Elastic Compute Cloud \(Amazon EC2\), and AWS CloudFormation\. For context, each procedure provides some basic information about each resource\.

Also, before you begin, make sure you have an Amazon EC2 key pair in the region in which you're creating your stack\. For more information, see [Amazon EC2 key pairs](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ec2-key-pairs.html) in the *Amazon EC2 User Guide for Linux Instances*\.

## Step 1: Add and connect resources<a name="working-with-templates-cfn-designer-walkthrough-createbasicwebserver-addresources"></a>

We'll use the AWS CloudFormation Designer drag\-and\-drop interface to add an Amazon EC2 instance and network resources, such as a VPC, subnet, route table, and Internet gateway\. After adding all the resources, we'll create connections between them\. For example, we'll associate the Internet gateway with a VPC\.

**To add resources to a template**

1. Open AWS CloudFormation Designer at [https://console\.aws\.amazon\.com/cloudformation/designer](https://console.aws.amazon.com/cloudformation/designer)\.

1. In the integrated editor on the lower half of the page, choose **Edit** \(![\[Image NOT FOUND\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/images/designer-edit-icon.png)\)\.

1. Change the template name to `BasicWebServerInVPC` and then press **Enter**\.

   Currently, we have a blank template that isn't valid\. In the next steps, we'll add resources to make it valid\.

1. In the **Resource types** pane, from within the **EC2** category, drag a **VPC** resource type onto the **Canvas** pane\.

   The resources are organized by resource categories\. All of the resources we're adding are in the **EC2** category\.

   AWS CloudFormation Designer immediately modifies your template to include a VPC resource, with the results looking similar to the following JSON snippet\.

   ```
     "Resources": {
       "VPC431KO": {
         "Type": "AWS::EC2::VPC",
         "Properties": {},
         "Metadata": {
           "AWS::CloudFormation::Designer": {
             "id": "445730ea-0d11-45ba-b6ac-12345EXAMPLE"
           }
         }
       }
     }
   ```

   The YAML snippet looks similar to the following\.

   ```
   Resources:
     VPC431KO:
       Type: 'AWS::EC2::VPC'
       Properties: {}
       Metadata:
         'AWS::CloudFormation::Designer':
           id: 9430b008-7a03-41ed-b63e-12345EXAMPLE
   ```

   Note that we still need to specify the VPC properties, such as the VPC's CIDR block\. We'll do that later\. This is true for all resources that we'll add\.

1. Rename the VPC\.
**Note**  
When you rename a resource, you rename its logical ID, which is the name that is referenced in the template \(not the name assigned when AWS CloudFormation creates the resource\)\. For more information, see [Resources](resources-section-structure.md)\.

   1. Choose the VPC resource\.

   1. In the integrated editor, choose the **Edit** icon \(![\[Image NOT FOUND\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/images/designer-edit-icon.png)\)\.

   1. Change the name to `VPC`, and then choose **Enter**\.

   Next, we'll add resources to the VPC\.

1. Drag a corner of the VPC resource to expand it so that it's large enough to fit several more resources\.

   We need to add a subnet because you can't add an EC2 instance, which hosts the website, directly into the VPC; instances must be located in a subnet\.

1. Add a **Subnet** resource type inside the VPC and rename it `PublicSubnet`\.

   We will use the subnet to allocate a range of IP addresses in the VPC that you can associate with other AWS resources, such as an Amazon EC2 instance\.

   When you add the subnet inside the VPC, AWS CloudFormation Designer automatically associates the subnet with the VPC\. This association is a container model, where resources inside the container are automatically associated with the container resource\.

1. Add an **Instance** resource type inside the `PublicSubnet` resource and rename it `WebServerInstance`\.

   The instance is a virtual computing environment where you'll host a basic website\. Similar to the way this worked with the subnet and VPC, adding the instance in the subnet automatically associates the instance with the subnet\.

1. Add a **SecurityGroup** resource type inside the VPC and rename it `WebServerSecurityGroup`\.

   The security group is a virtual firewall that controls the inbound and outbound traffic of the web server instance\. It's also required for instances in a VPC\. We'll need to associate the web server instance with this security group, which we'll do later when we specify the instance's properties\.

1. Add an **InternetGateway** resource type anywhere outside of the VPC and rename it `InternetGateway`\.

   The Internet gateway enables communication between the instance that is inside the VPC and the Internet\. Without the Internet gateway, no one can access your website\.

   Although, you can drag the Internet gateway inside the VPC, this doesn't create an association with the VPC\. The Internet gateway doesn't follow the container model; instead, you must drag a connection from the Internet gateway to the VPC, as described in the next step\.

1. Create a connection between the `InternetGateway` resource and the `VPC` resource\.

   1. On the `InternetGateway` resource, hover over the Internet gateway attachment \(`AWS::EC2::VPCGatewayAttachment`\)\.

   1. Drag a connection to the VPC\.

      The border of valid target resources changes color\. In this case, the VPC is the only valid target resource\. This connection creates an attachment resource that associates the Internet gateway with the VPC\.

1. Next, we need to add a route table and route to specify how to direct network traffic from within a subnet\. Add a **RouteTable** inside the VPC and rename it `PublicRouteTable`\.

   This associates a new route table with the VPC\.

1. To add a routing rule to the route table, add a **Route** resource type inside the `PublicRouteTable` resource and rename it `PublicRoute`\.

   We'll use the route to specify where to direct traffic\.

1. For the public route, we want the Internet gateway to be the destination target\. Use `GatewayId` to create a connection from the `PublicRoute` resource to the Internet gateway, similar to the way you created a connection between the Internet gateway and the VPC\.

   AWS CloudFormation can't associate a route with an Internet gateway until you associate the Internet gateway with the VPC\. This means we need to create an explicit dependency on the Internet gateway\-VPC attachment, as described in the next step\. For more information, see [DependsOn attribute](aws-attribute-dependson.md)\.

1. Create an explicit dependency between the `PublicRoute` resource and the Internet gateway\-VPC attachment\.

   1. On the `PublicRoute` resource, hover over the **DependsOn** dot\.

   1. Drag a connection to the Internet gateway\-VPC attachment \(`AWS::EC2::VPCGatewayAttachment`\)\.

      With `DependsOn` connections, AWS CloudFormation Designer creates a dependency \(a `DependsOn` attribute\), where the originating resource depends on the target resource\. In this case, AWS CloudFormation Designer adds a `DependsOn` attribute to the `PublicRoute` resource and specifies the gateway\-VPC attachment as a dependency\.

1. Create another dependency from the `WebServerInstance` resource to the `PublicRoute` resource\.

   The `WebServerInstance` resource depends on the public route to route traffic to the Internet\. Without the public route, the instance cannot send a signal \(using the cfn\-signal helper script\) to notify AWS CloudFormation when the instance configuration and application deployments are complete\.

1. Drag a connection from the `PublicRouteTable` resource to the `PublicSubnet` resource to associate the route table and subnet\.

   Now the public subnet will use the public route table to direct traffic\.

1. From the AWS CloudFormation Designer toolbar, save the template locally by using the **File** menu \(the file icon\)\.

   AWS CloudFormation Designer saves your template on your hard drive\. You can use the template later to create a stack\. We recommend that you save the template regularly to avoid losing changes\.

In this step, we added seven resources to your template and renamed their logical IDs with friendly names\. We also established visual connections with most of the resources to create associations and a dependency\. However, before we can create a stack with this template, we need to create a few more connections \(such as associating the instance with the security group\) and to specify properties for each resource\. In the next step, we'll walk through modifying other components of your template, such as input parameters, by using the AWS CloudFormation Designer integrated editor\.

## Step 2: Add parameters, mappings, and outputs<a name="working-with-templates-cfn-designer-walkthrough-createbasicwebserver-addother"></a>

Before we specify resource properties, we need to add other template components to make reusing the template in multiple environments easier\. In this step, we'll use the AWS CloudFormation Designer integrated editor to add parameters, mappings, and outputs\. Then, we can refer to these parameters and mappings when we specify resource properties\. The walkthrough provides sample JSON and YAML that you can use to copy and paste in to the integrated editor\.

**To add parameters**

Parameters are input values that you specify when you create a stack\. They're useful for passing in values so that you don't have hard coded values in templates\. For example, you don't need to hard code your web server's instance type in your template; instead, you can use a parameter to specify the instance type when you create a stack\. That way you can use the same template to create multiple web servers with different instance types\. For more information, see [Parameters](parameters-section-structure.md)\.

1. Click on an open area in the AWS CloudFormation Designer canvas\.

   Depending on what you have selected, the integrated editor shows either template\-level or resource\-level components that you can edit\. At the template\-level, you can edit all other sections of a template, such as template parameters, mappings, and outputs, except for the Resources section\. At the resource\-level, you can edit resource properties and attributes\.

   Clicking on an open area in the canvas allows you to edit template\-level components\. To edit resource\-level components, select a resource\.

1. In the integrated editor pane, choose the **Parameters** tab in the **Components** view\.

1. Copy the parameters in the following snippet and paste them into the integrated editor\.

   The following JSON snippet adds parameters for specifying your web server's instance type, an Amazon EC2 key\-pair name for SSH access to the web server, and the IP address range that can be used to access the web server using SSH\.

   ```
   {
     "Parameters": {
       "InstanceType" : {
         "Description" : "WebServer EC2 instance type",
         "Type" : "String",
         "Default" : "t2.small",
         "AllowedValues" : [ 
           "t1.micro", 
           "t2.nano", 
           "t2.micro", 
           "t2.small", 
           "t2.medium", 
           "t2.large", 
           "m1.small", 
           "m1.medium", 
           "m1.large", 
           "m1.xlarge", 
           "m2.xlarge", 
           "m2.2xlarge", 
           "m2.4xlarge", 
           "m3.medium", 
           "m3.large", 
           "m3.xlarge", 
           "m3.2xlarge", 
           "m4.large", 
           "m4.xlarge", 
           "m4.2xlarge", 
           "m4.4xlarge", 
           "m4.10xlarge", 
           "c1.medium", 
           "c1.xlarge", 
           "c3.large", 
           "c3.xlarge", 
           "c3.2xlarge", 
           "c3.4xlarge", 
           "c3.8xlarge", 
           "c4.large", 
           "c4.xlarge", 
           "c4.2xlarge", 
           "c4.4xlarge", 
           "c4.8xlarge", 
           "g2.2xlarge", 
           "g2.8xlarge", 
           "r3.large", 
           "r3.xlarge", 
           "r3.2xlarge", 
           "r3.4xlarge", 
           "r3.8xlarge", 
           "i2.xlarge", 
           "i2.2xlarge", 
           "i2.4xlarge", 
           "i2.8xlarge", 
           "d2.xlarge", 
           "d2.2xlarge", 
           "d2.4xlarge", 
           "d2.8xlarge", 
           "hi1.4xlarge", 
           "hs1.8xlarge", 
           "cr1.8xlarge", 
           "cc2.8xlarge", 
           "cg1.4xlarge"
         ],
         "ConstraintDescription" : "must be a valid EC2 instance type."
       },
       "KeyName": {
         "Description": "Name of an EC2 KeyPair to enable SSH access to the instance.",
         "Type": "AWS::EC2::KeyPair::KeyName",
         "ConstraintDescription": "must be the name of an existing EC2 KeyPair."
       },
       "SSHLocation": {
         "Description": " The IP address range that can be used to access the web server using SSH.",
         "Type": "String",
         "MinLength": "9",
         "MaxLength": "18",
         "Default": "0.0.0.0/0",
         "AllowedPattern": "(\\d{1,3})\\.(\\d{1,3})\\.(\\d{1,3})\\.(\\d{1,3})/(\\d{1,2})",
         "ConstraintDescription": "must be a valid IP CIDR range of the form x.x.x.x/x."
       }
     }
   }
   ```

   Here is the same snippet in YAML\.

   ```
   Parameters:
     InstanceType:
       Description: WebServer EC2 instance type
       Type: String
       Default: t2.small
       AllowedValues:
         - t1.micro
         - t2.nano
         - t2.micro
         - t2.small
         - t2.medium
         - t2.large
         - m1.small
         - m1.medium
         - m1.large
         - m1.xlarge
         - m2.xlarge
         - m2.2xlarge
         - m2.4xlarge
         - m3.medium
         - m3.large
         - m3.xlarge
         - m3.2xlarge
         - m4.large
         - m4.xlarge
         - m4.2xlarge
         - m4.4xlarge
         - m4.10xlarge
         - c1.medium
         - c1.xlarge
         - c3.large
         - c3.xlarge
         - c3.2xlarge
         - c3.4xlarge
         - c3.8xlarge
         - c4.large
         - c4.xlarge
         - c4.2xlarge
         - c4.4xlarge
         - c4.8xlarge
         - g2.2xlarge
         - g2.8xlarge
         - r3.large
         - r3.xlarge
         - r3.2xlarge
         - r3.4xlarge
         - r3.8xlarge
         - i2.xlarge
         - i2.2xlarge
         - i2.4xlarge
         - i2.8xlarge
         - d2.xlarge
         - d2.2xlarge
         - d2.4xlarge
         - d2.8xlarge
         - hi1.4xlarge
         - hs1.8xlarge
         - cr1.8xlarge
         - cc2.8xlarge
         - cg1.4xlarge
       ConstraintDescription: must be a valid EC2 instance type.
     KeyName:
       Description: Name of an EC2 KeyPair to enable SSH access to the instance.
       Type: 'AWS::EC2::KeyPair::KeyName'
       ConstraintDescription: must be the name of an existing EC2 KeyPair.
     SSHLocation:
       Description: ' The IP address range that can be used to access the web server using SSH.'
       Type: String
       MinLength: '9'
       MaxLength: '18'
       Default: 0.0.0.0/0
       AllowedPattern: '(\d{1,3})\.(\d{1,3})\.(\d{1,3})\.(\d{1,3})/(\d{1,2})'
       ConstraintDescription: must be a valid IP CIDR range of the form x.x.x.x/x.
   ```

**To add mappings**

Mappings are a set of keys that are associated with a set of name\-value pairs\. They're useful for specifying values based on an input parameter value\. For this walkthrough, we'll use a mapping to specify an AMI ID for an EC2 instance based on the instance type and region in which you create the stack\. For more information, see [Mappings](mappings-section-structure.md)\.

1. In the integrated editor pane, choose the **Mappings** tab\.

1. Copy the following JSON mappings and paste them into the integrated editor\.

   ```
   {      
     "Mappings" : {
       "AWSInstanceType2Arch" : {
         "t1.micro"    : { "Arch" : "HVM64"  },
         "t2.nano"     : { "Arch" : "HVM64"  },
         "t2.micro"    : { "Arch" : "HVM64"  },
         "t2.small"    : { "Arch" : "HVM64"  },
         "t2.medium"   : { "Arch" : "HVM64"  },
         "t2.large"    : { "Arch" : "HVM64"  },
         "m1.small"    : { "Arch" : "HVM64"  },
         "m1.medium"   : { "Arch" : "HVM64"  },
         "m1.large"    : { "Arch" : "HVM64"  },
         "m1.xlarge"   : { "Arch" : "HVM64"  },
         "m2.xlarge"   : { "Arch" : "HVM64"  },
         "m2.2xlarge"  : { "Arch" : "HVM64"  },
         "m2.4xlarge"  : { "Arch" : "HVM64"  },
         "m3.medium"   : { "Arch" : "HVM64"  },
         "m3.large"    : { "Arch" : "HVM64"  },
         "m3.xlarge"   : { "Arch" : "HVM64"  },
         "m3.2xlarge"  : { "Arch" : "HVM64"  },
         "m4.large"    : { "Arch" : "HVM64"  },
         "m4.xlarge"   : { "Arch" : "HVM64"  },
         "m4.2xlarge"  : { "Arch" : "HVM64"  },
         "m4.4xlarge"  : { "Arch" : "HVM64"  },
         "m4.10xlarge" : { "Arch" : "HVM64"  },
         "c1.medium"   : { "Arch" : "HVM64"  },
         "c1.xlarge"   : { "Arch" : "HVM64"  },
         "c3.large"    : { "Arch" : "HVM64"  },
         "c3.xlarge"   : { "Arch" : "HVM64"  },
         "c3.2xlarge"  : { "Arch" : "HVM64"  },
         "c3.4xlarge"  : { "Arch" : "HVM64"  },
         "c3.8xlarge"  : { "Arch" : "HVM64"  },
         "c4.large"    : { "Arch" : "HVM64"  },
         "c4.xlarge"   : { "Arch" : "HVM64"  },
         "c4.2xlarge"  : { "Arch" : "HVM64"  },
         "c4.4xlarge"  : { "Arch" : "HVM64"  },
         "c4.8xlarge"  : { "Arch" : "HVM64"  },
         "g2.2xlarge"  : { "Arch" : "HVMG2"  },
         "g2.8xlarge"  : { "Arch" : "HVMG2"  },
         "r3.large"    : { "Arch" : "HVM64"  },
         "r3.xlarge"   : { "Arch" : "HVM64"  },
         "r3.2xlarge"  : { "Arch" : "HVM64"  },
         "r3.4xlarge"  : { "Arch" : "HVM64"  },
         "r3.8xlarge"  : { "Arch" : "HVM64"  },
         "i2.xlarge"   : { "Arch" : "HVM64"  },
         "i2.2xlarge"  : { "Arch" : "HVM64"  },
         "i2.4xlarge"  : { "Arch" : "HVM64"  },
         "i2.8xlarge"  : { "Arch" : "HVM64"  },
         "d2.xlarge"   : { "Arch" : "HVM64"  },
         "d2.2xlarge"  : { "Arch" : "HVM64"  },
         "d2.4xlarge"  : { "Arch" : "HVM64"  },
         "d2.8xlarge"  : { "Arch" : "HVM64"  },
         "hi1.4xlarge" : { "Arch" : "HVM64"  },
         "hs1.8xlarge" : { "Arch" : "HVM64"  },
         "cr1.8xlarge" : { "Arch" : "HVM64"  },
         "cc2.8xlarge" : { "Arch" : "HVM64"  }
       },
       "AWSRegionArch2AMI" : {
         "us-east-1"        : {"HVM64" : "ami-0ff8a91507f77f867", "HVMG2" : "ami-0a584ac55a7631c0c"},
         "us-west-2"        : {"HVM64" : "ami-a0cfeed8", "HVMG2" : "ami-0e09505bc235aa82d"},
         "us-west-1"        : {"HVM64" : "ami-0bdb828fd58c52235", "HVMG2" : "ami-066ee5fd4a9ef77f1"},
         "eu-west-1"        : {"HVM64" : "ami-047bb4163c506cd98", "HVMG2" : "ami-0a7c483d527806435"},
         "eu-west-2"        : {"HVM64" : "ami-f976839e", "HVMG2" : "NOT_SUPPORTED"},
         "eu-west-3"        : {"HVM64" : "ami-0ebc281c20e89ba4b", "HVMG2" : "NOT_SUPPORTED"},
         "eu-central-1"     : {"HVM64" : "ami-0233214e13e500f77", "HVMG2" : "ami-06223d46a6d0661c7"},
         "ap-northeast-1"   : {"HVM64" : "ami-06cd52961ce9f0d85", "HVMG2" : "ami-053cdd503598e4a9d"},
         "ap-northeast-2"   : {"HVM64" : "ami-0a10b2721688ce9d2", "HVMG2" : "NOT_SUPPORTED"},
         "ap-northeast-3"   : {"HVM64" : "ami-0d98120a9fb693f07", "HVMG2" : "NOT_SUPPORTED"},
         "ap-southeast-1"   : {"HVM64" : "ami-08569b978cc4dfa10", "HVMG2" : "ami-0be9df32ae9f92309"},
         "ap-southeast-2"   : {"HVM64" : "ami-09b42976632b27e9b", "HVMG2" : "ami-0a9ce9fecc3d1daf8"},
         "ap-south-1"       : {"HVM64" : "ami-0912f71e06545ad88", "HVMG2" : "ami-097b15e89dbdcfcf4"},
         "us-east-2"        : {"HVM64" : "ami-0b59bfac6be064b78", "HVMG2" : "NOT_SUPPORTED"},
         "ca-central-1"     : {"HVM64" : "ami-0b18956f", "HVMG2" : "NOT_SUPPORTED"},
         "sa-east-1"        : {"HVM64" : "ami-07b14488da8ea02a0", "HVMG2" : "NOT_SUPPORTED"},
         "cn-north-1"       : {"HVM64" : "ami-0a4eaf6c4454eda75", "HVMG2" : "NOT_SUPPORTED"},
         "cn-northwest-1"   : {"HVM64" : "ami-6b6a7d09", "HVMG2" : "NOT_SUPPORTED"}
       }
     }
   }
   ```

   Here are the same mappings in YAML\.

   ```
   Mappings:
     AWSInstanceType2Arch:
       t1.micro:
         Arch: HVM64
       t2.nano:
         Arch: HVM64
       t2.micro:
         Arch: HVM64
       t2.small:
         Arch: HVM64
       t2.medium:
         Arch: HVM64
       t2.large:
         Arch: HVM64
       m1.small:
         Arch: HVM64
       m1.medium:
         Arch: HVM64
       m1.large:
         Arch: HVM64
       m1.xlarge:
         Arch: HVM64
       m2.xlarge:
         Arch: HVM64
       m2.2xlarge:
         Arch: HVM64
       m2.4xlarge:
         Arch: HVM64
       m3.medium:
         Arch: HVM64
       m3.large:
         Arch: HVM64
       m3.xlarge:
         Arch: HVM64
       m3.2xlarge:
         Arch: HVM64
       m4.large:
         Arch: HVM64
       m4.xlarge:
         Arch: HVM64
       m4.2xlarge:
         Arch: HVM64
       m4.4xlarge:
         Arch: HVM64
       m4.10xlarge:
         Arch: HVM64
       c1.medium:
         Arch: HVM64
       c1.xlarge:
         Arch: HVM64
       c3.large:
         Arch: HVM64
       c3.xlarge:
         Arch: HVM64
       c3.2xlarge:
         Arch: HVM64
       c3.4xlarge:
         Arch: HVM64
       c3.8xlarge:
         Arch: HVM64
       c4.large:
         Arch: HVM64
       c4.xlarge:
         Arch: HVM64
       c4.2xlarge:
         Arch: HVM64
       c4.4xlarge:
         Arch: HVM64
       c4.8xlarge:
         Arch: HVM64
       g2.2xlarge:
         Arch: HVMG2
       g2.8xlarge:
         Arch: HVMG2
       r3.large:
         Arch: HVM64
       r3.xlarge:
         Arch: HVM64
       r3.2xlarge:
         Arch: HVM64
       r3.4xlarge:
         Arch: HVM64
       r3.8xlarge:
         Arch: HVM64
       i2.xlarge:
         Arch: HVM64
       i2.2xlarge:
         Arch: HVM64
       i2.4xlarge:
         Arch: HVM64
       i2.8xlarge:
         Arch: HVM64
       d2.xlarge:
         Arch: HVM64
       d2.2xlarge:
         Arch: HVM64
       d2.4xlarge:
         Arch: HVM64
       d2.8xlarge:
         Arch: HVM64
       hi1.4xlarge:
         Arch: HVM64
       hs1.8xlarge:
         Arch: HVM64
       cr1.8xlarge:
         Arch: HVM64
       cc2.8xlarge:
         Arch: HVM64
     AWSRegionArch2AMI:
       us-east-1:
         HVM64: ami-0ff8a91507f77f867
         HVMG2: ami-0a584ac55a7631c0c
       us-west-2:
         HVM64: ami-a0cfeed8
         HVMG2: ami-0e09505bc235aa82d
       us-west-1:
         HVM64: ami-0bdb828fd58c52235
         HVMG2: ami-066ee5fd4a9ef77f1
       eu-west-1:
         HVM64: ami-047bb4163c506cd98
         HVMG2: ami-0a7c483d527806435
       eu-west-2:
         HVM64: ami-f976839e
         HVMG2: NOT_SUPPORTED
       eu-west-3:
         HVM64: ami-0ebc281c20e89ba4b
         HVMG2: NOT_SUPPORTED
       eu-central-1:
         HVM64: ami-0233214e13e500f77
         HVMG2: ami-06223d46a6d0661c7
       ap-northeast-1:
         HVM64: ami-06cd52961ce9f0d85
         HVMG2: ami-053cdd503598e4a9d
       ap-northeast-2:
         HVM64: ami-0a10b2721688ce9d2
         HVMG2: NOT_SUPPORTED
       ap-northeast-3:
         HVM64: ami-0d98120a9fb693f07
         HVMG2: NOT_SUPPORTED
       ap-southeast-1:
         HVM64: ami-08569b978cc4dfa10
         HVMG2: ami-0be9df32ae9f92309
       ap-southeast-2:
         HVM64: ami-09b42976632b27e9b
         HVMG2: ami-0a9ce9fecc3d1daf8
       ap-south-1:
         HVM64: ami-0912f71e06545ad88
         HVMG2: ami-097b15e89dbdcfcf4
       us-east-2:
         HVM64: ami-0b59bfac6be064b78
         HVMG2: NOT_SUPPORTED
       ca-central-1:
         HVM64: ami-0b18956f
         HVMG2: NOT_SUPPORTED
       sa-east-1:
         HVM64: ami-07b14488da8ea02a0
         HVMG2: NOT_SUPPORTED
       cn-north-1:
         HVM64: ami-0a4eaf6c4454eda75
         HVMG2: NOT_SUPPORTED
       cn-northwest-1:
         HVM64: ami-6b6a7d09
         HVMG2: NOT_SUPPORTED
   ```

**To add outputs**

Outputs declare values that you want available to a `describe stacks` API call or through the AWS CloudFormation console stack **Outputs** tab\. For this walkthrough, we'll output the website URL so that you can easily view the website after we create it\. For more information, see [Outputs](outputs-section-structure.md)\.

1. In the integrated editor pane, select the **Outputs** tab\.

1. Copy the following JSON output and paste it into the integrated editor\.

   The output uses an `Fn::GetAtt` intrinsic function to get the public IP of the web server instance\.

   ```
   {
     "Outputs": {
       "URL": {
         "Value": {
           "Fn::Join": [
             "",
             [
               "http://",
               {
                 "Fn::GetAtt": [
                   "WebServerInstance",
                   "PublicIp"
                 ]
               }
             ]
           ]
         },
         "Description": "Newly created application URL"
       }
     }
   }
   ```

   Here is the same output in YAML\.

   ```
   Outputs:
     URL:
       Value: !Join 
         - ''
         - - 'http://'
           - !GetAtt 
             - WebServerInstance
             - PublicIp
       Description: Newly created application URL
   ```

1. Save your template again so that you don't lose your changes\. You can safely save your changes to the same file that you created in the previous section\.

Now that the template parameters, mappings, and outputs are in place, we can specify resource properties\.

## Step 3: Specify resource properties<a name="working-with-templates-cfn-designer-walkthrough-createbasicwebserver-resourceproperties"></a>

Many resources have required properties that define their configurations or settings, such as which instance type to use for the web server\. Similar to what we did in the previous step, we'll use the AWS CloudFormation Designer integrated editor to specify resource properties\. We provide sample JSON and YAML that you can copy and paste into the integrated editor\.

**To specify resource properties**

1. On the AWS CloudFormation Designer canvas, choose the `VPC` resource\.

   The integrated editor shows the resource\-level components that you can edit, such as the resource properties and attributes\.

1. In the integrated editor pane, choose the **Properties** tab\.

1. Copy the following JSON snippet and paste it into the integrated editor between the **Properties** braces \(`{}`\)\.

   This snippet specifies DNS settings and the CIDR block of the VPC\.

   ```
           "EnableDnsSupport": "true",
           "EnableDnsHostnames": "true",
           "CidrBlock": "10.0.0.0/16"
   ```

   For YAML, type a new line after `Properties:` and paste the following snippet\.

   ```
         EnableDnsSupport: 'true'
         EnableDnsHostnames: 'true'
         CidrBlock: 10.0.0.0/16
   ```
**Note**  
For efficiency, we provide JSON and YAML snippets that you can copy and paste\. Note, however, that the editor has an auto\-complete feature that you can use to manually specify each property\. For more information, see [Integrated JSON and YAML editor](working-with-templates-cfn-designer-json-editor.md)\.

1. Repeat this process for the following resources:  
`PublicSubnet`  
Add the following CIDR block property after the VPC ID property\. AWS CloudFormation Designer automatically added the VPC ID property when you dragged the subnet inside the VPC\.  
You'll see a few other associations that AWS CloudFormation Designer automatically created for you\. Add just the new properties, which are in bold\.
JSON  

   ```
           "VpcId": {
             "Ref": "VPC"
           },
           "CidrBlock": "10.0.0.0/24"
   ```
YAML  

   ```
         VpcId: !Ref VPC
         CidrBlock: 10.0.0.0/24
   ```  
`PublicRoute`  
Add the following destination CIDR block property, which directs all traffic to the Internet gateway:  
JSON  

   ```
           "DestinationCidrBlock": "0.0.0.0/0",
           "RouteTableId": {
             "Ref": "PublicRouteTable"
           },        
           "GatewayId": {
             "Ref": "InternetGateway"
           }
   ```
YAML  

   ```
         DestinationCidrBlock: 0.0.0.0/0
         RouteTableId: !Ref PublicRouteTable
         GatewayId: !Ref InternetGateway
   ```  
`WebServerSecurityGroup`  
Add the following inbound rules that determine what traffic can reach the web server instance\. The rules allow all HTTP and certain SSH traffic, which you specify as a parameter value when you create a stack\.  
JSON  

   ```
           "VpcId": {
             "Ref": "VPC"
           },
           "GroupDescription" : "Allow access from HTTP and SSH traffic",
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
   ```
YAML  

   ```
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
`WebServerInstance`  
You need to specify a number of properties for the web server instance, so we'll highlight just a few for demonstration purposes\. The `InstanceType` and `ImageId` properties use the parameter and mapping values that we specified in the previous section\. When you create a stack, you specify the instance type as a parameter value\. The `ImageId` value is a mapping that is based on your stack's region and the instance type that you specified\.  
The `NetworkInterfaces` property specifies network settings for the web server instance\. This property allows us to associate the security group and subnet with the instance\. Although AWS CloudFormation Designer used the `SubnetId` property to associate the instance with the subnet, we need to use the `NetworkInterfaces` property because that's the only way to give the web server a public IP\. And when you specify the `NetworkInterfaces` property, you are required to specify the subnet and security group within that property\.  
In the `UserData` property, we specify configuration scripts that run after the instance is up and running\. All of the configuration information is defined in the instance's metadata, which we'll add in the next step\.  
Replace all properties with the following snippet:  
Do not append this snippet to existing properties\.
JSON  

   ```
          "InstanceType": {
             "Ref": "InstanceType"
           },
           "ImageId": {
             "Fn::FindInMap": [
               "AWSRegionArch2AMI",
               {
                 "Ref": "AWS::Region"
               },
               {
                 "Fn::FindInMap": [
                   "AWSInstanceType2Arch",
                   {
                     "Ref": "InstanceType"
                   },
                   "Arch"
                 ]
               }
             ]
           },
           "KeyName": {
             "Ref": "KeyName"
           },
           "NetworkInterfaces": [
             {
               "GroupSet": [
                 {
                   "Ref": "WebServerSecurityGroup"
                 }
               ],
               "AssociatePublicIpAddress": "true",
               "DeviceIndex": "0",
               "DeleteOnTermination": "true",
               "SubnetId": {
                 "Ref": "PublicSubnet"
               }
             }
           ],
           "UserData": {
             "Fn::Base64": {
               "Fn::Join": [
                 "",
                 [
                   "#!/bin/bash -xe\n",
                   "yum install -y aws-cfn-bootstrap\n",
                   "# Install the files and packages from the metadata\n",
                   "/opt/aws/bin/cfn-init -v ",
                   "         --stack ",
                   {
                     "Ref": "AWS::StackName"
                   },
                   "         --resource WebServerInstance ",
                   "         --configsets All ",
                   "         --region ",
                   {
                     "Ref": "AWS::Region"
                   },
                   "\n",
                   "# Signal the status from cfn-init\n",
                   "/opt/aws/bin/cfn-signal -e $? ",
                   "         --stack ",
                   {
                     "Ref": "AWS::StackName"
                   },
                   "         --resource WebServerInstance ",
                   "         --region ",
                   {
                     "Ref": "AWS::Region"
                   },
                   "\n"
                 ]
               ]
             }
           }
   ```
YAML  

   ```
         InstanceType: !Ref InstanceType
         ImageId: !FindInMap 
           - AWSRegionArch2AMI
           - !Ref 'AWS::Region'
           - !FindInMap 
             - AWSInstanceType2Arch
             - !Ref InstanceType
             - Arch
         KeyName: !Ref KeyName
         NetworkInterfaces:
           - GroupSet:
               - !Ref WebServerSecurityGroup
             AssociatePublicIpAddress: 'true'
             DeviceIndex: '0'
             DeleteOnTermination: 'true'
             SubnetId: !Ref PublicSubnet
         UserData: !Base64 
           'Fn::Join':
             - ''
             - - |
                 #!/bin/bash -xe
               - |
                 yum install -y aws-cfn-bootstrap
               - |
                 # Install the files and packages from the metadata
               - '/opt/aws/bin/cfn-init -v '
               - '         --stack '
               - !Ref 'AWS::StackName'
               - '         --resource WebServerInstance '
               - '         --configsets All '
               - '         --region '
               - !Ref 'AWS::Region'
               - |+
   
               - |
                 # Signal the status from cfn-init
               - '/opt/aws/bin/cfn-signal -e $? '
               - '         --stack '
               - !Ref 'AWS::StackName'
               - '         --resource WebServerInstance '
               - '         --region '
               - !Ref 'AWS::Region'
               - |+
   ```

1. Add the web server configuration metadata to the `WebServerInstance` resource\.

   1. Choose the `WebServerInstance` resource, and then choose the **Metadata** tab in the integrated editor pane\.

   1. *If you are authoring your template in JSON*: Within the `Metadata` braces \(`{}`\) and after the `AWS::CloudFormation::Designer` closing brace, add a comma \(`,`\)\.

   1. After the `AWS::CloudFormation::Designer` property, add the following snippet, which instructs the cfn\-init helper script to start the web server and create a basic web page\.

      JSON

      ```
              "AWS::CloudFormation::Init" : {
                "configSets" : {
                  "All" : [ "ConfigureSampleApp" ]
                },
                "ConfigureSampleApp" : {
                  "packages" : {
                    "yum" : {
                      "httpd" : []
                    }
                  },
                  "files" : {
                    "/var/www/html/index.html" : {
                      "content" : { "Fn::Join" : ["\n", [
                        "<h1>Congratulations, you have successfully launched the AWS CloudFormation sample.</h1>"
                      ]]},
                      "mode"    : "000644",
                      "owner"   : "root",
                      "group"   : "root"
                    }
                  },
                  "services" : {
                    "sysvinit" : {
                      "httpd"    : { "enabled" : "true", "ensureRunning" : "true" }
                    }
                  }
                }
              }
      ```

      YAML

      ```
            'AWS::CloudFormation::Init':
              configSets:
                All:
                  - ConfigureSampleApp
              ConfigureSampleApp:
                packages:
                  yum:
                    httpd: []
                files:
                  /var/www/html/index.html:
                    content: !Join 
                      - |+
      
                      - - >-
                          <h1>Congratulations, you have successfully launched the AWS
                          CloudFormation sample.</h1>
                    mode: '000644'
                    owner: root
                    group: root
                services:
                  sysvinit:
                    httpd:
                      enabled: 'true'
                      ensureRunning: 'true'
      ```

1. On the AWS CloudFormation Designer toolbar, choose **Validate template** \(![\[Image NOT FOUND\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/images/designer-validate-icon.png)\) to check for syntax errors in your template\.

   View and fix errors in the **Messages** pane, and then validate the template again\. If you don't see errors, your template is syntactically valid\.

1. Save your completed template to keep all the changes you made\.

You now have a complete AWS CloudFormation template that you can use to create a basic web server in a VPC\. To create the template, we first added and connected template resources by using the AWS CloudFormation Designer canvas pane\. Then, we used the integrated editor to add other template components and to specify resource properties\. In the next step, we'll use this template to create a stack\.

## Step 4: Provision resources<a name="working-with-templates-cfn-designer-walkthrough-createbasicwebserver-provision"></a>

To create a stack, you can launch the AWS CloudFormation Create Stack Wizard from AWS CloudFormation Designer\. We'll use the template that we created in the previous steps to create an AWS CloudFormation stack\. After AWS CloudFormation provisions all of your resources, you'll have a basic website up and running\.

**To create the stack**

1. On the AWS CloudFormation Designer toolbar, choose **Create Stack** \(the cloud icon\)\.

   AWS CloudFormation Designer saves the open template in an S3 bucket, and then launches the AWS CloudFormation Create Stack Wizard\. AWS CloudFormation uses the same S3 bucket that it creates whenever you upload templates\.

1. AWS CloudFormation automatically populates the template URL; choose **Next**\.

1. In the **Specify Details** section, enter a stack name in the **Stack name**  field\. For this example, use **BasicWebServerStack**\.

1. In the **Parameters** section, for the **KeyName** field, enter the name of a valid Amazon EC2 key pair in the same region you are creating the stack\.

1. Keep the other default parameter values and choose **Next**\.

1. For this walkthrough, you don't need to add tags or specify advanced settings, so choose **Next**\.

1. Ensure that the stack name and Amazon EC2 key\-pair name are correct, and then choose **Create**\.

It can take several minutes for AWS CloudFormation to create your stack\. To monitor progress, view the stack events\. For more information about viewing stack events, see [Viewing AWS CloudFormation stack data and resources on the AWS Management Console](cfn-console-view-stack-data-resources.md)\. After the stack is created, view the stack outputs and go to the sample website URL to verify that the website is running\. For more information, see [Viewing AWS CloudFormation stack data and resources on the AWS Management Console](cfn-console-view-stack-data-resources.md)\. 

Now that you've successfully created a template and launched a stack using AWS CloudFormation Designer, you can use the stack in the following walkthrough: [Walkthrough: Use AWS CloudFormation Designer to modify a stack's template](working-with-templates-cfn-designer-walkthrough-updatebasicwebserver.md), which modifies the template to create a scalable web server\.