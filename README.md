# filebeat-tomcat-hippo
Filebeat tomcat hippo CMS module



Don't forget to change your timezone @ /module/tomcat/hippo-XXX/ingest/pipeline.json:

{
    "date": {
    "field": "tomcat.hippo-site.timestamp",
    "target_field": "@timestamp",
    "formats": ["dd.MM.yyyy HH:mm:ss"],
    "timezone": "America/Los_Angeles",
    "ignore_failure": true
    }
}