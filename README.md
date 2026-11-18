# bPlayer

> [!IMPORTANT]
> **Archived — part of [Charon](https://github.com/unau-thorized/Charon-ClientSideMultimedia)**, a proof of concept (2020–2021) for client-side multimedia playback over SPICE. The concept was tested and worked. This repository contains the guest-side frontend and the client-side backend. See the Charon README for architecture, security & risk assessment, and possible improvements.

> [!CAUTION]
> **Use entirely at your own risk.** Experimental, unmaintained code provided "AS IS", without warranty of any kind and without support. It has known security weaknesses and is not suitable for production. The author shall not be liable for any claim, damage, or other liability arising from its use. See the [full disclaimer](https://github.com/unau-thorized/Charon-ClientSideMultimedia#disclaimer).

bPlayer Frontend / Backend

Status: Working prototype, very early stage

Test Configuration: 
1) Linux OS, Direct connection  (local socket), Backend <--> Frontend
2) Conduit connection (Linux Host / Windows Guest) Backend <--> Remote-Viewer <--> ConduitD <--> Frontend
  - Backend <--> Remote-Viewer patched : port automatically guessed by Backend
  - Remote-Viewer <--> ConduitD : specified in VM XML description
  - ConduitD <--> Frontend : conduit Listen on localhost:60999, frontend connect as tcp client
