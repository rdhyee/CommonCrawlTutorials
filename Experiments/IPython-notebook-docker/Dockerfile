FROM ipython/scipyserver

MAINTAINER Raymond Yee  <raymond.yee@gmail.com>

# pip install -e git+https://github.com/commoncrawl/gzipstream.git#egg=gzipstream didn't work
RUN cd /tmp && git clone https://github.com/commoncrawl/gzipstream.git && cd gzipstream && python setup.py install && cd /tmp && rm -rf /tmp/gzipstream

RUN pip install -U boto==2.8.0 && \
  pip install warc && \
  pip install s3cmd && \
  apt-get clean -y

ADD CommonCrawl_basics.ipynb /notebooks/CommonCrawl_basics.ipynb
ADD basics.ipynb /notebooks/basics.ipynb
ADD factorials.py  /notebooks/factorials.py

EXPOSE 8888
CMD /notebook.sh
