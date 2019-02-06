FROM cyberdojofoundation/clang
LABEL maintainer=jon@jaggersoft.com

RUN apt-get update \
 && apt-get --yes install \
 cmake \
 unzip \
 wget

RUN wget https://github.com/cgreen-devs/cgreen/archive/master.zip
RUN unzip master.zip
RUN cd cgreen-master
RUN mkdir build
RUN cd build
RUN cmake ..
RUN make
RUN make install

#ADD install.sh /
#RUN /install.sh && rm -f /install.sh

COPY red_amber_green.rb /usr/local/bin
