# EKS
EKS: eksctl +kuebctl
EKS sử dụng eksctl và kubectl và manual hands on trên console để eks-cluster có thể sử dụng các dịch vụ của AWS bằng cách cài các CSI-driver (EBS,EFS) hoặc các vài thứ khác tương tự của service bằng helm. Bản chất là Service-account trong EKS sẽ có 1 role (web-identify). SA sẽ gọi -> oidc bằng certification -> STS role trên:
![image](https://user-images.githubusercontent.com/36032208/211161594-893c3419-ed33-4c89-b7f2-0ca96a76293d.png)
Trong "12_Devops_" sẽ tạo 1 pipeline để auto-update file.yaml configure cho eks-cluster:
![image](https://user-images.githubusercontent.com/36032208/211161649-5e74c263-f68f-4bee-aac5-0576762f1984.png)
Các services EKS sử dụng:
![image](https://user-images.githubusercontent.com/36032208/211161663-61457b37-c3b7-482e-8d37-62a023530e50.png)
Và 1 phần scale cho EKS như HPA, VPA, Eks-cluster
