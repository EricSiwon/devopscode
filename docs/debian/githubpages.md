# Github Pages

```console
$ dig devopscode.fr +noall +answer -t A

devopscode.fr.          10800   IN      A       217.70.184.38
```

```console
dig www.devopscode.fr +noall +answer -t A

www.devopscode.fr.      10800   IN      CNAME   ericsiwon.github.io.
ericsiwon.github.io.    3600    IN      A       185.199.108.153
ericsiwon.github.io.    3600    IN      A       185.199.109.153
ericsiwon.github.io.    3600    IN      A       185.199.110.153
ericsiwon.github.io.    3600    IN      A       185.199.111.153
```


```console
dig www.devopscode.fr +nostats +nocomments +nocmd

;www.devopscode.fr.             IN      A
www.devopscode.fr.      10800   IN      CNAME   ericsiwon.github.io.
ericsiwon.github.io.    3600    IN      A       185.199.110.153
ericsiwon.github.io.    3600    IN      A       185.199.111.153
ericsiwon.github.io.    3600    IN      A       185.199.108.153
ericsiwon.github.io.    3600    IN      A       185.199.109.153
```

```console
dig devopscode.fr +nostats +nocomments +nocmd
;devopscode.fr.                 IN      A
devopscode.fr.          4927    IN      A       217.70.184.38
```

After Mise a jour DNS

dig devopscode.fr +nostats +nocomments +nocmd
;devopscode.fr.                 IN      A
devopscode.fr.          10739   IN      A       185.199.108.153
devopscode.fr.          10739   IN      A       185.199.111.153
devopscode.fr.          10739   IN      A       185.199.110.153
devopscode.fr.          10739   IN      A       185.199.109.153

dig www.devopscode.fr +nostats +nocomments +nocmd
;www.devopscode.fr.             IN      A
www.devopscode.fr.      10713   IN      CNAME   ericsiwon.github.io.
ericsiwon.github.io.    3466    IN      A       185.199.108.153
ericsiwon.github.io.    3466    IN      A       185.199.111.153
ericsiwon.github.io.    3466    IN      A       185.199.109.153
ericsiwon.github.io.    3466    IN      A       185.199.110.153

dig www.devopscode.fr +noall +answer -t A
www.devopscode.fr.      10668   IN      CNAME   ericsiwon.github.io.
ericsiwon.github.io.    3421    IN      A       185.199.110.153
ericsiwon.github.io.    3421    IN      A       185.199.108.153
ericsiwon.github.io.    3421    IN      A       185.199.111.153
ericsiwon.github.io.    3421    IN      A       185.199.109.153

dig devopscode.fr +noall +answer -t A
devopscode.fr.          10657   IN      A       185.199.109.153
devopscode.fr.          10657   IN      A       185.199.108.153
devopscode.fr.          10657   IN      A       185.199.111.153
devopscode.fr.          10657   IN      A       185.199.110.153