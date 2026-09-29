FROM osrf/ros:jazzy-desktop

ENV DEBIAN_FRONTEND=noninteractive

# Development tools
RUN apt-get update && apt-get install -y \
    build-essential \
    cmake \
    git \
    curl \
    wget \
    vim \
    nano \
    python3-pip \
    python3-rosdep \
    python3-colcon-common-extensions \
    gdb \
    && rm -rf /var/lib/apt/lists/*

# Initialize rosdep
RUN rosdep init || true

WORKDIR /ros2_ws

# Automatically source ROS 2 for every shell
RUN echo "source /opt/ros/jazzy/setup.bash" >> /root/.bashrc

CMD ["bash"]
