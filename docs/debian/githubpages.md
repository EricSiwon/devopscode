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

dig _github-pages-challenge-ericsiwon.github.io +nostats +nocomments +nocmd TXT