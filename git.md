
## Retrieving one or more file / folder from a Git repository
```
$ mkdir repo
$ cd repo
$ git init
$ git config core.sparseCheckout true
$ git remote add -f origin https://scm.domain.com/<group_name>/<project_name>.git
$ echo "playbooks/apache/" >> .git/info/sparse-checkout
$ echo "roles/tomcat/instance/tasks/instance.yml" >> .git/info/sparse-checkout
$ git pull origin master
```
