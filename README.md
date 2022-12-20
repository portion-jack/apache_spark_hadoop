# Apache Spark Hadoop setting

```
.
├── README.md
├── codes
│   ├── 01_pyspark.ipynb
│   ├── 03_rdd.ipynb
│   ├── 04_rdd.ipynb
│   ├── 05_rdd.ipynb
│   ├── 06_sparksql.ipynb
│   ├── pyspark_check.ipynb
│   └── team2_hw.ipynb
├── concepts
│   └── concepts.md
└── pyspark_check.ipynb

2 directories, 10 files

```

### Working on Docker

```
ver_1
docker search jupyter/all-spark-jupyter
docker pull jupyter/all-spark-jupyter
docker run \
--name spark_jupyter \
-it \
--mount type=bind,source=/Users/jack/Desktop/things/my_docker_pj,target=/root/main \
-p 8888:8888 \
jupyter/all-spark-jupyter
```

```
ver2


ipython

from notebook.auth import passwd
passwd()
Enter passwd
verify passwd


> .jupyter/jupyter_notebook_config.py
c = get_config()
c.NotebookApp.ip='localhost'
c.NotebookApp.open_browser=False
c.NotebookApp.password= 'argon2:$argon2id$v=19$m=10240,t=10,p=8$BWbO0rB7S4/JK9mKgkSu5g$yOc7VN2IxQq3G86uscF9h5XMNRhk8jg16763/wiQfCA'
c.NotebookApp.password_required=True
c.NotebookApp.port=8080
c.NotebookApp.iopub_data_rate_limit=1.0e10
c.NotebookApp.terminado_settings={'shell_command': ['/bin/bash']}  # terminal을 bash로 실행

.bashrc 
path setting

###
export HADOOP_HOME=/root/main/hadoop-2.10.2
export PATH=$PATH:$HADOOP_HOME/bin
export JAVA_HOME=/usr/lib/jvm/java-1.8.0-openjdk-amd64


export PYSPARK_PYTHON=python3
export PYTHONPATH=$PYTHONPATH:/root/main/spark-3.3.1-bin-hadoop2/python
export PYTHONPATH=$PYTHONPATH:/root/main/spark-3.3.1-bin-hadoop2/python/lib/py4j-0.10.9.5-src.zip
export SPARK_HOME=/root/main/spark-3.3.1-bin-hadoop2
###

to run jupyter and do open in local

jupyter notebook --ip 0.0.0.0 --allow-root
=> localhost:8888
```
