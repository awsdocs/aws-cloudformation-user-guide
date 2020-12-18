# Macro example: Creating and using a macro<a name="macros-example"></a>

The following example walks through the process of using macros, from defining the macro in a template, to creating a Lamdba function for the macro, and then to using the macro in a template\.

In this example, we create a simple macro that inserts the specified string in place of the specified target content in the processed template\. And then we'll use it to insert a blank `WaitHandleCondition` in the specified location in the processed template\. 

## Macro example: Macro definition template<a name="macros-example-definiton"></a>

Before using a macro, we first have to do two things: create the Lambda function that performs the desired template processing, and then make that Lambda function available to CloudFormation by creating a macro definition\. 

**Note**  
We'll examine the actual code for the Lambda function later in this topic\. 

The following sample template contains the definition for our example macro\. To make the macro available in a specific CloudFormation account, we create a stack from the template\. The macro definition specifies the macro name, a brief description, and references the ARN of the Lambda function that CloudFormation invokes when this macro is used in a template\. \(We have not included a **LogGroupName** or **LogRoleARN** property for error logging\.\) For more information, see [AWS::CloudFormation::Macro](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-cloudformation-macro.html)\.

In this example, assume that the stack created from this template is named **JavaMacroFunc**\. Because the macro `Name` property is set to the stack name, the resulting macro is named **JavaMacroFunc** as well\.

```
AWSTemplateFormatVersion: 2010-09-09
  Resources:
    Macro:
      Type: AWS::CloudFormation::Macro
      Properties:
        Name: !Sub '${AWS::StackName}'
        Description: Adds a blank WaitConditionHandle named 'WaitHandle'
        FunctionName: "arn:aws:lambda:us-east-1:012345678910:function:JavaMacroFunc"
```

## Macro example: Macro usage template<a name="macros-example-usage"></a>

To use our macro in this case, we're going to include it in a template using the [`Fn::Transform`](intrinsic-function-reference-transform.md) intrinsic function\.

When we create a stack using the template below, CloudFormation calls our example macro\. The underlying Lambda function replaces one specified string with another specified string\. In this case, the result is a blank [AWS::CloudFormation::WaitConditionHandle](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-waitconditionhandle.html) is inserted into the processed template\. 

Note the following: 
+ The macro to invoke is specified as **JavaMacroFunc**, which is from the previous macro definition example\.
+ The macro is passed two parameters, `target` and `replacement`, which represent the target string and its desired replacement value\.
+ The macro can operate on the contents of the `Type` node because `Type` is a sibling of the `Fn::Transform` function referencing the macro\.
+ The resulting [AWS::CloudFormation::WaitConditionHandle](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-waitconditionhandle.html) is named `2a`\.
+ The template also contains a template parameter, `ExampleParameter`, which the macro also has access to \(but doesn't use in this case\)\.

```
Parameters:
  ExampleParameter: 
    Type: String
    Default: 'SampleMacro'

Resources:
  2a: 
    Fn::Transform: 
      Name: "JavaMacroFunc"
      Parameters:
        replacement: 'AWS::CloudFormation::WaitConditionHandle' 
        target: '$$REPLACEMENT$$'
    Type: '$$REPLACEMENT$$'
```

## Macro example: Request event mapping<a name="macros-example-request"></a>

When CloudFormation processes our example template during stack creation, it passes the following event mapping to the Lambda function referenced in the **JavaMacroFunc** macro definition\.

Note that `fragment` contains JSON representing the template fragment that the macro can process\. This fragment consists of the siblings of the `Fn::Transform` function call, but not the function call itself\. Also, `params` contains JSON representing the macro parameters\. In this case, replacement and target\. Similarly, `templateParameterValues` contains JSON representing the parameters specified for the template as a whole\.
+ region

  `us-east-1`
+ accountId

  `012345678910`
+ fragment

  ```
  {
    "Type": "$$REPLACEMENT$$"
  }
  ```
+ transformId

  `012345678910::JavaMacroFunc`
+ params

  ```
  {
      "replacement": "AWS::CloudFormation::WaitConditionHandle", 
      "target": "$$REPLACEMENT$$"
  }
  ```
+ requestId

  `5dba79b5-f117-4de0-9ce4-d40363bfb6ab`
+ templateParameterValues

  ```
  {
      "ExampleParameter": "SampleMacro"
  }
  ```

## Macro example: Lambda function code<a name="macros-example-function"></a>

Following is the actual code for the Lambda function underlying the **JavaMacroFunc** example macro\. It iterates over the template fragment included in the response \(be it in string, list, or map format\), looking for the specified target string\. If it finds the specified target string, the Lambda function replaces the target string with the specified replacement string\. If not, the function leaves the template fragment unchanged\. Then, the function returns a map of the expected properties, discussed in detail below, to CloudFormation\.

```
package com.macroexample.lambda.demo;

import java.util.List;
import java.util.ArrayList;
import java.util.HashMap;
import java.util.Map;

import com.amazonaws.services.lambda.runtime.Context;
import com.amazonaws.services.lambda.runtime.RequestHandler;

public class LambdaFunctionHandler implements RequestHandler<Map<String, Object>, Map<String, Object>> {

	private static final String REPLACEMENT = "replacement";
	private static final String TARGET = "target";
	private static final String PARAMS = "params";
	private static final String FRAGMENT = "fragment";
	private static final String REQUESTID = "requestId";
	private static final String STATUS = "status";
	private static final String SUCCESS = "SUCCESS";
	private static final String FAILURE = "FAILURE";
    @Override
    public Map<String, Object> handleRequest(Map<String, Object> event, Context context) {
        // TODO: implement your handler
    	final Map<String, Object> responseMap = new HashMap<String, Object>();
        responseMap.put(REQUESTID, event.get(REQUESTID));
        responseMap.put(STATUS, FAILURE);
    	try {
	        if (!event.containsKey(PARAMS)) {
	        	throw new RuntimeException("Params are required");
	        }
	    	
	        final Map<String, Object> params = (Map<String, Object>) event.get(PARAMS);
	        if (!params.containsKey(REPLACEMENT) || !params.containsKey(TARGET)) {
	        	throw new RuntimeException("replacement or target under Params are required");
	        }
	    	
	    	final String replacement = (String) params.get(REPLACEMENT);
	    	final String target = (String) params.get(TARGET);
	    	final Object fragment = event.getOrDefault(FRAGMENT, new HashMap<String, Object>());
	    	final Object retFragment;
	    	if (fragment instanceof String) {
	    		retFragment = iterateAndReplace(replacement, target, (String) fragment);
	    	} else if (fragment instanceof List) {
	    		retFragment = iterateAndReplace(replacement, target, (List<Object>) fragment);
	    	} else if (fragment instanceof Map) {
	    		retFragment = iterateAndReplace(replacement, target, (Map<String, Object>) fragment);
	    	} else {
	    		retFragment = fragment;
	    	}
	        responseMap.put(STATUS, SUCCESS);
	        responseMap.put(FRAGMENT, retFragment);
	        return responseMap;
    	} catch (Exception e) {
    		e.printStackTrace();
    		context.getLogger().log(e.getMessage());
    		return responseMap;
    	}
    }
    
    private Map<String, Object> iterateAndReplace(final String replacement, final String target, final Map<String, Object> fragment) {
    	final Map<String, Object> retFragment = new HashMap<String, Object>();
    	final List<String> replacementKeys = new ArrayList<>();
    	fragment.forEach((k, v) -> {
    		if (v instanceof String) {
    			retFragment.put(k, iterateAndReplace(replacement, target, (String)v));
    		} else if (v instanceof List) {
    			retFragment.put(k, iterateAndReplace(replacement, target, (List<Object>)v));
    		} else if (v instanceof Map ) {
    			retFragment.put(k, iterateAndReplace(replacement, target, (Map<String, Object>) v));
    		} else {
    			retFragment.put(k, v);
    		}
    	});
    	return retFragment;
    }

    private List<Object> iterateAndReplace(final String replacement, final String target, final List<Object> fragment) {
    	final List<Object> retFragment = new ArrayList<>();
    	fragment.forEach(o -> {
    		if (o instanceof String) {
    			retFragment.add(iterateAndReplace(replacement, target, (String) o));
    		} else if (o instanceof List) {
    			retFragment.add(iterateAndReplace(replacement, target, (List<Object>) o));
    		} else if (o instanceof Map) {
    			retFragment.add(iterateAndReplace(replacement, target, (Map<String, Object>) o));
    		} else {
    			retFragment.add(o);
    		}
    	});
    	return retFragment;
    }
    
    private String iterateAndReplace(final String replacement, final String target, final String fragment) {
    	System.out.println(replacement + " == " + target + " == " + fragment );
    	if (fragment != null AND_AND fragment.equals(target))
    		return replacement;
    	return fragment;
    }
}
```

## Macro example: Lambda function response<a name="macros-example-response"></a>

Following is the mapping that the Lambda function returns to AWS CloudFormation for processing\. The `requestId` matches that sent from CloudFormation, and a `status` value of `SUCCESS` denotes that the Lambda function successfully processed the template fragment included in the request\. In this response, `fragment` contains JSON representing the content to insert into the processed template in place of the original template snippet\.
+ requestId

  `5dba79b5-f117-4de0-9ce4-d40363bfb6ab`
+ status

  `SUCCESS`
+ fragment

  ```
  {
    "Type": "AWS::CloudFormation::WaitConditionHandle"
  }
  ```

## Macro example: Resulting processed template<a name="macros-example-processed"></a>

After CloudFormation receives a successful response from the Lambda function, it inserts the returned template fragment into the processed template\.

Below is the resulting processed template for our example\. The `Fn::Transform` intrinsic function call that referenced the **JavaMacroFunc** macro is no longer included\. The template fragment returned by the Lambda function is included in the appropriate location, with the result that the content `"Type": "$$REPLACEMENT$$"` has been replaced with `"Type": "AWS::CloudFormation::WaitConditionHandle"`\. 

```
{
    "Parameters": {
        "ExampleParameter": {
            "Default": "SampleMacro", 
            "Type": "String"
        }
    }, 
    "Resources": {
        "2a": {
            "Type": "AWS::CloudFormation::WaitConditionHandle"
        }
    }
}
```

## Additional macro examples<a name="template-macros-examples-awslabs"></a>

In addition to this walkthrough in this guide, you can find example macros, including source code and templates, in the [Macros examples](https://github.com/awslabs/aws-cloudformation-templates/tree/master/aws/services/CloudFormation/MacrosExamples/) section of the [Amazon Web Services \- Labs](https://github.com/awslabs) repo on GitHub\. These examples are provided 'as\-is' for instructional purposes\. 