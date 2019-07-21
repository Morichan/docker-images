FROM gradle:5.5-jdk11
LABEL maintainer <Morichan morichan.keisuke.mori@gmail.com>
LABEL io.github.morichan.retuss.image.source https://github.com/morichan/retuss.git

ENV DISPLAY host.docker.internal:0.0

RUN apt-get update && \
    apt-get install -y --no-install-recommends \
      openjfx \
    && \
    rm -rf /var/lib/apt/lists/*

RUN git clone https://github.com/morichan/retuss.git

WORKDIR retuss

# 4 tests failed
# RUN gradle build

CMD ["gradle", "run"]
