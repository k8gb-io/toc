# k8gb 2022 Annual Review

This is a Kubernetes ToC Annual Review for the [k8gb](https://k8gb.io) project for 2022.


## Table of Contents

- [Background](#background)
- [DevStats](#devstats)
- [Maintainers](#maintainers)
- [Adoption](#adoption) 
- [Project goals](#project-goals) 
- [CNCF Membership](#cncf-membership)
- [Incubation](#incubation)
- [Project Links](#project-links)


## Background

k8gb is a completely open source, cloud native, global load balancing solution for Kubernetes. k8gb 
focuses on load balancing traffic across geographically dispersed Kubernetes clusters using multiple 
load balancing strategies to meet requirements such as region failover for high availability.

k8gb also cooperates with other CNCF projects such as:
- [coredns](https://coredns.io/)
- [ExternalDNS](https://github.com/kubernetes-sigs/external-dns)

k8gb implements the Kubernetes operator pattern and extends the Kubernetes with gslb custom resources at 
the same time it handles changes to Ingress resources with certain annotation on them. Internally it 
creates zone delegation on DNS level updates the DNS records according to the load balancing strategy 
and the result of readiness probes.

One can install the operator using [helm chart](https://artifacthub.io/packages/helm/k8gb/k8gb) or [OLM bundle](https://artifacthub.io/packages/olm/community-operators/k8gb).

k8gb was accepted as a CNCF Sandbox project on [March 30th, 2021](https://docs.google.com/spreadsheets/d/1Nnh_usr0tSZxaUpxTusqeIqKxMmvuEViRkyO9e_Do40/edit#gid=1136111842).


## DevStats

[k8gb's DevStats page](https://k8gb.devstats.cncf.io/d/15/new-prs-in-repository-groups?orgId=1&from=1609520400000&to=1641056399000&var-period=w&var-repogroup_name=All) shows the weekly number of 
newly opened pull requests on the main git repo.

| Metric       |  Pre-Sandbox |    Today     |
| ------------ | ------------ | ------------ |
| Stars        | ~100         | ~450         |
| Forks        | 10-20        | ~50          |


## Maintainers

There are six active maintainers working on the project (alphabetically):

| Maintainer           | GitHub ID                                         | Affiliation |
| -------------------- | ------------------------------------------------- | ----------- |
| Dinar Valev          | [k0da](https://github.com/k0da)                   | Absa        |
| Donovan Muller       | [donovanmuller](https://github.com/donovanmuller) | Absa        |
| Jiri Kremser         | [jkremser](https://github.com/jkremser)           | Absa        |
| Michal Kuritka       | [kuritka](https://github.com/kuritka)             | Absa        |
| Timofey Ilinykh      | [somaritane](https://github.com/somaritane)       | Absa        |
| Yury Tsarev          | [ytsarev](https://github.com/ytsarev)             | Upbound     |


## Adoption
k8gb is used in Absa for disaster recovery solution (the failover mode) where a critical application is 
redundantly deployed into two geographically dispersed Kubernetes clusters.

We have a feedback from Portuguese Commercial Bank that they are evaluating the k8gb for their needs.

Otherwise it is difficult to measure the adoption without incorporating some evil spy ware into k8gb (not going to happen).


## Last years achievements (optional)
- local deployment now uses Bind dns server as an example of edge dns server
- integration with OLM and `operatorhub.io`
- Q&A: FakeDNS, Terratests, various linters
- better observability (more metrics, convenience tools for showcasing the deployment)
- Ingress `v1beta1 -> v1` switch
- makefile & CI is now ready for multi-cluster deployments, not limited to two clusters
- fully automated release process based on a pull-request -> democratic


## Project Goals
// todo: delete me
> What are the current goals of the project? For example, are you working on major new features? Or are you concentrating on adoption or documentation?


## CNCF membership
// todo: delete me
> How can the CNCF help you achieve your upcoming goals?


## Incubation

Since we do not met the adoption [criteria](https://github.com/cncf/toc/blob/main/process/graduation_criteria.md#incubating-stage) yet,
 we would rather not aim for graduation yet. The goal of the project should be gathering the community 
 and get some early adopters. Currently the k8gb is being actively used by Absa group and it is being 
 evaluated by Portuguese Commercial Bank.


## Project Links
* [Website](https://k8gb.io/)
* [Github](https://github.com/k8gb-io/k8gb)
* [Weekly Meeting Minutes](https://docs.google.com/document/d/1YdpEVhtyCKvwFtXR7cn1Kn2Xc_tdNskoFnhHmFPbtA4/edit#heading=h.w7l85jeih9j6)
* [Project Calendar](https://calendar.google.com/calendar/u/0/embed?src=ena2n7rlpb6sj14llroc274uvs@group.calendar.google.com)
* [Youtube Channel](https://www.youtube.com/channel/UCwvtktvdZu_pg-t-INvuW5g)
