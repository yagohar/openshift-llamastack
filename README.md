# llamastack on openshift Manual
## documentation used
https://docs.google.com/document/d/1IfOfdZ9FjU1fQdLTGso0Ikg-j2uL9XZXem4jbZQSq6w/edit?tab=t.0
[
](https://github.com/opendatahub-io/llama-stack-k8s-operator/blob/odh/docs/odh/llama-stack-with-odh.md)
This is repo to replicate the llamastack work

```
root@bastion:~/development/openshift-ai/openshift-llamastack# oc get pods -n llama-agents
NAME           READY   STATUS    RESTARTS   AGE
llamaagent-0   2/2     Running   0          11m
root@bastion:~/development/openshift-ai/openshift-llamastack# oc get pods -n llama-stack-k8s-operator-system
NAME                                                           READY   STATUS    RESTARTS   AGE
llama-stack-k8s-operator-controller-manager-55fbf58664-vkn9d   1/1     Running   1          44h
root@bastion:~/development/openshift-ai/openshift-llamastack# oc get pods -n llama-user
No resources found in llama-user namespace.
root@bastion:~/development/openshift-ai/openshift-llamastack# oc get pods -n llama-dist
No resources found in llama-dist namespace.
root@bastion:~/development/openshift-ai/openshift-llamastack# oc get pods -n ollama-dist
NAME                                            READY   STATUS                            RESTARTS      AGE
llamastackdistribution-sample-6b8747758-96w7s   1/1     Running                           4 (41h ago)   44h
llamastackdistribution-sample-7d4cb86fc-2fmw2   0/1     Init:CreateContainerConfigError   0             43h
ollama-server-67b87d7fd6-ltpcd                  1/1     Running                           1             44h
root@bastion:~/development/openshift-ai/openshift-llamastack# oc get deployment -n ollama-dist
NAME                            READY   UP-TO-DATE   AVAILABLE   AGE
llamastackdistribution-sample   1/1     1            1           44h
ollama-server                   1/1     1            1           44h
root@bastion:~/development/openshift-ai/openshift-llamastack#
```
