Launch Docker as below:

docker run --rm -p 10000:8888  -p 6006-6015:6006-6015 -e JUPYTER_ENABLE_LAB=yes -e GRANT_SUDO=yes -v "$PWD":/home/jovyan/work kushukla/jupyter-r-tensorflow start-notebook.sh --NotebookApp.token=''



# Here is how rJava to be included in the Jupyter:
```
import rpy2.rinterface
%load_ext rpy2.ipython
%R dyn.load('/usr/lib/jvm/java-8-openjdk-amd64/jre/lib/amd64/server/libjvm.so')
%R install.packages(c('RJDBC', 'feather', 'tidyverse'), repos='http://cran.us.r-project.org')
%R library(RJDBC)
%R library(tidyverse)
```
