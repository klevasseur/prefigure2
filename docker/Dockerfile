FROM python:3.12-bookworm

# Update the package list and install necessary packages
RUN apt-get update && \
    apt-get install -y python3-dev python3-louis python3-pip npm nodejs libcairo2-dev pkg-config librsvg2-bin && \
    apt-get clean

RUN echo '/usr/lib/python3/dist-packages' > /usr/local/lib/python3.12/site-packages/louis.pth
RUN python3 -m pip install --upgrade pip
RUN pip install prefig[pycairo]
RUN prefig init
