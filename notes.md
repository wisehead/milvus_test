#1.下载安装
##1).Download an installation file
`wget https://github.com/milvus-io/milvus/releases/download/v2.0.1/milvus-standalone-docker-compose.yml -O docker-compose.yml`

##2).下载安装，Start Milvus
`sudo docker-compose up -d`

##3).Check the status of the containers.

`sudo docker-compose ps`

##4).Stop Milvus
To stop Milvus standalone, run:
`sudo docker-compose down`

##5).clean data
To delete data after stopping Milvus, run:
`sudo rm -rf  volumes`



#2.Hello World
`wget https://raw.githubusercontent.com/milvus-io/pymilvus/v2.0.1/examples/hello_milvus.py`


#3.PyMilvus 2.0.0

```
python3 -m pip install pymilvus==2.0.1
Verify installation
python3 -c "from pymilvus import Collection"
```

#4.Connect to a Milvus serve
Run `python3` in your terminal to operate in the Python interactive mode.

```
from pymilvus import connections
connections.connect(
  alias="default", 
  host='localhost', 
  port='19530'
)
```

Disconnect from a Milvus server.
`connections.disconnect("default")`



#5.Run Milvus using Python
`python3 hello_milvus.py
`
