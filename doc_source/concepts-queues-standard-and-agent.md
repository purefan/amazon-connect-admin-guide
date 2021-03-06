# Queues: Standard and Agent<a name="concepts-queues-standard-and-agent"></a>

There are two types of queues:
+ **Standard queues**: This is where contacts wait before they are routed to and accepted by agents\.
+ **Agent queues**: These queues are created automatically when you add an agent to your contact center\.

  Contacts are only routed to agent queues when explicitly sent there as part of a contact flow\. For example, you might route contacts to a specific agent who's responsible for certain customer issues, such as billing or premium support\. Or you might use agent queues to route to an agent's voice\-mail\. 

Contacts waiting in agent queues are higher priority than contacts waiting in standard queues\. Contacts in agent queues have the highest priority and zero delay: 
+ Highest priority: If there's another contact in the basic queue, Amazon Connect chooses to give the agent the contact from the agent queue first\.
+ Zero delay: If the agent is available, the contact immediately gets routed to them\.

In a [real\-time metrics report](create-real-time-report.md), you can monitor how many contacts are in standard queues and agent queues\. The following image shows a sample real\-time metrics Queues report where an Agents table and Agents queues table have been added\. 

![\[Image NOT FOUND\]](http://docs.aws.amazon.com/connect/latest/adminguide/images/rtm-standard-and-agent-queues.png)

When an agent gets a contact from a standard queue, the contact never appears in the agent queue\. It just goes directly to the agent\. 

**Tip**  
The metrics APIs don't support agent queues\.