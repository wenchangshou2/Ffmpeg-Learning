Ffmpeg在Linux下的编译步骤 \
   一、下载FFmpeg \
       git clone https://git.ffmpeg.org/ffmpeg.git \
   二、安装依赖包 \
       sudo apt-get update \
       sudo apt-get upgrade \
       sudo apt-get update -qq && sudo apt-get -y install autoconf automake build-essential cmake git \
       libass-dev libfreetype6-dev libsdl2-dev libtheora-dev libtool libva-dev libvdpau-dev libvorbis-dev \
       libxcb1-dev libxcb-shm0-dev libxcb-xfixes0-dev mercurial pkg-config texinfo wget zlib1g-dev
       
   sudo apt-get install nasm \
   sudo apt-get install yasm \
   sudo apt-get install libx264-dev \
   sudo apt-get install libx265-dev libnuma-dev -y \
   sudo apt-get install libvpx-dev \
   sudo apt-get install libfdk-aac-dev\
   sudo apt-get install libmp3lame-dev \
   sudo apt-get install libopus-dev \
   sudo apt-get install libspeex-dev -y

 三、配置Ffmpeg \
 cd ffmpeg/ \
 执行\
 ./configure --prefix=/usr/local/ffmpeg --enable-gpl --enable-nonfree --enable-libfdk-aac --enable-libx264 --enable-libx265 --enable-filter=delogo --enable-debug --disable-optimizations --enable-opengl --enable-libspeex --enable-libopus --enable-libmp3lame --enable-shared --enable-pthreads

 四、编译安装 \
 make \
 sudo make install

 五、查看FFMpeg版本是否安装成功 \
 ffmpeg -version



simplest_ffmpeg_streamer工程包含如下部分 \
 最简单的基于FFmpeg的推流器（以推送RTMP为例) \
 最简单的基于FFMPEG的推流器附件：收流器

 simplest_ffmpeg_format工程包含如下部分 \
 最简单的基于FFmpeg的封装格式处理：视音频分离器简化版（demuxer-simple）\
 最简单的基于FFmpeg的封装格式处理：视音频分离器（demuxer）\
 最简单的基于FFmpeg的封装格式处理：视音频复用器（muxer）\
 最简单的基于FFMPEG的封装格式处理：封装格式转换（remuxer）

 simplest_ffmpeg_demo工程包含如下部分 \
 1 Ffmpeg文件目录基本操作
 2 从MP4中分离出h264视频和aac音频

