# coco_notes
Notes and scripts I find interesting with coco

# Identify all pods using coco/osc/
    oc get pods -A -o json | jq '.items[] | select(.spec.runtimeClassName == "kata-remote") | "\(.metadata.namespace)/\(.metadata.name)"'
