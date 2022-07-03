# Complete setup of the system
This tutorial is for usage of Collaborative-IoT+House-of-IoT which ignores the setup of the HOI-WebClient. 
To get instructions on how to setup the Collaborative-IoT portion of the system, please visit the collaborative Org.

This tutorial is for no-sql usage.

## What do you need to setup?
You need to setup one ExternalController and one GeneralServer for the heart of the system.

# Running the GeneralServer

## Env variables needed to be set

```
1. The admin password for your server ("apw_hoi_gs").
2. The regular password for your server ("rpw_hoi_gs").
3. The super admin password for your server ("sapw_hoi_gs").
4. The twilio account sid for your server ("hoi_t_account_sid").
5. The twilio auth token for your server ("hoi_t_auth_token").
6. The twilio phone number for your server ("hoi_t_phone_number").
7. The password to connect to your external controller instance ("hoi_exc_s_pw").
```

## Config.json needed for general server

```
{
    "disconnecting": false, -> Does disconnecting require admin auth?
    "activating": true, -> Does activating require admin auth?
    "deactivating": false,  -> Does deactivating require admin auth?
    "viewing": true, -> Does viewing require admin auth?
    "host": "localhost", -> Host
    "port": 50888, -> Port
    "using_sql" :false, -> SQL usage? Remember this tutorial isn't for SQL usage!
    "device_specific":true, -> Device specific actions requires authentication?
    "external_controller_location":"wss://localhost:50224", -> Location of your external controller
    "relations":true} -> Adding/removing relations requires admin authenticaion(recommended to be true)
```

## Actual step by step to get the server running locally.
1. Clone the repo(`git clone https://github.com/House-of-IoT/HOI-GeneralServer`) and Clone the repo(`https://github.com/House-of-IoT/HOI.py`)
2. setup your config and env variables(explained above)
3. Make sure you have python installed 
4. Install HOI.py in the runtime by going into `HOI.py` and running `python install setup.py`
5. Start the server! `python main.py`
