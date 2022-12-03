FROM python
COPY . /
RUN pip install -r requirements.txt
ENV APP_COLOR=red
ENTRYPOINT [ "/bin/bash" ]
CMD [ "/script.sh" ]
