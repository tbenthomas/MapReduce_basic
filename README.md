# MapReduce

This repo provides two examples and a script to easily define and run mapper and reducer functions against Hadoop MapReduce.

Generally speaking, on the top level there are folders that must contain:

* mapper.py
* reducer.py
* sample directory with data to be copied in hdfs within docker container

*ENSURE THAT *.py FILES HAVE `chmod +x` PERMISSIONS*
(This is hadoop requirement)

## Usage

1. Download this repo
2. CD into this repo
3. Run the following

```
docker run -v $(pwd):/usr/local/hadoop/py -it sequenceiq/hadoop-docker:2.7.1 /usr/local/hadoop/py/py_runner.sh grep
```

expected output:

```
foo	6
quux	4
```

