# scenerio-1
                                        ####### SCENARIO-1 ###########
1) The build should trigger as soon as anyone in the dev team checks in code to master branch.
Solution:: We can triggert a perticular branch/branches whenever we have a new commit to those branches using "trigger" option in Azure Devops.

2) There will be test projects which will create and maintained in the solution along the Web and API. The
trigger should build all the 3 projects - Web, API and test.The build should not be successful if any test fails.
Solution:: It seems we have 3 different projects here. So I kept each project in a different folder like src/app1, src/app2, src/app3.
So that I created 3 diiferent jobs for each project. Each job fails if there are any errors in those test cases/building steps since I disabled "continueOnError" option.

3) The deployment of code and artifacts should be automated to Dev environment.
Solution:: I know Ansible and chef very well. So I use either of them here to configure the artifacts in Dev environment using these tools.

4) Upon successful deployment to the Dev environment, deployment should be easily promoted to QA
and Prod through automated process.
Solution:: If the deployment is successful, we can also automate the process using Ansible/chef to QA/Prod Env.

5) The deployments to QA and Prod should be enabled with Approvals from approvers only.
Solution:: If we want to deploy those builds to Prod/QA env, we can use any configuration tools here.


