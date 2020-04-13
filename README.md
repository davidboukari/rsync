# rsync

```bash
# rsync source destination
rsync -az source login@serveur.org:/destination

# Exclude files 
rsync -az --exclude="nom_de_dossier" source login@serveur.org:/destination

# Exclusion file
cat ExclusionRSync
tmp
.Trash
.cache
.PlayOnLinux

rsync -az --exclude-from=ExclusionRSync source login@serveur.org:/destination
 
```

```
    -a ou --archive : est un moyen rapide de dire que vous voulez la récursivité et préserver pratiquement tout. La seule exception est que si --files-from a été spécifiée alors -r n'est pas utilisée. Ceci est équivalent à -rlptgoD.
    -z ou --compress : compresse les données lors du transfert. (Limite la bande passante mais augmente l'utilisation processeur et le temps de transfert : inutile en réseau local ou avec très bon débit)

```
