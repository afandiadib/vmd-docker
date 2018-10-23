FROM nvidia/cudagl:9.0-runtime-centos7

MAINTAINER "Adib Afandi bin Abdullah <fendy90.oscura@gmail.com>"

RUN yum install -y perl csh make && \
    curl https://www.ks.uiuc.edu/Research/vmd/vmd-1.9.3/files/final/vmd-1.9.3.bin.LINUXAMD64-CUDA8-OptiX4-OSPRay111p1.opengl.tar.gz -o vmd-1.9.3.bin.LINUXAMD64-CUDA8-OptiX4-OSPRay111p1.opengl.tar.gz && \
    tar -xzf vmd-1.9.3.bin.LINUXAMD64-CUDA8-OptiX4-OSPRay111p1.opengl.tar.gz && \

    cd vmd-1.9.3 && ./configure LINUXAMD64 && \
    cd src && make install && \

    yum install -y libXinerama libXi libGL && \
    yum clean all && rm -rf /var/cache/yum/*

CMD vmd
