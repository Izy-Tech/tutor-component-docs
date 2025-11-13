# Documentação Componente

## Essa documentação aborda como customizar o componente e seus callbacks.

[Ir para Customização](#customizacao)

[Ir para Navegação de vídeos e textos](#navegacao)

[Ir para Enviar momento atual](#getcurrentcontent)

--- 

# Documentação Customização
<a id="customizacao"></a>
## 📦 Importando o ThemeManager (Obrigatório)


Para utilizar o `ThemeManager`, é necessário importar o módulo dentro da sua aplicação.

```js
import { ThemeManager } from './dist/theme-manager.js';
```

Caso esteja utilizando via HTML com `<script type="module">`, o import deve ser feito assim:

```html
<script type="module">
  import { ThemeManager } from './dist/theme-manager.js';

  ThemeManager.setDefaultTheme({
    /* ... */
  });
</script>
```

---

## 🖼️ Como usar SVG em ícones (closed icon, header, submit button etc.)

Além de imagens (`<img>`), também é possível utilizar SVG inline em qualquer ícone do tema.

### ✔️ Exemplo usando SVG no botão de enviar

```js
ThemeManager.setDefaultTheme({
  submitButtons: {
    submit: {
      svg: {
        content: `
        <svg width="24" height="24" viewBox="0 0 24 24" fill="none"
          xmlns="http://www.w3.org/2000/svg">
          <path d="M2 21L23 12L2 3V10L17 12L2 14V21Z" fill="#3B82F6"/>
        </svg>
        `
      }
    }
  }
});
```

### ✔️ Exemplo usando SVG no título

```js
ThemeManager.setDefaultTheme({
  header: {
    icon: {
      svg: `
        <svg width="20" height="20" fill="#3B82F6" viewBox="0 0 24 24">
          <circle cx="12" cy="12" r="10" />
        </svg>
      `
    }
  }
});
```

### ✔️ Exemplo usando SVG no botão fechado

```js
ThemeManager.setDefaultTheme({
  closed: {
    icon: `
      <svg width="24" height="24" fill="#3B82F6" viewBox="0 0 24 24">
        <path d="M3 12h18" stroke="#fff" stroke-width="2" />
      </svg>
    `
  }
});
```

---

## 🎨 Trabalhando com Temas (Default, Dark e Temas Customizados)

### ⭐ Tema padrão (Default)

```js
ThemeManager.setDefaultTheme({
  chat: { backgroundColor: '#ffffff' }
});
```

### 🌙 Tema escuro (Dark)

```js
ThemeManager.setDarkTheme({
  chat: { backgroundColor: '#1e1e1e' },
  header: { styles: { color: '#ffffff' }}
});
```

## 🎨 Criando seu próprio tema (Custom Theme)

```js
ThemeManager.setLightTheme({
  chat: {
    backgroundColor: '#f5e8ff'
  },
  header: {
    styles: {
      backgroundColor: '#a855f7',
      color: '#fff'
    }
  }
});
```

```js
ThemeManager.setDarkTheme({
  chat: {
    backgroundColor: '#1a1a1a'
  },
  header: {
    styles: {
      backgroundColor: '#333',
      color: '#fff'
    }
  }
});
```

```js
ThemeManager.setDefaultTheme({
  chat: {
    backgroundColor: '#ffffff'
  }
});
```

## 🔄 Alternando temas em runtime

```js
ThemeManager.setCurrentTheme('default');
ThemeManager.setCurrentTheme('dark');
ThemeManager.setCurrentTheme('light');
```

## 🖱️ Exemplo de botões para alternar temas

```html
<button onclick="ThemeManager.setCurrentTheme('default')">Tema Padrão</button>
<button onclick="ThemeManager.setCurrentTheme('dark')">Tema Escuro</button>
<button onclick="ThemeManager.setCurrentTheme('light')">Meu Tema Customizado</button>
```




> 💡 **Observação importante:**  
> Caso deseje utilizar uma fonte diferente da padrão, é necessário adicioná-la manualmente dentro da tag `<head>` do HTML.  
>   
> **Exemplo de inclusão de fonte personalizada:**
> ```html
> <head>
>   <link href="https://fonts.cdnfonts.com/css/stencil-paper" rel="stylesheet">
> </head>
> ```

## Chat minimizado 

### Default

<img width="366" height="150" alt="image" src="https://github.com/user-attachments/assets/5a60aa1e-8ed7-45e5-8881-cd5b56c297c4" />


### Ícone do chat minimizado 

Código:

```js
ThemeManager.setDefaultTheme({
  closed: {
    icon: `
      <img src="https://cdn-icons-png.flaticon.com/512/4712/4712009.png">
    `,
    tooltip: { text: 'Abrir documentação' },
    styles: {
      backgroundColor: '#3B82F6',
      borderRadius: '50%',
      width: '60px',
      height: '60px'
    }
  }
});
```


Resultado:  

<img width="361" height="150" alt="image" src="https://github.com/user-attachments/assets/490d5770-fc6e-41e6-9c1b-4cb78babf859" />


## Texto do chat minimizado:

Código:  
```js
ThemeManager.setDefaultTheme({  
  closed: {  
    icon: `  
      <img src="https://cdn-icons-png.flaticon.com/512/4712/4712009.png">  
    `,  
    tooltip: { text: 'Texto Chat Minimizado' },  
    styles: {  
      backgroundColor: '#3B82F6',  
      borderRadius: '50%',  
      width: '60px',  
      height: '60px'  
    }  
  }  
});
```

Resultado:  

<img width="367" height="147" alt="image" src="https://github.com/user-attachments/assets/768fcd72-61b4-4397-986a-dc482542eb65" />

## Fonte do texto do chat minimizado

Código:  
```js
ThemeManager.setDefaultTheme({  
  closed: {  
    icon: `  
      <img src="https://cdn-icons-png.flaticon.com/512/4712/4712009.png">  
    `,  
    tooltip: {  
      text: 'Exemplo font minimizada',  
      styles: {  
        fontFamily: '"Stencil Paper", sans-serif',  
        fontSize: '14px',  
        color: '#3B82F6',  
        backgroundColor: '#f0f4ff',  
        border: '1px solid #3B82F6',  
        padding: '6px 10px',  
        borderRadius: '6px'  
      }  
    }  
  }  
});
```

Resultado:  

<img width="417" height="163" alt="image" src="https://github.com/user-attachments/assets/1b805f59-41bd-4fb6-a5db-6e0462a84cdc" />

## Cor de fundo do texto do chat minimizado 

Código:
```js
ThemeManager.setDefaultTheme({  
  closed: {  
    icon: `  
      <img src="https://cdn-icons-png.flaticon.com/512/4712/4712009.png">  
    `,  
    tooltip: {  
      text: 'Exemplo font minimizada',  
      styles: {  
        fontFamily: '"Stencil Paper", sans-serif',  
        fontSize: '14px',  
        color: '#3B82F6',  
        backgroundColor: '#f0f4ff',  
        border: '1px solid #3B82F6',  
        padding: '6px 10px',  
        borderRadius: '6px'  
      }  
    },  
    styles: {  
      backgroundColor: '#3B82F6'  
    }  
  }  
});
```

Resultado:  

<img width="361" height="148" alt="image" src="https://github.com/user-attachments/assets/27298df4-908b-4539-bde0-efbd9f84ca87" />

### Cor do texto do chat minimizado 

Código:

```js
ThemeManager.setDefaultTheme({  
  closed: {  
    icon: `  
      <img src="https://cdn-icons-png.flaticon.com/512/4712/4712009.png">  
    `,  
    tooltip: {  
      text: 'Abrir documentação',  
      styles: {  
        fontFamily: '"Stencil Paper", sans-serif',  
        fontSize: '14px',  
        color: 'red',  
        backgroundColor: '#f0f4ff',  
        border: '1px solid #3B82F6',  
        padding: '6px 10px',  
        borderRadius: '6px'  
      }  
    }  
  }  
});
```

Resultado:  

<img width="428" height="189" alt="image" src="https://github.com/user-attachments/assets/06ef006d-77b1-4f9f-a132-6c6ecc9afb52" />

## Avatares

### Default

<img width="769" height="256" alt="image" src="https://github.com/user-attachments/assets/ffb9e87e-398c-4a18-8f20-34734446a2f4" />

### Avatar do bot

Código:  
```js
ThemeManager.setDefaultTheme({  
  avatars: {  
    ai: {  
      src: 'https://cdn-icons-png.flaticon.com/512/4712/4712027.png'  
    }  
  }  
});
```

Resultado:  

<img width="788" height="239" alt="image" src="https://github.com/user-attachments/assets/3f3a3887-09f7-43ae-9030-84066d241428" />

### Avatar do usuário

Código:  
```js
ThemeManager.setDefaultTheme({  
  avatars: {  
    ai: {  
      src: 'https://cdn-icons-png.flaticon.com/512/4712/4712027.png'  
    },  
    user: {  
      src: 'https://cdn-icons-png.flaticon.com/512/147/147144.png'  
    }  
  }  
});
```

Resultado:  

<img width="756" height="180" alt="image" src="https://github.com/user-attachments/assets/35124697-6e36-476b-a68f-3c1bf0bd6be9" />

## Mensagem do chat

### Default

<img width="744" height="180" alt="image" src="https://github.com/user-attachments/assets/8a558830-c8f1-43d6-9298-6baff9430b00" />

### Cor de fundo da mensagem do bot

```js
Código:  
ThemeManager.setDefaultTheme({  
  messages: {  
    default: {  
      ai: {  
        bubble: {  
          backgroundColor: 'red',  
          color: 'white'  
        }  
      }  
    }  
  }  
});
```

Resultado:  

<img width="728" height="184" alt="image" src="https://github.com/user-attachments/assets/c893f977-3b6c-49ac-a6a0-6ca6763e986e" />

### Cor de fundo da mensagem do usuário

Código:  
```js
ThemeManager.setDefaultTheme({  
  messages: {  
    default: {  
      ai: {  
        bubble: {  
          backgroundColor: 'red',  
          color: 'white'  
        }  
      },  
      user: {  
        bubble: {  
          backgroundColor: 'yellow',  
          color: 'black'  
        }  
      }  
    }  
  }  
});
```

Resultado:  

<img width="756" height="189" alt="image" src="https://github.com/user-attachments/assets/aeb8bc92-0141-4fe4-b3e5-0b4afd3ce8c4" />

### Cor do texto da mensagem do bot

Código:
```js
ThemeManager.setDefaultTheme({  
  messages: {  
    default: {  
      ai: {  
        bubble: {  
          backgroundColor: 'red',  
          color: 'white'  
        }  
      }  
    }  
  }  
});
```

Resultado:  

<img width="728" height="184" alt="image" src="https://github.com/user-attachments/assets/af321f8c-3036-4a16-84aa-e715698b9792" />

### Cor do texto da mensagem do usuário

Código:  
```js
ThemeManager.setDefaultTheme({  
  messages: {  
    default: {  
      ai: {  
        bubble: {  
          backgroundColor: 'red',  
          color: 'white'  
        }  
      },  
      user: {  
        bubble: {  
          backgroundColor: 'yellow',  
          color: 'black'  
        }  
      }  
    }  
  }  
});
```

Resultado:  

<img width="756" height="189" alt="image" src="https://github.com/user-attachments/assets/f4ea79e3-d020-4d56-a723-625df85651a5" />

### Fonte da mensagem do bot

Código:  
```js
  ThemeManager.setDefaultTheme({  
    messages: {  
      default: {  
        ai: {  
          bubble: {  
            backgroundColor: 'red',  
            fontFamily: '"Stencil Paper", sans-serif',  
            fontSize: '14px',  
            color: '#000000'  
          }  
        },  
        user: {  
          bubble: {  
            backgroundColor: 'yellow',  
            color: 'black'  
          }  
        }  
      }  
    }  
  });
```
Resultado:  

<img width="572" height="141" alt="image" src="https://github.com/user-attachments/assets/22ee1bf6-2fba-4be0-897a-d30b33499ddf" />

### Fonte do texto do usuário

Código  
```js
ThemeManager.setDefaultTheme({  
  messages: {  
    default: {  
      ai: {  
        bubble: {  
          backgroundColor: 'red',  
          fontFamily: '"Stencil Paper", sans-serif',  
          fontSize: '14px',  
          color: '#000000'  
        }  
      },  
      user: {  
        bubble: {  
          backgroundColor: 'yellow',  
          fontFamily: '"Stencil Paper", sans-serif',  
          fontSize: '14px',  
          color: '#000000'  
        }  
      }  
    }  
  }  
});
```
Resultado:  

<img width="730" height="195" alt="image" src="https://github.com/user-attachments/assets/ae61bc6f-4f65-44e9-9c95-e9e987bdb1bb" />

## Janela do chat

### Default

<img width="870" height="1109" alt="image" src="https://github.com/user-attachments/assets/c44a0193-7008-4f57-98a6-61f5a8d0db20" />

### Cor da caixa de texto de nova mensagem ("Como posso te ajudar?") 

Código:  
```js
ThemeManager.setDefaultTheme({  
  textInput: {  
    styles: {  
      container: {  
        backgroundColor: 'lightblue'  
      }  
    }  
  }  
});
```

Resultado:  

<img width="838" height="1084" alt="image" src="https://github.com/user-attachments/assets/fd942332-e702-4189-83bc-0594a5ee79cc" />

### Fonte do texto de nova mensagem

Código:  
```js
ThemeManager.setDefaultTheme({  
  textInput: {  
    styles: {  
      container: {  
        fontFamily: '"Stencil Paper", sans-serif',  
        fontSize: '14px',  
        color: '#000000'  
      }  
    }  
  }  
});
```

Resultado:  

<img width="800" height="1061" alt="image" src="https://github.com/user-attachments/assets/d8947217-69c3-4316-8889-2eb48b20c484" />

### Texto do placeholder de nova mensagem

Código:
```js
ThemeManager.setDefaultTheme({  
  textInput: {  
    styles: {  
      container: {  
        fontFamily: '"Stencil Paper", sans-serif',  
        fontSize: '14px',  
        color: '#000000'  
      }  
    }  
  }  
});
```

Resultado:  

<img width="797" height="1055" alt="image" src="https://github.com/user-attachments/assets/c214b969-d116-4f2a-b5d1-ffa8819a9127" />

### Ícone do enviar nova mensagem

Código:
```js
  ThemeManager.setDefaultTheme({
    submitButtons: {
      submit: {
        svg: {
          content: `
          <svg width="24" height="24" viewBox="0 0 24 24" fill="none"
            xmlns="http://www.w3.org/2000/svg">
            <path d="M2 21L23 12L2 3V10L17 12L2 14V21Z" fill="#3B82F6"/>
          </svg>
        `}
      }
    }
  });
```
Resultado:

<img width="455" height="151" alt="image" src="https://github.com/user-attachments/assets/0a797808-a16c-4a23-83ea-474b78c1afd6" />

### Cor de fundo da janela chat

Código:  
```js
ThemeManager.setDefaultTheme({  
  chat: {  
    backgroundColor: 'lightblue'  
  }  
});
```

Resultado:  

<img width="831" height="1073" alt="image" src="https://github.com/user-attachments/assets/925f0179-8a37-45c2-87a9-59c0f20d7d0b" />

### Balões do Chat 
### Default

<img width="620" height="284" alt="image" src="https://github.com/user-attachments/assets/3810555b-1dac-4382-9744-3c106e370c30" />

Cor dos balões de sugestão

Código:
```js
ThemeManager.setDefaultTheme({
      messageSuggestions: {
        default: {
          color: 'yellow',
        }       
      }
    });
```

Resultado:  

<img width="425" height="298" alt="image" src="https://github.com/user-attachments/assets/56ffde57-fb27-4bac-bae7-510297d8b913" />

### Cor da fonte dos balões de sugestão
```js
  ThemeManager.setDefaultTheme({
      messageSuggestions: {
        default: {
          color: 'darkblue',
        }
      }
    });
```
Resultado:

<img width="467" height="331" alt="image" src="https://github.com/user-attachments/assets/7bfea5b5-040c-4293-804d-f32dec9b8772" />

### Cor do hover (mouse em cima) dos balões de sugestão
```js
ThemeManager.setDefaultTheme({
      messageSuggestions: {
        default: {
          color: 'yellow',
        },
        hover: {
          backgroundColor: '#0078d4'
        }
      }
    });
```
Resultado:

<img width="509" height="347" alt="image" src="https://github.com/user-attachments/assets/566d7d91-dda5-4b4b-bf64-c0cc7852a22a" />

### Fonte dos balões de sugestão 

```js
Código:  
  ThemeManager.setDefaultTheme({  
    messages: {  
      default: {  
        'ai-suggestions': {  
          bubble: {  
            fontFamily: '"Stencil Paper", sans-serif',  
            fontSize: '14px'  
          }  
        }  
      }  
    }  
  });
```

Resultado:  

<img width="797" height="611" alt="image" src="https://github.com/user-attachments/assets/7680c4c6-fcea-4557-9223-b76159524df4" />

### Altura do chat (em %) em relação ao total da página quando utilizado em navegadores móveis e Permitir z-index customizado
Para alterar estilos do container externo do chat, basta definir via CSS como normalmente é feito e colocar na tag do componente.
Código:
```html
<style>
    .chat {
      position: fixed;
      bottom: 20px;
      right: 20px;
      max-height: 80vh;
      z-index: 9999;
    }
  </style>
  <tutor-chat class="chat" id="tutor-chat"></tutor-chat>
```
## Notificação/Alertas

(Estou aprendendo novos conteúdos sobre o produto ...)

### Default

<img width="777" height="319" alt="image" src="https://github.com/user-attachments/assets/4ca8bb88-b884-475f-b13e-f7d7881d1cd3" />

### Cor de fundo da notificação

Código:  
```js
ThemeManager.setDefaultTheme({  
  notificationArea: {  
    styles: {  
      backgroundColor: 'yellow'  
    }  
  }  
});
```

Resultado:  

<img width="728" height="331" alt="image" src="https://github.com/user-attachments/assets/16821324-494c-47ef-859b-df50cfdd2a6a" />

### Fonte da notificação

Código:  
```js
ThemeManager.setDefaultTheme({  
  notificationArea: {  
    styles: {  
      fontFamily: '"Stencil Paper", sans-serif',  
      fontSize: '14px',  
      color: '#92400E'  
    }  
  }  
});
```

Resultado:  

<img width="713" height="336" alt="image" src="https://github.com/user-attachments/assets/8f0d8ed6-4376-44a4-9bfe-de5bd0d77d06" />

### Cor do texto da notificação

Código:
```js
ThemeManager.setDefaultTheme({  
  notificationArea: {  
    styles: {  
      color: '#1E3A8A'  
    }  
  }  
});
```
Resultado:  

<img width="709" height="264" alt="image" src="https://github.com/user-attachments/assets/3b8b1eeb-f7ea-4d3b-be60-fd23f160be07" />

## Feedback

### Default

<img width="506" height="234" alt="image" src="https://github.com/user-attachments/assets/3f461471-149d-4103-9019-d0b222ac4d6b" />
<img width="613" height="377" alt="image" src="https://github.com/user-attachments/assets/84e06765-062b-40fc-974c-24c8f2734586" />
<img width="692" height="402" alt="image" src="https://github.com/user-attachments/assets/8acb3217-267a-418f-bd43-c5512f5333d2" />
<img width="464" height="195" alt="image" src="https://github.com/user-attachments/assets/92d65027-4a37-4950-9431-27abce07451d" />

### Ícone do feedback positivo (imagem de 24x24px)
Código:  
```js
ThemeManager.setDefaultTheme({  
  feedback: {  
    positiveAction: {  
      svg: `<img src="https://cdn-icons-png.flaticon.com/512/1828/1828640.png" width="24" height="24">`  
    }  
  }  
});
```

Resultado:  

<img width="528" height="269" alt="image" src="https://github.com/user-attachments/assets/a421f216-0e89-4e35-8f6b-11d151966a62" />

### Cor do botão de feedback positivo

Código:
```js
ThemeManager.setDefaultTheme({  
  feedback: {  
    positiveAction: {  
      styles: {  
        backgroundColor: '#22C55E',  
        borderRadius: '6px',  
        padding: '6px'  
      }  
    }  
  }  
});
```

Resultado:  

<img width="500" height="252" alt="image" src="https://github.com/user-attachments/assets/e6d97d32-b490-438c-adc1-47a9c0b96d1c" />

### Ícone do feedback negativo (imagem de 24x24px)

Código:
```js
ThemeManager.setDefaultTheme({  
  feedback: {  
    negativeAction: {  
      svg: `<img src="https://cdn-icons-png.flaticon.com/512/1828/1828665.png" width="24" height="24">`  
    }  
  }  
});
```

Resultado:  

<img width="545" height="248" alt="image" src="https://github.com/user-attachments/assets/d18f7d06-5eaf-421f-a5ff-8ca05cf11f7e" />

### Cor do botão de feedback negativo

Código:  
```js
ThemeManager.setDefaultTheme({  
  feedback: {  
    negativeAction: {  
      styles: {  
        backgroundColor: '#EF4444',  
        borderRadius: '6px',  
        padding: '6px'  
      }  
    }  
  }  
});
```

Resultado:  

<img width="503" height="261" alt="image" src="https://github.com/user-attachments/assets/42bd6806-a8f7-4f95-8fde-43ceca7d7815" />

### Fonte "Obrigado pelo feedback"

Código:
```js
ThemeManager.setDefaultTheme({  
  feedback: {  
    positiveAction: {  
      label: {  
        styles: {  
          fontFamily: '"Stencil Paper", sans-serif',  
          fontSize: '14px',  
          color: '#16A34A'  
        }  
      }  
    }  
  }  
});
```

Resultado:  

<img width="522" height="286" alt="image" src="https://github.com/user-attachments/assets/2ef2b24f-5b80-480d-a790-c9627d4d286d" />

### Cor "Obrigado pelo feedback"

Código:
```js
ThemeManager.setDefaultTheme({  
  feedback: {  
    positiveAction: {  
      label: {  
        styles: {  
          fontFamily: '"Stencil Paper", sans-serif',  
          fontSize: '14px',  
          color: '#16A34A'  
        }  
      }  
    }  
  }  
});
```

Resultado:  

<img width="522" height="286" alt="image" src="https://github.com/user-attachments/assets/cefeafe7-3a20-4739-889f-822bf79d8dcb" />

### Cor de fundo balão de sugestão ("Resposta incorreta", "Resposta muito longa", "Resposta fora do tema", "Outro")

Código:  
```js
    ThemeManager.setDefaultTheme({
      feedback: {
        negativeForm: {
          reasonButtons: {
            hoverBackgroundColor: '#FF0000',
            styles: {
              color: '#BB0000',
              backgroundColor: 'yellow'
            }
          }
        }
      }
    });
```
Resultado:

<img width="398" height="227" alt="image" src="https://github.com/user-attachments/assets/01c55c74-1f73-4003-a8cf-10de3c7c9148" />

### Cor do texto balão de sugestão

Código:  
```js
    ThemeManager.setDefaultTheme({
      messageSuggestions: {
        default: {
          color: '#fff',
          backgroundColor: '#000'
        },
        hover: {
          backgroundColor: '#0078d4'
        }
      }
    });
```
Resultado:

<img width="474" height="337" alt="image" src="https://github.com/user-attachments/assets/c81a1a4e-fba0-46f1-9eac-d2781da2cefb" />

### Texto "Que pena que a resposta não ajudou. Por favor, nos ajude a melhorar"

Código:  
```js
ThemeManager.setDefaultTheme({  
  feedback: {  
    negativeAction: {  
      label: {  
        text: 'Que pena que a resposta não ajudou. Esse é um TESTE!'  
      }  
    }  
  }  
});
```

Resultado:  

<img width="673" height="375" alt="image" src="https://github.com/user-attachments/assets/d5977010-c598-4d4a-bcb4-be7228ead7b5" />

### Cor botão "Enviar"

Código:  
```js
ThemeManager.setDefaultTheme({  
  feedback: {  
    submitButton: {  
      backgroundColor: 'red'  
    }  
  }  
});
```

Resultado:  

<img width="650" height="395" alt="image" src="https://github.com/user-attachments/assets/768208e6-451c-49e2-a3c4-77f5754884ec" />

## Título

### Default

<img width="808" height="302" alt="image" src="https://github.com/user-attachments/assets/fc2b4661-400f-461f-b224-8899b5674191" />

### Cor do texto do título

Código:
```js
ThemeManager.setDefaultTheme({  
  header: {  
    styles: {  
      color: 'red'  
    }  
  }  
});
```

Resultado:

<img width="708" height="266" alt="image" src="https://github.com/user-attachments/assets/39f6c0c2-d9bf-482c-ba36-eb0ef314a407" />

### Fonte do texto do título
Código:  
```js
  ThemeManager.setDefaultTheme({  
    header: {  
      styles: {  
        fontFamily: '"Stencil Paper", sans-serif',  
        fontSize: '18px'  
      }  
    }  
  });
```

Resultado:   

<img width="773" height="245" alt="image" src="https://github.com/user-attachments/assets/90e23f76-6be0-42de-b449-e052f72496d1" />

### Ícone do título a esquerda do texto (imagem de 24x24px)

Código:
```js
  ThemeManager.setDefaultTheme({
      header: {
        icon: {
          svg: "<img src='https://cdn-icons-png.flaticon.com/512/4712/4712027.png' />"
        }
      },
    });
```
Resultado:

<img width="242" height="87" alt="image" src="https://github.com/user-attachments/assets/d8b9d59e-3491-4b9a-9eb5-5fcb44ea3bd5" />

### Cor da barra de título

Código:
```js
ThemeManager.setDefaultTheme({  
  header: {  
    styles: {  
      backgroundColor: '#1E3A8A'  
    }  
  }  
});
```

Resultado:  

<img width="786" height="292" alt="image" src="https://github.com/user-attachments/assets/1d06a45f-e3b8-4bb0-b337-146d9f1a2b00" />

### Título customizado para janela, se não enviado usar o nome do curso

Código:  
```js
ThemeManager.setDefaultTheme({  
  header: {  
    title: {  
      text: 'Assistente do Curso de C# Performance'  
    }  
  }  
});
```

Resultado:  

<img width="733" height="198" alt="image" src="https://github.com/user-attachments/assets/29198ce4-0790-4ab2-9cac-8d182ee4754d" />

## Opções 
### Iniciar com o chat minimizado ou aberto (boolean)

Fechado Código  
```js
    tutorChat.options = {  
      organizationId: "4f0983fc-055c-44be-bafe-0f2d9e937f0b",  
      productId: "9206CEBB-17F0-5CFE-84A3-0C9B212FE1C8",  
      isExternalProductId: false,  
      getToken: getConsumerToken,  
      getCurrentContent: getCurrentContent,        
      baseAddress: 'https://localhost:7209',  
      startOpened: false,  
      showSuggestions: true  
    };
```

Resultado:  

<img width="369" height="169" alt="image" src="https://github.com/user-attachments/assets/53c03f38-9bb3-4a2f-b565-30a09a0014cf" />

Aberto código:  
```js
    tutorChat.options = {  
      organizationId: "4f0983fc-055c-44be-bafe-0f2d9e937f0b",  
      productId: "9206CEBB-17F0-5CFE-84A3-0C9B212FE1C8",  
      isExternalProductId: false,  
      getToken: getConsumerToken,  
      getCurrentContent: getCurrentContent,        
      baseAddress: 'https://localhost:7209',  
      startOpened: true,  
      showSuggestions: true  
    };
```

Resultado:  

<img width="783" height="988" alt="image" src="https://github.com/user-attachments/assets/808e2fe6-1f24-4996-85dc-498c94a830b6" />

### Exibir/não exibir balões de sugestão (boolean)

Código mostrar:  
```js
    tutorChat.options = {  
      organizationId: "4f0983fc-055c-44be-bafe-0f2d9e937f0b",  
      productId: "9206CEBB-17F0-5CFE-84A3-0C9B212FE1C8",  
      isExternalProductId: false,  
      getToken: getConsumerToken,  
      getCurrentContent: getCurrentContent,        
      baseAddress: 'https://localhost:7209',  
      startOpened: true,  
      showSuggestions: true  
    };
```
Resultado:  

<img width="789" height="542" alt="image" src="https://github.com/user-attachments/assets/2be1e6a2-53bc-4f86-8f1f-011046592d5b" />

Código não mostrar:  
```js
    tutorChat.options = {  
      organizationId: "4f0983fc-055c-44be-bafe-0f2d9e937f0b",  
      productId: "9206CEBB-17F0-5CFE-84A3-0C9B212FE1C8",  
      isExternalProductId: false,  
      getToken: getConsumerToken,  
      getCurrentContent: getCurrentContent,        
      baseAddress: 'https://localhost:7209',  
      startOpened: true,  
      showSuggestions: false  
    };
```

Resultado:  

<img width="786" height="336" alt="image" src="https://github.com/user-attachments/assets/a1d60a74-5092-4031-af97-28d714462337" />


--- 
<a id="navegacao-de-videos-e-textos"></a>
# Documentação — Navegação de Vídeo e Texto (videoNavigation / textNavigation)

Quando a IA identifica um conteúdo relevante dentro de um **vídeo** ou **documento PDF**, ela pode retornar o ponto exato onde aquele conteúdo aparece.  
Para isso, você deve implementar dois callbacks: **onVideoDocumentNavigation** e **onTextDocumentNavigation**.

Essas funções recebem um objeto contendo informações sobre o conteúdo indexado e devem redirecionar o usuário para o material correspondente no player do produtor.

---

## Navegação em Vídeos (`videoNavigation`)

Quando a IA entende que a resposta do usuário está relacionada a um trecho específico de um vídeo (ex.: “O conceito SOLID é explicado no minuto 2 do vídeo X”), ela dispara o callback:

```js
onVideoDocumentNavigation: (currentVideo) => this.videoNavigation(currentVideo)
```

O método recebe:

```ts
{
  id: string,
  name?: string,
  friendlyUrl?: string,
  startTime: number // em milissegundos
}
```

### O que o implementador do componente deve fazer (exemplo c# com Blazor)?

```c#
videoNavigation(currentVideo) {
    const productId = this.tutorChat?.options?.productId;

    const url = new URL(window.location.href);
    url.hash = '';
    url.pathname = `/products/${productId}/members`;
    url.search = '';

    url.searchParams.set('documentId', currentVideo.id);
    url.searchParams.set('position', Math.round(currentVideo.startTime ?? 0));

    this.blazorCallback.invokeMethodAsync('NavigateTo', url.toString(), true);
}
```

### Explicação

1. **Constrói uma URL para o player da plataforma**  
   - `/products/{productId}/members`
2. **Adiciona o ID do vídeo**  
   - `documentId = currentVideo.id`
3. **Marca o tempo do vídeo onde o conteúdo aparece**  
   - `position = startTime`
4. **Chama o Blazor** para executar a navegação real:  
   - `NavigateTo(url, true)`

### Resultado

Quando o usuário clica no link sugerido pela IA, ele é **redirecionado para o vídeo exatamente no segundo certo** que contém o conteúdo mencionado.

---

## Navegação em Documentos (PDF) — `textNavigation`

Quando o conteúdo relevante está em um material de texto (apostila, PDF, página 8, por exemplo), o callback é:

```js
onTextDocumentNavigation: (currentText) => this.textNavigation(currentText)
```

O objeto recebido:

```ts
{
  id: string,
  name?: string,
  friendlyUrl?: string,
  page: number
}
```

### O que o implementador do componente deve fazer (exemplo c# com Blazor)?

```js
textNavigation(currentText) {
    const productId = this.tutorChat?.options?.productId;

    const url = new URL(window.location.href);
    url.hash = '';
    url.pathname = `/products/${productId}/members`;
    url.search = '';

    url.searchParams.set('documentId', currentText.id);
    url.searchParams.set('position', currentText.page ?? 0);

    this.blazorCallback.invokeMethodAsync('NavigateTo', url.toString(), true);
}
```

### Explicação

1. Constrói a URL do player  
2. Usa o ID do documento PDF  
3. Define a página onde o tema aparece  
4. Aciona o Blazor para navegar

### Resultado

O usuário é direcionado **para exatamente a página do documento mencionada pela IA**.

---

## Como o clique dispara a navegação

Dentro do componente, quando o usuário clica em um item sugerido pela IA, este método é chamado:

```js
private async videoDocumentClick(event) {
  if (!this.options.onVideoDocumentNavigation) return;

  const target = event.currentTarget;
  if (!target) return;

  const dataset = target.dataset;

  await this.options.onVideoDocumentNavigation({
    name: dataset.name,
    friendlyUrl: dataset.friendlyUrl,
    id: dataset.id,
    startTime: dataset.startTime
  });
}
```

O mesmo ocorre para PDF (textNavigation).

## Resumo

- A IA monitora o conteúdo do curso (vídeos + PDFs)
- Quando identifica uma parte relevante:
  - Fornece um link para o trecho do vídeo **exato**
  - Ou para a **página correta** do PDF
- O Tutor dispara `onVideoDocumentNavigation` ou `onTextDocumentNavigation`
- Você redireciona seu usuário usando o método exibido acima

Isso permite que o aluno vá diretamente ao ponto que contém a explicação necessária — aumentando retenção e experiência.

---
<a id="getcurrentcontent"></a>
# Como funciona o `getCurrentContent`

O componente `<tutor-chat>` precisa saber **onde o aluno está atualmente no curso** para enviar essa informação ao backend da IA.  
Com isso, a IA consegue responder de forma contextualizada (ex.: *"você está na página 3", "você está no minuto 12 do vídeo"*).

Para isso existe a função callback:

```ts
getCurrentContent: () => Promise<CurrentContentResponse>
```

---

## O que o chat espera receber?

O componente sempre chamará `getCurrentContent()` antes de enviar uma mensagem para a IA.

O retorno deve seguir a interface:

```ts
export type CurrentContentResponse = {
  externalId: string;
  position: number;
}
```

### Significado dos campos

| Campo | Descrição |
|-------|-----------|
| **externalId** | Identificador do conteúdo atual (vídeo, PDF, ...). |
| **position** | Posição atual dentro do conteúdo. <br> Para **vídeos**, é o tempo em milissegundos. <br> Para **textos**, é o número da página atual. |

---

##  Exemplo real de retorno (do Blazor)

```csharp
[JSInvokable]
public async Task<object> GetCurrentContent()
{
    if (_current?.DocumentFileType == "Text")
    {
        return new
        {
            documentId = _current?.ExternalId is not null ? _current?.ExternalId : _current?.Id.ToString(),
            type = 1,
            position = CurrentPage,
            isExternalId = true
        };
    }
    else
    {
        var currentVideoTime = await GetCurrentTimeAsync();
        return new
        {
            documentId = _current?.ExternalId is not null ? _current?.ExternalId : _current?.Id.ToString(),
            type = 0,
            position = currentVideoTime,
            isExternalId = _current?.ExternalId is not null
        };
    }
}
```

---

##  Como o chat converte isso internamente

```ts
return {
  externalId: object.documentId,
  position: object.position
};
```

---

## Como o cliente deve implementar o `getCurrentContent`

### ✔ Exemplo para vídeo

```js
getCurrentContent: async () => {
  return {
    externalId: "video-aula-12",
    position: player.currentTime * 1000
  };
}
```

### Exemplo para PDF/texto

```js
getCurrentContent: async () => {
  return {
    externalId: "pdf-capitulo-3",
    position: pdfViewer.currentPage
  };
}
```

---

## Resumo técnico

- `getCurrentContent()` **é obrigatório**
- Deve retornar `{ externalId, position }`
- Para vídeos → posição em **milissegundos**
- Para PDFs/textos → posição é a **página atual**

---

Fim.
