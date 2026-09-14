# TechChalegger3 — GitOps

Este repositório contém **apenas manifestos Kubernetes**. Nenhum código de
aplicação e nenhuma credencial.

Ninguém edita a tag da imagem aqui na mão. Quem escreve é o pipeline do
repositório TechChalegger3, ao final de um build bem-sucedido. O ArgoCD
observa este repositório e aplica a diferença no cluster.

Secrets e ConfigMaps não estão aqui de propósito: são criados pelo
Terraform direto no cluster, porque carregam senha de banco e endereço
de recurso que muda a cada ambiente.

```
apps/<servico>/    deployment, service e (quando aplicável) hpa
ingress/           roteamento HTTP de entrada
```
