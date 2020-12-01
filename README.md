


## Articles

 - [Faasd with Caddy & Terraform](https://www.openfaas.com/blog/faasd-tls-terraform/) - demonstrates Caddy for Let's Encrypt as well as usage of secrets.


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
