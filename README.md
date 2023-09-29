# test-action.yml 
[![test-action.yml](https://github.com/rodrigociro/action-tester/actions/workflows/test-action.yml/badge.svg)](https://github.com/rodrigociro/action-tester/actions/workflows/test-action.yml)
- this repository will use one action:
https://github.com/rodrigociro/create-my-own-action.git

![image](https://github.com/rodrigociro/action-tester/assets/23638418/48456205-1647-4c5c-b157-90055048a72f)

# mutiple-actions-same-repo.yml 
[![CI](https://github.com/rodrigociro/action-tester/actions/workflows/multiple-actions-same-repo.yml/badge.svg)](https://github.com/rodrigociro/action-tester/actions/workflows/multiple-actions-same-repo.yml)
- this repository will use the multiple actions in the same branch differents paths.
- Create workflow with dependency
  
https://github.com/rodrigociro/create-multiple-actions.git

![image](https://github.com/rodrigociro/action-tester/assets/23638418/436ca62f-3212-469b-a903-764dede5e1e4)

# artifacts.yml
[![artifacts](https://github.com/rodrigociro/action-tester/actions/workflows/artifacts.yml/badge.svg)](https://github.com/rodrigociro/action-tester/actions/workflows/artifacts.yml)
- this repository will upload & download an "artefact".
- jobs in parallel

![image](https://github.com/rodrigociro/action-tester/assets/23638418/5779cd04-d427-4be1-98cb-ea6e1a030513)

# 4 jobs in CI
[![CI-4-jobs](https://github.com/rodrigociro/action-tester/actions/workflows/4jobsCI.yml/badge.svg)](https://github.com/rodrigociro/action-tester/actions/workflows/4jobsCI.yml)
- this repository execute 4 jobs.

![image](https://github.com/rodrigociro/action-tester/assets/23638418/031636d9-e7c7-40a9-a9c7-71767c51363f)



# DEVELOPMENT BRANCH TO MASTER BRANCH, VALIDATE CHECK "IS RELEASE"

- YAML when isRelease is equals FALSE

```
name: Controlm-Master branch
on:
  push:
    branches: [ "development-controlm" ]
  pull_request:
    branches: [ "development-controlm" ]

jobs:
  call-controlm-master:
    uses: rodrigociro/tsc-init/.github/workflows/control-m.yml@workflows
    with:
      runner: 'ubuntu-latest'
      isRelease: 'false'
    secrets: inherit
```


![image](https://github.com/rodrigociro/action-tester/assets/23638418/812f82b6-4acd-4680-ae39-f892ed6e0acd)



- YAML when isRelease is equals TRUE

```
name: Controlm-Master branch
on:
  push:
    branches: [ "development-controlm" ]
  pull_request:
    branches: [ "development-controlm" ]

jobs:
  call-controlm-master:
    uses: rodrigociro/tsc-init/.github/workflows/control-m.yml@workflows
    with:
      runner: 'ubuntu-latest'
      isRelease: 'true'
    secrets: inherit
```


![image](https://github.com/rodrigociro/action-tester/assets/23638418/832acbbd-9ba9-43f4-a321-f24eb633191c)



