FROM python:3-slim

RUN apt update && apt upgrade -y && apt install -y wget nmap python3-pip python3-distutils unzip git
RUN mkdir PyReconer
COPY PyReconer.py /PyReconer
WORKDIR /PyReconer
RUN mkdir output
RUN wget https://github.com/OWASP/Amass/releases/download/v3.14.2/amass_linux_amd64.zip && unzip amass_linux_amd64.zip && mv amass_linux_amd64 amass
RUN git clone https://github.com/FortyNorthSecurity/EyeWitness.git && ./EyeWitness/Python/setup/setup.sh
RUN python3 -m pip install netaddr selenium

ENTRYPOINT ["python3", "PyReconer.py"]
