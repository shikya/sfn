# SFN -  Reverse NFS
Reversed Network File System

## Goals

TLDR; Enable file sharing behind NAT

Files/Folders behind the NAT are getting updated or listed in system X.

System Y can be used as a proxy to list, update, create, delete files of the X.

Files/Folders can be mouted as a virtual Files/Folders in the hosted service, Hence giving a look and feel as a native file.

This will allow to remount/link the files to any other service. And server Y can be act like a Files/Folders proxy server to the internet.

## Basic Assumption

System Y must have a static ip or DNS attched.

System X may or may not have static ip or DNS attached

Senario A: If a static ip or DNS is attached then it is better to use any NFS protocols

SFN does not want to replace senario A, It is only suitable for senario in Goals

## Standard Usage

SFN will come with 2 services. A and B.

1. Source(A) - to be installed on system X
2. Destination(B) - to be installed on system Y

### Flow

#### for B
B is to be installed on any internet exposed system

Once B is started a port will be opened to recive communicatiobn requests/data from A.

A request from A will come to create a bidirectional channel

#### for A

A is installed on system where internet can be accessed.

Once installed, A can be given a directory which files can be shared to B.

Address of B can be added in config to create a bidirection channel.

A will periodically send status and query for pending commands.


## Communication protocol options

* gRPC over HTTP
* REST
* WebSocket
* BOSH
* Server-sent events
* HTTP/2
* WebRTC
* server push
* REST
* IPFS
* Chia
