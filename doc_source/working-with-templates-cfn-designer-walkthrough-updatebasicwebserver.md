# Walkthrough: Use AWS CloudFormation Designer to modify a stack's template<a name="working-with-templates-cfn-designer-walkthrough-updatebasicwebserver"></a>

You can use AWS CloudFormation Designer to easily modify a stack's template, and then submit it to AWS CloudFormation to update the stack\. Typically, when you modify a stack, you need to get a copy of its template, modify the template in a text editor, and then use AWS CloudFormation to update the stack\. With AWS CloudFormation Designer, you can quickly get a copy of any running stack's template, modify it, and then update the stack without ever leaving the console\. 

In this walkthrough, we'll start with a [basic web server](working-with-templates-cfn-designer-walkthrough-createbasicwebserver.md) stack, and then modify it so that the web server is scalable and durable\. 

By the end of the walkthrough, you'll have a template similar to the following sample: [https://console\.aws\.amazon\.com/cloudformation/designer/home?templateUrl=https://s3\.amazonaws\.com/cloudformation\-examples/sample\-as\-vpc\.template&region=us\-east\-1](https://console.aws.amazon.com/cloudformation/designer/home?templateUrl=https://s3.amazonaws.com/cloudformation-examples/sample-as-vpc.template&region=us-east-1)\.

In this walkthrough, we will complete the following steps:

1. [Get a stack's template\.](#working-with-templates-cfn-designer-walkthrough-updatebasicwebserver-get-template)

   We'll get a copy of a running stack's template; the same basic web server stack in the following walkthrough: [Walkthrough: Use AWS CloudFormation Designer to create a basic web server](working-with-templates-cfn-designer-walkthrough-createbasicwebserver.md)\.

1. [Modify the template\.](#working-with-templates-cfn-designer-walkthrough-updatebasicwebserver-modify-template)

   We'll use AWS CloudFormation Designer to modify the stack's template so that your website is scalable and durable by replacing the EC2 instance with an Auto Scaling group and an Elastic Load Balancing load balancer\. 

1. [Update the stack\.](#working-with-templates-cfn-designer-walkthrough-updatebasicwebserver-update-stack)

   After saving the modifications, we'll update the basic web server stack with the modified template\.
**Note**  
AWS CloudFormation is a free service; however, you are charged for the AWS resources you include in your stacks at the current rate for each\. For more information about AWS pricing, see the detail page for each product on [http://aws\.amazon\.com](http://aws.amazon.com)\.

1. [Delete the stack\.](#working-with-templates-cfn-designer-walkthrough-updatebasicwebserver-delete-stack)

   We'll delete the stack to clean up all of the resources\.

Prerequisites

This walkthrough assumes that you have a working knowledge of Amazon Virtual Private Cloud \(Amazon VPC\), Auto Scaling, Elastic Load Balancing, and AWS CloudFormation\. For context, each procedure provides some basic information about each resource\.

Additionally, the walkthrough assumes that you completed the following walkthrough: [Walkthrough: Use AWS CloudFormation Designer to create a basic web server](working-with-templates-cfn-designer-walkthrough-createbasicwebserver.md)\. From that walkthrough, you should have a running stack named `BasicWebServerStack`\.

## Step 1: Get a stack template<a name="working-with-templates-cfn-designer-walkthrough-updatebasicwebserver-get-template"></a>

In this step, we'll use AWS CloudFormation Designer to get and open a copy of a running stack's template\.

**To get a copy of a running stack's template**

1. Open the AWS CloudFormation console at [https://console\.aws\.amazon\.com/cloudformation/](https://console.aws.amazon.com/cloudformation/)\.

1. From the list of stacks, select the `BasicWebServerStack`\.

1. Choose **Actions**, and then **View/Edit template in Designer**\.

AWS CloudFormation gets a copy of the `BasicWebServerStack` stack's template and displays it in AWS CloudFormation Designer, where you can view the template resources and their relationships\. In the following step, we'll use AWS CloudFormation Designer to modify the template\.

## Step 2: Modify a template<a name="working-with-templates-cfn-designer-walkthrough-updatebasicwebserver-modify-template"></a>

We'll modify the basic web server template by using AWS CloudFormation Designer's drag\-and\-drop interface and integrated JSON and YAML editor to replace the single Amazon EC2 instance with an Auto Scaling group and load balancer to make the web site scalable\. If traffic to the web site suddenly increases, use Auto Scaling to quickly increase the number of web servers\. The load balancer will equally distributes the traffic among the instances\.

**To modify a stack template**

1. Remove the `WebServerInstance` resource\.

   1. Right\-click the `WebServerInstance` resource\.

   1. From the resource menu, choose **Delete** \(![\[Image NOT FOUND\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/images/designer-resourcemenu-delete.png)\)\.

   1. Choose **OK** to confirm\.

1. From the **Resource types** pane, add the following resources into the `PublicSubnet` resource: **AutoScalingGroup**, **LaunchConfiguration**, and **LoadBalancer**\. Before adding resources, you might need to expand the subnet to include all the resources\.

   The resources are organized by resource categories\. The Auto Scaling group and launch configuration are in the **AutoScaling** category, and the load balancer is in the **ElasticLoadBalancing** category\.
**Note**  
These resources do not follow the container model, so AWS CloudFormation Designer doesn't automatically associate them with the subnet\. We'll create connections later on in this step\.

1. From the **Resource types** pane in the **EC2** category, add the **SecurityGroup** resource anywhere in the VPC except in the subnet\.

   This security group will control the inbound and outbound traffic of the load balancer\.

1. Rename the resources to make them easier to identify:
   + Rename **AutoScalingGroup** to `WebServerFleet`
   + Rename **LaunchConfiguration** to `WebServerLaunchConfig`
   + Rename **LoadBalancer** to `PublicElasticLoadBalancer`
   + Rename **SecurityGroup** to `PublicLoadBalancerSecurityGroup`

1. Create associations for the resources that you added\.

   1. Associate the load balancer and Auto Scaling group resources with the public subnet:
      + From the `PublicElasticLoadBalancer` resource, drag the `AWS::EC2::Subnet (Property: Subnets)` connection to the `PublicSubnet` resource\.
      + From the `WebServerFleet` resource, drag the `AWS::EC2::Subnet (Property: VPCZoneIdentifier)` connection to the `PublicSubnet` resource\.

   1. Associate the load balancer with its security group:
      + From the `PublicElasticLoadBalancer` resource, drag the `AWS::EC2::SecurityGroup (Property: SecurityGroups)` connection to the `PublicLoadBalancerSecurityGroup` resource\.

   1. Associate the Auto Scaling group with the load balancer and launch configuration:
      + From the `WebServerFleet` resource, drag the `AWS::ElasticLoadBalancing::LoadBalancer (Property: LoadBalancerNames)` connection to the `PublicElasticLoadBalancer` resource\.
      + From the `WebServerFleet` resource, drag the `AWS::ElasticLoadBalancing::LaunchConfiguration (Property: LaunchConfigurationName)` connection to the `WebServerLaunchConfig` resource\.

   1. Associate the launch configuration with the security group:
      + From the `WebServerLaunchConfig` resource, drag the `AWS::EC2::SecurityGroup (Property: SecurityGroups)` connection to the `WebServerSecurityGroup` resource\.

   1. Define a dependency for the Auto Scaling group to the public route:
      + From the `WebServerFleet` resource, drag the `DependsOn` connection to the `PublicRoute` resource\.

      This dependency means that AWS CloudFormation won't create the `WebServerFleet` resource until the public route is complete\. Otherwise, if the public route isn't available when the web server instances are starting up, they won't be able to send signals \(using the cfn\-signal helper script\) to notify AWS CloudFormation when their configurations and application deployments are complete\.

1. Specify the properties for the resources that you added\.

   1. On the AWS CloudFormation Designer canvas, choose the `PublicElasticLoadBalancer` resource\.

   1. In the integrated editor pane, choose the **Properties** tab, and then copy the following snippet and paste it between the **Properties** braces \(`{}`\)\.

      AWS CloudFormation Designer automatically added the security group and subnet association, so you need to add only the `Listeners` and `HealthCheck` properties\. The `Listeners` property specifies where and what type of traffic to listen for, and the `HealthCheck` property describes the settings for determining the health status of the load balancer\.

      JSON

      ```
                "Listeners": [
                {
                  "LoadBalancerPort": "80",
                  "InstancePort": "80",
                  "Protocol": "HTTP"
                }
              ],
              "HealthCheck": {
                "Target": "HTTP:80/",
                "HealthyThreshold": "3",
                "UnhealthyThreshold": "5",
                "Interval": "90",
                "Timeout": "60"
              },
              "SecurityGroups": [
                {
                  "Ref": "PublicLoadBalancerSecurityGroup"
                }
              ],
              "Subnets": [
                {
                  "Ref": "PublicSubnet"
                }
              ]
      ```

      YAML

      ```
            Listeners:
              - LoadBalancerPort: '80'
                InstancePort: '80'
                Protocol: HTTP
            HealthCheck:
              Target: 'HTTP:80/'
              HealthyThreshold: '3'
              UnhealthyThreshold: '5'
              Interval: '90'
              Timeout: '60'
            SecurityGroups:
              - !Ref PublicLoadBalancerSecurityGroup
            Subnets:
              - !Ref PublicSubnet
      ```

   1. Repeat this process for the following resources:  
`WebServerFleet`  
Add the `MaxSize`, `MinSize`, and `DesiredCapacity` properties\. These properties specify the maximum and minimum number of instances that you can launch in the Auto Scaling group and the initial number of instances to start with\. The desired capacity value refers to a new parameter, which we'll add later in this procedure\.  
JSON  

      ```
              "MinSize": "1",
              "MaxSize": "10",
              "DesiredCapacity": {
                "Ref": "WebServerCount"
              },
              "VPCZoneIdentifier": [
                {
                  "Ref": "PublicSubnet"
                }
              ],
              "LaunchConfigurationName": {
                "Ref": "WebServerLaunchConfig"
              },
              "LoadBalancerNames": [
                {
                  "Ref": "PublicElasticLoadBalancer"
                }
              ]
      ```
YAML  

      ```
            MinSize: '1'
            MaxSize: '10'
            DesiredCapacity: !Ref WebServerCount
            VPCZoneIdentifier:
              - !Ref PublicSubnet
            LaunchConfigurationName: !Ref WebServerLaunchConfig
            LoadBalancerNames:
              - !Ref PublicElasticLoadBalancer
      ```  
`PublicLoadBalancerSecurityGroup`  
Add the following inbound and outbound rules that determine the traffic that can reach and leave the load balancer\. The rules allows all HTTP traffic to reach and leave the load balancer\.  
JSON  

      ```
              "GroupDescription": "Public Elastic Load Balancing security group with HTTP access on port 80 from the Internet",
              "SecurityGroupIngress": [
                {
                  "IpProtocol": "tcp",
                  "FromPort": "80",
                  "ToPort": "80",
                  "CidrIp": "0.0.0.0/0"
                }
              ],
              "SecurityGroupEgress": [
                {
                  "IpProtocol": "tcp",
                  "FromPort": "80",
                  "ToPort": "80",
                  "CidrIp": "0.0.0.0/0"
                }
              ],
              "VpcId": {
                "Ref": "VPC"
              }
      ```
YAML  

      ```
            GroupDescription: >-
              Public Elastic Load Balancing security group with HTTP access on port 80
              from the Internet
            SecurityGroupIngress:
              - IpProtocol: tcp
                FromPort: '80'
                ToPort: '80'
                CidrIp: 0.0.0.0/0
            SecurityGroupEgress:
              - IpProtocol: tcp
                FromPort: '80'
                ToPort: '80'
                CidrIp: 0.0.0.0/0
            VpcId: !Ref VPC
      ```  
`WebServerSecurityGroup`  
Modify the HTTP inbound rule to allow only traffic from the load balancer\.  
JSON  

      ```
              "GroupDescription": "Allow access from load balancer and SSH traffic",
              "SecurityGroupIngress": [
                {
                  "IpProtocol": "tcp",
                  "FromPort": "80",
                  "ToPort": "80",
                  "SourceSecurityGroupId": {
                    "Ref": "PublicLoadBalancerSecurityGroup"
                  }
                },
                {
                  "IpProtocol": "tcp",
                  "FromPort": "22",
                  "ToPort": "22",
                  "CidrIp": {
                    "Ref": "SSHLocation"
                  }
                }
              ],
              "VpcId": {
                "Ref": "VPC"
              }
      ```
YAML  

      ```
            VpcId: !Ref VPC
            GroupDescription: Allow access from load balancer and SSH traffic
            SecurityGroupIngress:
              - IpProtocol: tcp
                FromPort: '80'
                ToPort: '80'
                SourceSecurityGroupId: !Ref PublicLoadBalancerSecurityGroup
              - IpProtocol: tcp
                FromPort: '22'
                ToPort: '22'
                CidrIp: !Ref SSHLocation
      ```  
`WebServerLaunchConfig`  
The launch configuration has a number of different properties that you need to specify, so we'll highlight just a few of them\. The `InstanceType` and `ImageId` properties use the parameter and mapping values that were already specified in the template\. You specify the instance type as a parameter value when you create a stack\. The `ImageId` value is a mapping that is based on your stack's region and the instance type that you specified\.  
In the `UserData` property, we specify configurations scripts that run after the instance is up and running\. All of the configuration information is defined in the instance's metadata, which we'll add in the next step\.  
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
              "AssociatePublicIpAddress": "true",
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
                      "         --resource WebServerLaunchConfig ",
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
                      "         --resource WebServerFleet ",
                      "         --region ",
                      {
                        "Ref": "AWS::Region"
                      },
                      "\n"
                    ]
                  ]
                }
              },
              "SecurityGroups": [
                {
                  "Ref": "WebServerSecurityGroup"
                }
              ]
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
            AssociatePublicIpAddress: 'true'
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
                  - '         --resource WebServerLaunchConfig '
                  - '         --configsets All '
                  - '         --region '
                  - !Ref 'AWS::Region'
                  - |+
      
                  - |
                    # Signal the status from cfn-init
                  - '/opt/aws/bin/cfn-signal -e $? '
                  - '         --stack '
                  - !Ref 'AWS::StackName'
                  - '         --resource WebServerFleet '
                  - '         --region '
                  - !Ref 'AWS::Region'
                  - |+
      
            SecurityGroups:
              - !Ref WebServerSecurityGroup
      ```

1. Add the launch configuration metadata to the `WebServerLaunchConfig` resource, which instructs the cfn\-init helper script to start the web server and create a basic web page\.

   1. Choose the `WebServerLaunchConfig` resource, and then choose the **Metadata** tab in the integrated editor\.

   1. *If you are authoring your template in JSON*: Within the `Metadata` braces \(`{}`\), after the `AWS::CloudFormation::Designer` closing brace, add a comma \(`,`\)\.

   1. Add the following snippet, which instructs the cfn\-init helper script to start the web server and create a basic web page, after the `AWS::CloudFormation::Designer` property\.

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

1. Add the `WebServerCount` parameter\. This parameter specifies how many instances to create when AWS CloudFormation creates the Auto Scaling group\.

   1. Click on an open area on the AWS CloudFormation Designer canvas\.

   1. In the integrated editor pane, choose the **Parameters** tab\.

   1. Add the following parameter in the integrated editor\. If you're authoring the template in JSON, add a comma as needed\.

      JSON

      ```
          "WebServerCount": {
            "Description": "Number of Amazon EC2 instances to launch for the WebServer server",
            "Type": "Number",
            "Default": "1"
          }
      ```

      YAML

      ```
        WebServerCount:
          Description: Number of Amazon EC2 instances to launch for the WebServer server
          Type: Number
          Default: '1'
      ```

1. Modify the template output to show the DNS name of the load balancer\.

   1. In the integrated editor pane, choose the **Outputs** tab\.

   1. Modify the JSON to use the load balancer DNS name, as shown in the following snippet\.

      JSON

      ```
      {
        "Outputs": {
          "URL": {
            "Value": {
              "Fn::GetAtt": [
                "PublicElasticLoadBalancer",
                "DNSName"
              ]
            },
            "Description": "Newly created application URL"
          }
        }
      }
      ```

      If you're authoring your template in YAML, use the following snippet\.

      ```
      Outputs:
        URL:
          Value: !GetAtt 
            - PublicElasticLoadBalancer
            - DNSName
          Description: Newly created application URL
      ```

1. On the AWS CloudFormation Designer toolbar, choose **Validate template** \(![\[Image NOT FOUND\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/images/designer-validate-icon.png)\) to check for syntax errors in your template\.

   View and fix errors in the **Messages** pane, and then validate the template again\. If you don't see errors, your template is syntactically valid\.

1. From the AWS CloudFormation Designer toolbar, save the template locally by choosing **File** \(![\[Image NOT FOUND\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/images/designer-file-menu.png)\) and then **Save**\.

You now have a modified AWS CloudFormation template that you can use to update the basic web server stack\. In the next step, we'll use this template to update the basic web server stack\.

## Step 3: Update the stack<a name="working-with-templates-cfn-designer-walkthrough-updatebasicwebserver-update-stack"></a>

To implement your template changes, we need to update the basic web server stack\. You can launch the AWS CloudFormation Update Stack Wizard directly from AWS CloudFormation Designer\.

**To update the stack**

1. On the AWS CloudFormation Designer toolbar, choose **Create Stack** \(![\[Image NOT FOUND\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/images/designer-create-stack-icon.png)\)\.

   AWS CloudFormation Designer saves the opened template in an S3 bucket and then launches the AWS CloudFormation Update Stack Wizard\. Because we modified the `BasicWebServerStack` stack's template, AWS CloudFormation launches the Update Stack Wizard for that stack\.

1. AWS CloudFormation automatically populates the template URL; choose **Next**\.

1. In the **Stack** section, in the **Name** field, verify that the stack name is `BasicWebServerStack`\.

1. In the **Parameters** section, use the existing values; choose **Next**\.

1. For this walkthrough, you don't need to add tags or specify advanced settings, so choose **Next**\.

1. Ensure that the stack name is correct, and then choose **Update**\.

It can take several minutes for AWS CloudFormation to update your stack\. To monitor progress, view the stack events\. For more information, see [Viewing AWS CloudFormation stack data and resources on the AWS Management Console](cfn-console-view-stack-data-resources.md)\. After the stack is updated, view the stack outputs and go to the website URL to verify that the website is running\. For more information, see [Viewing AWS CloudFormation stack data and resources on the AWS Management Console](cfn-console-view-stack-data-resources.md)\. You successfully updated a template and a stack using AWS CloudFormation Designer\.

To ensure that you are not charged for unwanted services, you can delete this stack\.

## Step 4: Clean up resources<a name="working-with-templates-cfn-designer-walkthrough-updatebasicwebserver-delete-stack"></a>

To make sure you are not charged for unwanted services, delete your stack and it's resources\.

**To delete the stack**

1. From the AWS CloudFormation console, choose the **BasicWebServerStack** stack\.

1. Choose **Delete Stack**\.

1. In the confirmation message, choose **Yes, Delete**\.

It can take several minutes for AWS CloudFormation to delete your stack\. To monitor progress, view the stack events\. After the stack is deleted, all the resources that you created are deleted\. Now that you understand how to use AWS CloudFormation Designer, you can use it to build and modify your own templates\. 