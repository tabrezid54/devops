FROM python
COPY . /
RUN pip install -r requirements.txt
ENV APP_COLOR=green
ENTRYPOINT [ "/bin/bash" ]
CMD [ "/script.sh" ]
