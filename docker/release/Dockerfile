FROM silvade/todobackend-base:latest
MAINTAINER Steve de Silva <steve.desilva@gmail.com>

#Copy application artifacts - target -> weelhouse folder in the image
COPY target /wheelhouse

# Install application
# Activate virtual environment 
# --no-index -f /wheelhouse = Only install from containers wheelhouse folder (no downloading externally done via build stage)
#  rm -rf /wheelhouse = clean up wheelhouse folder after build
# todobackend = must match the name in setup.py file. N.B. pip install looks at setup.py file
RUN . /appenv/bin/activate && \
    pip install --no-index -f /wheelhouse todobackend && \
    rm -rf /wheelhouse