FROM vanessa/boxes

# docker build -t vanessa/confucious-actions:fail

LABEL "com.github.actions.name"="Confucious Pull Request Fail"
LABEL "com.github.actions.description"="Provides the user with emoji wisdom on pull request failure."
LABEL "com.github.actions.icon"="activity"
LABEL "com.github.actions.color"="red"

COPY fail.sh /fail.sh

# Replaces default message for container
COPY /fail-messages.txt /messages.txt
COPY /post_message.py /post_message.py

RUN chmod u+x /fail.sh && \
    chmod u+x /post_message.py
ENTRYPOINT ["/fail.sh"]
