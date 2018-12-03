# redash-kubernetes
Redash cluster setup on kubernetes

# Create ssl and push it to k8s

* `openssl req -x509 -nodes -days 365 -newkey rsa:2048 -keyout ./cert.key -out ./cert.crt -subj "/C=GB/ST=New York/L=New York/O=Domain/OU=IT Department/CN=redash.net"`

* `kubectl create secret tls tls-secret --key ./cert.key --cert ./cert.crt `