
### **Projeto: Alimentador Automático com Arduino**

**Componentes Principais:**
- **Arduino**: Microcontrolador responsável por gerenciar todas as funções do sistema.
- **Display LCD I2C**: Interface para exibir informações como o tempo de contagem, modos de operação, e status do sistema.
- **4 Botões**: Utilizados para interagir com o sistema, configurando tempos e iniciando/parando o alimentador.
- **Motor ou Relé**: Acionado para liberar a comida no momento programado.

**Funcionalidades:**

1. **Interface com Display LCD I2C**:
   - O display LCD exibe o tempo restante ou o tempo decorrido, dependendo do modo selecionado.
   - As informações mostradas incluem o status do alimentador (ativado ou desativado) e o modo de contagem (crescente ou decrescente).

2. **Botões de Controle**:
   - **Botão 1 (Iniciar/Parar)**: Inicia ou para o temporizador.
   - **Botão 2 (Modo Crescente/Decrescente)**: Alterna entre o modo de contagem crescente (cronômetro) e decrescente (timer).
   - **Botão 3 (Ajuste de Tempo)**: Aumenta ou diminui o tempo desejado para a contagem (em segundos, minutos, etc.). Pode funcionar em conjunto com o botão 4 para ajuste preciso.
   - **Botão 4 (Confirmação/Reset)**: Confirma a configuração do tempo ou reseta o temporizador.

3. **Temporizador**:
   - O temporizador pode operar em dois modos: **crescente** (cronômetro) e **decrescente** (timer).
   - No modo **crescente**, o tempo começa em zero e aumenta até que o usuário pare a contagem manualmente.
   - No modo **decrescente**, o usuário define um tempo, e o temporizador conta de trás para frente até chegar a zero.
   - Quando o tempo atinge zero no modo decrescente, ou ao atingir o tempo máximo pré-definido no modo crescente, o Arduino envia um pulso para ativar o motor ou relé.

4. **Ativação do Motor ou Relé**:
   - O motor ou relé é acionado no final da contagem (quando o tempo chega a zero ou atinge o tempo máximo).
   - Este acionamento libera a quantidade pré-determinada de comida para o alimentador.

5. **Indicação de Status**:
   - O display LCD também pode indicar mensagens de status, como "Alimentador Ativado", "Tempo Restante: 00:00", "Modo: Crescente", etc.
   - LEDs podem ser adicionados para indicar visualmente o status do sistema (opcional).

**Aplicações:**
- Ideal para alimentar automaticamente animais de estimação em horários específicos.
- Pode ser adaptado para outras aplicações que requerem temporização precisa e acionamento de mecanismos.
