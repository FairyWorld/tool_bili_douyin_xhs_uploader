# bili_douyin_xhs_uploader

国内视频网站的uploader,用来批量上传视频

### Install

#pip list --format=freeze > requirements.txt
conda create -n uploader python=3.9

conda activate worker

pip install -r requirements.txt --proxy=127.0.0.1:10809

将对应网址的cookie放在cookies/bili_cookies.json,cookies/xhs_cookies.json,cookies/douyin_cookies.json

### Usage

```shell
# 判断数据库中是否存在,存在就不上传了
python main.py --platform xhs --video_url "https://test" --video_path "files/test/11.mp4" --video_name "我只在乎你鄧麗君" --description "我只在乎你鄧麗君 琵琶 演奏"

python main.py --platform douyin --video_url "https://test" --video_path "files/test/11.mp4" --video_name "我只在乎你鄧麗君" --description "我只在乎你鄧麗君 琵琶 演奏"

python main.py --platform bili --video_url "https://test" --video_path "files/test/11.mp4" --video_name "我只在乎你鄧麗君" --description "我只在乎你鄧麗君 琵琶 演奏"
```


