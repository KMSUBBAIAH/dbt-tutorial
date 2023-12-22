### Welcome to my dbt tutorial
I'll be following the dbt series created by [Kahan](https://www.youtube.com/@KahanDataSolutions)

This is to document any issues I encounter and record the solutions to them.

##### Steps:
1. Creating a python virtual environment and installing requirements
    ```console
    pip install virtualenv
    virtualenv venv
    cd venv/Scripts
    ./activate
    pip install -r requirements.txt
    ```
2. Creating dbt project
    ```console
    dbt init dbt-tutorial
    ```
3. Changing the profiles.yml created in the 'C' drive following the below profiles_template.yml for snowflake integration, for other datawarehouse integration, refer: [Documentation](https://docs.getdbt.com/docs/core/connect-data-platform/about-core-connections)

4. Run the below command to check if it connect, and all checks passed!, run the next command
    ```console
    dbt debug

    # next
    dbt run
    ```
    * the dbt run command will run the sample models in the models folder and create them in the warehouse given in the profiles.yml

___Error 1: Error encountered was all check passed but the model was not being created, and the error it gave was to give (use warehouse wh_name) in the config, but it didn't work.
***Cause & Solution:***
The problem was i gave the parameters in profiles.yml in lowercase, and changin all to uppercase solved my issue___
