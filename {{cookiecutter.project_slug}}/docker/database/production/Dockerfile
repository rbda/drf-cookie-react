FROM postgres:10.1
MAINTAINER {{ cookiecutter.author_name }} <{{ cookiecutter.email }}>

RUN mkdir -p /docker-entrypoint-initdb.d
COPY src/init-user.sh /docker-entrypoint-initdb.d/

COPY docker-healthcheck /usr/local/bin/
HEALTHCHECK --interval=30s --timeout=30s CMD ["docker-healthcheck"]