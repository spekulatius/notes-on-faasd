


## Articles

 - [Faasd with Caddy & Terraform](https://www.openfaas.com/blog/faasd-tls-terraform/) - demonstrates Caddy for Let's Encrypt as well as usage of secrets.


## Videos

 - [Hands-on with faasd & Inlets](https://www.youtube.com/watch?v=AFx0Wap3Z8E)
 - [faasd walk-through with cloud-init and Multipass](https://www.youtube.com/watch?v=WX1tZoSXy8E)
 - [Meet Derek, the contribution bot for GitHub](https://www.youtube.com/watch?v=ibPwVggXAFI)


## Handy One-Liners

Mostly utilizing [faas cli](https://github.com/openfaas/faas-cli) here are some one-liners to shortcut typing:

### Login

```bash
export IP="faas1" &&
export PASSWORD=$(ssh root@$IP "sudo cat /var/lib/faasd/secrets/basic-auth-password") &&
export OPENFAAS_URL=http://$IP:8080 &&
echo $PASSWORD | faas-cli login --password-stdin
```

You can also use a hostname as IP.
