# ourCloud
---- 
## About
This project is spawned from me (Bastian Inuk Christensen) being a huge sufferer of NIH (Not Invented Here) syndrome, and also being incredibly in love with swift.
---- 
## Installation
TBD
---- 
## Goals and wishes
I decided to start a cloud storage solution that does two things, which later is going to be expanded.
1. Serve as a cloud storage solution anyone can access from anywhere in the world.
2. Talk with Samba and Netatalk, to _also_ deliver data over home networks.
And later I wish to expand with a plugin system. This will likely be a set of microservices, that conforms to a standard, and if done as wished, don’t even have to be coded in Swift, but can coded in any language the author wishes!
---- 
## Plugin structure
The plugin system has yet to be made, and is far from being under development.

I (Bastian) propose we separate plugins into small programs. We use _REST_ for the plugins to talk to the host. The proposed lifecycle goes as follows:
1. The user runs any plugin on their system, in a docker, jail, another port or a remote device.
2. On the host service, the user tells the host service (later the plugin has to announce itself somehow) how to find the plugin (**IP**:**PORT**) and maybe even credentials. Unless there’s configurations on the plugin, the user doesn’t have to do anything from here.
3. The plugin will tell the host what it _can_ handle, the specs has to be figured out later, and when getting a request from the host, it has to be able to return HTML & JSON for any request, unless we figure something out.
This is a _MASSIVE_ project, I realise that, and once it’s somewhat stable, it’ll be spun out into it’s own package.
---- 
## Contribute
Fork and merge, this project is FOSS, and will stay that way forever, and by nature, that means you as a user can contribute your own code to the project, be mindful that we take pride in the code being purely Swift.’
---- 


