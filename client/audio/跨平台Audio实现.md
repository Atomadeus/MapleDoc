
冒险岛音频资源的存放位置在**Sound.wz**当中，通过指定路径（Bgm00.img/SleepyWood）可以得到对应音频的二进制信息(资源读取参考[WzTools](https://github.com/flwmxd/WzTools)的实现)

# 基本信息

在冒险岛中，音频为以下的数据结构
<br>**int unknown**
<br>**int size** 当前音频的长度
<br>**int unknown1**
<br>**byte * 51 header**
<br>**byte type** (type == 12时 存的pcm二进制数据 否则为mp3数据)

在header部分存放当前音频的基本信息
<br>1.采样率 simple
<br>2.位数 rate
<br>3.通道数 channel

# 整体架构

![View Pic](https://github.com/flwmxd/flwmxd.github.io/blob/master/img/audio.png)

### 技术选型
###### Android平台使用OpenSLES播放
###### iOS平台使用[openal](www.openal.org/)播放
###### 桌面平台使用[Bass](http://www.un4seen.com/)

***
OpenAL 和 OpenSLES 播放声音之前需要给定当前声音的
<br>1.采样率 simple
<br>2.位数 rate
<br>3.通道数 channel

Android 
 ``` cpp
		SLDataFormat_PCM dataSourceFormat = {
		   SL_DATAFORMAT_PCM, pcmData.numChannels, pcmData.sampleRate * 1000,
			pcmData.bitsPerSample, pcmData.containerSize,
			pcmData.channelMask, pcmData.endianness
		};
```

iOS 
 ``` cpp
		ALenum format = 0;
		alGenBuffers(1, &bufferID);
        switch (data.numChannels)
        {
            case 1:
                if (data.bitsPerSample == 8)
                    format = AL_FORMAT_MONO8;
                    else
                        format = AL_FORMAT_MONO16;
                        break;
            case 2:
                if (data.bitsPerSample  == 8)
                    format = AL_FORMAT_STEREO8;
                    else
                        format = AL_FORMAT_STEREO16;
                        break;
        }

		alBufferData(bufferID, format, data.pcmBuffer->data(), data.pcmBuffer->size(), data.sampleRate);
		if ((ret = alGetError()) != AL_NO_ERROR)
		{
			Log("error alBufferData %x", ret);
		}
		alSourceQueueBuffers(outSourceId, 1, &bufferID);
        alSourcei(outSourceId, AL_LOOPING,  loop?AL_TRUE:AL_FALSE);
		play();
```

***


### 音乐类型

###### 1.背景音乐
###### 2.音效（主要是技能，吃药等出发的短时音频）

其中对于音效可以做缓存处理（使用[Lru](https://github.com/flwmxd/flwmxd.github.io/blob/master/client/cache/LruCache.md)算法）


### 解码相关

音频播放属于C/S 模式，音频的具体播放器抽象成了Server，因此投递数据给Server之前需要对原始Mp3进行解码才能播放


![View Pic](https://github.com/flwmxd/flwmxd.github.io/blob/master/img/audio_decoder.png)

