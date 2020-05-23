# Introduction to Pivotal Application Service (PAS) 101

This tutorial is a simplified version of the [one](https://tanzu.vmware.com/tutorials/getting-started/introduction) documented by [Pivotal](https://tanzu.vmware.com/).

## Initial Setup

- Ensure you have a PAS account.

- Download and install the [Cloud Foundry Command Line Interface](https://github.com/cloudfoundry/cli#installers-and-compressed-binaries) (cf CLI).

- Test that the cf CLI works:
  > `cf help`
  
- Download the app with git:
  > `git clone https://github.com/cloudfoundry-samples/cf-sample-app-spring.git`
  
- Navigate to the app directory:
  > `cd cf-sample-app-spring`
  
## 15-minute tutorial for learning PAS app deployment concepts

- Open a Terminal windows.

- Navigate to the app directory:
  > `cd \Documents\apps\cf-sample-app-spring-master\cf-sample-app-spring-master`
  
- Sign in to PAS:
  > `cf login -a https://api.sys.nonprod.platform.your-company.com --sso`
  
- Push the app to PAS:
  > `cf push`
  
- Open the sample app in your browser.

- View a snapshot of recent logs:
  > `cf logs cf-demo --recent`
  
- Increase the number of app instances:
  > `cf scale cf-demo -i 2`
  
- Check the status of the app:
  > `cf app cf-demo`
  
- List the available services in the Marketplace:
  > `cf marketplace`
  
- List the available MySQL plans:
  > `cf marketplace -s p.mysql`
  
- Create a service instance with the free plan:
  > `cf create-service p.mysql db-small cf-demo-db`
  
- Check the status of the service:
  > `cf services`
  
- Bind the newly created service to the app:
  > `cf bind-service cf-demo cf-demo-db`
  
- Restage the app:
  > `cf restage cf-demo`
  
- Verify the new service is bound to the app:
  > `cf services`

## Topics to explore

- [PAS Concepts](https://docs.pivotal.io/platform/application-service/2-9/concepts/index.html)

- [Explore PAS/PKS Services](https://network.pivotal.io/)

- [The Open Service Broker API project](https://www.openservicebrokerapi.org/)

- [Starting, Restarting, and Restaging Apps](https://docs.run.pivotal.io/devguide/deploy-apps/start-restart-restage.html)

- [Config Server](https://docs.run.pivotal.io/spring-cloud-services/config-server/index.html)

- [Blue-green deployment](https://docs.pivotal.io/platform/application-service/2-9/devguide/deploy-apps/blue-green.html)

- [App Logging in CF](https://docs.cloudfoundry.org/devguide/deploy-apps/streaming-logs.html)

- [.NET Core Cookbook](https://dotnet-cookbook.cfapps.io/core/)

- [Planning Orgs and Spaces](https://docs.cloudfoundry.org/concepts/orgs-and-spaces.html)

- [Pivotal Template App Migration Dojo Cookbook Site](https://github.com/vmwarepivotallabs/modernization-cookbook-template)

- [A pattern language for microservices](https://microservices.io/patterns/index.html)

