# Using modules to encapsulate and reuse resource configurations<a name="modules"></a>

*Module*s are a way for you to package resource configurations for inclusion across stack templates, in a transparent, manageable, and repeatable way\. Modules can encapsulate common service configurations and best practices as modular, customizable building blocks for you to include in your stack templates\. Modules enable you to include resource configurations that incorporate best practices, expert domain knowledge, and accepted guidelines \(for areas such as security, compliance, governance, and industry regulations\) in your templates, without having to acquire deep knowledge of the intricacies of the resource implementation\.

For example, a domain expert in networking could create a module that contains built\-in security groups and ingress/egress rules that adhere to security guidelines\. You could then include that module in your template to provision secure networking infrastructure in your stack\-\-without having to spend time figuring out how VPCs, subnets, security groups, and gateways work\. And because modules are versioned, if security guidelines change over time, the module author can create a new version of the module that incorporates those changes\.

Characteristics of using modules in your templates include:
+ *Predictability*: A module must adhere to the schema it registers in the CloudFormation registry, so you know what resources it can resolve to once you include it in your template\.
+ *Reusability*: You can use the same module across multiple templates and accounts\.
+ *Traceability*: CloudFormation retains knowledge of which resources in a stack were provisioned from a module, enabling you to easily understand the source of resource changes\.
+ *Manageability*: Once you've registered a module, you can manage it through the CloudFormation registry, including versioning and account and region availability\.

A module can contain:
+ One or more resources to be provisioned from the module, along with any associated data, such as outputs or conditions\.
+ Any *module parameters*, which enable you to specify custom values whenever the module is used\.

For information on developing module types, see [Developing module types](https://docs.aws.amazon.com/cloudformation-cli/latest/userguide/modules-develop.html) in the *CloudFormation Command Line Interface User Guide*\.

## Using modules in a template<a name="modules-using.title"></a>

To use a module, make sure it is [registered](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/registry.html#registry-register) in the account and region in which you want to use it\. You register modules in the CloudFormation registry as private extensions\. Then, treat it much as you would an individual resource:
+ Include it in the `[Resources](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/resources-section-structure.html)` section of your template\.
+ Specify any necessary properties for the module\.

When you initiate a stack operation, CloudFormation generates a processed template that resolves any included modules into the appropriate resources\. Use [change sets](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-changesets.html) to preview the resources to be added or updated prior to actually executing the stack operation\.

Consider the following example: you have a template that contains both resources and modules\. The template contains one individual resource, **ResourceA**, as well as a module, **ModuleParent**\. That module contains two resources, **ResourceB** and **ResourceC**, as well as a nested module, **ModuleChild**\. **ModuleChild** contains a single resource, **ResourceD**\. If you create a stack from this template, CloudFormation processes the template and resolves the modules to the appropriate resources\. The resulting stack has four resources: **ResourceA**, **ResourceB**, **ResourceC**, and **ResourceD**\.

![\[During a stack operation, CloudFormation resolves the two modules included in the stack template into the appropriate four resources.\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/images/modules-resource-inclusion.png)

CloudFormation keeps track of which resources in a stack were created from modules\. You can view this information on the **Events**, **Resources**, and **Drifts** tabs for a given stack, and it is also included in change set previews\. 

Modules are distinguishable from resources in a template because they adhere to the following four\-part naming convention, as opposed to the typical three\-part convention used by resources:

`organization::service::usecase::MODULE`

## Using parameters to specify module values<a name="module-using-params"></a>

Modules can include module parameters\. Much like template parameters, module parameters enable you to input custom values to your module from the template \(or module\) that contains it\. The module can then use these values to set properties of the resources it contains\. 

You can also define template parameters that in turn set module properties, so that users can input values that get passed to the module at the time of the stack operation\. For more information about defining template parameters, see [Parameters](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/parameters-section-structure.html)\.

Likewise, if a module contains a nested module that includes module parameters, you can:
+ Specify the values for the nested module's parameters directly in the parent module\.
+ Define corresponding module parameters in the parent module that enable the nested module's parameters to be set by the template \(or module\) in which the parent module is contained\.

### Using template parameters to specify module parameter values<a name="module-using-params-example-1"></a>

The following example shows how to define template parameters that pass values to a module\. 

Here, the template containing `My::S3::SampleBucket::MODULE` defines a template parameter, `BucketName`, that enables the user to specify an S3 bucket name during the stack operation\.

```
// Template containing My::S3::SampleBucket::MODULE
{
  "Parameters": {
    "BucketName": {
      "Description": "Name for your sample bucket",
      "Type": "String"
    }
  },
  "Resources": {
    "MyBucket": {
      "Type": "My::S3::SampleBucket::MODULE",
      "Properties": {
        "BucketName": {
          "Ref": "BucketName"
        }
      }
    }
  }
}
```

### Specifying properties on resources in a child module from the parent module<a name="module-using-params-example-2"></a>

The following example illustrates how to specify parameter values in a module that is nested within another module\. 

This first module, `My::S3::SampleBucketPrivate::MODULE`, will be the child module\. It defines two parameters: `BucketName` and `AccessControl`\. The values specified for these parameters are used to specify the `BucketName` and `AccessControl` properties of the `AWS::S3::Bucket` resource the module contains\. Below is the template fragment for `My::S3::SampleBucketPrivate::MODULE`\.

```
// My::S3::SampleBucketPrivate::MODULE
{
    "AWSTemplateFormatVersion": "2010-09-09",
    "Description": "A sample S3 Bucket with Versioning and DeletionPolicy.",
    "Parameters": {
        "BucketName": {
            "Description": "Name for the bucket",
            "Type": "String"
        },
        "AccessControl": {
            "Description": "AccessControl for the bucket",
            "Type": "String"
        }
    },
    "Resources": {
        "S3Bucket": {
            "Type": "AWS::S3::Bucket",
            "Properties": {
                "BucketName": {
                    "Ref": "BucketName"
                },
                "AccessControl": {
                    "Ref": "AccessControl"
                },
                "DeletionPolicy": "Retain",
                "VersioningConfiguration": {
                    "Status": "Enabled"
                }
            }
        }
    }
}
```

Next, the previous module is nested within a parent module, `My::S3::SampleBucket::MODULE`\. The parent module, `My::S3::SampleBucket::MODULE`, sets the child module parameters in the following ways: 
+ It sets the AccessControl parameter of `My::S3::SampleBucketPrivate::MODULE` to `Private`\.
+ For `BucketName`, it defines a module parameter, which will enable the bucket name to be specified in the template \(or module\) that contains `My::S3::SampleBucket::MODULE`\.

```
// My::S3::SampleBucket::MODULE
{
  "AWSTemplateFormatVersion": "2010-09-09",
  "Description": "A sample S3 Bucket. With Private AccessControl.",
  "Parameters": {
    "BucketName": {
      "Description": "Name for your sample bucket",
      "Type": "String"
    }
  },
  "Resources": {
    "MyBucket": {
      "Type": "My::S3::SampleBucketPrivate::MODULE",
      "Properties": {
        "BucketName": {
          "Ref": "BucketName"
        },
        "AccessControl" : "Private"
      }
    }
  }
}
```

### Specifying constraints for module parameters<a name="modules-using-parameters-constraints"></a>

Module parameters do not support [Type or Constraint](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/parameters-section-structure.html#parameters-section-structure-properties) enforcement\. To perform type or constraint checking on a module parameter, create a template parameter with the desired constraints, then reference that template parameter in your module parameter\.

## Referencing resources in a module<a name="module-ref-resources"></a>

Resources in a module can be referenced by logical name\. The fully\-qualified logical name of a resource contained in a module can be constructed by combining:
+ The logical name specified for the module in the containing template \(or containing module\)\.
+ The logical name for the resource, specified in the module\.

In this way, you can use `GetAtt` and `Ref` intrinsic functions to access property values on module resources\.

In the following example, the template references a property in a module to set a corresponding property on a resource in the template itself\.

Suppose that the `My::S3::SampleBucket::MODULE` module contains an `AWS::S3::Bucket` resource with the logical name of `S3Bucket`\. To reference the bucket name of this resource using the `Ref` intrinsic function, combine the logical name given the module in the template, `MyBucket`, with the logical name of the resource in the module, `S3Bucket`, to get the fully qualified logical name of the resource: `MyBucketS3Bucket`\.

The logical names of resources contained in a module are specified in the module's schema\. You can access that schema in the following ways:
+ Finding the module in the CloudFormation registry\. The **Schema** tab displays the module schema\.
+ Using the [DescribeType](https://docs.aws.amazon.com/AWSCloudFormation/latest/APIReference/API_DescribeType.html) API to return the module details, which includes the schema\.

```
// Template that uses My::S3::SampleBucket::MODULE
{
  "Parameters": {
    "BucketName": {
      "Description": "Name for your sample bucket",
      "Type": "String"
    }
  },
  "Resources": {
    "MyBucket": {
      "Type": "My::S3::SampleBucket::MODULE",
      "Properties": {
        "BucketName": {
          "Ref": "BucketName"
        }
      }
    },
    "someQueueToMakeItExciting" : {
      "Type" : "AWS::SQS::Queue",
      "Properties": {
        "QueueName": 
          { "Fn::GetAtt" : [ "MyBucketS3Bucket", "BucketName" ] }
      }
    }
  }
}
```

## Considerations when using modules<a name="module-considerations"></a>
+ There is no additional charge for using modules\. You pay only for the resources those modules resolve to in your stacks\.
+ CloudFormation quotas, such as the maximum number of resources allowed in a stack, or the maximum size of the template body, apply to the processed template whether the resources included in that template come from modules or not\. For more information, see [AWS CloudFormation quotas](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/cloudformation-limits.html)\.
+ Tags you specify at the *stack* level are assigned to the individual resources derived from the module\.
+ Helper scripts specified at the module level do not propagate to the individual resources contained in the module when CloudFormation processes the template\.
+ Outputs specified in the module are propagated to outputs at the template level\.

  Each output will be assigned a logical ID that is a concatenation of the module logical name and the output name as defined in the module\. For more information on outputs, see [Outputs](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/outputs-section-structure.html)\.
+ Parameters specified in the module are not propagated to parameters at the template level\.

  However, you can create template\-level parameters that reference module\-level parameters\. For more information, see [Using parameters to specify module values](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/module-using-params.html)\.

## Module registration and versioning<a name="module-versioning"></a>

You register and manage the modules in your account and region using the CloudFormation registry\. For more information, see [Using the AWS CloudFormation registry](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/registry.html)\.

You can register multiple versions of the same module in a given account and region\. Keep in mind the following considerations:
+ A module must be registered in the account and region in which you want to use it\.
+ During stack operations, CloudFormation uses whatever version of the module that is currently registered as the default version *in the account and region in which the stack operation is being performed*\. This includes modules that are nested in other modules\.

  Therefore, be aware that if you have different versions of the same module registered as the default version in different accounts or regions, using the same template may result in different results\.

  For more information, see [Specifying which version of an extension to use](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/registry.html)\.
+ During stack operations, CloudFormation uses whatever version of the *resource* that is currently registered as the default version in the account and region in which the stack operation is being performed\. This includes the resources generated by including modules\.
+ Changing the default version of a module does not initiate any stack update operation\. However, the next time you perform a stack operation with any template containing that module, such as a stack update, CloudFormation will use the new default version in the operation\.

  The one exception to this is performing a stack update with the **use previous template** option specified, as described below\.
+ For stack update operations, if you specify the **use previous template** option, CloudFormation uses the previous processed template for the stack update, and does not reprocess the module for any changes you might have made to it\.
+ To guarantee uniform results, if you are including modules in a stack template for use with stack sets, you should ensure that the same version of the module is set as the default version in all the accounts and regions in which you are planning to deploy your stack instances\. This includes for modules that are nested in other modules\. For more information on stack sets, see [Working with stack sets](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/what-is-cfnstacksets.html)\.

For more information on registering new versions of a module, or changing the default version of a module, see [Using the AWS CloudFormation registry](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/registry.html)\.