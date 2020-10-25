trigger:
- task: Docker@2
  inputs:
    containerRegistry: 'DockerRegistryServiceConnection'
    repository: 'DockerRegistryServiceConnection'
    command: 'buildAndPush'
    Dockerfile: '**/Dockerfile'
- master