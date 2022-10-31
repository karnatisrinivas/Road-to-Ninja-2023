## 🤔 What is GitOps?

GitOps is a set of practices where the entire application delivery is managed by Git, it includes infra, code as config, automation to update and rollbacks.

## But why????

Let's consider an scenario where your application is deployed in a K8s cluster. Steps followed *without* GitOps:

- First the dev's code, and push to the code repo using a VCS.
- Then the Automated pipelines you already deployed in your code base will perform lint checks,  generate an container image, and push it to docker hub.
- Your image is now stored in your Container registry.
- You might have another automated pipeline, that will have access to your entire cluster create an deployment which will create deploy solution with "kubectl"
- Your application is now deployed.

## This works, but what the concern????

1. You are performing the actions using `kubectl` or by some API.
2. In order to deploy the app, the ci platform you use needs to have full access to the cluster. 

## How this works with GitOps:

- So upto image registry, the steps we perform are same. 
- Here we maintain another repo, which will have all the manifests that we need for our deployment.
- In GitOps, we will install a GitOps controller in the cluster which will continuosly watches our second repo. Any change in the repo will make the changes in cluster. ( Current state to Desired state).



<br>

### Here you have everything managed by git, both source code and deployment. There is no external endpoint with full access to the cluster. GitOps controller which always try to match the current state to the desired state is an plus. 


<br>

## GitOps Key Principles:

- A system managed by GitOps needs its application desired state expressed *Declaratively*.
- Entire system is versioned in git and hold the entire history.
- Changes are approved automatically and applied to system. (Pulled automatically).
- These agents continuosly observe the actual system and apply the changes to meet the desired state.

 
