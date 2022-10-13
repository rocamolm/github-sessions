
## YAML quick notes

```yml
name: CI

on:
  push:
    branches: [ feature/** ]
    tags: 
    - v1 
    paths:
    - 'test/*'

jobs:
  build:
    runs-on: os

    steps:
      - uses: actions
  
  other:
    runs-on: os

    steps:
      - uses: actions
        with:
          secret: ${{ secret.my_secret }}

      - name: simple run
        run: echo Hola
      
      - name: multi run
        run: |
          echo hola
          echo adios
```

| Virtual Environment  | YAML workflow label            |
|----------------------|--------------------------------|
| Windows Server 2019  | windows-latest or windows-2019 |
| Ubuntu 18.04         | ubuntu-latest or Ubuntu-18.04  |
| Ubuntu 16.04         | ubuntu-16.04                   |
| macOS catalina 10.15 | macos-latest or macos-10.15    |

* Linux
    - Red Hat Enterprise Linux 7
    - CentOS 7
    - Oracle Linux 7
    - Fedora 29 or later
    - Debian or later
    - Ubuntu 16.04
    - Linux Mint 18 or later
    - openSUSE 15 or later
    - SUSE Enterprise Linux (SLES) 12
    - SP2 or later
* Windows
    - Windows 7 64-bit
    - Windows 8.1 64-bit
    - Windows 10 64-bit
    - Windows Server 2012 R2 64-bit
    - Windows Server 2016  64-bit
    - Windows Server 2019  64-bit
* MacOS
    - macOS 10.13 (High Sierra) or Later

Webhook 