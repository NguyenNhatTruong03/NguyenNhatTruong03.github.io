---
title : "Setup Step Function"
date :  "`r Sys.Date()`" 
weight : 8
chapter : false
pre : " <b> 8. </b> "
---

Step Function will help build a workflow connecting Lambda such as: Lambda-Transcribe, Lambda-Translate, Lambda-Notify created in the previous steps.

## Installation

Go to the Step Function control page and Get started.

![Upload](/images/8.stepfun/n.png)

Select the necessary services.

{{% notice note %}}
Select a service to use and drag it to the *Drag first state here position. For the next services, drag it in and place it below the previous service.

{{% /notice %}}

![Upload](/images/8.stepfun/n1.png)

Detailed settings for each service.

![Upload](/images/8.stepfun/n2.png)

{{% notice info %}}
Select the correct Function name that matches each lambda service you are installing.
{{% /notice %}}

![Upload](/images/8.stepfun/n3.png)

![Upload](/images/8.stepfun/n4.png)

Set time out for worlflow to avoid when the running time exceeds the set time, worlflow will not successfully perform the next tasks in the step function.

![Upload](/images/8.stepfun/n5.png)

Each time running worlflow in a step function, it creates an **Excutions** and if the Execution times out, it can be re-run.

There is a table listing the Executions with information related to the Executions.

![Upload](/images/8.stepfun/n6.png)

Finally, copy the ARN of this step function to call the Step Function using lambda in the next step.

![Upload](/images/8.stepfun/n7.png)