# AWS::CloudFormation::Init<a name="aws-resource-init"></a>

Use the AWS::CloudFormation::Init type to include metadata on an Amazon EC2 instance for the cfn\-init helper script\. If your template calls the cfn\-init script, the script looks for resource metadata rooted in the AWS::CloudFormation::Init metadata key\. For more information about cfn\-init, see [cfn\-init](cfn-init.md)\.

cfn\-init supports all metadata types for Linux systems\. It supports metadata types for Windows with conditions that are described in the sections that follow\.

For an example of using AWS::CloudFormation::Init and the cfn\-init helper script, see [Deploying applications on Amazon EC2 with AWS CloudFormation](deploying.applications.md)\.

For an example that shows how to use cfn\-init to create a Windows stack, see [Bootstrapping AWS CloudFormation Windows stacks](cfn-windows-stacks-bootstrapping.md)\.

## Syntax<a name="aws-resource-cloudformation-init-syntax"></a>

The configuration is separated into sections\. The following template snippet shows how you can attach metadata for cfn\-init to an Amazon EC2 instance resource within the template\.

The metadata is organized into config keys, which you can group into configsets\. You can specify a configset when you call cfn\-init in your template\. If you don't specify a configset, cfn\-init looks for a single config key named *config*\.

**Note**  
The cfn\-init helper script processes these configuration sections in the following order: packages, groups, users, sources, files, commands, and then services\. If you require a different order, separate your sections into different config keys, and then use a configset that specifies the order in which the config keys should be processed\.

### JSON<a name="aws-resource-cloudformation-init-syntax.json"></a>

```
"Resources": {
  "MyInstance": {
    "Type": "AWS::EC2::Instance",
    "Metadata" : {
      "AWS::CloudFormation::Init" : {
        "config" : {
          "packages" : {
            :
          },
          "groups" : {
            :
          },
          "users" : {
            :
          },
          "sources" : {
            :
          },
          "files" : {
            :
          },
          "commands" : {
            :
          },
          "services" : {
            :
          }
        }
      }
    },
    "Properties": {
      :
    }
  }
}
```

### YAML<a name="aws-resource-cloudformation-init-syntax.yaml"></a>

```
Resources: 
  MyInstance: 
    Type: AWS::EC2::Instance
    Metadata: 
      AWS::CloudFormation::Init: 
        config: 
          packages: 
            :
          groups: 
            :
          users: 
            :
          sources: 
            :
          files: 
            :
          commands: 
            :
          services: 
            :
    Properties: 
      :
```

**Note**  
To specify the `AWS::CloudFormation::Init` property for an Amazon EC2 instances, see [Amazon Linux example](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/cfn-init.html#cfn-init-Examples)\.

## Configsets<a name="aws-resource-init-configsets"></a>

If you want to create more than one config key and to have cfn\-init process them in a specific order, create a configset that contains the config keys in the desired order\. 

### Single configset<a name="w7739ab1c27c15c15c23c13b4"></a>

The following template snippet creates configsets named `ascending` and `descending` that each contain two config keys\.

#### JSON<a name="aws-resource-cloudformation-init-configset-example1.json"></a>

```
"AWS::CloudFormation::Init" : {
    "configSets" : {
        "ascending" : [ "config1" , "config2" ],
        "descending" : [ "config2" , "config1" ]
    },
    "config1" : {
        "commands" : {
            "test" : {
                "command" : "echo \"$CFNTEST\" > test.txt",
                "env" : { "CFNTEST" : "I come from config1." },
                "cwd" : "~"
            }
        }
    },
    "config2" : {
        "commands" : {
            "test" : {
                "command" : "echo \"$CFNTEST\" > test.txt",
                "env" : { "CFNTEST" : "I come from config2" },
                "cwd" : "~"
            }
        }
    }
}
```

#### YAML<a name="aws-resource-cloudformation-init-configset-example1.yaml"></a>

```
AWS::CloudFormation::Init: 
  configSets: 
    ascending: 
      - "config1"
      - "config2"
    descending: 
      - "config2"
      - "config1"
  config1: 
    commands: 
      test: 
        command: "echo \"$CFNTEST\" > test.txt"
        env: 
          CFNTEST: "I come from config1."
        cwd: "~"
  config2: 
    commands: 
      test: 
        command: "echo \"$CFNTEST\" > test.txt"
        env: 
          CFNTEST: "I come from config2"
        cwd: "~"
```

#### Related cfn\-init calls<a name="w7739ab1c27c15c15c23c13b4b8"></a>

The following example calls to cfn\-init refer to the preceding example configsets\. The example calls are abbreviated for clarity, see [cfn\-init](cfn-init.md) for the complete syntax\.
+ If a call to cfn\-init specifies the `ascending` configset:

  ```
  cfn-init -c ascending
  ```

  the script processes `config1` and then processes `config2` and the test\.txt file would contain the text `I come from config2`\.
+ If a call to cfn\-init specifies the `descending` configset:

  ```
  cfn-init -c descending
  ```

  the script processes `config2` and then processes `config1` and the test\.txt file would contain the text `I come from config1`\.

### Multiple configsets<a name="w7739ab1c27c15c15c23c13b6"></a>

You can create multiple configsets, and call a series of them using your cfn\-init script\. Each configset can contain a list of config keys or references to other configsets\. For example, the following template snippet creates three configsets\. The first configset, `test1`, contains one config key named `1`\. The second configset, `test2`, contains a reference to the `test1` configset and one config key named `2`\. The third configset, default, contains a reference to the configset `test2`\.

#### JSON<a name="aws-resource-cloudformation-init-configset-example2.json"></a>

```
"AWS::CloudFormation::Init" : {
    "configSets" : {
        "test1" : [ "1" ],
        "test2" : [ { "ConfigSet" : "test1" }, "2" ],
        "default" : [ { "ConfigSet" : "test2" } ]
    },
    "1" : {
        "commands" : {
            "test" : {
                "command" : "echo \"$MAGIC\" > test.txt",
                "env" : { "MAGIC" : "I come from the environment!" },
                "cwd" : "~"
            }
        }
    },
    "2" : {
        "commands" : {
            "test" : {
                "command" : "echo \"$MAGIC\" >> test.txt",
                "env" : { "MAGIC" : "I am test 2!" },
                "cwd" : "~"
            }
        }
    }
}
```

#### YAML<a name="aws-resource-cloudformation-init-configset-example2.yaml"></a>

```
AWS::CloudFormation::Init: 
  1: 
    commands: 
      test: 
        command: "echo \"$MAGIC\" > test.txt"
        env: 
          MAGIC: "I come from the environment!"
        cwd: "~"
  2: 
    commands: 
      test: 
        command: "echo \"$MAGIC\" >> test.txt"
        env: 
          MAGIC: "I am test 2!"
        cwd: "~"
  configSets: 
    test1: 
      - "1"
    test2: 
      - 
        ConfigSet: "test1"
      - "2"
    default: 
      - 
        ConfigSet: "test2"
```

#### Related cfn\-init calls<a name="w7739ab1c27c15c15c23c13b6b8"></a>

The following calls to cfn\-init refer to the configSets declared in the preceding template snippet\. The example calls are abbreviated for clarity, see [cfn\-init](cfn-init.md) for the complete syntax\.
+ If you specify `test1` only:

  ```
  cfn-init -c test1
  ```

  cfn\-init processes config key `1` only\.
+ If you specify `test2` only:

  ```
  cfn-init -c test2
  ```

  cfn\-init processes config key `1` and then processes config key `2`\.
+ If you specify the `default` configset \(or no configsets at all\):

  ```
  cfn-init -c default
  ```

  you get the same behavior that you would if you specify configset `test2`\.

## Commands<a name="aws-resource-init-commands"></a>

You can use the commands key to execute commands on the EC2 instance\. The commands are processed in alphabetical order by name\.


| Key | Description | 
| --- | --- | 
|  command  |  Required\. Either an array or a string specifying the command to run\. If you use an array, you do not need to escape space characters or enclose command parameters in quotes\. Don't use the array to specify multiple commands\.  | 
|  env  |  Optional\. Sets environment variables for the command\. This property overwrites, rather than appends, the existing environment\.  | 
|  cwd  |  Optional\. The working directory  | 
|  test  |  Optional\. A test command that determines whether cfn\-init runs commands that are specified in the command key\. If the test passes, cfn\-init runs the commands\. The cfn\-init script runs the test in a command interpreter, such as Bash or `cmd.exe`\. Whether a test passes depends on the exit code that the interpreter returns\. For Linux, the test command must return an exit code of `0` for the test to pass\. For Windows, the test command must return an %ERRORLEVEL% of `0`\.  | 
|  ignoreErrors  |  Optional\. A Boolean value that determines whether cfn\-init continues to run if the command in contained in the command key fails \(returns a non\-zero value\)\. Set to `true` if you want cfn\-init to continue running even if the command fails\. Set to `false` if you want cfn\-init to stop running if the command fails\. The default value is `false`\.  | 
|  waitAfterCompletion  |  Optional\. For Windows systems only\. Specifies how long to wait \(in seconds\) after a command has finished in case the command causes a reboot\. The default value is 60 seconds and a value of "forever" directs cfn\-init to exit and resume only after the reboot is complete\. Set this value to `0` if you do not want to wait for every command\.   | 

### Example<a name="w7739ab1c27c15c15c23c15b6"></a>

The following example snippet calls the echo command if the `~/test.txt` file doesn't exist\.

#### JSON<a name="aws-resource-init-commands-example.json"></a>

```
"commands" : {
    "test" : {
        "command" : "echo \"$MAGIC\" > test.txt",
        "env" : { "MAGIC" : "I come from the environment!" },
        "cwd" : "~",
        "test" : "test ! -e ~/test.txt",
        "ignoreErrors" : "false"
    },
    "test2" : {
        "command" : "echo \"$MAGIC2\" > test2.txt",
        "env" : { "MAGIC2" : "I come from the environment!" },
        "cwd" : "~",
        "test" : "test ! -e ~/test2.txt",
        "ignoreErrors" : "false"
    }
}
```

#### YAML<a name="aws-resource-init-commands-example.yaml"></a>

```
commands: 
  test: 
    command: "echo \"$MAGIC\" > test.txt"
    env: 
      MAGIC: "I come from the environment!"
    cwd: "~"
    test: "test ! -e ~/test.txt"
    ignoreErrors: "false"
  test2: 
    command: "echo \"$MAGIC2\" > test2.txt"
    env: 
      MAGIC2: "I come from the environment!"
    cwd: "~"
    test: "test ! -e ~/test2.txt"
    ignoreErrors: "false"
```

## Files<a name="aws-resource-init-files"></a>

You can use the `files` key to create files on the EC2 instance\. The content can be either inline in the template or the content can be pulled from a URL\. The files are written to disk in lexicographic order\. The following table lists the supported keys\.


| Key | Description | 
| --- | --- | 
|  content  |  Either a string or a properly formatted JSON object\. If you use a JSON object as your content, the JSON will be written to a file on disk\. Any intrinsic functions such as Fn::GetAtt or Ref are evaluated before the JSON object is written to disk\. When you create a symlink, specify the symlink target as the content\.  If you create a symlink, the helper script modifies the permissions of the target file\. Currently, you can't create a symlink without modifying the permissions of the target file\.   | 
|  source  |  A URL to load the file from\. This option cannot be specified with the content key\.  | 
|  encoding  |  The encoding format\. Only used if the content is a string\. Encoding is not applied if you are using a source\. Valid values: `plain` \| `base64`  | 
|  group  |  The name of the owning group for this file\. Not supported for Windows systems\.  | 
|  owner  |  The name of the owning user for this file\. Not supported for Windows systems\.  | 
|  mode  |  A six\-digit octal value representing the mode for this file\. Not supported for Windows systems\. Use the first three digits for symlinks and the last three digits for setting permissions\. To create a symlink, specify **120*xxx***, where `xxx` defines the permissions of the target file\. To specify permissions for a file, use the last three digits, such as **000644**\.  | 
|  authentication  |  The name of an authentication method to use\. This overrides any default authentication\. You can use this property to select an authentication method you define with the [AWS::CloudFormation::Authentication](aws-resource-authentication.md) resource\.  | 
|  context  |  Specifies a context for files that are to be processed as [Mustache templates](http://mustache.github.com/mustache.5.html)\. To use this key, you must have installed aws\-cfn\-bootstrap 1\.3\-11 or later as well as [pystache](https://github.com/defunkt/pystache)\.  | 

### Examples<a name="w7739ab1c27c15c15c23c17b6"></a>

The following example snippet creates a file named setup\.mysql as part of a larger installation\.

**Example JSON**  

```
"files" : {
  "/tmp/setup.mysql" : {
    "content" : { "Fn::Join" : ["", [
      "CREATE DATABASE ", { "Ref" : "DBName" }, ";\n",
      "CREATE USER '", { "Ref" : "DBUsername" }, "'@'localhost' IDENTIFIED BY '",
                       { "Ref" : "DBPassword" }, "';\n",
      "GRANT ALL ON ", { "Ref" : "DBName" }, ".* TO '", { "Ref" : "DBUsername" },
                       "'@'localhost';\n",
      "FLUSH PRIVILEGES;\n"
      ]]},
    "mode"  : "000644",
    "owner" : "root",
    "group" : "root"
  }
}
```

**Example YAML**  

```
files: 
  /tmp/setup.mysql: 
    content: !Sub |
      CREATE DATABASE ${DBName};
      CREATE USER '${DBUsername}'@'localhost' IDENTIFIED BY '${DBPassword}';
      GRANT ALL ON ${DBName}.* TO '${DBUsername}'@'localhost';
      FLUSH PRIVILEGES;
    mode: "000644"
    owner: "root"
    group: "root"
```

The full template is available at: [https://s3\.amazonaws\.com/cloudformation\-templates\-us\-east\-1/Drupal\_Single\_Instance\.template](https://s3.amazonaws.com/cloudformation-templates-us-east-1/Drupal_Single_Instance.template)

The following example snippet creates a symlink `/tmp/myfile2.txt` that points at an existing file `/tmp/myfile1.txt`\. The permissions of the target file `/tmp/myfile1.txt` is defined by the mode value `644`\. 

**Example JSON**  

```
"files" : {
  "/tmp/myfile2.txt" : {
    "content" : "/tmp/myfile1.txt",
    "mode" : "120644"
  }
}
```

**Example YAML**  

```
files: 
  /tmp/myfile2.txt: 
    content: "/tmp/myfile1.txt"
    mode: "120644"
```

Mustache templates are used primarily to create configuration files\. For example, you can store a configuration file in an S3 bucket and interpolate Refs and GetAtts from the template, instead of using [`Fn::Join`](intrinsic-function-reference-join.md)\. The following example snippet outputs "Content for test9" to `/tmp/test9.txt`\.

**Example JSON**  

```
"files" : {
    "/tmp/test9.txt" : {
        "content" : "Content for {{name}}",
        "context" : { "name" : "test9" }
    }
}
```

**Example YAML**  

```
files: 
  /tmp/test9.txt: 
    content: "Content for {{name}}"
    context: 
      name: "test9"
```

When working with Mustache templates, note the following:
+ The context key must be present for the files to be processed\.
+ The context key must be a key\-value map, but it can be nested\.
+ You can process files with inline content by using the content key and remote files by using the source key\. 
+ Mustache support depends on the pystache version\. Version 0\.5\.2 supports the [Mustache 1\.1\.2 specification](https://github.com/mustache/spec/tree/v1.1.2)\. 

## Groups<a name="aws-resource-init-groups"></a>

You can use the groups key to create Linux/UNIX groups and to assign group IDs\. The groups key is not supported for Windows systems\.

To create a group, add a new key\-value pair that maps a new group name to an optional group ID\. The groups key can contain one or more group names\. The following table lists the available keys\.


| Key | Description | 
| --- | --- | 
|   `gid`  |  A group ID number\. If a group ID is specified, and the group already exists by name, the group creation will fail\. If another group has the specified group ID, the OS may reject the group creation\. Example: `{ "gid" : "23" }`  | 

### Example snippet<a name="aws-resource-init-groups-snippet"></a>

The following snippet specifies a group named `groupOne` without assigning a group ID and a group named `groupTwo` that specified a group ID value of `45`\.

#### JSON<a name="aws-resource-init-groups-snippet.json"></a>

```
"groups" : {
    "groupOne" : {},
    "groupTwo" : { "gid" : "45" }
}
```

#### YAML<a name="aws-resource-init-groups-snippet.yaml"></a>

```
groups: 
  groupOne: {}
  groupTwo: 
    gid: "45"
```

## Packages<a name="aws-resource-init-packages"></a>

You can use the packages key to download and install pre\-packaged applications and components\. On Windows systems, the packages key supports only the MSI installer\.

### Supported package formats<a name="aws-resource-init-packages-formats"></a>

The cfn\-init script currently supports the following package formats: apt, msi, python, rpm, rubygems, and yum\. Packages are processed in the following order: rpm, yum/apt, and then rubygems and python\. There is no ordering between rubygems and python, and packages within each package manager are not guaranteed to be installed in any order\.

### Specifying versions<a name="aws-resource-init-packages-versions"></a>

Within each package manager, each package is specified as a package name and a list of versions\. The version can be a string, a list of versions, or an empty string or list\. An empty string or list indicates that you want the latest version\. For rpm manager, the version is specified as a path to a file on disk or a URL\.

If you specify a version of a package, cfn\-init will attempt to install that version even if a newer version of the package is already installed on the instance\. Some package managers support multiple versions, but others may not\. Please check the documentation for your package manager for more information\. If you do not specify a version and a version of the package is already installed, the cfn\-init script will not install a new version—it will assume that you want to keep and use the existing version\.

### Example snippets<a name="aws-resource-init-packages-snippet"></a>

#### RPM, yum, and Rubygems<a name="w7739ab1c27c15c15c23c21b8b2"></a>

The following snippet specifies a version URL for rpm, requests the latest versions from yum, and version 0\.10\.2 of chef from rubygems:

##### JSON<a name="aws-resource-init-packages-example1.json"></a>

```
"rpm" : {
  "epel" : "http://download.fedoraproject.org/pub/epel/5/i386/epel-release-5-4.noarch.rpm"
},
"yum" : {
  "httpd" : [],
  "php" : [],
  "wordpress" : []
},
"rubygems" : {
  "chef" : [ "0.10.2" ]
}
```

##### YAML<a name="aws-resource-init-packages-example1.yaml"></a>

```
rpm: 
  epel: "http://download.fedoraproject.org/pub/epel/5/i386/epel-release-5-4.noarch.rpm"
yum: 
  httpd: []
  php: []
  wordpress: []
rubygems: 
  chef: 
    - "0.10.2"
```

#### MSI package<a name="w7739ab1c27c15c15c23c21b8b4"></a>

The following snippet specifies a URL for an MSI package:

##### JSON<a name="aws-resource-init-packages-example2.json"></a>

```
"msi" : {
  "awscli" : "https://s3.amazonaws.com/aws-cli/AWSCLI64.msi"
}
```

##### YAML<a name="aws-resource-init-packages-example2.yaml"></a>

```
msi: 
  awscli: "https://s3.amazonaws.com/aws-cli/AWSCLI64.msi"
```

## Services<a name="aws-resource-init-services"></a>

You can use the services key to define which services should be enabled or disabled when the instance is launched\. On Linux systems, this key is supported by using sysvinit\. On Windows systems, it is supported by using the Windows service manager\.

The services key also allows you to specify dependencies on sources, packages and files so that if a restart is needed due to files being installed, cfn\-init will take care of the service restart\. For example, if you download the Apache HTTP Server package, the package installation will automatically start the Apache HTTP Server during the stack creation process\. However, if the Apache HTTP Server configuration is updated later in the stack creation process, the update won't take effect unless the Apache server is restarted\. You can use the services key to ensure that the Apache HTTP service is restarted\.

The following table lists the supported keys\.


| Key | Description | 
| --- | --- | 
|  ensureRunning  |  Set to true to ensure that the service is running after cfn\-init finishes\. Set to false to ensure that the service is not running after cfn\-init finishes\. Omit this key to make no changes to the service state\.  | 
|  enabled  |  Set to true to ensure that the service will be started automatically upon boot\. Set to false to ensure that the service will not be started automatically upon boot\. Omit this key to make no changes to this property\.  | 
|  files  |  A list of files\. If cfn\-init changes one directly via the files block, this service will be restarted  | 
|  sources  |  A list of directories\. If cfn\-init expands an archive into one of these directories, this service will be restarted\.  | 
|  packages  |  A map of package manager to list of package names\. If cfn\-init installs or updates one of these packages, this service will be restarted\.  | 
|  commands  |  A list of command names\. If cfn\-init runs the specified command, this service will be restarted\.  | 

### Examples<a name="w7739ab1c27c15c15c23c23c10"></a>

#### Linux<a name="w7739ab1c27c15c15c23c23c10b2"></a>

The following Linux snippet configures the services as follows:
+ The nginx service will be restarted if either /etc/nginx/nginx\.conf or /var/www/html are modified by cfn\-init\.
+ The php\-fastcgi service will be restarted if cfn\-init installs or updates php or spawn\-fcgi using yum\.
+ The sendmail service will be stopped and disabled\.

##### JSON<a name="aws-resource-init-services-example1.json"></a>

```
"services" : {
  "sysvinit" : {
    "nginx" : {
      "enabled" : "true",
      "ensureRunning" : "true",
      "files" : ["/etc/nginx/nginx.conf"],
      "sources" : ["/var/www/html"]
    },
    "php-fastcgi" : {
      "enabled" : "true",
      "ensureRunning" : "true",
      "packages" : { "yum" : ["php", "spawn-fcgi"] }
    },
    "sendmail" : {
      "enabled" : "false",
      "ensureRunning" : "false"
    }
  }
}
```

##### YAML<a name="aws-resource-init-services-example1.yaml"></a>

```
services: 
  sysvinit: 
    nginx: 
      enabled: "true"
      ensureRunning: "true"
      files: 
        - "/etc/nginx/nginx.conf"
      sources: 
        - "/var/www/html"
    php-fastcgi: 
      enabled: "true"
      ensureRunning: "true"
      packages: 
        yum: 
          - "php"
          - "spawn-fcgi"
    sendmail: 
      enabled: "false"
      ensureRunning: "false"
```

#### Windows<a name="w7739ab1c27c15c15c23c23c10b4"></a>

The following Windows snippet starts the `cfn-hup` service, sets it to automatic, and restarts the service if `cfn-init` modifies the specified configuration files:

##### JSON<a name="aws-resource-init-services-example2.json"></a>

```
"services" : {
  "windows" : {
    "cfn-hup" : {
      "enabled" : "true",
      "ensureRunning" : "true",
      "files" : ["c:\\cfn\\cfn-hup.conf", "c:\\cfn\\hooks.d\\cfn-auto-reloader.conf"]
    }
  }
}
```

##### YAML<a name="aws-resource-init-services-example2.yaml"></a>

```
services: 
  windows: 
    cfn-hup: 
      enabled: "true"
      ensureRunning: "true"
      files: 
        - "c:\\cfn\\cfn-hup.conf"
        - "c:\\cfn\\hooks.d\\cfn-auto-reloader.conf"
```

## Sources<a name="aws-resource-init-sources"></a>

You can use the sources key to download an archive file and unpack it in a target directory on the EC2 instance\. This key is fully supported for both Linux and Windows systems\.

**Supported formats**  
Supported formats are tar, tar\+gzip, tar\+bz2 and zip\.

### Examples<a name="w7739ab1c27c15c15c23c25b6"></a>

#### GitHub<a name="w7739ab1c27c15c15c23c25b6b2"></a>

If you use GitHub as a source control system, you can use cfn\-init and the sources package mechanism to pull a specific version of your application\. GitHub allows you to create a zip or a tar from a specific version via a URL as follows:

```
https://github.com/<your directory>/(zipball|tarball)/<version> 
```

For example, the following snippet pulls down version *master* as a `.tar` file\.

##### JSON<a name="aws-resource-init-sources-example1.json"></a>

```
"sources" : {
  "/etc/puppet" : "https://github.com/user1/cfn-demo/tarball/master"
  }
```

##### YAML<a name="aws-resource-init-sources-example1.yaml"></a>

```
sources: 
  /etc/puppet: "https://github.com/user1/cfn-demo/tarball/master"
```

#### S3 Bucket<a name="w7739ab1c27c15c15c23c25b6b4"></a>

The following example downloads a zip file from an Amazon S3 bucket and unpacks it into /etc/myapp:

**Note**  
You can use authentication credentials for a source\. However, you cannot put an authentication key in the sources block\. Instead, include a buckets key in your S3AccessCreds block\. For more information on Amazon S3 authentication credentials, see [AWS::CloudFormation::Authentication](aws-resource-authentication.md)\.  
For an example, see the [example template](https://s3.amazonaws.com/cloudformation-templates-us-east-1/S3Bucket_SourceAuth.template)\.

##### JSON<a name="aws-resource-init-sources-example2.json"></a>

```
"sources" : {
  "/etc/myapp" : "https://s3.amazonaws.com/mybucket/myapp.tar.gz"
  }
```

##### YAML<a name="aws-resource-init-sources-example2.yaml"></a>

```
sources: 
  /etc/myapp: "https://s3.amazonaws.com/mybucket/myapp.tar.gz"
```

## Users<a name="aws-resource-init-users"></a>

You can use the users key to create Linux/UNIX users on the EC2 instance\. The users key is not supported for Windows systems\.

The following table lists the supported keys\.


| Key | Description | 
| --- | --- | 
|  uid  |  A user ID\. The creation process fails if the user name exists with a different user ID\. If the user ID is already assigned to an existing user the operating system may reject the creation request\.  | 
|  groups  |  A list of group names\. The user will be added to each group in the list\.  | 
|  homeDir  |  The user's home directory\.  | 

### Example<a name="w7739ab1c27c15c15c23c27b8"></a>

Users are created as non\-interactive system users with a shell of /sbin/nologin\. This is by design and cannot be modified\.

#### JSON<a name="aws-resource-init-users-example.json"></a>

```
"users" : {
    "myUser" : {
        "groups" : ["groupOne", "groupTwo"],
        "uid" : "50",
        "homeDir" : "/tmp"
    }
}
```

#### YAML<a name="aws-resource-init-users-example.yaml"></a>

```
users: 
  myUser: 
    groups: 
      - "groupOne"
      - "groupTwo"
    uid: "50"
    homeDir: "/tmp"
```