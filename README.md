### Júlio César Zuppa Araújo
Analista Desenvolvedor de Sistemas. Curitiba/PR - Brasil



#### Contatos
<a href="https://wa.me/5541988654956">
  <img src="https://img.shields.io/badge/WHATSAPP-%2325D366.svg?&style=for-the-badge&logo=whatsapp&logoColor=white"/>
</a>
<a href="mailto:juliozuppa@gmail.com">
  <img src="https://img.shields.io/badge/gmail-%23D14836.svg?&style=for-the-badge&logo=gmail&logoColor=white"/>
</a>

#### Redes Sociais
<a href="https://www.linkedin.com/in/juliozuppa/">
  <img src="https://img.shields.io/badge/linkedin-%230077B5.svg?&style=for-the-badge&logo=linkedin&logoColor=white"/>
</a>


// Remember old renderer, if overridden, or proxy to default renderer
var defaultRender = md.renderer.rules.link_open || function(tokens, idx, options, env, self) {
  return self.renderToken(tokens, idx, options);
};

md.renderer.rules.link_open = function (tokens, idx, options, env, self) {
  // If you are sure other plugins can't add `target` - drop check below
  var aIndex = tokens[idx].attrIndex('target');

  if (aIndex < 0) {
    tokens[idx].attrPush(['target', '_blank']); // add new attribute
  } else {
    tokens[idx].attrs[aIndex][1] = '_blank';    // replace value of existing attr
  }

  // pass token to default renderer.
  return defaultRender(tokens, idx, options, env, self);
};


<!--
**juliozuppa/juliozuppa** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->
