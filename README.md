# AR Cut Paste api

## Setup

```bash
virtualenv -p python3.7 venv
source venv/bin/activate
pip install -r requirements.txt
```

## Run

Replace `192.168.0.12` by your Photoshop remote connection host.

Replace `49494` by your Photoshop remote connection port (49494 is default on photoshop settings).

Replace `123456` by your Photoshop remote connection password.

Replace `http://X.X.X.X` by your basnet connection host.

The `basnet_service_host` is optional (only needed if you've deployed the service
on a platform using an ingress gateway such as Knative / Cloud Run).

```python
python src/main.py \
    --photoshop_host="192.168.0.12" \
    --photoshop_port=49494 \
    --photoshop_password=123456 \
    --basnet_service_ip="http://X.X.X.X" \
    --basnet_service_host="basnet-http.default.example.com"
```
