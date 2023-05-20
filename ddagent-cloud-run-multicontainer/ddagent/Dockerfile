FROM gcr.io/datadoghq/agent:latest
COPY config.yaml /etc/datadog-agent/datadog.yaml

EXPOSE 8126

ENV DD_API_KEY=<DD_API_KEY>
ENV DD_SITE=datadoghq.com
ENV DD_APM_ENABLED=true
