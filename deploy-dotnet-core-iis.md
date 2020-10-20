# Deploy ASP .Net Core on IIS Server (Windows)

## Notas

* [Permita o uso de Scripts Externos no Powershell ](https://docs.microsoft.com/en-us/powershell/module/microsoft.powershell.security/set-executionpolicy?view=powershell-7)

* Certifique-se de possuir o IIS Instalado

* Certifique-se que o site está previamente criado e configurado no IIS

* Mude a versão de acordo com o SDK .Net Core do Projeto

```yaml
    - name: Setup .NET Core
      uses: actions/setup-dotnet@v1
      with:
        dotnet-version: $version
```

* Ajuste o caminho de Deploy

```yaml
    - name: Publish
      run: dotnet publish -c Release -o ${{path}}/${{sitefolder}}  
```

