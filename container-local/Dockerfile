FROM python:3.11-bookworm

# Time zone
ENV TZ=Asia/Tokyo
RUN ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && echo $TZ > /etc/timezone

# Update
RUN apt-get update && apt-get install -y \
    wget curl

# Open Interpreter
RUN pip install open-interpreter
RUN pip install numpy matplotlib pandas

WORKDIR /root
