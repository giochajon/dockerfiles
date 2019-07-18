from ubuntu:18.04
RUN apt-get update 
RUN apt-get install -y curl 
RUN apt-get install ocl-icd-libopencl1 
RUN curl -L -o MinerGate.deb "https://drive.google.com/uc?export=download&id=11L9r4eOFYH7djK3Z5llTy5VrMlRWZBmM"
RUN dpkg -i MinerGate.deb
#CMD setsid minergate-cli -u giochajon@gmail.com --xmr >> ~/mining.txt
RUN /bin/bash
