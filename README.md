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

List of valid timezones can be found here: https://en.wikipedia.org/wiki/List_of_tz_database_time_zones

Also make sure to change your /module/tomcat/hippo-XXX/manifest.yml to reflect your environment
