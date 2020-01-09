Steps for pulling in latest from astronomer airflow:

1. `git remote add upstream git@github.com:astronomer/airflow.git`
1. `git fetch upstream --tags`
1. `git checkout tags/<version you want> -b kairos_<version>`
1. Change `setup.py`:
  - `name='apache-airflow'` -> `name='kastro-apache-airflow`
  - `tenacity` also needs to allow for 5.0.4: `tenacity>=4.12.0, <=5.0.4`
