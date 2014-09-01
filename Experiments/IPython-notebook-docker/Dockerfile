FROM ipython/scipyserver

MAINTAINER Raymond Yee  <raymond.yee@gmail.com>

RUN cd /tmp && git clone https://github.com/commoncrawl/gzipstream.git && cd gzipstream && python setup.py install && cd /tmp && rm -rf /tmp/gzipstream

RUN pip install -U boto==2.8.0 && \
  pip install warc && \
  apt-get clean -y


EXPOSE 8888
CMD /notebook.sh
