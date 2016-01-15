FROM vroomanj/notebook:latest

MAINTAINER Justin Vrooman <vroomanj@egr.msu.edu>

ADD singleuser.py /usr/local/bin/jupyterhub-singleuser
RUN chmod 755 /usr/local/bin/jupyterhub-singleuser

EXPOSE 8888

# Hackity hack?
ADD sudoers /etc/sudoers

# ENV SHELL /bin/bash

ADD systemuser.sh /srv/singleuser/systemuser.sh
CMD ["sh", "/srv/singleuser/systemuser.sh"]
