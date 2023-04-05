# wg-deploy

[EN](#wg-deploy-1)

Простой плейбук для конфигурации WireGuard сервера.

Для работы с WireGuard используется коллекция 
[lablabs.wireguard](https://github.com/lablabs/ansible-collection-wireguard).

### Пример использования

```shell
ansible-playbook create.yaml -e hostname=my.wireguard.server
```

Так же `hostname` будет запрошен интерактивно в случае, если не был задан через `-e`. 

### Использование для других клиентов

Текущее решение содержит конфигурацию клиентов, для другой конфигурации
измените значение `wireguard_peers` в `inventory/main.yaml`. Так же на разных
дистрибутивах и в разных облачных решениях может отличаться значение
`wireguard_out_interface`.

---

# wg-deploy

[RU](#wg-deploy)

A simple playbook for configuring WireGuard server.

For all wireguard interaction [lablabs.wireguard](https://github.com/lablabs/ansible-collection-wireguard)
collection is used.

### Example usage

```shell
ansible-playbook create.yaml -e hostname=my.wireguard.server
```

You can skip defining `hostname` variable.
In this case it will be prompted interactively.

### Other clients usage

Current inventory contains list of clients in `wireguard_peers`,
it is defined at `inventory/main.yaml`.
Note that `wireguard_out_interface` can differ depending on OS and network configuration.
