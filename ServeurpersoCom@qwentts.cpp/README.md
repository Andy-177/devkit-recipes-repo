# ServeurpersoCom qwentts.cpp
模型推荐使用`qwen-talker-1.7b-voicedesign-Q8_0.gguf`和`qwen-tokenizer-12hz-Q8_0.gguf`

下载好这两个模型文件后放到models文件夹里就行，没有请自行创建

```
echo "你好，这是设计出来的声音。" | qwen-tts.exe --model models/qwen-talker-1.7b-voicedesign-Q8_0.gguf --codec models/qwen-tokenizer-12hz-Q8_0.gguf --instruct "gender: Male. age: Middle-aged. pitch: Low. speed: Slow. texture: Warm and smooth. tone: Friendly." -o output.wav
```
