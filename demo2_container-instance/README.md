### Start a container instance

1. Go to _Podman Desktop_ > _Containers_ > _Create_ > _Existing Image_
2. Select image `quay.io/acancell-redhat-talks/ibm_txc_24_milan/demo-container`
3. Click on _Play Image_
4. Set the following parameters in the _Basic_ tab:
    - _Container name_: `demo-container`
    - _Port mapping_: 
        - _Host port_: `8080`
        - _Container port_: `8000`
5. Click on _Start Container_

### Check the container instance

1. Go to _Podman Desktop_ > _Containers_ 
2. Select tab _Running_
3. Select the running container `demo-container`
4. Go to _Action_ > _Open Browser_ 

### Check the container isolation

1. Go to _Podman Desktop_ > _Containers_ 
2. Select tab _Running_
3. Select the running container `demo-container`
4. Go to _Action_ > _Open Terminal_
5. Run the command:
~~~
ps -ax | grep 'http.server'
~~~
6. Note how `http.server` has PID equals to `1`
7. Open a shell on the host machine and run again the command:
~~~
ps -ax | grep 'http.server'
~~~
8. Note how `http.server` has a different PID