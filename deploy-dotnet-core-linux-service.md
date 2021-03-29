# Deploy ASP .Net Core on Linux Server

## Notas

* Certifique-se que você use uma conta de usuário com as permissões necessárias

* Certifique-se de usar um serviço de Web Instalado ([Apache](https://docs.microsoft.com/pt-br/aspnet/core/host-and-deploy/linux-apache?view=aspnetcore-5.0) ou [Nginx](https://docs.microsoft.com/pt-br/aspnet/core/host-and-deploy/linux-nginx?view=aspnetcore-5.0))

* Certifique-se o site está previamente configurado

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

