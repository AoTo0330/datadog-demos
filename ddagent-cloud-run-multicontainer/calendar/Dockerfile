# Unless explicitly stated otherwise all files in this repository are dual-licensed
# under the Apache 2.0 or BSD3 Licenses.
#
# This product includes software developed at Datadog (https://www.datadoghq.com/)
# Copyright 2022 Datadog, Inc.
FROM python:3

ENV DD_SERVICE="calendar"
ENV DD_ENV="dev"
ENV DD_VERSION="0.1.0"
# ENV DD_TRACE_STARTUP_LOGS="true"
# ENV DD_TRACE_DEBUG="true"

LABEL com.datadoghq.tags.service="calendar"
LABEL com.datadoghq.tags.env="dev"
LABEL com.datadoghq.tags.version="0.1.0"

WORKDIR /home

COPY requirements.txt /home
COPY /calendar /home/calendar

RUN pip install -r requirements.txt

# Run the application with Datadog
CMD ["ddtrace-run", "python", "calendar/app.py"] 
