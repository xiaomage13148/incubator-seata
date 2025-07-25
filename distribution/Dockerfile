FROM java:8

# set label
LABEL maintainer="Seata <seata.io>"

WORKDIR /$BASE_DIR

# ADD FORM distribution
ADD bin/ /seata-server/bin
ADD ext/ /seata-server/ext
ADD target/ /seata-server/target
ADD lib/ /seata-server/lib
ADD conf/ /seata-server/conf
ADD LICENSE /seata-server/LICENSE

# set extra environment
ENV LOADER_PATH="/seata-server/lib"
ENV TZ="Asia/Shanghai"
CMD ["bash","-c","/seata-server/bin/seata-server.sh && tail -f /dev/null"]