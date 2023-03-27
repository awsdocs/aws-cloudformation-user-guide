# AWS::Pipes::Pipe PipeEnrichmentParameters<a name="aws-properties-pipes-pipe-pipeenrichmentparameters"></a>

The parameters required to set up enrichment on your pipe\.

## Syntax<a name="aws-properties-pipes-pipe-pipeenrichmentparameters-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-pipes-pipe-pipeenrichmentparameters-syntax.json"></a>

```
{
  "[HttpParameters](#cfn-pipes-pipe-pipeenrichmentparameters-httpparameters)" : PipeEnrichmentHttpParameters,
  "[InputTemplate](#cfn-pipes-pipe-pipeenrichmentparameters-inputtemplate)" : String
}
```

### YAML<a name="aws-properties-pipes-pipe-pipeenrichmentparameters-syntax.yaml"></a>

```
  [HttpParameters](#cfn-pipes-pipe-pipeenrichmentparameters-httpparameters): 
    PipeEnrichmentHttpParameters
  [InputTemplate](#cfn-pipes-pipe-pipeenrichmentparameters-inputtemplate): String
```

## Properties<a name="aws-properties-pipes-pipe-pipeenrichmentparameters-properties"></a>

`HttpParameters`  <a name="cfn-pipes-pipe-pipeenrichmentparameters-httpparameters"></a>
Contains the HTTP parameters to use when the target is a API Gateway REST endpoint or EventBridge ApiDestination\.  
If you specify an API Gateway REST API or EventBridge ApiDestination as a target, you can use this parameter to specify headers, path parameters, and query string keys/values as part of your target invoking request\. If you're using ApiDestinations, the corresponding Connection can also have these values configured\. In case of any conflicting keys, values from the Connection take precedence\.  
*Required*: No  
*Type*: [PipeEnrichmentHttpParameters](aws-properties-pipes-pipe-pipeenrichmenthttpparameters.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`InputTemplate`  <a name="cfn-pipes-pipe-pipeenrichmentparameters-inputtemplate"></a>
Valid JSON text passed to the enrichment\. In this case, nothing from the event itself is passed to the enrichment\. For more information, see [The JavaScript Object Notation \(JSON\) Data Interchange Format](http://www.rfc-editor.org/rfc/rfc7159.txt)\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)