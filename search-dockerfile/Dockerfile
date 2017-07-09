FROM jetty:9.3.10

MAINTAINER Robert Kaye <rob@metabrainz.org>

WORKDIR $JETTY_HOME
RUN curl -o $JETTY_HOME/webapps/ROOT.war http://ftp.musicbrainz.org/pub/musicbrainz/search/servlet/searchserver.war

WORKDIR /home/search
RUN curl -o /home/search/index.jar http://ftp.musicbrainz.org/pub/musicbrainz/search/index/index.jar

COPY index.sh /home/search

VOLUME ["/home/search/data"]
