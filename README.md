# sfn
Reverse Network File System

## Goals

Files/Folders behind the NAT are getting updated or listed in system X.

System Y can be used as a proxy to list, update, create, delete files of the X.

Files/Folders can be mouted as a virtual Files/Folders in the hosted service, Hence giving a look and feel as a native file.

This will allow to remount/link the files to any other service. And server Y can be act like a Files/Folders proxy server to the internet.

## Basic Assumption

System Y must have a static ip or DNS attched.

System X may or may not have static ip or DNS attached

Senario A: If a static ip or DNS is attached then it is better to use any NFS protocols

SFN does not want to replace senario A, It is only suitable for senario in Goals


## Communication protocol options

* gRPC
* REST
* WebSocket
* BOSH
* Server-sent events
* HTTP/2
* WebRTC
* server push
* REST
