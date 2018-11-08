FROM nvidia/cudagl:9.0-runtime-centos7

MAINTAINER "Adib Afandi bin Abdullah <fendy90.oscura@gmail.com>"

RUN yum install -y perl csh make && \
    curl https://www.ks.uiuc.edu/Research/vmd/vmd-1.9.4/files/alpha/vmd-1.9.4a12.bin.LINUXAMD64-CUDA9-OptiX411-OSPRay140.opengl.tar.gz -o vmd.tar.gz && \
    tar -xzf vmd.tar.gz && \

    cd vmd-1.9.4a12 && ./configure LINUXAMD64 && \
    cd src && make install && \

    yum install -y libXinerama libXi libGL && \
    yum clean all && rm -rf /var/cache/yum/*

CMD vmd
