# chan_respoke-musicbot

A simple Asterisk installation with the Respoke channel driver configured
to connect to a Respoke application as the endpoint 'musicbot' and play 
music when called.

## usage 
- To build this image, clone the repo and build using docker:
    
    ```bash
    git clone https://github.com/respoke/chan_respoke-musicbot-example.git
    cd chan_respoke-musicbot-example
    docker build -t musicbot .
    ```


- run the image:

    ```bash
    docker run -e RESPOKE_APP_SECRET=your_application_secret \
               --net=host musicbot
    ```


- fire up a web application that connects to the same app, and place a call
to the `musicbot` endpointId


- you should hear music play!

## license
[MIT](https://github.com/respoke/chan_respoke-musicbot-example/blob/master/LICENSE)
