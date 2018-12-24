# Documents

# __Backend server__
The coders uses supervisor to start all the relevant services. To check the config, go to conf → supervisord.conf. Pay particular attention to app.ini and app.py. Under supervisord, this is the main application that houses hserver.

Under create_app, configure is called to load the various settings from configuration files and environment variables. After which pyramid’s make_wsgi_app will be called where by the web service will be running with the configurations.

# __Hypothesis__

1. Under embedding-examples → postmessage-config, example shows that ../client.js will be loaded

2. Under client.js, the script calls http://hserver:5000/embed.js (backend) to retrieve the JS. In the hypothesis server, embed.js maps to embed under the file redirects and h → util → redirects.py. The backend service will route to http://hserver:3001/hypothesis 

