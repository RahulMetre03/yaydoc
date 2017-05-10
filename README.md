# yaydoc

[![Join the chat at https://gitter.im/fossasia/yaydoc](https://badges.gitter.im/fossasia/yaydoc.svg)](https://gitter.im/fossasia/yaydoc?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

> Docs! Yay!
# Usage
- generate github personal token by following this guide (https://help.github.com/articles/creating-a-personal-access-token-for-the-command-line/)
- set the following environment variable in the travis       
     1) AUTHOR      (author of the repository)
     2) DOCPATH     (path of the documentation)
     3) GITURL      (https url not ssh)
     4) PROJECTNAME (project name)
     5) VERSION     (version of project)



 your git url should look like this
  ```shell
  https://<username>:<token>@github.com/<organisation or username>/<repname>
  ```
- configure the travis as follow
```yml
language: python
python:
  - 3.5

script:
- wget https://raw.githubusercontent.com/fossasia/yaydoc/master/generate.sh
- chmod +x ./generate.sh
- pip install sphinx
- ./generate.sh
```
