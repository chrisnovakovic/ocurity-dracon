subinclude("//build/defs:dracon")

dracon_pipeline(
    name = "python-project",
    components = [
        "//components/base:k8s",
        "//components/consumers/mongodb:k8s",
        "//components/consumers/elasticsearch:k8s",
        "//components/enrichers/aggregator:k8s",
        "//components/enrichers/deduplication:k8s",
        "//components/producers/aggregator:k8s",
        "//components/producers/python-bandit:k8s",
        "//components/producers/python-pip-safety:k8s",
        "//components/sources/git:k8s",
    ],
    kube_context = "//build/k8s/k3d:dracon",
    kustomization_yaml = "kustomization.yaml",
    pipelinerun = "pipelinerun/pipelinerun.yaml",
)
