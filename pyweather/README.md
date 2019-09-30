# PyWeather Application
A simple two tier web app running on kubernetes that returns the 5 day forecast for a city provided. It uses the [Metaweather](https://www.metaweather.com/) service.

Both tiers are maintained through a deployment and exposed via a service of their own.

### Backend
The backend service uses a ClusterIP to make the service accessible only within the cluster.

### Frontend
The frontend service has a configurable backend URL variable that can be configured with an environment variable. The deployment sets it as the service name defined in the backend's service manifest.  
Its service uses a NodePort and can be accessed with the IP of a node running in the cluster (*note: in `minikube`, this is the cluster's IP*).

## Running It All
Everything can be set up with the following command (from this directory):  
`kubectl apply -f weather-frontend/manifests/ -f weather-backend/manifests/`  
The frontend is exposed on port `30003` and can then be hit by using a node IP with this port.  
`http://{nodeIP}:30003/{city}`  
`http://{nodeIP}:30003/toronto`