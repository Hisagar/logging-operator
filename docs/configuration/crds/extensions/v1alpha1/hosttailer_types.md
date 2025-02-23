---
title: HostTailer
weight: 200
generated_file: true
---

## HostTailerSpec

HostTailerSpec defines the desired state of HostTailer

### fileTailers ([]FileTailer, optional) {#hosttailerspec-filetailers}

List of file tailers 

Default: -

### systemdTailers ([]SystemdTailer, optional) {#hosttailerspec-systemdtailers}

List of systemd tailers 

Default: -

### enableRecreateWorkloadOnImmutableFieldChange (bool, optional) {#hosttailerspec-enablerecreateworkloadonimmutablefieldchange}

EnableRecreateWorkloadOnImmutableFieldChange enables the operator to recreate the daemonset (and possibly other resource in the future) in case there is a change in an immutable field that otherwise couldn't be managed with a simple update. 

Default: -

### workloadMetaOverrides (*types.MetaBase, optional) {#hosttailerspec-workloadmetaoverrides}

Override metadata of the created resources 

Default: -

### workloadOverrides (*types.PodSpecBase, optional) {#hosttailerspec-workloadoverrides}

Override podSpec fields for the given daemonset 

Default: -


## HostTailerStatus

HostTailerStatus defines the observed state of HostTailer


## HostTailer

HostTailer is the Schema for the hosttailers API

###  (metav1.TypeMeta, required) {#hosttailer-}

Default: -

### metadata (metav1.ObjectMeta, optional) {#hosttailer-metadata}

Default: -

### spec (HostTailerSpec, optional) {#hosttailer-spec}

Default: -

### status (HostTailerStatus, optional) {#hosttailer-status}

Default: -


## HostTailerList

HostTailerList contains a list of HostTailer

###  (metav1.TypeMeta, required) {#hosttailerlist-}

Default: -

### metadata (metav1.ListMeta, optional) {#hosttailerlist-metadata}

Default: -

### items ([]HostTailer, required) {#hosttailerlist-items}

Default: -


## FileTailer

FileTailer configuration options

### name (string, required) {#filetailer-name}

Name for the tailer 

Default: -

### path (string, optional) {#filetailer-path}

Path to the loggable file 

Default: -

### disabled (bool, optional) {#filetailer-disabled}

Disable tailing the file 

Default: -

### containerOverrides (*types.ContainerBase, optional) {#filetailer-containeroverrides}

Override container fields for the given tailer 

Default: -


## SystemdTailer

SystemdTailer configuration options

### name (string, required) {#systemdtailer-name}

Name for the tailer 

Default: -

### path (string, optional) {#systemdtailer-path}

Override systemd log path 

Default: -

### disabled (bool, optional) {#systemdtailer-disabled}

Disable component 

Default: -

### systemdFilter (string, optional) {#systemdtailer-systemdfilter}

Filter to select systemd unit example: kubelet.service 

Default: -

### maxEntries (int, optional) {#systemdtailer-maxentries}

Maximum entries to read when starting to tail logs to avoid high pressure 

Default: -

### containerOverrides (*types.ContainerBase, optional) {#systemdtailer-containeroverrides}

Override container fields for the given tailer 

Default: -


