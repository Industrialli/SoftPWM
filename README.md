# SoftPWM

Implementação do PWM via software para controlar saidas digitais isoladas da Industrialli Hub.
Problemas:
  -Delay do ISO1H812G em Turn-On e Turn-Off de 64us ~ 170us;
  -Para altas frêquencias o sinal PWM é comprometido;
  -Devido ao fato do PWM via software necessitar de um loop sem preempção para gerar o sinal PWM, a função PWM deve ser a única em execução no processador.

Soluções:
  -Um IC superior ao ISO1H812G;
  -Utilizaliçao de threads para softPWM;
  -Implementação do PWM via hardware.
