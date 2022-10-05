# GPG configuring steps using Scoop

Get [Scoop](https://scoop.sh/)

## Configuring GPG signing

GitHub [steps](https://docs.github.com/en/authentication/managing-commit-signature-verification/generating-a-new-gpg-key#generating-a-gpg-key) for generating GPG key

Commands used
```powershell
gpg --full-generate-key
```

```powershell
gpg --list-secret-keys --keyid-format=long
```

```powershell
gpg --armor --export [GPG key ID]
```

### Configuring local GitHub
```powershell
git config --global user.signingkey [GPG key ID]
```
```powershell
git config --global commit.gpgsign true
```
```powershell
git config --global gpg.program "C:\Users\currentUser\scoop\apps\gpg\current\bin\gpg.exe"
```