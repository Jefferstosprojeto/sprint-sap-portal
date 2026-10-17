# Sprint 28 dias — SAP HANA Cloud · Datasphere · SAC

Portal de estudos e de mercado: plano diário de 28 dias (2–3h/dia) para reativar
SAP HANA Cloud, aprender SAP Datasphere e explorar BW Bridge, com links para cursos
oficiais gratuitos da SAP, tutoriais hands-on e vídeos.

**Abrir:** https://jefferstosprojeto.github.io/sprint-sap-portal/

## Aba Sprint

- Plano dia a dia com objetivo e carga horária
- Links para SAP Learning, developers.sap.com e YouTube
- Mapa de tradução BW/4HANA → Datasphere
- Progresso marcável (guardado no browser)

## Aba Mercado & rates

- Faixas de day rate por país, separando **onshore local** do que chega a quem
  factura de fora — são grandezas diferentes e não se comparam na mesma coluna
- Calculadora da cadeia de intermediação: quanto de um orçamento sobrevive a
  uma e a duas camadas de consultoria
- Contexto do mercado freelance DACH em 2026, a partir do Freelancer-Kompass
  (5.412 respostas, 340.000 perfis)

> A tese que a aba defende: **o preço nearshore não é um preço de mercado — é o
> preço onshore menos as camadas de intermediação.** Logo há duas alavancas para
> o subir, e não uma: trocar de mercado sobe o topo da cadeia, encurtar a cadeia
> sobe a fatia que fica connosco.

Os números de rate são referências de estudos públicos, e o modelo de margens está
explicitamente assinalado na própria página como estimativa, não como medição.

## Aba Candidaturas + career-ops

A fila de vagas desta aba liga-se ao [career-ops](https://github.com/career-ops-hq/career-ops),
instalado localmente em `..\career-ops` (fora deste repositório: o CV e os relatórios
nunca são publicados).

```
cd ..\career-ops
node sync-portal.mjs --import   # fila do portal -> data/pipeline.md (só anúncios diretos, sem duplicados)
claude                          # depois: /career-ops pipeline  (avalia, gera CV e carta)
node sync-portal.mjs            # nota + estado de volta para a aba (bloco careerOpsData no index.html)
```

O botão **Exportar fila para career-ops** na aba faz o mesmo que o `--import`, mas pela
área de transferência. Uma vaga com estado `Applied` (ou mais adiante) no career-ops passa
para *Submetidas*. Só a nota, o estado, a data e se há CV gerado chegam à página.

---

Página única, sem dependências externas. Funciona offline depois de carregada.
