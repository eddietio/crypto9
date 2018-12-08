# ETHSINGAPORE - Team Crypto9 (Hammad Tariq & Eddie Tio)

Decentralized Exchange that makes use of on-chain liquidity pools - supporting Kyber.

## Getting Started

These instructions will get you a copy of the project up and running on your local machine for testing purposes.

### Prerequisites

You will need to have docker and docker-compose installed in your environment.

### Installing

Create a new folder named crypto9 and clone the repository in the empty folder.
```
git clone https://github.com/eddietio/crypto9.git 
```

Change the volume bindings to relevant paths on your system in docker-compose.yml

```
    - "<PATH TO SOME FOLDER>/ipfs-docker-staging:/export"
    - "<PATH TO SOME FOLDER>/ipfs-docker-data:/data/ipfs"
    - "<PATH TO CURRENT FOLDER>/ipfs/data:/root"
```

Run docker-compose up to bring up the ipfs container
```
docker-compose up
```

Add the files folder to ipfs

```
docker container exec -it ipfs-node ipfs add files -r 
```

The last hash returned will be used to access the site

```
http://ipfs.io/ipfs/<HASH>
```

## Built With

* [Bootstrap 4.1.3](https://getbootstrap.com/) - The web framework used
* [Kyber](https://https://kyber.network/) - On-chain liquidity protocol
* [JQuery](https://jquery.com/) - Javascript library



## Authors

* **Hammad Tariq** - (https://github.com/hammadtq)
* **Eddie Tio** - (https://github.com/eddietio)


## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details

## Acknowledgments

* Thanks to the organizers, volunteers and participants of ETHSINGAPORE 2018.