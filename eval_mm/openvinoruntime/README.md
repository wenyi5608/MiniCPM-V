# OpenVINO™ backend on MiniCPM-V
* Step 1. create python environment

``` sh
conda create -n ov_minicpmv2 python=3.10
conda activate ov_minicpmv2
pip install -r requirements.txt
pip install --pre -U openvino openvino-tokenizers --extra-index-url https://storage.openvinotoolkit.org/simple/wheels/nightly
```

* Step2. Convert minicpmv2 model to OpenVINO™ IR(Intermediate Representation).
``` sh
python ov_convert_minicpm-v-2.py -m /path/to/minicpmv2 -o /path/to/minicpmv2_ov
```

* Step3. Testing
``` sh
python ov_minicpm-v2-test.py -m /path/to/minicpmv2_ov -pic /path/to/airplane.jpeg -p 描述画面内容
```

