# Ciclo-de-vida-da-activity-

# Aluno : Renê César 

# Clico de vida 
- A classe Activity é quem gerencia a interface com o usuário, ela quem recebe as requisições, as trata e processa.

1 - onCreate(): Ela é a primeira função a ser executada em uma Activity, geralmente a responsável por carregar os layouts do XML e outras operações de inicialização e é executada apenas uma vez. O parâmetro savedInstanceState contém os dados da instância anterior da atividade, caso ela esteja sendo recriada após uma mudança de configuração, como rotação da tela.

2 - onStart(): É chamada imediatamente após a onCreate() e também quando uma Activity que estava em background volta a ter foco,no caso a atividade se torna visível para o usuário. Você pode implementar aqui comportamentos que devem ocorrer toda vez que a atividade se tornar visível, como registrar ouvintes de eventos.

3 - onResume(): Assim como a onStart(), é chamada na inicialização da Activity e também quando uma Activity volta a ter foco. E qual a diferença entre as duas? A onStart() só é chamada quando a Activity não estava mais visível e volta a ter o foco, a onResume() é chamada nas “retomadas de foco”. Você pode iniciar animações, inicializar componentes que consomem CPU ou iniciar serviços que devem ser executados continuamente.

4 - onPause(): É a primeira função a ser invocada quando a Activity perde o foco (isso ocorre quando uma nova Activity é iniciada). Geralmente usado para parar animações, pausar processamentos que não são necessários enquanto a atividade não está visível, ou salvar dados que devem persistir entre mudanças de configuração.

5 - onStop(): Só é chamada quando a Activity fica completamente encoberta por outra Activity. Usado para liberar recursos que não são mais necessários quando a atividade não está ativa.

6 - onDestroy(): A última função a ser executada depois dela a Activity é considerada “morta” ou seja nao pode mais ser relançada, se o usuário voltar a requisitar essa Activity um novo objeto será contruído. Onde deve liberar todos os recursos que a atividade está segurando, como conexões de banco de dados, recursos não gerenciados,entre outros. 

7 - onRestart(): É chamada imediatamente antes da onStart(), quando uma Activity volta a ter o foco depois de estar em background. Sendo chamada quando a atividade está sendo reiniciada após ser parada.

Com esses métodos permite uma experiência de usuário fluida e eficiente.


