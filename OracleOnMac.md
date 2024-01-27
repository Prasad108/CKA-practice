# How to run oracledb on mac m1? 

 1. install Colima - container runtimes on macOS (and Linux) with minimal setup.

      brew install colima

 2. start Colima

      colima start --arch x86_64 --memory 3

 3. run docker image with volume 

    run docker image with volume
    
    docker run -d -p 1521:1521 -e ORACLE_PASSWORD=oracle -v oracle-volume:/opt/oracle/oradata gvenzl/oracle-xe

 5. connect with sql plus

      docker exec -it hardcore_lumiere /bin/bash
    
      $ORACLE_HOME/bin/sqlplus system/oracle@//localhost:1521/xe
