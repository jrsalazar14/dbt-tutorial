# Jaffle Shop

## Project Overview

Jaffle Shop is a dbt (data build tool) project that transforms and models data for a fictional shop. This project demonstrates best practices in data modeling and transformation using dbt.

## Project Structure

The project follows the standard dbt project structure:

- `models/`: Contains SQL models
  - `staging/`: Staging models that clean up raw data
  - `schema.yml`: YAML file containing model descriptions and column tests
- `analyses/`: (Not shown in provided files, but standard dbt structure)
- `tests/`: (Not shown in provided files, but standard dbt structure)
- `seeds/`: (Not shown in provided files, but standard dbt structure)
- `macros/`: (Not shown in provided files, but standard dbt structure)
- `snapshots/`: (Not shown in provided files, but standard dbt structure)
- `dbt_project.yml`: Main configuration file for the dbt project

## Models

### Staging Models

1. `stg_customers`: Cleans up customer data
2. `stg_orders`: Cleans up order data

### Core Models

1. `customers`: One record per customer, including first order date and order count

## Data Sources

The project uses data from the `dbt-tutorial.jaffle_shop` dataset, specifically:

- `jaffle_shop.customers`
- `jaffle_shop.orders`

## Configuration

- The project is named "jaffle_shop" and uses version 1.0.0
- Models in the main jaffle_shop directory are materialized as tables
- Models in the staging subdirectory are materialized as views

## Getting Started

1. Ensure you have dbt installed and configured
2. Clone this repository
3. Set up your `profiles.yml` file with the necessary credentials
4. Run `dbt deps` to install any dependencies
5. Run `dbt compile` to compile the project
6. Run `dbt run` to build the models
7. Run `dbt test` to run the tests defined in `schema.yml`
