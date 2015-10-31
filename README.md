# chan_respoke-musicbot

A simple Asterisk installation with the Respoke channel driver configured
to connect to a Respoke application as the endpoint 'musicbot' and play 
music when called.

## to run
- build the Dockerfile:
    
    ```
    docker build -t musicbot .
    ```

- run the image:

    ```
    docker run -e RESPOKE_APP_SECRET=your_application_secret \
               musicbot
    ```

- fire up a web application that connects to the same app, and place a call
to the `musicbot` endpointId
- you should hear music play!
