## Project Overview

This project is an extension of PaddleSpeech's TTS (Text-to-Speech) streaming service, supporting mixed Chinese and English TTS as well as speaker ID selection. With our extension, users can utilize text-to-speech functionalities more flexibly.

## File Description

This project includes the following main files:

1. **pretrained_models.py**: This is a modified model list file sourced from the PaddleSpeech library. You need to replace this file in your PaddleSpeech installation directory.

2. **tts_engine**: This is another modified file that should be replaced in a specific PaddleSpeech path to ensure the smooth operation of the streaming TTS service.

## Usage Instructions

### Install NLTK DATA
1、make sure you have NLTK support, and you need install necessary data operator
```python
ntlk.down('averaged_perceptron_tagger')
```

### Replace Files

1. Find your PaddleSpeech installation path by using the following command:
   ```bash
   pip show paddlespeech
   ```
   
2. Replace the `pretrained_models.py` file in the following path:
   ```
   <your PaddleSpeech installation location>/site-packages/paddlespeech/resource/
   ```

3. Replace the `tts_engine` file in the following path:
   ```
   <your PaddleSpeech installation location>/site-packages/paddlespeech/server/engine/tts/online/onnx/
   ```

### Run Streaming TTS Service

Use PP-TTS_mix_streaming's `tts_online_application` to run your streaming TTS service. You can start it with the following command:
```bash
python -m paddlespeech.server    ./tts_online_application.yaml
```

## Environment Requirements

Ensure your environment meets the following requirements:

- PaddleSpeech version: 1.2.0
- PaddlePaddle version: 2.3.2

For more environment configurations, please refer to the `requirements.txt` file.

## Contributing

Feel free to submit Issues or Pull Requests to improve and enhance the project. Your contributions are highly appreciated!

## License

This project is licensed under the Apache License 2.0. For more details, please refer to the license file.
