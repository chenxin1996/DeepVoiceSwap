# DeepVoiceSwap
## 整体思路
1.使用[facefusion](https://github.com/facefusion/facefusion)将原视频的中国面孔替换为外国人面孔。    
2.使用FFmpeg提取中文语音，并使用Whisper将语音转为中文文本。   
3.通过api调用llm，将文本翻译为英文。   
4.使用[kokoro](https://huggingface.co/hexgrad/Kokoro-82M)将中文语音转为英语，并FFmpeg将语音替换回去。   
5.采用latentsync对齐嘴型。   
