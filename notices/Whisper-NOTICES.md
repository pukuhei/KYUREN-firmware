# whisper.cpp

KYUREN Companion's optional offline transcription backend is intended to use
[`whisper.cpp`](https://github.com/ggml-org/whisper.cpp), pinned to
`f049fff95a089aa9969deb009cdd4892b3e74916` (v1.9.1).

`whisper.cpp` is distributed under the MIT License. KYUREN embeds the
following upstream license text in `THIRD_PARTY_NOTICES.md`.

> MIT License
>
> Copyright (c) 2023-2026 The ggml authors
>
> Permission is hereby granted, free of charge, to any person obtaining a copy
> of this software and associated documentation files (the "Software"), to deal
> in the Software without restriction, including without limitation the rights
> to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
> copies of the Software, and to permit persons to whom the Software is
> furnished to do so, subject to the following conditions:
>
> The above copyright notice and this permission notice shall be included in all
> copies or substantial portions of the Software.
>
> THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
> IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
> FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
> AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
> LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
> OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
> SOFTWARE.

## OpenAI Whisper model weights

The bundled `ggml-small.bin` is a conversion of OpenAI's multilingual Whisper
small model. OpenAI publishes the Whisper model weights under the MIT License;
the model attribution and license text are preserved here separately from the
`whisper.cpp` implementation attribution.

> MIT License
>
> Copyright (c) 2022 OpenAI
>
> Permission is hereby granted, free of charge, to any person obtaining a copy
> of this software and associated documentation files (the "Software"), to deal
> in the Software without restriction, including without limitation the rights
> to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
> copies of the Software, and to permit persons to whom the Software is
> furnished to do so, subject to the following conditions:
>
> The above copyright notice and this permission notice shall be included in all
> copies or substantial portions of the Software.
>
> THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
> IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
> FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
> AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
> LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
> OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
> SOFTWARE.

No model binary is stored in source control. The release app and PKG include
one verified copy in the Companion resource bundle. The release input is the
multilingual `ggml-small.bin` from repository commit
`5359861c739e955e79d9a303bcbc70fb988958b1`, SHA-256
`1be3a9b2063867b937e64e2ec7483364a79917e157fa98c5d94b5c1fffea987b`,
487,601,967 bytes.
