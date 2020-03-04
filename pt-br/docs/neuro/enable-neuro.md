Title: Ativar o Neuro

# Ativar o Neuro

Para a integração 4biz/Neuro funcionar, você deve:

- Ter a versão 8.0.0.0 ou superior da 4biz
- Ter o 4biz configurado para acesso HTTPS: //
- Ter os parâmetros de integração configurados no 4biz


![Neuro Conection][1]

- **Parâmetro 309:**

    ```sh
    Value: Yes
    ```

- **Parâmetro 310:**

Exemplo:

    ```sh
    https://localhost:8443/cit-esi-web
    ```

- **Parâmetro 311:**

Exemplo:

    ```sh
    citsmart.local\neuro.user
    ```
    

!!! success "USUÁRIO NEURO"
    Para que a integração funcione corretamente é necessário que o usuário de serviço criado para o Neuro contenha no campo login o atributo de identificação do domínio, ou seja, "citsmart.local" (ex. O usuário "Neuro" deverá ter no campo login a seguinte informação  "citsmart.local\neuro.user").


[1]:images/neuro-conection.png
