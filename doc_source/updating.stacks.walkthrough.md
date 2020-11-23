# Walkthrough: Updating a stack<a name="updating.stacks.walkthrough"></a>

With AWS CloudFormation, you can update the properties for resources in your existing stacks\. These changes can range from simple configuration changes, such as updating the alarm threshold on a CloudWatch alarm, to more complex changes, such as updating the Amazon Machine Image \(AMI\) running on an Amazon EC2 instance\. Many of the AWS resources in a template can be updated, and we continue to add support for more\.

This section walks through a simple progression of updates of a running stack\. It shows how the use of templates makes it possible to use a version control system for the configuration of your AWS infrastructure, just as you use version control for the software you are running\. We will walk through the following steps:

1. [Create the initial stack](#updating.create.initial.stack)—create a stack using a base Amazon Linux AMI, installing the Apache Web Server and a simple PHP application using the AWS CloudFormation helper scripts\.

1. [Update the application](#update.application)—update one of the files in the application and deploy the software using AWS CloudFormation\.

1.  [Update the instance type](#update.walkthrough.instance.type)—change the instance type of the underlying Amazon EC2 instance\.

1.  [Update the AMI on an Amazon EC2 instance](#update.walkthrough.ami)—change the Amazon Machine Image \(AMI\) for the Amazon EC2 instance in your stack\.

1. [Add a key pair to an instance](#update.walkthrough.security.group)—add an Amazon EC2 key pair to the instance, and then update the security group to allow SSH access to the instance\.

1. [Change the stack's resources](#update.walkthrough.change.resources)—add and remove resources from the stack, converting it to an auto\-scaled, load\-balanced application by updating the template\.

## A simple application<a name="updating.simple.application"></a>

We'll begin by creating a stack that we can use throughout the rest of this section\. We have provided a simple template that launches a single instance PHP web application hosted on the Apache Web Server and running on an Amazon Linux AMI\.

The Apache Web Server, PHP, and the simple PHP application are all installed by the AWS CloudFormation helper scripts that are installed by default on the Amazon Linux AMI\. The following template snippet shows the metadata that describes the packages and files to install, in this case the Apache Web Server and the PHP infrastructure from the Yum repository for the Amazon Linux AMI\. The snippet also shows the Services section, which ensures that the Apache Web Server is running\. In the Properties section of the Amazon EC2 instance definition, the UserData property contains the CloudInit script that calls cfn\-init to install the packages and files\.

```
  "WebServerInstance": {
    "Type" : "AWS::EC2::Instance",
    "Metadata" : {
      "AWS::CloudFormation::Init" : {
        "config" : {
          "packages" : {
            "yum" : {
              "httpd"             : [],
              "php"               : []
            }
          },

          "files" : {

            "/var/www/html/index.php" : {
              "content" : { "Fn::Join" : ["", [
                "<?php\n",
                "echo '<h1>AWS CloudFormation sample PHP application</h1>';\n",
                "echo '<p>", { "Ref" : "WelcomeMessage" }, "</p>';\n",
                "?>\n"
              ]]},
              "mode"    : "000644",
              "owner"   : "apache",
              "group"   : "apache"
            },
          },

          :

          "services" : {
            "sysvinit" : {
              "httpd"    : { "enabled" : "true", "ensureRunning" : "true" }
            }
          }
        }
      }
    },

    "Properties": {
      :
      "UserData"       : { "Fn::Base64" : { "Fn::Join" : ["", [
        "#!/bin/bash\n",
        "yum install -y aws-cfn-bootstrap\n",

        :

        "# Install the files and packages from the metadata\n",
        "/opt/aws/bin/cfn-init -v ",
        "         --stack ", { "Ref" : "AWS::StackName" },
        "         --resource WebServerInstance ",
        "         --region ", { "Ref" : "AWS::Region" }, "\n", 
        :
      ]]}}
    }
  },
```

The application itself is a very simple two\-line "Hello, World" example that is entirely defined within the template\. For a real\-world application, the files may be stored on Amazon S3, GitHub, or another repository and referenced from the template\. AWS CloudFormation can download packages \(such as RPMs or RubyGems\), as well as reference individual files and expand `.zip` and `.tar` files to create the application artifacts on the Amazon EC2 instance\.

The template enables and configures the cfn\-hup daemon to listen for changes to the configuration defined in the metadata for the Amazon EC2 instance\. By using the cfn\-hup daemon, you can update application software, such as the version of Apache or PHP, or you can update the PHP application file itself from AWS CloudFormation\. The following snippet from the same Amazon EC2 resource in the template shows the pieces necessary to configure cfn\-hup to call cfn\-init to update the software if any changes to the metadata are detected:

```
  "WebServerInstance": {
    "Type" : "AWS::EC2::Instance",
    "Metadata" : {
      "AWS::CloudFormation::Init" : {
        "config" : {

            :

          "files" : {

            :

            "/etc/cfn/cfn-hup.conf" : {
              "content" : { "Fn::Join" : ["", [
                "[main]\n",
                "stack=", { "Ref" : "AWS::StackName" }, "\n",
                "region=", { "Ref" : "AWS::Region" }, "\n"
              ]]},
              "mode"    : "000400",
              "owner"   : "root",
              "group"   : "root"
            },

            "/etc/cfn/hooks.d/cfn-auto-reloader.conf" : {
              "content": { "Fn::Join" : ["", [
                "[cfn-auto-reloader-hook]\n",
                "triggers=post.update\n",
                "path=Resources.WebServerInstance.Metadata.AWS::CloudFormation::Init\n",
                "action=/opt/aws/bin/cfn-init -s ", { "Ref" : "AWS::StackId" }, " -r WebServerInstance ",
                " --region     ", { "Ref" : "AWS::Region" }, "\n",  
                "runas=root\n"
              ]]}
            }
          },
          :
    },

    "Properties": {

         :

      "UserData"       : { "Fn::Base64" : { "Fn::Join" : ["", [

        :

        "# Start up the cfn-hup daemon to listen for changes to the Web Server metadata\n",
        "/opt/aws/bin/cfn-hup || error_exit 'Failed to start cfn-hup'\n",  

        :
      ]]}}
    }
  },
```

To complete the stack, the template creates an Amazon EC2 security group\.

```
{
  "AWSTemplateFormatVersion" : "2010-09-09",

  "Description" : "AWS CloudFormation Sample Template: Sample template that can be used to test EC2 updates. **WARNING** This template creates an Amazon Ec2 Instance. You will be billed for the AWS resources used if you create a stack from this template.",
  
  "Parameters" : {
          
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
    }
  },
    
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
  },
    
  "Resources" : {   

    "WebServerInstance": {  
      "Type" : "AWS::EC2::Instance",
      "Metadata" : {
        "Comment" : "Install a simple PHP application",
        "AWS::CloudFormation::Init" : {
          "config" : {
            "packages" : {
              "yum" : {
                "httpd"             : [],
                "php"               : []
              }
            },

            "files" : {

              "/var/www/html/index.php" : {
                "content" : { "Fn::Join" : ["", [
                  "<?php\n",
                  "echo '<h1>AWS CloudFormation sample PHP application</h1>';\n",
                  "?>\n"
                ]]},
                "mode"    : "000644",
                "owner"   : "apache",
                "group"   : "apache"
              },


              "/etc/cfn/cfn-hup.conf" : {
                "content" : { "Fn::Join" : ["", [
                  "[main]\n",
                  "stack=", { "Ref" : "AWS::StackId" }, "\n",
                  "region=", { "Ref" : "AWS::Region" }, "\n"
                ]]},
                "mode"    : "000400",
                "owner"   : "root",
                "group"   : "root"
              },

              "/etc/cfn/hooks.d/cfn-auto-reloader.conf" : {
                "content": { "Fn::Join" : ["", [
                  "[cfn-auto-reloader-hook]\n",
                  "triggers=post.update\n",
                  "path=Resources.WebServerInstance.Metadata.AWS::CloudFormation::Init\n",
                  "action=/opt/aws/bin/cfn-init -s ", { "Ref" : "AWS::StackId" }, " -r WebServerInstance ",
                                                   " --region     ", { "Ref" : "AWS::Region" }, "\n",
                  "runas=root\n"
                ]]}
              }
            },

            "services" : {
              "sysvinit" : {
                "httpd"    : { "enabled" : "true", "ensureRunning" : "true" },
                "cfn-hup" : { "enabled" : "true", "ensureRunning" : "true",
                    "files" : ["/etc/cfn/cfn-hup.conf", "/etc/cfn/hooks.d/cfn-auto-reloader.conf"]}
              }
            }
          }
        }
      },

      "Properties": {
        "ImageId" : { "Fn::FindInMap" : [ "AWSRegionArch2AMI", { "Ref" : "AWS::Region" },
                          { "Fn::FindInMap" : [ "AWSInstanceType2Arch", { "Ref" : "InstanceType" }, "Arch" ] } ] },
        "InstanceType"   : { "Ref" : "InstanceType" },
        "SecurityGroups" : [ {"Ref" : "WebServerSecurityGroup"} ],
        "UserData"       : { "Fn::Base64" : { "Fn::Join" : ["", [
             "#!/bin/bash -xe\n",
             "yum install -y aws-cfn-bootstrap\n",

             "# Install the files and packages from the metadata\n",
             "/opt/aws/bin/cfn-init -v ",
             "         --stack ", { "Ref" : "AWS::StackName" },
             "         --resource WebServerInstance ",
             "         --region ", { "Ref" : "AWS::Region" }, "\n",

             "# Start up the cfn-hup daemon to listen for changes to the Web Server metadata\n",
             "/opt/aws/bin/cfn-hup || error_exit 'Failed to start cfn-hup'\n",  

             "# Signal the status from cfn-init\n",
             "/opt/aws/bin/cfn-signal -e $? ",
             "         --stack ", { "Ref" : "AWS::StackName" },
             "         --resource WebServerInstance ",
             "         --region ", { "Ref" : "AWS::Region" }, "\n"
        ]]}}        
      },
      "CreationPolicy" : {
        "ResourceSignal" : {
          "Timeout" : "PT5M"
        }
      }
    },

    "WebServerSecurityGroup" : {
      "Type" : "AWS::EC2::SecurityGroup",
      "Properties" : {
        "GroupDescription" : "Enable HTTP access via port 80",
        "SecurityGroupIngress" : [
          {"IpProtocol" : "tcp", "FromPort" : "80", "ToPort" : "80", "CidrIp" : "0.0.0.0/0"}
        ]
      }      
    }          
  },
  
  "Outputs" : {
    "WebsiteURL" : {
      "Description" : "Application URL",
      "Value" : { "Fn::Join" : ["", ["http://", { "Fn::GetAtt" : [ "WebServerInstance", "PublicDnsName" ]}]] }
    }
  }
}
```

This example uses a single Amazon EC2 instance, but you can use the same mechanisms on more complex solutions that make use of Elastic Load Balancers and Auto Scaling groups to manage a collection of application servers\. There are, however, some special considerations for Auto Scaling groups\. For more information, see [Updating Auto Scaling groups](#updating.autoscaling)\.

## Create the initial stack<a name="updating.create.initial.stack"></a>

For the purposes of this example, we’ll use the AWS Management Console to create an initial stack from the sample template\.

**Warning**  
Completing this procedure will deploy live AWS services\. You will be charged the standard usage rates as long as these services are running\.

**To create the stack from the AWS Management Console**

1. Copy the previous template and save it locally on your system as a text file\. Note the location because you'll need to use the file in a subsequent step\.

1. Log in to the AWS CloudFormation console at [ https://console\.aws\.amazon\.com/cloudformation ](https://console.aws.amazon.com/cloudformation)\.

1. Click **Create New Stack**\.

1. In the **Create New Stack** wizard, on the **Select Template** screen, type **UpdateTutorial** in the **Name** field\. On the same page, select **Upload a template to Amazon S3** and browse to the file that you downloaded in the first step, and then click **Next**\.

1. On the **Specify Parameters** screen, in the **Instance Type** box, type **t1\.micro**\. Then click **Next**\.

1. On the **Options** screen, click **Next**\.

1. On the **Review** screen, verify that all the settings are as you want them, and then click **Create**\.

After the status of your stack is CREATE\_COMPLETE, the output tab will display the URL of your website\. If you click the value of the WebsiteURL output, you will see your new PHP application working\.

## Update the application<a name="update.application"></a>

Now that we have deployed the stack, let's update the application\. We'll make a simple change to the text that is printed out by the application\. To do so, we’ll add an echo command to the index\.php file as shown in this template snippet:

```
"WebServerInstance": {
      "Type" : "AWS::EC2::Instance",
      "Metadata" : {
        "AWS::CloudFormation::Init" : {
          "config" : {
              :

            "files" : {

              "/var/www/html/index.php" : {
                "content" : { "Fn::Join" : ["", [
                  "<?php\n",
                  "echo '<h1>AWS CloudFormation sample PHP application</h1>';\n",
                  "echo 'Updated version via UpdateStack';\n ",
                  "?>\n"
                ]]},
                "mode"    : "000644",
                "owner"   : "apache",
                "group"   : "apache"
              },

              :

      }
    },
```

Use a text editor to manually edit the template file that you saved locally\.

Now, we'll update the stack\.

**To update the stack from the AWS Management Console**

1. Log in to the AWS CloudFormation console, at: [ https://console\.aws\.amazon\.com/cloudformation](https://console.aws.amazon.com/cloudformation)\.

1. On the AWS CloudFormation dashboard, click the stack you created previously, and then click **Update Stack**\.

1. In the **Update Stack** wizard, on the **Select Template** screen, select **Upload a template to Amazon S3**, select the modified template, and then click **Next**\. 

1. On the **Options** screen, click **Next**\.

1. Click **Next** because the stack doesn't have a stack policy\. All resources can be updated without an overriding policy\.

1. On the **Review** screen, verify that all the settings are as you want them, and then click **Update**\.

If you update the stack from the AWS Management Console, you will notice that the parameters that were used to create the initial stack are prepopulated on the **Parameters** page of the **Update Stack** wizard\. If you use the `aws cloudformation update-stack` command, be sure to type in the same values for the parameters that you used originally to create the stack\.

When your stack is in the UPDATE\_COMPLETE state, you can click the WebsiteURL output value again to verify that the changes to your application have taken effect\. By default, the cfn\-hup daemon runs every 15 minutes, so it may take up to 15 minutes for the application to change once the stack has been updated\.

To see the set of resources that were updated, go to the AWS CloudFormation console\. On the **Events** tab, look at the stack events\. In this particular case, the metadata for the Amazon EC2 instance WebServerInstance was updated, which caused AWS CloudFormation to also reevaluate the other resources \(`WebServerSecurityGroup`\) to ensure that there were no other changes\. None of the other stack resources were modified\. AWS CloudFormation will update only those resources in the stack that are affected by any changes to the stack\. Such changes can be direct, such as property or metadata changes, or they can be due to dependencies or data flows through Ref, GetAtt, or other intrinsic template functions\.

This simple update illustrates the process; however, you can make much more complex changes to the files and packages that are deployed to your Amazon EC2 instances\. For example, you might decide that you need to add MySQL to the instance, along with PHP support for MySQL\. To do so, simply add the additional packages and files along with any additional services to the configuration and then update the stack to deploy the changes\. In the following template snippet, the changes are highlighted in red:

```
    "WebServerInstance": {
      "Type" : "AWS::EC2::Instance",
      "Metadata" : {
        "Comment" : "Install a simple PHP application",
        "AWS::CloudFormation::Init" : {
          "config" : {
            "packages" : {
              "yum" : {
                "httpd"             : [],
                "php"               : [],
                "php-mysql"         : [],
                "mysql-server"      : [],
                "mysql-libs"        : [],
                "mysql"             : []
              }
            },

            :

            "services" : {
              "sysvinit" : {
                "httpd"    : { "enabled" : "true", "ensureRunning" : "true" },
                "cfn-hup" : { "enabled" : "true", "ensureRunning" : "true",
                    "files" : ["/etc/cfn/cfn-hup.conf", "/etc/cfn/hooks.d/cfn-auto-reloader.conf"]},
                "mysqld"   : { "enabled" : "true", "ensureRunning" : "true" }
              }
            }
          }
        }
      },

      "Properties": {
           :
      }
    }
```

You can update the CloudFormation metadata to update to new versions of the packages used by the application\. In the previous examples, the version property for each package is empty, indicating that cfn\-init should install the latest version of the package\.

```
     "packages" : {
       "yum" : {
         "httpd"             : [],
         "php"               : []
      }
```

You can optionally specify a version string for a package\. If you change the version string in subsequent update stack calls, the new version of the package will be deployed\. Here's an example of using version numbers for RubyGems packages\. Any package that supports versioning can have specific versions\.

```
  "packages" : {
    "rubygems" : {
      "mysql"           : [],
      "rubygems-update" : ["1.6.2"],
      "rake"            : ["0.8.7"],
      "rails"           : ["2.3.11"]
    }
    }
```

### Updating Auto Scaling groups<a name="updating.autoscaling"></a>

If you are using Auto Scaling groups in your template, as opposed to Amazon EC2 instance resources, updating the application will work in exactly the same way; however, AWS CloudFormation does not provide any synchronization or serialization across the Amazon EC2 instances in an Auto Scaling group\. The cfn\-hup daemon on each host will run independently and update the application on its own schedule\. When you use cfn\-hup to update the on\-instance configuration, each instance will run the cfn\-hup hooks on its own schedule; there is no coordination between the instances in the stack\. You should consider the following:
+ If the cfn\-hup changes run on all Amazon EC2 instances in the Auto Scaling group at the same time, your service might be unavailable during the update\.
+ If the cfn\-hup changes run at different times, old and new versions of the software may be running at the same\.

To avoid these issues, consider forcing a rolling update on your instances in the Auto Scaling group\. For more information, see [UpdatePolicy attribute](aws-attribute-updatepolicy.md)\.

## Changing resource properties<a name="update.walkthrough.changing.resource.properties"></a>

With AWS CloudFormation, you can change the properties of an existing resource in the stack\. The following sections describe various updates that solve specific problems; however, any property of any resource that supports updating in the stack can be modified as necessary\.

### Update the instance type<a name="update.walkthrough.instance.type"></a>

The stack we have built so far uses a t1\.micro Amazon EC2 instance\. Let's suppose that your newly created website is getting more traffic than a t1\.micro instance can handle, and now you want to move to an m1\.small Amazon EC2 instance type\. If the architecture of the instance type changes, the instance will be created with a different AMI\. If you check out the mappings in the template, you will see that both the t1\.micro and m1\.small are the same architectures and use the same Amazon Linux AMIs\.

```
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
```

Let's use the template that we modified in the previous section to change the instance type\. Because InstanceType was an input parameter to the template, we don't need to modify the template; we can simply change the value of the parameter in the Stack Update wizard, on the Specify Parameters page\.

**To update the stack from the AWS Management Console**

1. Log in to the AWS CloudFormation console at [https://console\.aws\.amazon\.com/cloudformation](https://console.aws.amazon.com/cloudformation)\.

1. On the AWS CloudFormation dashboard, click the stack you created previously, and then click **Update Stack**\.

1. In the **Update Stack** wizard, on the **Select Template** screen, select **Use current template**, and then click **Next**\. 

   The Specify Details page appears with the parameters that were used to create the initial stack are pre\-populated in the **Specify Parameters** section\.

1. Change the value of the **InstanceType** text box from `t1.micro` to `m1.small`\. Then, click **Next**\.

1. On the **Options** screen, click **Next**\.

1. Click **Next** because the stack doesn't have a stack policy\. All resources can be updated without an overriding policy\.

1. On the **Review** screen, verify that all the settings are as you want them, and then click **Update**\.

You can dynamically change the instance type of an EBS\-backed Amazon EC2 instance by starting and stopping the instance\. AWS CloudFormation tries to optimize the change by updating the instance type and restarting the instance, so the instance ID does not change\. When the instance is restarted, however, the public IP address of the instance does change\. To ensure that the Elastic IP address is bound correctly after the change, AWS CloudFormation will also update the Elastic IP address\. You can see the changes in the AWS CloudFormation console on the Events tab\.

To check the instance type from the AWS Management Console, open the Amazon EC2 console, and locate your instance there\.

### Update the AMI on an Amazon EC2 instance<a name="update.walkthrough.ami"></a>

Now let's look at how we might change the Amazon Machine Image \(AMI\) running on the instance\. We will trigger the AMI change by updating the stack to use a new Amazon EC2 instance type, such as t2\.medium, which is an HVM64 instance type\. 

As in the previous section, we’ll use our existing template to change the instance type used by our example stack\. In the Stack Update wizard, on the Specify Parameters page, change the value of the Instance Type\.

In this case, we cannot simply start and stop the instance to modify the AMI; AWS CloudFormation considers this a change to an immutable property of the resource\. In order to make a change to an immutable property, AWS CloudFormation must launch a replacement resource, in this case a new Amazon EC2 instance running the new AMI\.

After the new instance is running, AWS CloudFormation updates the other resources in the stack to point to the new resource\. When all new resources are created, the old resource is deleted, a process known as UPDATE\_CLEANUP\. This time, you will notice that the instance ID and application URL of the instance in the stack has changed as a result of the update\. The events in the Event table contain a description "Requested update has a change to an immutable property and hence creating a new physical resource" to indicate that a resource was replaced\.

If you have application code written into the AMI that you want to update, you can use the same stack update mechanism to update the AMI to load your new application\.

**To update the AMI for an instance on your stack**

1. Create your new AMIs containing your application or operating system changes\. For more information, go to [Creating your own AMIs](http://docs.aws.amazon.com/AWSEC2/latest/UserGuide/creating-an-ami.html) in the *Amazon EC2 User Guide for Linux Instances*\.

1. Update your template to incorporate the new AMI IDs\.

1. Update the stack, either from the AWS Management Console as explained in [Update the application](#update.application) or by using the AWS command [https://docs.aws.amazon.com/cli/latest/reference/cloudformation/update-stack.html](https://docs.aws.amazon.com/cli/latest/reference/cloudformation/update-stack.html)\.

When you update the stack, AWS CloudFormation detects that the AMI ID has changed, and then it triggers a stack update in the same way as we triggered the one above\.

### Update the Amazon EC2 launch configuration for an Auto Scaling group<a name="update.walkthrough.launch.config"></a>

If you are using Auto Scaling groups rather than Amazon EC2 instances, the process of updating the running instances is a little different\. With Auto Scaling resources, the configuration of the Amazon EC2 instances, such as the instance type or the AMI ID is encapsulated in the Auto Scaling launch configuration\. You can make changes to the launch configuration in the same way as we made changes to the Amazon EC2 instance resources in the previous sections\. However, changing the launch configuration does not impact any of the running Amazon EC2 instances in the Auto Scaling group\. An updated launch configuration applies only to new instances that are created after the update\.

If you want to propagate the change to your launch configuration across all the instances in your Auto Scaling group, you can use an update attribute\. For more information, see [UpdatePolicy attribute](aws-attribute-updatepolicy.md)\.

## Adding resource properties<a name="update.walkthrough.adding.properties"></a>

So far, we've looked at changing existing properties of a resource in a template\. You can also add properties that were not originally specified in the template\. To illustrate that, we’ll add an Amazon EC2 key pair to an existing EC2 instance and then open up port 22 in the Amazon EC2 Security Group so that you can use Secure Shell \(SSH\) to access the instance\.

### Add a key pair to an instance<a name="update.walkthrough.security.group"></a>

**To add SSH access to an existing Amazon EC2 instance**

1. Add two additional parameters to the template to pass in the name of an existing Amazon EC2 key pair and SSH location\.

   ```
     "Parameters" : {
   
       "KeyName" : {
         "Description" : "Name of an existing Amazon EC2 key pair for SSH access",
         "Type": "AWS::EC2::KeyPair::KeyName"
       },
       "SSHLocation" : {
         "Description" : " The IP address range that can be used to SSH to the EC2 instances",
         "Type": "String",
         "MinLength": "9",
         "MaxLength": "18",
         "Default": "0.0.0.0/0",
         "AllowedPattern": "(\\d{1,3})\\.(\\d{1,3})\\.(\\d{1,3})\\.(\\d{1,3})/(\\d{1,2})",
         "ConstraintDescription": "must be a valid IP CIDR range of the form x.x.x.x/x."
       }  
       :
     },
   ```

1. Add the KeyName property to the Amazon EC2 instance\.

   ```
             "WebServerInstance": {
             "Type" : "AWS::EC2::Instance",
             :
             "Properties": {
             :
             "KeyName" : { "Ref" : "KeyName" },
             :
             }
             },
   ```

1. Add port 22 and the SSH location to the ingress rules for the Amazon EC2 security group\.

   ```
       "WebServerSecurityGroup" : {
         "Type" : "AWS::EC2::SecurityGroup",
         "Properties" : {
           "GroupDescription" : "Enable HTTP and SSH",
           "SecurityGroupIngress" : [
             {"IpProtocol" : "tcp", "FromPort" : "22", "ToPort" : "22", "CidrIp" : { "Ref" : "SSHLocation"}},
             {"IpProtocol" : "tcp", "FromPort" : "80", "ToPort" : "80", "CidrIp" :  "0.0.0.0/0"}
           ]
         }
       },
   ```

1. Update the stack, either from the AWS Management Console as explained in [Update the application](#update.application) or by using the AWS command [https://docs.aws.amazon.com/cli/latest/reference/cloudformation/update-stack.html](https://docs.aws.amazon.com/cli/latest/reference/cloudformation/update-stack.html)\.

## Change the stack's resources<a name="update.walkthrough.change.resources"></a>

Since application needs can change over time, AWS CloudFormation allows you to change the set of resources that make up the stack\. To demonstrate, we’ll take the single instance application from [Adding resource properties](#update.walkthrough.adding.properties) and convert it to an auto\-scaled, load\-balanced application by updating the stack\.

This will create a simple, single instance PHP application using an Elastic IP address\. We'll now turn the application into a highly available, auto\-scaled, load balanced application by changing its resources during an update\.

1. Add an Elastic Load Balancer resource\.

   ```
       "ElasticLoadBalancer" : {
         "Type" : "AWS::ElasticLoadBalancing::LoadBalancer",
         "Properties" : {
           "CrossZone" : "true",
           "AvailabilityZones" : { "Fn::GetAZs" : "" },
           "LBCookieStickinessPolicy" : [ {
             "PolicyName" : "CookieBasedPolicy",
             "CookieExpirationPeriod" : "30"
           } ],
           "Listeners" : [ {
             "LoadBalancerPort" : "80",
             "InstancePort" : "80",
             "Protocol" : "HTTP",
             "PolicyNames" : [ "CookieBasedPolicy" ]
           } ],
           "HealthCheck" : {
             "Target" : "HTTP:80/",
             "HealthyThreshold" : "2",
             "UnhealthyThreshold" : "5",
             "Interval" : "10",
             "Timeout" : "5"
           }
         }
       }
   ```

1. Convert the EC2 instance in the template into an Auto Scaling Launch Configuration\. The properties are identical, so we only need to change the type name from:

   ```
   "WebServerInstance": {
     "Type" : "AWS::EC2::Instance",
   ```

   to:

   ```
   "LaunchConfig": {
     "Type" : "AWS::AutoScaling::LaunchConfiguration",
   ```

   For clarity in the template, we changed the name of the resource from *WebServerInstance* to *LaunchConfig*, so you’ll need to update the resource name referenced by cfn\-init and cfn\-hup \(just search for WebServerInstance and replace it with LaunchConfig, except for cfn\-signal\)\. For cfn\-signal, you'll need to signal the Auto Scaling group \(WebServerGroup\) not the instance, as shown in the following snippet:

   ```
                "# Signal the status from cfn-init\n",
                "/opt/aws/bin/cfn-signal -e $? ",
                "         --stack ", { "Ref" : "AWS::StackName" },
                "         --resource WebServerGroup ",
                "         --region ", { "Ref" : "AWS::Region" }, "\n"
   ```

1. Add an Auto Scaling Group resource\.

   ```
       "WebServerGroup" : {
         "Type" : "AWS::AutoScaling::AutoScalingGroup",
         "Properties" : {
           "AvailabilityZones" : { "Fn::GetAZs" : "" },
           "LaunchConfigurationName" : { "Ref" : "LaunchConfig" },
           "MinSize" : "1",
           "DesiredCapacity" : "1",
           "MaxSize" : "5",
           "LoadBalancerNames" : [ { "Ref" : "ElasticLoadBalancer" } ]
         },
         "CreationPolicy" : {
           "ResourceSignal" : {
             "Timeout" : "PT15M"
           }
         },
         "UpdatePolicy": {
           "AutoScalingRollingUpdate": {
             "MinInstancesInService": "1",
             "MaxBatchSize": "1",
             "PauseTime" : "PT15M",
             "WaitOnResourceSignals": "true"
           }
         }
       }
   ```

1. Update the Security Group definition to lock down the traffic to the instances from the load balancer\.

   ```
       "WebServerSecurityGroup" : {
         "Type" : "AWS::EC2::SecurityGroup",
         "Properties" : {
           "GroupDescription" : "Enable HTTP access via port 80 locked down to the ELB and SSH access",
           "SecurityGroupIngress" : [
             {"IpProtocol" : "tcp", "FromPort" : "80", "ToPort" : "80", "SourceSecurityGroupOwnerId" : {"Fn::GetAtt" : ["ElasticLoadBalancer", "SourceSecurityGroup.OwnerAlias"]},
   "SourceSecurityGroupName" : {"Fn::GetAtt" : ["ElasticLoadBalancer", "SourceSecurityGroup.GroupName"]}},
             {"IpProtocol" : "tcp", "FromPort" : "22", "ToPort" : "22", "CidrIp" : { "Ref" : "SSHLocation"}}
           ]
         }
       }
   ```

1. Update the Outputs to return the DNS Name of the Elastic Load Balancer as the location of the application from:

   ```
   "WebsiteURL" : {
     "Value" : { "Fn::Join" : ["", ["http://", 
         { "Fn::GetAtt" : [ "WebServerInstance", "PublicDnsName" ]}]]},
     "Description" : "Application URL"
   }
   ```

   to:

   ```
   "WebsiteURL" : {
     "Value" : { "Fn::Join" : ["", ["http://", 
         { "Fn::GetAtt" : [ "ElasticLoadBalancer", "DNSName" ]}]]},
     "Description" : "Application URL"
   }
   ```

For reference, the following sample shows the complete template\. If you use this template to update the stack, you will convert your simple, single instance application into a highly available, multi\-AZ, auto\-scaled and load balanced application\. Only the resources that need to be updated will be altered, so had there been any data stores for this application, the data would have remained intact\. Now, you can use AWS CloudFormation to grow or enhance your stacks as your requirements change\.

```
{
  "AWSTemplateFormatVersion" : "2010-09-09",

  "Description" : "AWS CloudFormation Sample Template: Sample template that can be used to test EC2 updates. **WARNING** This template creates an Amazon Ec2 Instance. You will be billed for the AWS resources used if you create a stack from this template.",
  
  "Parameters" : {
  
    "KeyName": {
      "Description" : "Name of an existing EC2 KeyPair to enable SSH access to the instance",
      "Type": "AWS::EC2::KeyPair::KeyName",
      "ConstraintDescription" : "must be the name of an existing EC2 KeyPair."
    },

    "SSHLocation" : {
      "Description" : " The IP address range that can be used to SSH to the EC2 instances",
      "Type": "String",
      "MinLength": "9",
      "MaxLength": "18",
      "Default": "0.0.0.0/0",
      "AllowedPattern": "(\\d{1,3})\\.(\\d{1,3})\\.(\\d{1,3})\\.(\\d{1,3})/(\\d{1,2})",
      "ConstraintDescription": "must be a valid IP CIDR range of the form x.x.x.x/x."
    },
    
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
    }
  },
  
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
  },
    
  "Resources" : {   
  
    "ElasticLoadBalancer" : {
      "Type" : "AWS::ElasticLoadBalancing::LoadBalancer",
      "Properties" : {
        "CrossZone" : "true",
        "AvailabilityZones" : { "Fn::GetAZs" : "" },
        "LBCookieStickinessPolicy" : [ {
          "PolicyName" : "CookieBasedPolicy",
          "CookieExpirationPeriod" : "30"
        } ],
        "Listeners" : [ {
          "LoadBalancerPort" : "80",
          "InstancePort" : "80",
          "Protocol" : "HTTP",
          "PolicyNames" : [ "CookieBasedPolicy" ]
        } ],
        "HealthCheck" : {
          "Target" : "HTTP:80/",
          "HealthyThreshold" : "2",
          "UnhealthyThreshold" : "5",
          "Interval" : "10",
          "Timeout" : "5"
        }
      }
    },
    
    "WebServerGroup" : {
      "Type" : "AWS::AutoScaling::AutoScalingGroup",
      "Properties" : {
        "AvailabilityZones" : { "Fn::GetAZs" : "" },
        "LaunchConfigurationName" : { "Ref" : "LaunchConfig" },
        "MinSize" : "1",
        "DesiredCapacity" : "1",
        "MaxSize" : "5",
        "LoadBalancerNames" : [ { "Ref" : "ElasticLoadBalancer" } ]
      },
      "CreationPolicy" : {
        "ResourceSignal" : {
          "Timeout" : "PT15M"
        }
      },
      "UpdatePolicy": {
        "AutoScalingRollingUpdate": {
          "MinInstancesInService": "1",
          "MaxBatchSize": "1",
          "PauseTime" : "PT15M",
          "WaitOnResourceSignals": "true"
        }
      }
    },
    
    "LaunchConfig": {  
      "Type" : "AWS::AutoScaling::LaunchConfiguration",
      "Metadata" : {
        "Comment" : "Install a simple PHP application",
        "AWS::CloudFormation::Init" : {
          "config" : {
            "packages" : {
              "yum" : {
                "httpd"             : [],
                "php"               : []
              }
            },

            "files" : {

              "/var/www/html/index.php" : {
                "content" : { "Fn::Join" : ["", [
                  "<?php\n",
                  "echo '<h1>AWS CloudFormation sample PHP application</h1>';\n",
                  "echo 'Updated version via UpdateStack';\n ",
                  "?>\n"
                ]]},
                "mode"    : "000644",
                "owner"   : "apache",
                "group"   : "apache"
              },


              "/etc/cfn/cfn-hup.conf" : {
                "content" : { "Fn::Join" : ["", [
                  "[main]\n",
                  "stack=", { "Ref" : "AWS::StackId" }, "\n",
                  "region=", { "Ref" : "AWS::Region" }, "\n"
                ]]},
                "mode"    : "000400",
                "owner"   : "root",
                "group"   : "root"
              },

              "/etc/cfn/hooks.d/cfn-auto-reloader.conf" : {
                "content": { "Fn::Join" : ["", [
                  "[cfn-auto-reloader-hook]\n",
                  "triggers=post.update\n",
                  "path=Resources.LaunchConfig.Metadata.AWS::CloudFormation::Init\n",
                  "action=/opt/aws/bin/cfn-init -s ", { "Ref" : "AWS::StackId" }, " -r LaunchConfig ",
                                                   " --region     ", { "Ref" : "AWS::Region" }, "\n",
                  "runas=root\n"
                ]]}
              }
            },

            "services" : {
              "sysvinit" : {
                "httpd"    : { "enabled" : "true", "ensureRunning" : "true" },
                "cfn-hup" : { "enabled" : "true", "ensureRunning" : "true",
                    "files" : ["/etc/cfn/cfn-hup.conf", "/etc/cfn/hooks.d/cfn-auto-reloader.conf"]}
              }
            }
          }
        }
      },

      "Properties": {
        "ImageId" : { "Fn::FindInMap" : [ "AWSRegionArch2AMI", { "Ref" : "AWS::Region" },
                          { "Fn::FindInMap" : [ "AWSInstanceType2Arch", { "Ref" : "InstanceType" }, "Arch" ] } ] },
        "InstanceType"   : { "Ref" : "InstanceType" },
        "KeyName"        : { "Ref" : "KeyName" },
        "SecurityGroups" : [ {"Ref" : "WebServerSecurityGroup"} ],
        "UserData"       : { "Fn::Base64" : { "Fn::Join" : ["", [
             "#!/bin/bash -xe\n",
             "yum install -y aws-cfn-bootstrap\n",

             "# Install the files and packages from the metadata\n",
             "/opt/aws/bin/cfn-init -v ",
             "         --stack ", { "Ref" : "AWS::StackName" },
             "         --resource LaunchConfig ",
             "         --region ", { "Ref" : "AWS::Region" }, "\n",
             
             "# Start up the cfn-hup daemon to listen for changes to the Web Server metadata\n",
             "/opt/aws/bin/cfn-hup || error_exit 'Failed to start cfn-hup'\n",  

             "# Signal the status from cfn-init\n",
             "/opt/aws/bin/cfn-signal -e $? ",
             "         --stack ", { "Ref" : "AWS::StackName" },
             "         --resource WebServerGroup ",
             "         --region ", { "Ref" : "AWS::Region" }, "\n"
        ]]}}        
      }
    },

    "WebServerSecurityGroup" : {
      "Type" : "AWS::EC2::SecurityGroup",
      "Properties" : {
        "GroupDescription" : "Enable HTTP access via port 80 locked down to the ELB and SSH access",
        "SecurityGroupIngress" : [
          {"IpProtocol" : "tcp", "FromPort" : "80", "ToPort" : "80", "SourceSecurityGroupOwnerId" : {"Fn::GetAtt" : ["ElasticLoadBalancer", "SourceSecurityGroup.OwnerAlias"]},"SourceSecurityGroupName" : {"Fn::GetAtt" : ["ElasticLoadBalancer", "SourceSecurityGroup.GroupName"]}},
          {"IpProtocol" : "tcp", "FromPort" : "22", "ToPort" : "22", "CidrIp" : { "Ref" : "SSHLocation"}}
        ]
      }
    }          
  },
  
  "Outputs" : {
    "WebsiteURL" : {
      "Description" : "Application URL",
      "Value" : { "Fn::Join" : ["", ["http://", { "Fn::GetAtt" : [ "ElasticLoadBalancer", "DNSName" ]}]] }
    }
  }
}
```

## Availability and impact considerations<a name="update.walkthrough.impact"></a>

Different properties have different impacts on the resources in the stack\. You can use AWS CloudFormation to update any property; however, before you make any changes, you should consider these questions:

1. How does the update affect the resource itself? For example, updating an alarm threshold will render the alarm inactive during the update\. As we have seen, changing the instance type requires that the instance be stopped and restarted\. AWS CloudFormation uses the Update or Modify actions for the underlying resources to make changes to resources\. To understand the impact of updates, you should check the documentation for the specific resources\.

1. Is the change mutable or immutable? Some changes to resource properties, such as changing the AMI on an Amazon EC2 instance, are not supported by the underlying services\. In the case of mutable changes, AWS CloudFormation will use the Update or Modify type APIs for the underlying resources\. For immutable property changes, AWS CloudFormation will create new resources with the updated properties and then link them to the stack before deleting the old resources\. Although AWS CloudFormation tries to reduce the down time of the stack resources, replacing a resource is a multistep process, and it will take time\. During stack reconfiguration, your application will not be fully operational\. For example, it may not be able to serve requests or access a database\.

## Related resources<a name="update.walkthrough.related"></a>

For more information about using AWS CloudFormation to start applications and on integrating with other configuration and deployment services such as Puppet and Opscode Chef, see the following whitepapers:
+  [ Bootstrapping applications via AWS CloudFormation](https://s3.amazonaws.com/cloudformation-examples/BoostrappingApplicationsWithAWSCloudFormation.pdf) 
+  [ Integrating AWS CloudFormation with Opscode Chef](https://s3.amazonaws.com/cloudformation-examples/IntegratingAWSCloudFormationWithOpscodeChef.pdf) 
+  [ Integrating AWS CloudFormation with Puppet](https://s3.amazonaws.com/cloudformation-examples/IntegratingAWSCloudFormationWithPuppet.pdf) 

The template used throughout this section is a "Hello, World" PHP application\. The template library also has an Amazon ElastiCache sample template that shows how to integrate a PHP application with ElasticCache using cfn\-hup and cfn\-init to respond to changes in the Amazon ElastiCache Cache Cluster configuration, all of which can be performed by Update Stack\.