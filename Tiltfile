def create_namespace(name):
    k8s_yaml(blob("""apiVersion: v1
kind: Namespace
metadata:
  name: %s
""" % name))

name = "chaos-mesh"

create_namespace(name)

k8s_yaml(helm("charts/chaos-mesh", name = "%s-operator" % name, namespace = name))
