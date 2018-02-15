FROM openshift/jenkins-slave-base-centos7

# This image is used to run jenkins-jobs and PAPR itself.

RUN yum install -y epel-release && \
    yum install -y python2-pip && \
    yum clean all -y && \
    rm -rf /var/cache/yum && \
    pip install jenkins-job-builder

# we don't need root; we run as the `jenkins` user created
# in the base image.
USER 1001
