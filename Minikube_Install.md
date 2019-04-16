### Minikube install commands for macOS
整个过程需要到 Google 域下下载文件，必须开代理。Mac 上开 `SS + Proxifier` ,Proxifier 的 `Rules` 添加 `curl; git-remote-https; minikube; VBoxHeadless` 
走本地代理“SOCKS5”。遇到超时错误需要检查代理。如网络代理无问题，需要反复重试（实用 brew cask 来安装 virtualbox). 本机不能上 Google 或者代理设置错误都将浪费很多时间。

```shell
kubectl
kubectl get namespaces
kubectl proxy
brew cask install minikube
minikube start
brew install hyperkit
minikube start --vm-driver hyperkit
minikube start
minikube start --alsologtostderr -v=9
minikube status
kubeadm init phase control-plane all --config /var/lib/kubeadm.yaml
brew cask uninstall --force virtualbox;
brew cask install virtualbox
brew uninstall hyperkit
brew cask install virtualbox
brew cask uninstall virtualbox
brew cask install virtualbox
minikube start
rm -rf ~/.kube  ~/.minikube
minikube start
minikube delete
minikube start
kubectl version
ping 192.168.99.101
minikube status
kubectl cluster-info
minikube dashboard
kubectl run hello-go --image=shapeshed/hello-go --port=8080\n
kubectl expose deployment hello-go --type=NodePort\n
kubectl get pod
minikube service hello-go --url
docker ps
kubectl get pod
minikube service hello-go --url
kubectl cluster-info
kubectl get nodes
kubectl run first-deployment --image=katacoda/docker-http-server --port=80
kubectl get pods
kubectl expose deployment first-deployment --port=80 --type=NodePort
export PORT=$(kubectl get svc first-deployment -o go-template='{{range.spec.ports}}{{if .nodePort}}{{.nodePort}}{{"\n"}}{{end}}{{end}}')\n\n
echo $PORT
curl host01:$PORT
minikube service hello-go --url\n
docker ps
docker ps -a
minikube service first-deployment --url\n

```
