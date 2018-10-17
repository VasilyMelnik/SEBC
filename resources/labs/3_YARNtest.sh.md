#!/bin/sh
# Confirm the path values given below correspond to your installation

MR=/opt/cloudera/parcels/CDH/lib/hadoop-0.20-mapreduce
HADOOP=/opt/cloudera/parcels/CDH/bin

# Mark start of the loop
echo Testing loop started on `date`

# Mapper containers
for i in 4 8
do
   # Reducer containers
   for j in 1 2 
   do                 
      # Container memory
      for k in 512 1024 
      do          
         echo Mapper count $i
		 echo Reducer count $j
         echo Container memory $k
         # Set mapper JVM heap 
         MAP_MB=`echo "($k*0.8)/1" | bc` 
         echo Mapper memory $MAP_MB	
         # Set reducer JVM heap 
         RED_MB=`echo "($k*0.8)/1" | bc` 
         echo Reducer memory $RED_MB
        
		
        time hadoop jar ${MR}/hadoop-examples.jar teragen \
                     -Dmapreduce.job.maps=$i \
                     -Ddfs.replication=1 \
                     -Dmapreduce.map.memory.mb=$k \
                     -Dmapreduce.map.java.opts.max.heap=$MAP_MB \
                     -Dmapreduce.reduce.memory.mb=$k \
                     -Dmapreduce.reduce.java.opts.max.heap=$RED_MB \
                     100000000 /results/tg-10GB-${i}-${j}-${k} 1>teragen_${i}_${j}_${k}.out 2>teragen_${i}_${j}_${k}.err                       
        echo teragen time
       time hadoop jar $MR/hadoop-examples.jar terasort \
                     -Dmapreduce.job.maps=$i \
                     -Ddfs.replication=1 \
                     -Dmapreduce.job.reduces=$j \
                     -Dmapreduce.map.memory.mb=$k \
                     -Dmapreduce.map.java.opts.max.heap=$MAP_MB \
                     -Dmapreduce.reduce.memory.mb=$k \
                     -Dmapreduce.reduce.java.opts.max.heap=$RED_MB \
                  /results/tg-10GB-${i}-${j}-${k}  \
                     /results/ts-10GB-${i}-${j}-${k} 1>terasort_${i}_${j}_${k}.out 2>terasort_${i}_${j}_${k}.err                         
        echo terasort time  
        $HADOOP/hadoop fs -rm -r -skipTrash /results/tg-10GB-${i}-${j}-${k}                         
        $HADOOP/hadoop fs -rm -r -skipTrash /results/ts-10GB-${i}-${j}-${k}                 
      done
   done
done

echo Testing loop ended on `date`
