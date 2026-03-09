<!-- TÍTULO -->
<div align="center">
<h2>DESAFIO QA BEEDOO 2026</h2>
<h1>PORTAL DE GERENCIAMENTO DE CURSOS</h1>
<p><b>URL</b>: <a href="https://creative-sherbet-a51eac.netlify.app/" target="_blank">https://creative-sherbet-a51eac.netlify.app</a></p>
<p><b>PLANILHA</b>: <a href="https://docs.google.com/spreadsheets/d/1FaV01kPm4anXbsDjQufmM8v18mzblixO/edit?usp=drive_link&ouid=104363433007387649076&rtpof=true&sd=true" target="_blank">https://docs.google.com/spreadsheets/d/1FaV01kPm4anXbsDjQufmM8v18mzblixO/edit?usp=drive_link&ouid=104363433007387649076&rtpof=true&sd=true</a></p>
<p><b>EVIDÊNCIAS</b>: <a href="https://drive.google.com/drive/folders/1rfE7MAfelSBJx5UXAJ3jWNmqY01MkmAG?usp=drive_link" target="_blank">https://drive.google.com/drive/folders/1rfE7MAfelSBJx5UXAJ3jWNmqY01MkmAG?usp=drive_link</a></p>
</div>

<br>

<!-- OBJETIVO DA APLICAÇÃO -->
<div>
<h2>► OBJETIVO DA APLICAÇÃO</h2>
<p>A aplicação é um portal de gerenciamento de cursos voltado para o ramo educacional. Seu objetivo principal é permitir que gestores ou administradores cadastrem e listem cursos disponíveis na plataforma.</p>
<p>Sua interface é simples e direta, onde é composta por dois módulos:</p>
<ul>
  <li>Cadastro: formulário para registro de novos cursos.</li>
  <li>Listagem: visualização dos cursos cadastrados</li>
</ul>
</div>

<br>

<!-- FLUXOS DA APLICAÇÂO-->
<div>
<h2>► FLUXOS DA APLICAÇÃO</h2>

<!-- FLUXO 1-->
<div>
<h3>1 - CADASTRO DE CURSO</h3>
<p>Rota: <code>/new-course</code></p>
<ul>
  <li><b>1.1</b> - Usuário acessa a tela de cadastro;</li>
  <li><b>1.2</b> - Preenche os campos do formulário: "nome do curso", "descrição", "instrutor", "url da imagem da capa", "data início/fim", "número de vagas", "tipo de curso";</li>
  <li><b>1.2.1</b> - Se "tipo de curso" for "PRESENCIAL" então usuário preenche campo "endereço";</li>
  <li><b>1.2.2</b> - Se "tipo de curso" for "ONLINE" então usuário preenche campo "link de inscrição";</li>
  <li><b>1.3</b> - Clica no botão "CADASTRAR CURSO";</li>
  <li><b>1.4</b> - Curso é cadastrado com mensagem de sucesso e usuário é redirecionado para a lista dos cursos cadastrados;</li>
</ul>
<img src="assets/cadastro de curso.svg" alt="Fluxo de cadastro de curso." width="600px">  
</div>

<!-- FLUXO 2-->
<div>
<h3>2 - LISTAGEM DE CURSOS</h3>
<p>Rota: <code>/</code></p>
<ul>
  <li><b>2.1</b> - Usuário acessa a tela de listagem;</li>
  <li><b>2.2</b> - Servidor retorna a lista de cursos cadastrados;</li>
  <li><b>2.3</b> - Usuário visualiza os cursos na lista com os campos: "tipo de curso" ,"nome do curso", "descrição", "data início/fim", "número de vagas", botão "EXCLUIR CURSO";</li>
  <li><b>2.3.1</b> - Caso não haja cursos cadastrados, página fica em branco apenas com título e navbar.</li>
</ul>
<img src="assets/listagem de curso.svg" alt="Fluxo de listagem de cursos." width="600px">  
</div>  
</div>

<br>

<!-- DECISÕES TOMADAS PARA A CRIAÇÃO DOS TESTES -->
<div>
<h2>► DECISÕES TOMADAS PARA A CRIAÇÃO DOS TESTES</h2>

<div>
<h3>1 - TESTE MANUAL</h3>
<p>Priorizar os testes manuais teve como objetivo inicial a identificar comportamentos reais da aplicação, descobrir bugs não documentados, entender a experiência do usuário e mapear cenários não óbvios.</p>
</div>

<div>
<h3>2 - TESTES FUNCIONAIS</h3>
<p>A ideia foi concentar os esforços nos fluxos principais de negócio, como os cenários positivos e negativos do cadastro de curso, listagem de cursos, exclusão de cursos, validações de campos obrigatórios, validações de formato dos campos como data e URLs e comportamento condicional.</p>
</div>

<div>
<h3>3 - CENÁRIOS DE TESTES</h3>
<p>A cobertura de testes foi definida com foco em proporcionar máxima qualidade e confiabilidade. Cenários positivos representam 30% dos testes, cobrindo os fluxos principais onde tudo funciona conforme esperado. Cenários negativos e validações compõem 50% do escopo, garantindo que a aplicação trate adequadamente dados inválidos e situações de erro. Por fim, cenários alternativos e edge cases correspondem a 20% dos testes, capturando situações inesperadas e comportamentos extremos que podem não ser óbvios à primeira vista.</p>
</div>

<div>
<h3>4 - SEVERIDADE DE BUGS</h3>
<p><b>Bugs críticos:</b> são aqueles que impedem completamente o uso da funcionalidade principal, bloqueando o fluxo de trabalho essencial.

<b>Bugs de severidade alta:</b> indicam que a funcionalidade está comprometida, porém existe algum workaround ou caminho alternativo que permite ao usuário completar a tarefa, mesmo que com dificuldade. 

<b>Bugs de severidade média:</b> representam problemas de usabilidade ou validação que afetam a experiência, mas não impedem o uso das funcionalidades. 

<b>Bugs de severidade baixa:</b> são melhorias visuais ou de experiência que têm impacto mínimo na operação do sistema.</p>
</div>

</div>

<br>

<!-- RACIOCÍNIO DURANTE A ANÁLISE -->
<div>
<h2>► RACIOCÍNIO DURANTE A ANÁLISE</h2>

<div>
<h3>FASE 1</h3>
<p>A primeira fase consistiu em uma exploração abrangente da aplicação. Inicialmente, realizei o acesso à aplicação para verificar sua disponibilidade e responsividade em diferentes condições.

Em seguida, conduzi um mapeamento de rotas completo, identificando todas as URLs disponíveis e compreendendo como a navegação entre as páginas é estruturada. Durante essa exploração, fiz a identificação de elementos presentes na interface, catalogando botões, formulários, campos de entrada e outros componentes interativos. 

Por fim, dediquei atenção especial à observação de comportamentos do sistema, analisando como mensagens são exibidas, quais validações são aplicadas e como os redirecionamentos funcionam após ações do usuário.</p>
</div>

<div>
<h3>FASE 2</h3>
<p>Ao analisar o formulário de cadastro, identifiquei os seguintes campos:</p>
<table>
  <thead>
    <tr>
      <th>Campo</th>
      <th>Tipo</th>
      <th>Obrigatório</th>
      <th>Validação Esperada</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Nome do Curso</td>
      <td>Texto</td>
      <td>✅</td>
      <td>Não vazio, tamanho mínimo</td>
    </tr>
    <tr>
      <td>Descrição</td>
      <td>Texto longo</td>
      <td>✅</td>
      <td>Não vazio</td>
    </tr>
    <tr>
      <td>Instrutor</td>
      <td>Texto</td>
      <td>✅</td>
      <td>Não vazio</td>
    </tr>
    <tr>
      <td>URL da Imagem</td>
      <td>URL</td>
      <td>✅</td>
      <td>Formato de URL válido</td>
    </tr>
    <tr>
      <td>Data Início</td>
      <td>Data</td>
      <td>✅</td>
      <td>Não pode ser passada</td>
    </tr>
    <tr>
      <td>Data Fim</td>
      <td>Data</td>
      <td>✅</td>
      <td>Deve ser >= Data Início</td>
    </tr>
    <tr>
      <td>Número de Vagas</td>
      <td>Número</td>
      <td>✅</td>
      <td>Valor positivo, inteiro</td>
    </tr>
    <tr>
      <td>Tipo de Curso</td>
      <td>Dropdown</td>
      <td>✅</td>
      <td>PRESENCIAL ou ONLINE</td>
    </tr>
    <tr>
      <td>Endereço</td>
      <td>Texto</td>
      <td>⚠️ Condicional</td>
      <td>Obrigatório se PRESENCIAL</td>
    </tr>
    <tr>
      <td>Link de Inscrição</td>
      <td>URL</td>
      <td>⚠️ Condicional</td>
      <td>Obrigatório se ONLINE</td>
    </tr>
  </tbody>
</table>
</div>

<div>
<h3>FASE 3</h3>
<p>Durante a análise, identifiquei os seguintes riscos potenciais:</p>
<table>
  <thead>
    <tr>
      <th>Severidade</th>
      <th>ID</th>
      <th>Descrição do risco</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td rowspan="3">Crítico</td>
      <td><b>R1</b></td>
      <td>Perda de dados ao cadastrar curso sem validação adequada de campos, resultando em registros inconsistentes no banco de dados.</td>
    </tr>
    <tr>
      <td><b>R2</b></td>
      <td>Exclusão acidental de cursos sem confirmação prévia, representando risco de perda irreversível de informações importantes.</td>
    </tr>
    <tr>
      <td><b>R3</b></td>
      <td>Dados inconsistentes ao alternar tipo de curso no formulário, podendo gerar cursos com configurações contraditórias.</td>
    </tr>
    <tr>
      <td rowspan="3">Médio</td>
      <td><b>R4</b></td>
      <td>Validação inadequada de URLs que pode resultar em imagens quebradas na interface.</td>
    </tr>
    <tr>
      <td><b>R5</b></td>
      <td>Datas inválidas que permitam cadastro de cursos expirados ou com períodos incoerentes.</td>
    </tr>
    <tr>
      <td><b>R6</b></td>
      <td>Número de vagas negativo ou zero, comprometendo a integridade dos dados apresentados.</td>
    </tr>
    <tr>
      <td rowspan="3">Baixo</td>
      <td><b>R7</b></td>
      <td>Usabilidade em dispositivos móveis, afetando a experiência mas não a funcionalidade core.</td>
    </tr>
    <tr>
      <td><b>R8</b></td>
      <td>Mensagens de erro genéricas que dificultam mas não impedem a correção de problemas.</td>
    </tr>
    <tr>
      <td><b>R9</b></td>
      <td>Falta de feedback visual durante operações, causando incerteza mas não impedindo o uso.</td>
    </tr>
  </tbody>
</table>
</div>

<div>
<h3>FASE 4</h3>
<p>Com base nos riscos, priorizei os testes da seguinte forma:</p>
<table>
  <thead>
    <tr>
      <th>Prioridade</th>
      <th>Testes</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Alta (P1)</td>
      <td>
        • Cadastro com todos os campos válidos tanto para cursos PRESENCIAIS quanto ONLINE, garantindo que o fluxo principal funcione perfeitamente;<br>
        • Validações de campos obrigatórios;<br>
        • Validação crítica de datas onde início deve ser anterior ao fim;<br>
        • Funcionalidade de exclusão de curso.
      </td>
    </tr>
    <tr>
      <td>Média (P2)</td>
      <td>
        • Validação de URL de imagem para garantir que apenas links válidos sejam aceitos;<br>
        • Validação de número de vagas verificando limites e formatos;<br>
        • Comportamento ao alternar tipo de curso durante o preenchimento;<br>
        • Cadastro com caracteres especiais em diversos campos;<br>
        • Comportamento da listagem quando não há cursos cadastrados.
      </td>
    </tr>
    <tr>
      <td>Baixa (P3)</td>
      <td>
        • Verificação da clareza das mensagens de erro apresentadas;<br>
        • Layout responsivo em diferentes dispositivos;<br>
        • Performance do sistema ao lidar com muitos cursos cadastrados;<br>
        • Fluidez da navegação entre as diferentes telas da aplicação.
      </td>
    </tr>
  </tbody>
</table>
</div>
</div>

<br>

<!-- PONTOS CRÍTICOS IDENTIFICADOS -->
<div>
<h2>► PONTOS CRÍTICOS IDENTIFICADOS</h2>

<table>
  <thead>
    <tr>
      <th>ID</th>
      <th>Ponto crítico</th>
      <th>Criticidade</th>
      <th>Descrição e testes</th>
      <th>Impacto</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><b>PC-1</b></td>
      <td>VALIDAÇÃO DE CAMPOS OBRIGATÓRIOS</td>
      <td>🔴 ALTA</td>
      <td>
        A aplicação deve impedir o cadastro quando campos obrigatórios estão vazios.<br><br>
        <b>TESTES:</b><br>
        • Submissão de formulário com campo vazio;<br>
        • Preenchimento usando apenas espaços em branco como valor;<br>
        • Inserção de apenas caracteres especiais sem conteúdo válido;<br>
        • Verificação do comportamento quando campos não atendem ao tamanho mínimo exigido.
      </td>
      <td>Dados inconsistentes no banco de dados comprometem a integridade do sistema.</td>
    </tr>
    <tr>
      <td><b>PC-2</b></td>
      <td>LÓGICA CONDICIONAL (TIPO DE CURSO)</td>
      <td>🔴 ALTA</td>
      <td>
        Campos "Endereço" e "Link de Inscrição" devem aparecer/desaparecer conforme o tipo selecionado.<br><br>
        <b>CENÁRIOS CRÍTICOS:</b><br>
        • Usuário preenche o endereço, altera o tipo para ONLINE e depois retorna para PRESENCIAL, verificando se os dados são preservados ou limpos adequadamente;<br>
        • Submeter o formulário quando há dados preenchidos em campos que foram ocultados pela mudança de tipo;<br>
        • Validar o comportamento ao alternar o tipo de curso múltiplas vezes durante o preenchimento.
      </td>
      <td>Cursos cadastrados com informações erradas (endereço em curso online ou vice-versa).</td>
    </tr>
    <tr>
      <td><b>PC-3</b></td>
      <td>VALIDAÇÃO DE DATAS</td>
      <td>🟡 MÉDIA-ALTA</td>
      <td>
        Data de início não pode ser posterior à data de fim.<br><br>
        <b>CENÁRIOS DE RISCO:</b><br>
        • Data de fim é anterior à data de início;<br>
        • Data de início está no passado;<br>
        • Data de fim está muito distante no futuro (possivelmente indicando erro de digitação);<br>
        • Ambas as datas são iguais.
      </td>
      <td>Cursos com períodos inválidos aparecem na listagem.</td>
    </tr>
    <tr>
      <td><b>PC-4</b></td>
      <td>VALIDAÇÃO DE URLs</td>
      <td>🟡 MÉDIA</td>
      <td>
        URLs de imagem e link de inscrição devem ser válidos.<br><br>
        <b>TESTES NECESSÁRIOS:</b><br>
        • URLs sem protocolo (http/https);<br>
        • URLs malformadas que não seguem o padrão correto;<br>
        • URLs que tecnicamente são válidas mas não retornam uma imagem quando acessadas;<br>
        • URLs contendo caracteres inválidos ou que não foram devidamente codificadas.
      </td>
      <td>Imagens quebradas na interface, links inacessíveis.</td>
    </tr>
    <tr>
      <td><b>PC-5</b></td>
      <td>EXCLUSÃO DE CURSO</td>
      <td>🔴 ALTA</td>
      <td>
        Funcionalidade que permite remover cursos da lista.<br><br>
        <b>PREOCUPAÇÕES:</b><br>
        • Ausência de diálogo de confirmação antes de executar a exclusão;<br>
        • Possibilidade de exclusão acidental de cursos;<br>
        • Verificar se existe alguma reversibilidade da ação (como função de desfazer ou lixeira);<br>
        • Avaliar a qualidade do feedback apresentado ao usuário após a conclusão da exclusão.
      </td>
      <td>Perda de dados sem possibilidade de recuperação.</td>
    </tr>
    <tr>
      <td><b>PC-6</b></td>
      <td>PERSISTÊNCIA DE DADOS</td>
      <td>🔴 ALTA</td>
      <td>
        Cursos cadastrados devem persistir após refresh da página.<br><br>
        <b>TESTES:</b><br>
        • Cadastrar um curso e atualizar a página para verificar se os dados permanecem;<br>
        • Cadastrar e fechar completamente o navegador para testar a durabilidade do armazenamento;<br>
        • Investigar se os dados são salvos localmente (LocalStorage/SessionStorage) ou em servidor.
      </td>
      <td>Perda de trabalho do usuário.</td>
    </tr>
    <tr>
      <td><b>PC-7</b></td>
      <td>NÚMERO DE VAGAS</td>
      <td>🟢 MÉDIA-BAIXA</td>
      <td>
        Campo deve aceitar apenas números inteiros positivos.<br><br>
        <b>VALIDAÇÕES:</b><br>
        • Números negativos para garantir rejeição;<br>
        • Zero vagas (que não faz sentido em um curso);<br>
        • Números decimais quando apenas inteiros são esperados;<br>
        • Valores extremamente grandes que excedem limites razoáveis;<br>
        • Caracteres não numéricos para verificar a robustez da validação de tipo.
      </td>
      <td>Dados incorretos sobre disponibilidade de vagas.</td>
    </tr>
  </tbody>
</table>
</div>

<br>

<!-- ESTRATÉGIA DE TESTES -->
<div>
<h2>► ESTRATÉGIA DE TESTES</h2>

<div>
<h3>1 - TESTES FUNCIONAIS</h3>
<p>Esta categoria abrange a verificação de que cada funcionalidade atende aos requisitos estabelecidos, incluindo a validação dos fluxos principais (happy path) onde tudo funciona conforme esperado, e o teste das integrações entre os diferentes módulos do sistema.</p>
</div>

<div>
<h3>2 - TESTES DE VALIDAÇÃO</h3>
<p>Focados em garantir que a aplicação valida corretamente todos os inputs do usuário. Isso inclui a verificação de campos obrigatórios, validação de formatos específicos de dados como URLs, datas e números, respeitá-los aos limites de caracteres estabelecidos, e o tratamento adequado de caracteres especiais.</p>
</div>

<div>
<h3>3 - TESTES NEGATIVOS</h3>
<p>Esses testes visam verificar como o sistema se comporta em situações de erro. Incluem o envio de formulário completamente vazio, fornecimento de dados inválidos em diversos campos, tentativa de combinações não permitidas de valores, e execução de ações em ordem incorreta ou inesperada.</p>
</div>

<div>
<h3>4 - TESTES DE USABILIDADE</h3>
<p>Avaliação da experiência do usuário ao interagir com a aplicação, verificando a clareza das mensagens apresentadas, a facilidade de navegação entre as diferentes telas e funcionalidades, a qualidade do feedback visual fornecido ao usuário durante operações, e a responsividade da interface em diferentes tamanhos de tela.</p>
</div>

<div>
<h3>5 - TESTES DE INTEGRAÇÃO</h3>
<p>Verificam se os diferentes módulos trabalham corretamente em conjunto. Os testes principais incluem o fluxo de cadastro até a visualização na listagem, o processo de exclusão e consequente atualização da lista de cursos, e a persistência dos dados após recarregar a página.</p>
</div>
</div>

<br>

<!-- TÉCNICAS DE TESTE -->
<div>
<h2>► TÉCNICAS DE TESTE UTILIZADAS</h2>

<div>
<h3>1 - PARTICIONAMENTO DE EQUIVALÊNCIA</h3>
<p>Dividir inputs em classes válidas e inválidas:</p>
<p><b>Exemplo: Número de Vagas</b> - Para este campo, as classes válidas incluem valores como 1, 10, 100 e 999, representando quantidades realistas e aceitas pelo sistema. Já as classes inválidas abrangem -1 (número negativo), 0 (zero vagas não faz sentido), 1.5 (decimal quando se espera inteiro), e "abc" (caracteres não numéricos).</p>
</div>

<div>
<h3>2 - ANÁLISE DE VALOR LIMITE</h3>
<p>Testar os extremos de cada partição:</p>
<p><b>Exemplo: Nome do Curso</b> - Os testes devem cobrir o limite mínimo de 1 caractere para verificar se o sistema aceita nomes muito curtos, um valor válido comum de aproximadamente 50 caracteres representando uso normal, e o limite máximo testando com 255 caracteres (geralmente aceito) e 256 caracteres (provavelmente rejeitado) para validar o comportamento nas bordas da capacidade do campo.</p>
</div>

<div>
<h3>3 - TABELA DE DECISÃO</h3>
<p>Para lógica condicional do tipo de curso:</p>
<table>
  <thead>
    <tr>
      <th>Tipo</th>
      <th>Endereço Preenchido</th>
      <th>Link Preenchido</th>
      <th>Resultado Esperado</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>PRESENCIAL</td>
      <td>✅</td>
      <td>❌</td>
      <td>Cadastro OK</td>
    </tr>
    <tr>
      <td>PRESENCIAL</td>
      <td>❌</td>
      <td>❌</td>
      <td>Erro: Endereço obrigatório</td>
    </tr>
    <tr>
      <td>ONLINE</td>
      <td>❌</td>
      <td>✅</td>
      <td>Cadastro OK</td>
    </tr>
    <tr>
      <td>ONLINE</td>
      <td>❌</td>
      <td>❌</td>
      <td>Erro: Link obrigatório</td>
    </tr>
  </tbody>
</table>
</div>

<div>
<h3>4 - TESTES EXPLORATÓRIOS</h3>
<p>Esta abordagem permite testar sequências não planejadas que surgem naturalmente durante o uso, simulando o comportamento real e imprevisível do usuário final, o que frequentemente revela bugs não mapeados durante a análise formal de requisitos. Através da exploração livre, conseguimos descobrir edge cases e interações inesperadas que testes estruturados podem não cobrir.</p>
</div>
</div>


<br>

<!-- CATEGORIZAÇÃO DE BUGS -->
<div>
<h2>► CATEGORIZAÇÃO DE BUGS</h2>

<div>
<h3>🔴 CRÍTICO (BLOCKER)</h3>
<p>Bugs críticos são aqueles que causam impacto devastador no sistema. Incluem situações onde a aplicação não carrega completamente, cenários onde é impossível cadastrar curso tornando o sistema inutilizável para seu propósito principal, casos de perda de dados que comprometem a confiabilidade, e erros que impedem completamente o uso das funcionalidades essenciais sem qualquer alternativa disponível.</p>
</div>

<div>
<h3>🟠 ALTO (MAJOR)</h3>
<p>Bugs de alta severidade representam falhas significativas onde validações importantes estão falhando comprometendo a integridade dos dados, funcionalidades não operam como esperado causando frustração e retrabalho ao usuário, porém ainda existe um workaround complexo que permite ao usuário atingir seu objetivo através de caminhos alternativos não ideais.</p>
</div>

<div>
<h3>🟡 MÉDIO (MINOR)</h3>
<p>Bugs médios abrangem problemas de usabilidade que dificultam mas não impedem o uso do sistema, mensagens de erro incorretas ou confusas que prejudicam a experiência mas não bloqueiam ações, e validações secundárias falhando em campos ou cenários menos críticos para o fluxo principal do negócio.</p>
</div>

<div>
<h3>🟢 BAIXO (TRIVIAL)</h3>
<p>Bugs de baixa severidade envolvem problemas visuais ou estéticos que não afetam a funcionalidade, oportunidades de melhoria de experiência que tornariam o sistema mais agradável mas não são essenciais, e inconsistências de texto como erros de digitação ou problemas de tradução que têm impacto mínimo na operação.</p>
</div>
</div>

<br>

<!-- APRENDIZADOS E OBSERVAÇÕES -->
<div>
<h2>► APRENDIZADOS E OBSERVAÇÕES</h2>

<div>
<h3>USO DE IA NO DESAFIO</h3>
<p>Durante este desafio, utilizei ferramentas de IA como apoio estratégico em três áreas principais. Primeiramente, na <b>estruturação da documentação</b>, onde a IA auxiliou na organização lógica do conteúdo, garantindo um fluxo coerente de informações. Em seguida, na <b>identificação de cenários</b>, onde obtive sugestões de casos de teste adicionais que poderiam ter sido negligenciados em uma análise inicial. Por fim, na <b>análise de riscos</b>, utilizando a capacidade da IA para realizar um mapeamento sistemático de pontos críticos da aplicação.</p>

<p>É importante ressaltar que todas as sugestões foram submetidas a um processo rigoroso de validação. Realizei revisão manual de todos os cenários sugeridos pela IA, adaptando os casos de teste ao contexto real e específico da aplicação em análise. Além disso, questionei ativamente sugestões genéricas que não se aplicavam adequadamente ao caso, complementando as recomendações automatizadas com minha experiência prática de QA.</p>
</div>
</div>

<br>

---

<div align="center">
<p><b>By:</b> Gabriel Lima</p>
</div>


