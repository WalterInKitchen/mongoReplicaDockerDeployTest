FROM mongo

# copy scripts to home
RUN echo 'copy scripts to image'
COPY scripts /home/scripts/

# copy security keys
RUN echo 'copy keys to image'
COPY keys /home/keys/
RUN chown mongodb:mongodb /home/keys/*
RUN chmod 0400 /home/keys/*