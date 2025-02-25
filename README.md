# xtts-server-macOS
Install xtts-server guide for macOS: https://github.com/daswer123/xtts-api-server && https://docs.sillytavern.app/extensions/xtts/

# Chromium based browser
use chromium based browsers as other browsers seem to have issues with this.

```
mkdir xtts
cd xtts
mkdir speakers
mkdir output
brew install miniconda
conda init zsh
source ~/.zshrc
conda create -n xtts
conda activate xtts
conda install python=3.10
pip install xtts-api-server pydub
pip install torch==2.1.1 torchaudio==2.1.1 torchvision --index-url https://download.pytorch.org/whl/cu118
python -m xtts_api_server --streaming-mode-improve
```
# Docker Build
Need to build for arm64:
```
https://docs.docker.com/engine/install/ (Instal Docker Engine)
git clone https://github.com/daswer123/xtts-api-server.git
cd docker
docker build --platform linux/arm64 -t xtts-api-server-arm .
python -m xtts_api_server --streaming-mode --use-cache -ms local -d cpu
```
