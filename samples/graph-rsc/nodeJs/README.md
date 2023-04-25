* configurationUrl:
    `https://smartq.ddns.net/worker1/graph-rsc/configure` for production
    `https://${ SUB_DOMAIN }.ngrok-free.app/configure` for development

* build image:
  ```
  podman build -t graph-rsc:$(date +%s) .
  ```    

* start container :
  ```
  podman run -d \
    --name graph-rsc \
    --pod ms-teams-samples \
    -v /home/ken/ms-teams-samples/graph-rsc.env:/app/.env \
    localhost/graph-rsc:1682410333
  ```  