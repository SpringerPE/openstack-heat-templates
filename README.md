# OpenStack Orchestration

About Heat
==========

The mission of the OpenStack Orchestration program is to create a human- and machine-accessible 
service for managing the entire lifecycle of infrastructure and applications within OpenStack clouds.

Heat is the main project in the OpenStack Orchestration program. It implements an orchestration 
engine to launch multiple composite cloud applications based on templates in the form of text 
files that can be treated like code. A native Heat template format is evolving, but Heat also 
endeavours to provide compatibility with the AWS CloudFormation template format, so that many 
existing CloudFormation templates can be launched on OpenStack. 

Heat provides both an OpenStack-native ReST API and a CloudFormation-compatible Query API.


About Hot
=========

HOT is a new template format meant to replace the Heat CloudFormation-compatible format (CFN) 
as the native format supported by the Heat over time. 

A detailed specification of HOT can be found at Heat Orchestration Template (HOT) Specification.

http://docs.openstack.org/developer/heat/template_guide/


Using the templates
===================

Load the template in Project > Orchestration > Stacks > Launch Stack. You have to choose the file 
and provide a name for the new Stack and the rest of parameters. After that, the stack will be 
created, you can see the output and resources by clicking in the name.


Be patient, it can take 5 minutes or more to complete all the tasks!


Moreover, you can create it by using the command line, for example:

```
$ heat stack-create chef-server --template-file=chef-server.yaml --parameters="ssh_key_name=jriguera"

$ heat stack-list

$ heat stack-show chef-server
    
```


