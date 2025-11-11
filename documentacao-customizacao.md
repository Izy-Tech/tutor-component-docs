# Documentação Customização

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
<img width="366" height="150" alt="image" src="https://github.com/user-attachments/assets/5186c418-ee90-4fa8-ade2-fef28cb1540b" />
<img width="366" height="150" alt="image" src="https://github.com/user-attachments/assets/4866b89e-ccc7-49d3-bea7-4065d1748140" />

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
<img width="361" height="150" alt="image" src="https://github.com/user-attachments/assets/8bdb58bf-4f7b-4360-9eda-d6fcdc0d534c" />

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
<img width="367" height="147" alt="image" src="https://github.com/user-attachments/assets/67a6a086-fa7a-4f05-97ef-3bd1100c860a" />

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
<img width="417" height="163" alt="image" src="https://github.com/user-attachments/assets/b075577c-508e-45cb-a3d3-8550d83edb06" />

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
<img width="361" height="148" alt="image" src="https://github.com/user-attachments/assets/260b3b0e-6164-4415-8935-a6cd9f70cd68" />

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
<img width="428" height="189" alt="image" src="https://github.com/user-attachments/assets/67c4a3dd-79dc-4f7b-ace5-3cd87d93f3c8" />

## Avatares

### Default

<img width="769" height="256" alt="image" src="https://github.com/user-attachments/assets/6971df75-2d96-4a4f-87b4-7b8356d956c6" />

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
<img width="788" height="239" alt="image" src="https://github.com/user-attachments/assets/c403b3f7-2737-4018-a32c-3806e5a49b46" />

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
<img width="756" height="180" alt="image" src="https://github.com/user-attachments/assets/66c6f0eb-4f51-46b5-a25f-e271972b70b5" />

## Mensagem do chat

### Default
<img width="744" height="180" alt="image" src="https://github.com/user-attachments/assets/85a6aa0a-4501-4046-bcd7-07c00c191151" />

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
<img width="728" height="184" alt="image" src="https://github.com/user-attachments/assets/6aeabbf3-50e9-4af0-9e0c-205072f82ca2" />

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
<img width="756" height="189" alt="image" src="https://github.com/user-attachments/assets/23339564-9908-4649-8730-a8254138207b" />

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
<img width="728" height="184" alt="image" src="https://github.com/user-attachments/assets/20fea71c-069b-43bd-8687-255188037844" />

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
<img width="756" height="189" alt="image" src="https://github.com/user-attachments/assets/b94fd792-4263-4075-9f70-1bced85e1dff" />

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
<img width="572" height="141" alt="image" src="https://github.com/user-attachments/assets/4f68367f-3b4c-4cf9-a827-223262786ae2" />

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
<img width="730" height="195" alt="image" src="https://github.com/user-attachments/assets/68d149af-2995-4d3e-a022-a2a6bcf39892" />

## Janela do chat

### Default
<img width="870" height="1109" alt="image" src="https://github.com/user-attachments/assets/916e6015-8032-4846-83b1-319381f023ba" />

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
<img width="838" height="1084" alt="image" src="https://github.com/user-attachments/assets/e9e32381-e390-428f-bfa5-095fa3447199" />

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
<img width="800" height="1061" alt="image" src="https://github.com/user-attachments/assets/518e250b-d2d4-4f4a-b43b-8a3b900b98be" />

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
<img width="797" height="1055" alt="image" src="https://github.com/user-attachments/assets/3a495d59-8b88-4150-8be8-8449ce9abc6e" />

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

<img width="455" height="151" alt="image" src="https://github.com/user-attachments/assets/1d7ec072-a730-4448-b516-60ae30132d00" />

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
<img width="831" height="1073" alt="image" src="https://github.com/user-attachments/assets/02b4ca53-86f8-4abc-87d9-f283e2531330" />

### Balões do Chat 
### Default
<img width="620" height="284" alt="image" src="https://github.com/user-attachments/assets/e655577f-203a-48da-96cf-2e18a6813b2b" />

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

<img width="425" height="298" alt="image" src="https://github.com/user-attachments/assets/a1c0cf4b-25aa-4c7a-8d9c-c9969c23fe77" />


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

<img width="467" height="331" alt="image" src="https://github.com/user-attachments/assets/0755abad-879a-4067-b234-34608bbdc1e3" />

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
<img width="509" height="347" alt="image" src="https://github.com/user-attachments/assets/0054b03e-33d6-45c0-a6fd-85b661533d5f" />


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

<img width="797" height="611" alt="image" src="https://github.com/user-attachments/assets/6ff22608-836b-4a17-b80d-297d59b3121a" />


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
<img width="777" height="319" alt="image" src="https://github.com/user-attachments/assets/69e9234f-71a2-4f90-ab23-6b2feca78052" />

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
<img width="728" height="331" alt="image" src="https://github.com/user-attachments/assets/f2290f7d-37c4-47e9-b05b-618da22c8546" />

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
<img width="713" height="336" alt="image" src="https://github.com/user-attachments/assets/bd58f921-6962-4677-bb5a-56ccc887a9c6" />

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
<img width="709" height="264" alt="image" src="https://github.com/user-attachments/assets/5f5575bd-dfcb-4efd-89b4-ce91465c7dc3" />

## Feedback

### Default
<img width="506" height="234" alt="image" src="https://github.com/user-attachments/assets/4d473e9b-d453-4409-b1b9-bf03280a0bc2" />
<img width="613" height="377" alt="image" src="https://github.com/user-attachments/assets/9699d28c-6988-40b0-b968-06f8a7fb20cb" />
<img width="692" height="402" alt="image" src="https://github.com/user-attachments/assets/01a732cd-ef85-433f-af49-ed0e9426e648" />
<img width="464" height="195" alt="image" src="https://github.com/user-attachments/assets/9a7a32ae-8658-42be-bdff-8263c0ba4d8d" />

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
<img width="528" height="269" alt="image" src="https://github.com/user-attachments/assets/b0f0eb8e-7a9e-44c0-b620-cf3446e6ce7d" />

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
<img width="500" height="252" alt="image" src="https://github.com/user-attachments/assets/02b1fb2e-ce6d-4545-93a7-5c3053b56597" />

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
<img width="545" height="248" alt="image" src="https://github.com/user-attachments/assets/2a333070-6eae-4df9-a016-0e9405990754" />

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
<img width="503" height="261" alt="image" src="https://github.com/user-attachments/assets/5ff21645-ef54-4cfb-9d8a-cb90a049a577" />

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
<img width="522" height="286" alt="image" src="https://github.com/user-attachments/assets/71c06946-551b-4e3a-9ad0-bb0f105c78ce" />

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
<img width="522" height="286" alt="image" src="https://github.com/user-attachments/assets/ad0fdc3a-164b-49cb-bedd-0c64bbe56369" />

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

<img width="398" height="227" alt="image" src="https://github.com/user-attachments/assets/c5d8e52d-88f5-462b-8ce3-5b6be70e1129" />

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

<img width="474" height="337" alt="image" src="https://github.com/user-attachments/assets/6ea46b3e-58c0-4be5-9040-74a452e2313f" />


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
<img width="673" height="375" alt="image" src="https://github.com/user-attachments/assets/591665b6-1272-4068-8126-1a0db55e37ae" />

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
<img width="650" height="395" alt="image" src="https://github.com/user-attachments/assets/fb53d29e-d063-4ef4-a573-b9103190befc" />

## Título

### Default
<img width="808" height="302" alt="image" src="https://github.com/user-attachments/assets/4e4a73fd-2219-434a-b3fd-2912e24bd306" />

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

<img width="708" height="266" alt="image" src="https://github.com/user-attachments/assets/931fcccf-9699-4b72-a1bc-f1be583a9e12" />

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
<img width="773" height="245" alt="image" src="https://github.com/user-attachments/assets/ca492c6f-1c45-4404-9402-610feb52aa9a" />

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

<img width="242" height="87" alt="image" src="https://github.com/user-attachments/assets/25ef4082-bc0c-4053-804b-7928636fce14" />

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
<img width="786" height="292" alt="image" src="https://github.com/user-attachments/assets/ba978d1b-d345-490e-a5db-218dc1c9939c" />

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
<img width="733" height="198" alt="image" src="https://github.com/user-attachments/assets/828f12c2-6008-4eb2-af61-ad48a9cb15c9" />

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
      avatar: 'https://cdn-icons-png.flaticon.com/512/147/147142.png',  
      baseAddress: 'https://localhost:7209',  
      startOpened: false,  
      showSuggestions: true  
    };
```

Resultado:  
<img width="369" height="169" alt="image" src="https://github.com/user-attachments/assets/635e047a-a5c1-40a9-acc3-023aafab9be4" />

Aberto código:  
```js
    tutorChat.options = {  
      organizationId: "4f0983fc-055c-44be-bafe-0f2d9e937f0b",  
      productId: "9206CEBB-17F0-5CFE-84A3-0C9B212FE1C8",  
      isExternalProductId: false,  
      getToken: getConsumerToken,  
      getCurrentContent: getCurrentContent,  
      avatar: 'https://cdn-icons-png.flaticon.com/512/147/147142.png',  
      baseAddress: 'https://localhost:7209',  
      startOpened: true,  
      showSuggestions: true  
    };
```

Resultado:  
<img width="783" height="988" alt="image" src="https://github.com/user-attachments/assets/39305559-63ae-4de7-a6b7-7f907f80682f" />

### Exibir/não exibir balões de sugestão (boolean)

Código mostrar:  
```js
    tutorChat.options = {  
      organizationId: "4f0983fc-055c-44be-bafe-0f2d9e937f0b",  
      productId: "9206CEBB-17F0-5CFE-84A3-0C9B212FE1C8",  
      isExternalProductId: false,  
      getToken: getConsumerToken,  
      getCurrentContent: getCurrentContent,  
      avatar: 'https://cdn-icons-png.flaticon.com/512/147/147142.png',  
      baseAddress: 'https://localhost:7209',  
      startOpened: true,  
      showSuggestions: true  
    };
```

Resultado:  
<img width="789" height="542" alt="image" src="https://github.com/user-attachments/assets/70438942-e70c-4006-b24e-2bf70c63d8b5" />

Código não mostrar:  
```js
    tutorChat.options = {  
      organizationId: "4f0983fc-055c-44be-bafe-0f2d9e937f0b",  
      productId: "9206CEBB-17F0-5CFE-84A3-0C9B212FE1C8",  
      isExternalProductId: false,  
      getToken: getConsumerToken,  
      getCurrentContent: getCurrentContent,  
      avatar: 'https://cdn-icons-png.flaticon.com/512/147/147142.png',  
      baseAddress: 'https://localhost:7209',  
      startOpened: true,  
      showSuggestions: false  
    };
```

Resultado:  
<img width="786" height="336" alt="image" src="https://github.com/user-attachments/assets/a2192805-7c3a-418f-b122-633962fcff5a" />




