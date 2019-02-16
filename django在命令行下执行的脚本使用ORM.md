项目中需要写一个deamon来处理，需要在deamon脚本中使用到DjangoORM来操作数据库
在deamon script中初始化一个Django environment

## settings.py
from os.path import join \n
import os.path \n
settings_path = os.path.abspath(os.path.dirname(__file__)) \n

## deamon.py
import sys \n
import settings \n
from django.core.management import setup_environ \n
sys.path.append(settings.settings_path) \n
setup_environ(settings) \n