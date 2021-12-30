---
marp: true
---

<!-- _class: invert -->

## Amazon EKS

* Amazon Elastic Kubernetes Service (Amazon EKS) is a managed container service
  to run and scale Kubernetes applications in the cloud or on-premises.

* Amazon EKS is certified Kubernetes-conformant, so existing applications that
    run on upstream Kubernetes are compatible with Amazon EKS.

* Amazon EKS automatically manages the availability and scalability of the
  Kubernetes control plane nodes responsible for scheduling containers, managing
  application availability, storing cluster data, and other key tasks.

---

## Amazon EKS - EC2 + Fargate

* Amazon EKS lets you run your Kubernetes applications on both

  * Amazon Elastic Compute Cloud (Amazon EC2) and

  * AWS Fargate.

* With Amazon EKS, you take advantage of all the performance, scale,
  reliability, and availability of AWS infrastructure, as well as integrations
  with AWS networking and security, such as application load balancers (ALBs)
  for load distribution, AWS Identity and Access Management (IAM) integration
  with role-based access control (RBAC), and AWS Virtual Private Cloud (VPC)
  support for pod networking.

---

<!-- _class: invert -->

## AWS Fargate

* AWS Fargate is a serverless, pay-as-you-go compute engine that lets you focus
  on building applications without managing servers. AWS Fargate is compatible
  with both Amazon Elastic Container Service (ECS) and Amazon Elastic Kubernetes
  Service (EKS).

---

![](https://d1.awsstatic.com/re19/FargateonEKS/Product-Page-Diagram_Fargate%402x.a20fb2b15c2aebeda3a44dbbb0b10b82fb89aa6a.png)

---

## Web Apps, APIs, and Microservices

* Build and deploy your applications, APIs, and microservices architectures with
  the speed and immutability of containers. **Fargate** removes the need to own,
  run, and manage the lifecycle of a compute infrastructure so that you can
  focus on what matters most: your applications.

---

## Container Workloads

* Use **Fargate** with Amazon ECS or Amazon EKS to easily run and scale your
  containerized data processing workloads. Fargate also enables you to migrate
  and run your Amazon ECS Windows containers without refactoring or
  rearchitecting your legacy applications.

---

## AI and ML Training Applications

* Create an AI and ML development environment that is flexible and portable.
  With **Fargate**, achieve the scalability you need to boost server capacity
  without over-provisioning—to train, test, and deploy your machine learning
  (ML) models.

---

## Optimize Costs

* With **Fargate** there are no upfront expenses, pay for only the resources
  used. Further optimize with Compute Savings Plans and Fargate Spot, then use
  Graviton2 powered Fargate for up to 40% price performance improvements.

---

<!-- _class: invert -->

## Eksctl + Fargate

* With *eksctl* an EKS cluster is just the command line switch *--fargate* away:

```
eksctl create cluster \
    --name ${CLUSTER_NAME} \
    --nodes 3 \
    --fargate \
    --region ${AWS_DEFAULT_REGION}
```