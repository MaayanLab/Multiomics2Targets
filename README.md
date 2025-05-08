# MULTIOMICS2TARGETS: 
### Expression2Kinases & Target Ranger

Currently hosted at: https://multiomics2targets.maayanlab.cloud/


## Getting Started
To run in development:
```bash
# prepare .env file & review
cp .env.example .env
# create and activate python3.8 (or python3.9) virtual environment
python3.9 -m venv venv
source venv/bin/activate
pip install -r requirements.txt
# install relevant R dependencies
R -e "source('setup.R')"
# run in development
appyter main.ipynb
```

## Running locally
To run the Multiomics2Targets app locally first ensure that [Docker](https://www.docker.com/) is installed, and then run the following command:
```bash
docker run --device /dev/fuse --cap-add SYS_ADMIN --security-opt apparmor:unconfined -p 5000:5000 -it maayanlab/x2ktr:0.1.05
```
To receive automatically generated descriptions of the results, you need to provide an [OpenAI API Key](https://openai.com/index/openai-api/) as an environment variable:
```bash
docker run --device /dev/fuse --cap-add SYS_ADMIN --security-opt apparmor:unconfined -p 5000:5000 -e OPENAI_API_KEY=sk-… -it maayanlab/x2ktr:0.1.05
```

