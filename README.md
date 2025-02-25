# xtts-server-macOS
Install xtts-server guide for macOS: https://github.com/daswer123/xtts-api-server && https://docs.sillytavern.app/extensions/xtts/

```
mkdir xtts
cd xtts
mkdir speakers
mkdir output
brew install miniconda
conda create -n xtts
conda activate xtts
conda install python=3.10
pip install xtts-api-server pydub
pip install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cu118
python -m xtts_api_server
```
