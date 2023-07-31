# so-vits-svc-5.0

## Setup Environment

Install PyTorch and project dependencies
```
pip install -i https://pypi.tuna.tsinghua.edu.cn/simple -r requirements.txt
```

## Inference

Export inference model: text encoder, Flow network, Decoder network
```
python svc_export.py --config configs/base.yaml --checkpoint_path chkpt/sovits5.0/***.pt
```

Run svc_inference.py file.
```
python svc_inference.py --config configs/base.yaml --model sovits5.0.pth --spk ./data_svc/singer/your_singer.spk.npy --wave test.wav --shift 0
```

- ```--spk``` path to speaker file
+ ```--wave``` path to wave file
