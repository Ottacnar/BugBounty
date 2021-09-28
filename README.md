# BugBounty
Tools for Recon
- [Amass](https://github.com/OWASP/Amass)
- [Assetfinder](https://github.com/tomnomnom/assetfinder)
- [Chaos](https://github.com/projectdiscovery/chaos-client)
- [Findomain](https://github.com/Findomain/Findomain)
- [Haktrails](https://github.com/hakluke/haktrails)
- [Subfinder](https://github.com/projectdiscovery/subfinder)

# Recon de Subdomínos

###  Busca por subdomíos, retirando os duplicados com ANEW

```
amass enum -d <domain> -o <subs>

```
```
assetfinder -subs_only <domain> | anew <subs>

```
```
chaos -d <domain> | anew <subs>

```
```
findomain -t <domain> -q -u <subs>

```
```
echo "domain" | haktrails subdomains| anew <subs>

```
```
subfinder -d <domain> | anew <subs>

```
