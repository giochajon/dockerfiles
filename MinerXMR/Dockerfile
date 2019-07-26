from ubuntu:18.04
RUN apt-get update && apt-get install build-essential cmake libuv1-dev libmicrohttpd-dev libssl-dev git -y
RUN git clone https://github.com/xmrig/xmrig.git \
&& cd /xmrig \
&& mkdir /xmrig/build \
&& cd /xmrig/build \
&& /usr/bin/cmake ../ \
&& /usr/bin/make 

#setsid /xmrig/build/xmrig -o ca.minexmr.com:4444 -u 49Yj8rCSpvUWADijKUWpQyMYKQ66bqx2ZTWRE95P3zKWTGkzS5xyGkWb5AJ3eZdMM68TqoShCfd5QMfZkM4LHdk91hA6yHj.smallcomp29000 >> /xmrig/xmrigstatlog.txt
#docker build --tag=xmrminer .
#docker run -it --rm xmrminer
