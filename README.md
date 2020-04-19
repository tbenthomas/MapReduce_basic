# MapReduce
This repo is a clone of https://github.com/mottaquikarim/STA9760_MapReduce . In this repo the mapper.py in the grep folder has been edited to allow user input of regex expressions to our mapper function, allowing the user to mange any type of search in their mapreduce job. 

This repo provides 
## Usage

1. Download this repo
2. CD into this repo
3. Run the following

```
docker run \
  -v $(pwd):/usr/local/hadoop/py \
  -it sequenceiq/hadoop-docker:2.7.1 \
  /usr/local/hadoop/py/py_runner.sh grep {pattern}

The {pattern should be replace by any kind of pattern or valid regular expression. 

Example use:
docker run \
  -v $(pwd):/usr/local/hadoop/py \
  -it sequenceiq/hadoop-docker:2.7.1 \
  /usr/local/hadoop/py/py_runner.sh grep oo
  
Expected output:
foo	6

Another example:
docker run \
  -v $(pwd):/usr/local/hadoop/py \
  -it sequenceiq/hadoop-docker:2.7.1 \
  /usr/local/hadoop/py/py_runner.sh grep q+
  
Expected output:
quux	4

```
```
