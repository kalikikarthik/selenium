#selenium











-------------------------------------------------
ALLHOSTS=`uniquelist $WEBSVRS $BKGDSVR $PROCSVRS $JOBSVRS $SESMSVR`
echo "Disk Use%"
for i in ${ALLHOSTS} ; do
    echo $i - `ssh $i df -h . | tail -1 | awk '{print $5}'`
done
