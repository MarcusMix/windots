
# 📄 Instalação e Configuração do GlazeWM + PowerToys Run no Windows

## 1. Instalar o GlazeWM

**Usando o winget:**

```powershell
winget install GlazeWM.GlazeWM
```

> Este comando baixa e instala o GlazeWM automaticamente.

---

## 2. Configurar o GlazeWM

### 2.1 Criar a pasta de configuração

O GlazeWM procura o arquivo de configuração em:

```
C:\Users\SeuUsuário\AppData\Roaming\glazewm\config.yaml
```

Crie a pasta e o arquivo manualmente:

```powershell
mkdir C:\Users\SeuUsuário\AppData\Roaming\glazewm
New-Item -Path C:\Users\SeuUsuário\AppData\Roaming\glazewm\config.yaml
```

(Substitua `SeuUsuário` pelo seu nome de usuário do Windows.)

### 2.2 Configurar o `config.yaml`

Abra o arquivo para edição:

```powershell
notepad C:\Users\SeuUsuário\AppData\Roaming\glazewm\config.yaml
```

Cole a configuração básica abaixo:

```yaml
mod_key: Alt

bindings:
  - command: focus-left
    binding: Alt+H
  - command: focus-right
    binding: Alt+L
  - command: focus-up
    binding: Alt+K
  - command: focus-down
    binding: Alt+J
  - command: reload-config
    binding: Alt+Shift+R
```

### 2.3 Rodar o GlazeWM

Execute no terminal:

```powershell
glazewm
```

O GlazeWM iniciará e começará a gerenciar suas janelas.

### 2.4 (Opcional) Rodar o GlazeWM automaticamente com o Windows

- Pressione `Win + R`, digite `shell:startup`, e pressione Enter.
- Cole um **atalho** para o `glazewm.exe` dentro da pasta de inicialização.

---

## 3. Instalar o PowerToys (para usar o PowerToys Run)

**Usando o winget:**

```powershell
winget install Microsoft.PowerToys
```

**Ou manualmente:**

- Acesse [https://learn.microsoft.com/en-us/windows/powertoys/](https://learn.microsoft.com/en-us/windows/powertoys/)
- Baixe o instalador da versão mais recente via GitHub.
- Instale normalmente.

---

## 4. Usar o PowerToys Run

- Após instalar o PowerToys, abra o app e vá até a seção **PowerToys Run**.
- Certifique-se de que a funcionalidade está **ativada**.
- Atalho padrão para abrir o PowerToys Run:

  ```
  Alt + Space
  ```

  (Você pode mudar o atalho nas configurações se quiser.)

- Agora você pode pesquisar rapidamente por programas, arquivos, pastas e executar comandos.

---

# ✅ Resumo rápido

| Item               | Comando Principal                                | Observação                                       |
|--------------------|--------------------------------------------------|--------------------------------------------------|
| Instalar GlazeWM    | `winget install GlazeWM.GlazeWM`                 | Gerenciador de janelas estilo Tiling             |
| Criar config        | `mkdir` + `New-Item` para `config.yaml`           | Configuração manual inicial obrigatória          |
| Rodar GlazeWM       | `glazewm`                                         | Gerencia janelas ao rodar                        |
| Instalar PowerToys  | `winget install Microsoft.PowerToys`              | Vem com PowerToys Run e outras ferramentas úteis |
| Atalho PowerToys Run| `Alt + Space`                                     | Pode ser personalizado                          |


# Explicação das Teclas de Atalho (Keybinds) no GlazeWM

Aqui estão as teclas de atalho configuradas para o GlazeWM:

## Modo de Redimensionamento

Essas teclas permitem redimensionar as janelas.

- **Reduzir a largura da janela em 2%**: `alt+h` ou `alt+esquerda`
- **Aumentar a largura da janela em 2%**: `alt+l` ou `alt+direita`
- **Aumentar a altura da janela em 2%**: `alt+k` ou `alt+cima`
- **Reduzir a altura da janela em 2%**: `alt+j` ou `alt+baixo`
- **Sair do modo de redimensionamento**: `enter` ou `escape`

## Modo de Pausa

Quando o modo de pausa está ativo, todas as teclas de atalho são desativadas, exceto a tecla para desativar o modo de pausa.

- **Ativar/desativar modo de pausa**: `alt+shift+p`

## Mudança de Foco (Foco de Janela)

Essas teclas permitem mover o foco para outra janela.

- **Focar na janela à esquerda**: `alt+h` ou `alt+esquerda`
- **Focar na janela à direita**: `alt+l` ou `alt+direita`
- **Focar na janela acima**: `alt+k` ou `alt+cima`
- **Focar na janela abaixo**: `alt+j` ou `alt+baixo`

## Mover Janela

Essas teclas permitem mover a janela focada em uma direção.

- **Mover janela à esquerda**: `alt+shift+h` ou `alt+shift+esquerda`
- **Mover janela à direita**: `alt+shift+l` ou `alt+shift+direita`
- **Mover janela acima**: `alt+shift+k` ou `alt+shift+cima`
- **Mover janela abaixo**: `alt+shift+j` ou `alt+shift+baixo`

## Redimensionar Janela (Modo de Redimensionamento)

No modo de redimensionamento, você pode redimensionar as janelas usando as teclas de seta ou HJKL.

- **Ativar modo de redimensionamento**: `alt+r`

## Tiling e Modo de Exibição

Essas teclas permitem alternar entre diferentes modos de exibição e controlar o comportamento das janelas.

- **Alternar entre o modo de tiling e o modo flutuante**: `alt+t`
- **Alternar para o modo fullscreen (tela cheia)**: `alt+f`
- **Minimizar a janela focada**: `alt+m`
- **Fechar a janela focada**: `alt+shift+q`
- **Sair do GlazeWM**: `alt+shift+e`
- **Recarregar a configuração do GlazeWM**: `alt+shift+r`
- **Redesenhar todas as janelas**: `alt+enter`

## Focar em Workspaces

Essas teclas permitem navegar entre os workspaces configurados.

- **Focar no próximo workspace**: `alt+s`
- **Focar no workspace anterior**: `alt+a`
- **Focar no workspace mais recente**: `alt+d`
- **Focar nos workspaces numerados (1 a 9)**:
  - `alt+1` a `alt+9`

## Mover Janela entre Workspaces

Essas teclas permitem mover a janela atual para outro workspace.

- **Mover a janela para o workspace 1-9 e focar nele**: `alt+shift+1` a `alt+shift+9`
- **Mover a janela para o workspace à esquerda/direita/acima/abaixo**: `alt+shift+a` (esquerda), `alt+shift+f` (direita), `alt+shift+d` (cima), `alt+shift+s` (baixo)

## Abrir Terminais

Essas teclas permitem abrir terminais diretamente.

- **Abrir o terminal PowerShell**: `alt+enter`
- **Abrir o terminal CMD**: `alt+enter`
"""