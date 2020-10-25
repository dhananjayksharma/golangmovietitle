trigger:
- task: Docker@2
  inputs:
    containerRegistry: 'DockerRegistryServiceConnection'
    repository: 'DockerRegistryServiceConnection'
    command: 'buildAndPush'
    Dockerfile: '**/Dockerfile'
- master



trigger:
- task: AzureCLI@2
  inputs:
    azureSubscription: 'Free Trial(ef3ad59f-4873-47ba-921a-633a05520850)'
    scriptType: 'bash'
    scriptLocation: 'scriptPath'
    scriptPath: 'azureConnectionSubscription'
- master


