---
layout: post
---

Запуск pyspark в jupyter notebook:

# optional, jdk if you don't have one installed system wide:

* download jdk zip from https://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html and unpack to project folder.

* download spark zip from http://spark.apache.org/downloads.html, unpack to the project folder

* set environment variables to use the jdk:

    export PROJECT_HOME=/home/sashka/Projects/pyspark-demo
    export JAVA_HOME=$PROJECT_HOME/jdk1.8.0_181
    export SPARK_HOME=$PROJECT_HOME/spark-2.4.0-bin-hadoop2.7
    export PATH=$JAVA_HOME/bin:$SPARK_HOME/bin:$PATH


# Python Virtualenv

(треба щоб не конфліктувати з системним менеджером пакетів, і тримати всі залежності локально для проекта)

В папочці проекта:

Створити віртуальне середовище пітона:

    virtualenv env -p python3

включити цей енвайронмент:

    . env/bin/activate.sh

поставити jupiter:

    pip install jupyter


встановити змінні середовища для запуску піспарка:

    export PYSPARK_PYTHON=`which python`
    export PYSPARK_DRIVER_PYTHON=jupyter
    export PYSPARK_DRIVER_PYTHON_OPTS='notebook'










