# AWS::OpsWorksCM::Server EngineAttribute<a name="aws-properties-opsworkscm-server-engineattribute"></a>

The `EngineAttribute` property type specifies administrator credentials for an AWS OpsWorks for Chef Automate or OpsWorks for Puppet Enterprise server\. `EngineAttribute` is a property of the `AWS::OpsWorksCM::Server` resource type\.

## Syntax<a name="aws-properties-opsworkscm-server-engineattribute-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-opsworkscm-server-engineattribute-syntax.json"></a>

```
{
  "[Name](#cfn-opsworkscm-server-engineattribute-name)" : String,
  "[Value](#cfn-opsworkscm-server-engineattribute-value)" : String
}
```

### YAML<a name="aws-properties-opsworkscm-server-engineattribute-syntax.yaml"></a>

```
  [Name](#cfn-opsworkscm-server-engineattribute-name): String
  [Value](#cfn-opsworkscm-server-engineattribute-value): String
```

## Properties<a name="aws-properties-opsworkscm-server-engineattribute-properties"></a>

`Name`  <a name="cfn-opsworkscm-server-engineattribute-name"></a>
The name of the engine attribute\.  
 **Attribute name for Chef Automate servers:**   
+  `CHEF_AUTOMATE_ADMIN_PASSWORD` 
 **Attribute names for Puppet Enterprise servers:**   
+  `PUPPET_ADMIN_PASSWORD` 
+  `PUPPET_R10K_REMOTE` 
+  `PUPPET_R10K_PRIVATE_KEY` 
*Required*: No  
*Type*: String  
*Maximum*: `10000`  
*Pattern*: `(?s).*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Value`  <a name="cfn-opsworkscm-server-engineattribute-value"></a>
The value of the engine attribute\.  
 **Attribute value for Chef Automate servers:**   
+  `CHEF_AUTOMATE_PIVOTAL_KEY`: A base64\-encoded RSA public key\. The corresponding private key is required to access the Chef API\. You can generate this key by running the following [OpenSSL](https://www.openssl.org/) command on Linux\-based computers\.

   `openssl genrsa -out pivotal_key_file_name.pem 2048` 

  On Windows\-based computers, you can use the PuTTYgen utility to generate a base64\-encoded RSA private key\. For more information, see [PuTTYgen \- Key Generator for PuTTY on Windows](https://www.ssh.com/ssh/putty/windows/puttygen) on SSH\.com\.
 **Attribute values for Puppet Enterprise servers:**   
+  `PUPPET_ADMIN_PASSWORD`: An administrator password that you can use to sign in to the Puppet Enterprise console webpage after the server is online\. The password must use between 8 and 32 ASCII characters\.
+  `PUPPET_R10K_REMOTE`: The r10k remote is the URL of your control repository \(for example, ssh://git@your\.git\-repo\.com:user/control\-repo\.git\)\. Specifying an r10k remote opens TCP port 8170\.
+  `PUPPET_R10K_PRIVATE_KEY`: If you are using a private Git repository, add `PUPPET_R10K_PRIVATE_KEY` to specify a PEM\-encoded private SSH key\.
*Required*: No  
*Type*: String  
*Maximum*: `10000`  
*Pattern*: `(?s).*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-opsworkscm-server-engineattribute--seealso"></a>
+  [Create a Chef Automate Server in AWS CloudFormation](https://docs.aws.amazon.com/opsworks/latest/userguide/opscm-create-server-cfn.html) in the *AWS OpsWorks User Guide* 
+  [Create a Puppet Enterprise Master in AWS CloudFormation](https://docs.aws.amazon.com/opsworks/latest/userguide/opspup-create-server-cfn.html) in the *AWS OpsWorks User Guide* 
+  [ `CreateServer` ](https://docs.aws.amazon.com/opsworks-cm/latest/APIReference/API_CreateServer.html) in the *AWS OpsWorks CM API Reference* 

