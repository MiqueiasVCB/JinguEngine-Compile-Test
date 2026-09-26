JINGU ENGINE CLEANUP87 - GITHUB COMPILE KIT (FULL GODOT DEFAULT EXPORT MATRIX + JINGU UWP)
==========================================================================================

OBJETIVO
--------
Compilar TODOS os templates oficiais/padrao da matriz de distribuicao Godot 4.7.x preservada
pela Jingu, sem excluir arquiteturas/variantes oficiais, e adicionar UWP x86_64 como extensao Jingu.

Este kit NAO contem resultados fabricados. O fato de os source gates locais terem passado NAO significa
que os builds GitHub abaixo ja passaram. A compilacao real continua PENDING_NOT_RUN ate o workflow rodar.

ARQUIVOS
--------
- JINGU_ENGINE_CLEANUP87_SOURCE.zip
- JinguEngine_v1.0.0_uwp_templates_x86_64.zip
- .github/workflows/jingu-export-templates.yml
- .github/workflows/jingu-editor-builds.yml

SHA-256 OBRIGATORIOS PARA O WORKFLOW
-------------------------------------
source_sha256:
44d1cb728193847ad0acf087ea028c59149ee4ceae742d449bb5cd06021ce6af

uwp_sha256:
3f65fd860e1421ed22d905e0c1c96dc06b2db7e5c2d5fee6544eca250a6a65cc

MATRIZ DO TPZ FINAL
-------------------
Windows: x86_32, x86_64, arm64 (debug/release + console)
Linux: x86_32, x86_64, arm32, arm64 (debug/release)
Android: arm32, arm64, x86_32, x86_64 -> android_debug.apk/android_release.apk + android_source.zip
Web: normal, GDExtension, single-threaded e GDExtension single-threaded (debug/release)
macOS: universal x86_64 + arm64
iOS: device + simulator
visionOS: device + simulator
ICU data
UWP Jingu: x86_64
version.txt / estrutura Jingu 1.0.0.stable

COMO USAR
---------
1. Copie/extrair o CONTEUDO deste kit na raiz do repositorio de compilacao.
2. Commit/push.
3. GitHub -> Actions -> "Jingu Engine - Complete Export Templates" -> Run workflow.
4. Informe EXATAMENTE os dois SHA-256 acima.
5. Nao publique a v1.0.0 ainda.
6. Se algum job falhar, preserve e envie os logs/artefatos de evidencia; nao marque PASS manualmente.
7. Se todos os jobs concluirem, baixe o artefato "JinguEngine-1.0.0-Complete-Export-Templates"
   e valide o TPZ fisicamente no Template Manager antes do freeze/publicacao.

STATUS DESTA ENTREGA
--------------------
Source gates: PASS 167 / FAIL 0 (local + source empacotada)
Testes sinteticos do empacotador: PASS 27 / FAIL 0
Compilacao real GitHub da matriz completa: PENDING_NOT_RUN
Smoke/export fisico da matriz completa: PENDING_NOT_RUN
