# docker-user-wrapper

Add user with the same `uid` of local user to docker image to avoid permissions issue.

```bash
Usage: ./dupper [--tag TAG] IMAGE_TAG

-t, --tag     [TAG]     New tag image   [default: dupper_IMAGE_TAG]
-u, --user    [USER]    Custom username [default: $USER]
--add-group   [GROUP]   Add user to group
--to-file     [FILE]    Dump Dockerfile to file
-v, --verbose           Print debug data

Examples:
./dupper php:7.2
./dupper ubuntu:latest --tag custom_tag
./dupper alpine:latest --user custom_user
./dupper apache:latest --to-file Dockerfile
./dupper php:7.2 -v --add-group www-data
```
