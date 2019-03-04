FROM ros:melodic-perception 

RUN apt-get -qq update -y && apt-get -qq install build-essential openssh-client sudo -y --no-install-recommends

RUN mkdir -p /build/ws/

ADD ./ /build/ws/src

SHELL [ "bash", "-c" ]

RUN rosdep update
RUN apt-get install -y $(rosdep install --from-paths -i -y -s /build/ws/src | grep 'apt-get install' | rev | cut -f1 -d' ' | rev | paste -s)
RUN source /opt/ros/$(ls /opt/ros/ | head -n 1)/setup.bash && cd /build/ws/ && catkin_make_isolated
