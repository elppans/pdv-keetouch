# pdv-keetouch
### Instalação do driver "KeeTouch Touchscreen" no Ubuntu 22.04

- **Sistema operacional utilizado:** InstaladorPDV-2.U2204.519.1.10-64  
- **Identificação do driver (via `lsusb`):**  
  `Bus 001 Device 002: ID 1aad:0001 KeeTouch Touchscreen`  
- **Pacote:** `linuxupdd_05.01.1431_64.tgz`

---

### Etapas de instalação (via interface gráfica):

```
mkdir -p ~/driver
cp linuxupdd_05.01.1431_64.tgz ~/driver
cd ~/driver
tar -zxvf linuxupdd_05.01.1431_64.tgz
./setup
```

Durante o processo, será exibida uma janela de configuração. Selecione a opção:  
**KeeTouch, USB Series, USB**

![Imgur](https://i.imgur.com/F1wb9DF.png)

Após a instalação, clique em **"Close"** na janela final e reinicie o sistema com o comando:

<img title="" src="https://i.imgur.com/oLZEFRy.png" alt="" data-align="center">

```
reboot
```

### Pós instalação

Após a instalação do driver, a **marca do touch é reconhecida corretamente**, conforme retorno do comando:  
   

```
xinput --list
```

![linuxupdd_05.01.1431_64-003](https://i.imgur.com/fHrNX5f.png)

___

## Calibrar o Touch

Vá até o diretório "`/opt/tbupddlx`" e faça o comando para calibrar e manter as configurações de coordenadas:

> Para a configuração, deve ter comunicação externa, senão não será possível configurar

```
./upddcalib
```

![linuxupdd_05.01.1431_64-004](https://i.imgur.com/7b0nNgn.png)

Após a calibração, o touch irá funcionar normalmente. Para testar se funciona após iniciar, reinicie o sistema.

![linuxupdd_05.01.1431_64-005](https://i.imgur.com/gjGta0X.png)
