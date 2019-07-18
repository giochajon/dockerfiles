from ubuntu:18.04
RUN apt-get update
RUN apt-get install build-essential cmake libuv1-dev libmicrohttpd-dev libssl-dev git -y
RUN git clone https://github.com/xmrig/xmrig.git
RUN cd xmrig
RUN mkdir build
RUN cd build
RUN cmake ..
RUN make

#setsid ./xmrig -o ca.minexmr.com:4444 -u 49Yj8rCSpvUWADijKUWpQyMYKQ66bqx2ZTWRE95P3zKWTGkzS5xyGkWb5AJ3eZdMM68TqoShCfd5QMfZkM4LHdk91hA6yHj.smallcomp29000 >> ./xmrigstatlog.txt
#docker build --tag=xmrminer .
#docker run -it --rm xmrminer
