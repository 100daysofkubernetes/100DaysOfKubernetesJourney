# Runecast Analyzer for Kubernetes - KubeCon wrap up reading

## Introduction
I reached out to [Kev Johnson](https://twitter.com/kev_johnson) from Runecast, so that I could deploy their tool and analyze a Kubernetes cluster. [Runecast implements](https://www.runecast.com/blog/runecast-analyzer-4-5-introduces-kubernetes-best-practices-security-checks) checks against the [CIS Benchmark for Kubernetes](https://www.cisecurity.org/benchmark/kubernetes/). I did actually find an issue with their deployment in my lab, Kev connected me to one of their engineers to look into it and help resolve. I believe this made them rethink their Helm Chart configuration too. Great service especially as I was just poking around at the software. 

Runecast have a great solution for monitoring complaince in your environment for a number of your platforms, and they are rapidly expanding to additional platorms as well.

Kubecon finished a few days ago, but I've not even scratched the surface and there's too much I need to go back and watch, or watch again!
## Research
- [3 Key Takeaways from KubeCon EU 2021](https://thenewstack.io/3-key-takeaways-from-kubecon-eu-2021/)
- [KubeCon EU 2021 Recap - A Celebration of Kubernete](https://www.weave.works/blog/kubecon-eu-2021-recap-a-celebration-of-kubernetes)
- [This Week in Programming: What’s the Takeaway of KubeCon EU 2021?](https://thenewstack.io/this-week-in-programming-whats-the-takeaway-of-kubecon-eu-2021/)
- [KubeCon EU 2021: Developers, Developers, Developers (and Control Planes)](https://blog.getambassador.io/kubecon-eu-2021-developers-developers-developers-and-control-planes-1ed8f9bd5703)
- [KubeCon Europe 2021 Wrapup](https://loft.sh/blog/kubecon-europe-2021-wrapup/)
- [KubeCon EU 2021: Tetrate Takeaways](https://www.tetrate.io/blog/kubecon-eu-2/)
## Try yourself
- Runecast - you can deploy the analyzer directly in your kubernetes cluster [using Helm](https://helm.runecast.com/#examples) or you can run it outside of the cluster and then connect it using a service account. See the documentation. 
  - [Get a Runecast NFR](https://vexpert.runecast.com/free-runecast-nfr-license)
  - [Get a trial for Runecast software](https://portal.runecast.com/registration)
