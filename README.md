Launch Docker as below:

docker run --rm -p 10000:8888  -p 6006-6015:6006-6015 -e JUPYTER_ENABLE_LAB=yes -e GRANT_SUDO=yes -v "$PWD":/home/jovyan/work kushukla/jupyter-r-tensorflow start-notebook.sh --NotebookApp.token=''
