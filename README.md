# GeoParser

MEMEX GeoParser Project.

## Environment Requirements

- Python 2.7
- Django 1.8 (tested with 1.8.19)
- pip (legacy version compatible with Python 2.7)
- Java 8 (required for Gazetteer services)

**Note:** 
- Modern systems (e.g., Mac M1/M2 chips) may encounter Docker build failures due to architecture mismatches.
- It is recommended to use prebuilt Docker images whenever possible to avoid dependency issues.

To set up a Python 2.7 virtual environment using pyenv:

```bash
pyenv install 2.7.18
pyenv virtualenv 2.7.18 geoparser-env
pyenv activate geoparser-env
pip install -r requirements.txt
```

## Docker Installation Tips

If you face problems building Docker images locally, you can pull the prebuilt image:

```bash
docker pull nasajplmemex/geo-parser
docker run -p 9998:9998 nasajplmemex/geo-parser
```

This method avoids most local build issues and speeds up the deployment process.

## Quick Start

1. Clone the repository:
    ```bash
    git clone https://github.com/nasa-jpl-memex/GeoParser.git
    ```
2. Navigate to the project directory.
3. Set up Python 2.7 environment and install dependencies.
4. (Optional) Start Gazetteer and Solr services if needed.
5. Run Django server:
    ```bash
    python manage.py runserver
    ```
6. Visit `http://localhost:8000` to access the GeoParser Web UI.

## Additional Notes

- Ensure that your Gazetteer service is running and properly indexed using GeoNames data.
- For Tika Server integration, ensure correct `config.txt` setup for geo endpoint configurations.
