# Ado a Ado — voz de IA

Modelos usados pela opção **"Mulher de verdade (IA)"** do modificador de voz do
Ado a Ado. O app baixa estes arquivos sozinho, uma vez, quando alguém escolhe
essa voz. Eles rodam no próprio PC, na placa de vídeo, e nada é enviado para
servidor nenhum.

Este repositório tem só os modelos. Não tem o código do app.

## Arquivos (Release `v1`)

| Arquivo | O que é | Origem | Licença |
|---|---|---|---|
| `hubert.onnx` | Entende o que está sendo falado (sem a voz) | HuBERT base do [RVC](https://github.com/RVC-Project/Retrieval-based-Voice-Conversion-WebUI), convertido para ONNX com pesos em float16 | MIT |
| `voz-leni.onnx` | A voz: fala o conteúdo com a voz da modelo | Treinado com RVC v2 (48 kHz), a partir do modelo base do RVC | MIT |
| `crepe-tiny.onnx` | Mede o tom da fala | [CREPE](https://github.com/marl/crepe) tiny, pesos do [torchcrepe](https://github.com/maxrmorrison/torchcrepe) convertidos para ONNX | MIT |
| `ort-wasm-simd-threaded.asyncify.wasm` | Motor que roda os modelos | [ONNX Runtime Web](https://github.com/microsoft/onnxruntime) 1.31.1 | MIT |

## De onde vem a voz

A voz foi treinada com cerca de 47 minutos da leitora **Leni**, do
[LibriVox](https://librivox.org/reader/2961), lendo *Senhora*, de José de Alencar
([gravação](https://archive.org/details/senhora_0910_librivox)). As gravações
do LibriVox são de domínio público.

A voz gerada é sintética. Não use para se passar pela leitora nem por ninguém.
