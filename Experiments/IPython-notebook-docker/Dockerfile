FROM ipython/scipyserver

MAINTAINER Raymond Yee  <raymond.yee@gmail.com>

RUN pip install -U boto==2.8.0 && \
  pip install warc && \
  pip install -e git+https://github.com/commoncrawl/gzipstream.git#egg=gzipstream && \
  apt-get clean -y

EXPOSE 8888
CMD /notebook.sh
