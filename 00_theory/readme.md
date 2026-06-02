# Теория

- [DuckLake v1.0: The Lakehouse Format Built on SQL Reaches Production-Readiness](https://ducklake.select/2026/04/13/ducklake-10/)
- [DuckLake Docs](https://ducklake.select/docs/stable/)

## Виды проектирования Data-платформ

### DWH

![](https://motherduck.com/_next/image/?url=https%3A%2F%2Fmotherduck-com-web-prod.s3.amazonaws.com%2Fassets%2Fimg%2Ftrad_olap_6adeb3f1f8.png&w=1920&q=75)

### Data Lake

![](https://motherduck.com/_next/image/?url=https%3A%2F%2Fmotherduck-com-web-prod.s3.amazonaws.com%2Fassets%2Fimg%2Fdatalake_019f24a5b5.png&w=1920&q=75)

### Data LakeHouse

![](https://motherduck.com/_next/image/?url=https%3A%2F%2Fmotherduck-com-web-prod.s3.amazonaws.com%2Fassets%2Fimg%2Flakehouse_8305538ffd.png&w=1920&q=75)

## Табличные форматы

### Apache Iceberg

- [apache/iceberg-rest-fixture:1.10.1](https://hub.docker.com/layers/apache/iceberg-rest-fixture/1.10.1/images/sha256-319afc30ef94300f79987b1d185c4911576db0cdfaa98246cb42757ec4d53463)
- [apache-iceberg-1.10.1/docker/iceberg-rest-fixture/Dockerfile](https://github.com/apache/iceberg/blob/apache-iceberg-1.10.1/docker/iceberg-rest-fixture/Dockerfile)

![](https://iceberg.apache.org/assets/images/iceberg-metadata.png)

![](https://motherduck.com/_next/image/?url=https%3A%2F%2Fmotherduck-com-web-prod.s3.amazonaws.com%2Fassets%2Fimg%2Ficeberg_scan_78a634bf34.png&w=1920&q=75)

```mermaid
graph TD
    A([Начало: INSERT]) --> B[1. Запрос к Postgres: <br>Узнать имя текущего JSON-файла метаданных]
    B --> C[2. Запись данных: <br>Скидываем новые .parquet файлы в S3]
    C --> D[3. Запись описания: <br>Создаем новые файлы манифестов .avro и .json в S3]
    D --> E[4. Финал в Postgres: <br>Переключаем указатель со старого JSON на новый JSON]
    E --> F([Конец: Данные вставлены])
```

### DuckLake

![](https://motherduck.com/_next/image/?url=https%3A%2F%2Fmotherduck-com-web-prod.s3.amazonaws.com%2Fassets%2Fimg%2Fducklake_523fc1046a.png&w=1920&q=75)

```mermaid
graph TD
    A([Начало: INSERT]) --> B[1. База данных DuckLake: <br>Открываем транзакцию]
    B --> C[2. Запись данных: <br>Скидываем новые .parquet файлы в S3 / на диск]
    C --> D[3. База данных DuckLake: <br>Построчно записываем пути к новым .parquet файлам]
    D --> E[4. Финал в Базе данных: <br>Делаем COMMIT транзакции]
    E --> F([Конец: Данные вставлены])
```
