FROM python
COPY . /
RUN pip install -r requirements.txt
ENV APP_COLOR=pink
ENTRYPOINT [ "/bin/bash" ]
CMD [ "/script.sh" ]
