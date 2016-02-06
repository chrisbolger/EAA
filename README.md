# EAA
Enterprise Application Architecture
#!/bin/bash

# store the number of process

# into variable cnt
cntall=`ps -ef | wc -l`
echo "total number $cntall"

#total number of processes
cntroot=`ps -ef | grep root | wc -l`
echo "total number of root processess $cntroot"

#
# bash integer equality operator
cntnonroot=`expr $cntall - $cntroot`
echo "Count $cntnonroot"
#
if [ "$cntroot" -gt "$1" ];
then
  echo "number of processes exceeded". /home/eaauser/eaa/logs/log2.txt
fi

