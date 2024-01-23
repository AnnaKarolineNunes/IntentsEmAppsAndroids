## Criando intents em Apps Android com java

## Descrição
Em Android com Java, um "intent" é um objeto que representa a intenção de realizar uma ação, como iniciar uma nova atividade (tela), enviar uma mensagem de broadcast, ou iniciar um serviço. Intents são usados para facilitar a comunicação entre diferentes componentes do aplicativo ou entre aplicativos distintos no sistema Android. Eles carregam informações sobre a ação desejada e podem incluir dados adicionais, como parâmetros ou mensagens. Intents são fundamentais para a interação e coordenação de atividades dentro de um aplicativo Android.

## Capturas de Tela

![image](https://github.com/AnnaKarolineNunes/IntentsEmAppsAndroids/assets/101477642/8a347add-3321-4c25-8a5d-2e07b6a20b20)

## Passo a passo de como criar uma intent para realizar a ação de ligação

Se desejarmos, por exemplo, direcionar o usuário automaticamente para uma chamada telefônica a partir de uma tela específica, devemos seguir estes passos:

- Passo 1 No arquivo AndroidManifest.xml, entre as tags <package> e <application>, adicione a seguinte permissão para solicitar ao usuário a permissão para realizar chamadas telefônicas no aplicativo:
  ```
  <?xml version="1.0" encoding="utf-8"?>
  <manifest xmlns:android="http://schemas.android.com/apk/res/android"
    package="com.cursoandroid.appatmconsultoria">
  
    <uses-permission android:name="android.permission.CALL_PHONE" />
  
    <application ... >
  </manifest>

- Passo 2  É necessário realizar uma validação de permissão. No arquivo MainActivity.java, crie um método antes do método OnSupportNavigateUp(), e implemente uma intent para a ação desejada utilizando startActivity()
  ```
    public void enviarEmail(){
        Intent intent = new Intent( Intent.ACTION_DIAL, Uri.parse("tel:01199763486"));
        startActivity( intent ); // faz a intent, abrindo o app que faz ligaçoes 
    }

Nota: Lembre-se de adaptar os detalhes conforme necessário para atender às necessidades específicas do seu aplicativo.
