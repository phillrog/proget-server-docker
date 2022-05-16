# proget-server-docker
Com o proget é possível criar um servidor para hospedar pacotes. Montar um docker registry privado e muito mais.


# Como rodar ?

Acessar https://my.inedo.com/, criar uma conta e aderir uma licença FREE. 

![image](https://user-images.githubusercontent.com/8622005/168664019-fe8de029-2601-436f-840d-1fe8079868bb.png)

Em seguida executar ```docker-compose up```, navegar até http://localhost/administration/licensing e colocar a licença lá.
Assim será possível criar os repositórios.

![image](https://user-images.githubusercontent.com/8622005/168664298-2f496bcb-eecc-483a-ba14-fef5ed0f7a9a.png)

# Exemplo utilizado

### Imagem de teste
```docker pull hello-world```

### Uma nova tag
 ```docker tag hello-world localhost/docker-registry-local/hello-world:proget_v1```
 
### Login
docker login localhost/docker-registry-local/

Obs: Utilizar usuário Admin e senha Admin ou trocar a senha.

### Push
``` docker push  localhost/docker-registry-local/hello-world:proget_v1```

# Resultado

![image](https://user-images.githubusercontent.com/8622005/168663640-e09e6f43-bb64-48e5-8a43-01141ebd29bc.png)

