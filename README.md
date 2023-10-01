# Nestjs Elasticsearch,Logstash AND Kibana (ELK) Application

## GitHub App with Docker Compose

This GitHub repository contains a Docker Compose configuration for setting up a development environment with the following services:

- **NestJS API**
  - Database (typeorm).
  - Seeding.
  - Config Service (@nestjs/config).
  - Mailing (nodemailer).
  - Sign in and sign up via email.
  - Social sign in (Apple, Facebook, Google, Twitter).
  - Admin and User roles.
  - I18N (nestjs-i18n).
  - File uploads. Support local and Amazon S3 drivers.
  - Swagger.
  - E2E and units tests.
  - Docker.
  - CI (Github Actions).)
- **Elasticsearch**
- **Logstash**
- **Kibana**
- **Filebeat**
- **PostgreSQL**
- **Cadvisor**
- **Caddy**

### Prerequisites

Before you start using this Docker Compose configuration, ensure you have the following prerequisites installed on your system:

- [Docker](https://www.docker.com/get-started)
- [Docker Compose](https://docs.docker.com/compose/install/)

### Getting Started

1. Clone this repository to your local machine.

```bash
git clone <repository-url>
cd <repository-directory>
```

2. Customize environment variables (if necessary) by modifying the .env file.

3. Start the services using Docker Compose.

```bash
docker-compose up -d
```

The services will start running in the background.

### Accessing Services

- NestJS API: Accessible at http://localhost:3000
- Elasticsearch: Accessible at http://localhost:9200
- Logstash: Accessible at http://localhost:5044 (TCP) and http://localhost:5000 (TCP and UDP)
- Kibana: Accessible at http://localhost:5601
- Filebeat: Containerized Filebeat is configured to collect and ship logs to Elasticsearch.
- PostgreSQL: Accessible at localhost:${DATABASE_PORT} (Default port is set in .env)
- Caddy: A web server for reverse proxy, accessible at http://localhost and https://localhost. Configuration can be customized in Caddyfile.

### Customizing Configuration

You can customize the configuration for each service by editing the corresponding configuration files in the respective service folders (e.g., `elasticsearch/config/elasticsearch.yml`, `logstash/config/logstash.yml`, `kibana/config/kibana.yml`, etc.).

### Monitoring

- Cadvisor: Provides container monitoring accessible at http://localhost:8080
- Stopping the Services
  To stop the services and remove the containers, run:

```bash
docker-compose down
```

### Contributing

If you have any improvements or suggestions for this Docker Compose configuration, please feel free to contribute by creating a pull request.

### License

This project is licensed under the MIT License - see the LICENSE file for details.

### Author

- Olawale Afuye

### Credits

@Brocoders
@techvlad
