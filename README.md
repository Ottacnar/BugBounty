# BugBounty
Tools for Recon


# Recon de Subdomínos

- [Chaos](https://github.com/projectdiscovery/chaos-client)

###  .bashrc shortcut OFJAAAH

```bash
reconjs(){
gau -subs $1 |grep -iE '\.js'|grep -iEv '(\.jsp|\.json)' >> js.txt ; cat js.txt | anti-burl | awk '{print $4}' | sort -u >> AliveJs.txt
}
cert(){
curl -s "[https://crt.sh/?q=%.$1&output=json](https://crt.sh/?q=%25.$1&output=json)" | jq -r '.[].name_value' | sed 's/\*\.//g' | anew
}
anubis(){
curl -s "[https://jldc.me/anubis/subdomains/$1](https://jldc.me/anubis/subdomains/$1)" | grep -Po "((http|https):\/\/)?(([\w.-]*)\.([\w]*)\.([A-z]))\w+" | anew
}
```
