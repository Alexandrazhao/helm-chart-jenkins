# Helm Chart For Jenkins
This project is to write a helm chart for Jenkins, and this will show you some basic helm commands to interact with. 
After building a helm list, using ```helm upgrade --install REALEASE-NAME jenkins/jenkins```
- This is a created helm chart for jenkins, if you want to create a new helm chart, run ```helm create REALEASE-NAME``` to generate a new helm chart.

1. ```helm list``` to show all helm list you built.
2. ```helm lint``` to check your code.
3. ```helm template .``` to checkout your executing files in template folder.
4. All executing files are saved in `templates` folder. All parameters' value are saved in `values.yaml` file.
5. In this case, we set the value of ```replicas: {{ .Values.replicaCount }}``` in `values.yaml` as 5. Then we can run
```helm upgrade REALEASE-NAME ./REPO_NAME --set replicaCount=8``` to upgrade the ```{{ .Values.replicaCount }}``` to 8.
6. Run ```helm get values REALEASE-NAME``` to checkout the value you upgraded. Or run ```helm get -a values REALEASE-NAME``` to checkout all values in the helm chart. 
7. Run ```helm rollback REALEASE-NAME VERSION``` to rollback to the previous version. 


