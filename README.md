# Containerlab Hello World

## How to use

First, deploy the topology, either by cloning the repository and deploying it:

```
git clone https://github.com/vista-/clab-helloworld
cd clab-helloworld
containerlab deploy
```

or by using the shorthand for deploying a remote topology:

```
containerlab deploy -t https://github.com/vista-/clab-helloworld
```

To test the deployed topology, run a ping from `host1` to `host2`:

```
$ docker exec clab-helloworld-host1 ping 10.0.0.2
PING 10.0.0.2 (10.0.0.2): 56 data bytes
64 bytes from 10.0.0.2: seq=0 ttl=64 time=1.037 ms
```

And you're done!

You can then destroy the topology by doing a `containerlab destroy -t https://github.com/vista-/clab-helloworld`.
