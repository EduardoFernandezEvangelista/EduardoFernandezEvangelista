# 📱🌙 Flutter — Desenvolvimento Mobile com Dark Theme

Repositório educacional desenvolvido para estudar e praticar o desenvolvimento de aplicativos móveis utilizando **Flutter** e a linguagem **Dart**, com foco na criação de interfaces modernas utilizando **Dark Theme (Tema Escuro)** e componentes do **Material Design 3**.

O objetivo deste projeto é aprender progressivamente desde os conceitos básicos do Flutter até a criação de uma aplicação mobile organizada, com múltiplas telas, navegação, imagens, botões, componentes reutilizáveis e temas personalizados.

---

## 🎯 Objetivo do Projeto

Este repositório tem como objetivo aprender e praticar:

* 📱 Desenvolvimento de aplicativos móveis com Flutter.
* 🧱 Estrutura básica de um projeto Flutter.
* 🧩 Widgets fundamentais.
* 🎨 Criação de interfaces modernas.
* 🌙 Utilização de Dark Theme.
* ☀️ Tema claro e tema escuro.
* 🔘 Botões e interações.
* 🖼️ Exibição de imagens.
* 📁 Utilização de imagens locais.
* 🌐 Utilização de imagens através da internet.
* 🔗 Criação de links externos.
* 🧭 Navegação entre telas.
* 🔙 Retorno para a última tela navegada.
* 📱 Barra de navegação inferior.
* 🎯 Utilização de ícones.
* 🖼️ Logo do aplicativo.
* 📦 Organização da interface.
* 🔄 Componentes reutilizáveis.
* 📁 Organização de projetos.
* 🧠 Boas práticas de desenvolvimento.

---

# 🚀 O que é Flutter?

**Flutter** é um framework de desenvolvimento criado para construir aplicações multiplataforma utilizando uma única base de código.

Com Flutter, é possível desenvolver aplicações para:

* 🤖 Android.
* 🍎 iOS.
* 🌐 Web.
* 🖥️ Windows.
* 🖥️ macOS.
* 🐧 Linux.

Flutter utiliza principalmente a linguagem **Dart**.

A principal característica do Flutter é a utilização de **Widgets**.

Praticamente todos os elementos da interface são widgets.

Por exemplo:

* Um texto é um widget.
* Um botão é um widget.
* Uma imagem é um widget.
* Uma coluna é um widget.
* Uma tela inteira pode ser um widget.

---

## 🎯 Flutter e Dart

A linguagem utilizada para desenvolver aplicações Flutter é o **Dart**.

Exemplo simples:

```dart
void main() {
  print('Olá, Flutter!');
}
```

A função `main()` representa o ponto inicial de execução de um programa Dart.

No Flutter, normalmente utilizamos `runApp()` para iniciar a aplicação.

```dart
void main() {
  runApp(const MeuApp());
}
```

---

# 🧩 O que são Widgets?

Widgets são os componentes utilizados para construir a interface de uma aplicação Flutter.

Exemplo:

```dart
Text('Olá, Flutter!');
```

O código acima cria um texto.

Outro exemplo:

```dart
Icon(Icons.home);
```

Cria um ícone.

Outro:

```dart
ElevatedButton(
  onPressed: () {},
  child: const Text('Clique aqui'),
);
```

Cria um botão.

---

# ⚡ StatelessWidget e StatefulWidget

No Flutter existem diferentes tipos de widgets.

Os dois principais são:

* `StatelessWidget`
* `StatefulWidget`

---

## 📄 StatelessWidget

Um `StatelessWidget` representa um widget que não possui estado interno que muda durante sua utilização.

Exemplo:

```dart
class TelaInicial extends StatelessWidget {
  const TelaInicial({super.key});

  @override
  Widget build(BuildContext context) {
    return const Text('Olá!');
  }
}
```

Utilize `StatelessWidget` quando o conteúdo da interface não precisa ser alterado dinamicamente.

---

## 🔄 StatefulWidget

Um `StatefulWidget` possui um estado que pode ser alterado durante a execução da aplicação.

Exemplo:

```dart
class Contador extends StatefulWidget {
  const Contador({super.key});

  @override
  State<Contador> createState() => _ContadorState();
}

class _ContadorState extends State<Contador> {
  int contador = 0;

  @override
  Widget build(BuildContext context) {
    return Column(
      children: [
        Text('Valor: $contador'),
        ElevatedButton(
          onPressed: () {
            setState(() {
              contador++;
            });
          },
          child: const Text('Adicionar'),
        ),
      ],
    );
  }
}
```

O método `setState()` informa ao Flutter que o estado foi alterado e que a interface precisa ser reconstruída.

---

# 🧱 Estrutura Básica de um Projeto Flutter

Uma estrutura básica pode ser organizada da seguinte forma:

```text
meu_app/
│
├── android/
├── ios/
├── lib/
│   └── main.dart
├── assets/
│   └── images/
├── test/
├── pubspec.yaml
└── README.md
```

---

## 📁 `lib/`

A pasta `lib` normalmente contém o código principal da aplicação.

Exemplo:

```text
lib/
├── main.dart
├── pages/
├── widgets/
├── themes/
└── routes/
```

---

## ▶️ `main.dart`

O arquivo `main.dart` normalmente representa o ponto inicial da aplicação.

Exemplo:

```dart
import 'package:flutter/material.dart';

void main() {
  runApp(const MeuApp());
}

class MeuApp extends StatelessWidget {
  const MeuApp({super.key});

  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      home: Scaffold(
        body: Center(
          child: Text('Olá, Flutter!'),
        ),
      ),
    );
  }
}
```

---

## 🖼️ `assets/`

A pasta `assets` é utilizada para armazenar recursos da aplicação.

Por exemplo:

```text
assets/
└── images/
    ├── logo.png
    └── flutter.png
```

Podemos armazenar:

* Imagens.
* Logos.
* Ícones.
* Arquivos JSON.
* Fontes.
* Outros recursos.

---

## 📦 `pubspec.yaml`

O arquivo `pubspec.yaml` é utilizado para configurar o projeto.

Entre suas funções estão:

* Adicionar dependências.
* Configurar imagens.
* Configurar fontes.
* Definir informações do projeto.

Exemplo de configuração de imagens:

```yaml
flutter:
  assets:
    - assets/images/
```

---

# ▶️ Primeiro Aplicativo Flutter

Exemplo básico:

```dart
import 'package:flutter/material.dart';

void main() {
  runApp(const MeuApp());
}

class MeuApp extends StatelessWidget {
  const MeuApp({super.key});

  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      home: Scaffold(
        appBar: AppBar(
          title: const Text('Meu Primeiro App'),
        ),
        body: const Center(
          child: Text(
            'Olá, Flutter!',
          ),
        ),
      ),
    );
  }
}
```

---

## 🔍 Explicação do código

### `main()`

Representa o ponto inicial da aplicação.

```dart
void main() {
}
```

---

### `runApp()`

Inicia a aplicação Flutter.

```dart
runApp(const MeuApp());
```

---

### `MaterialApp`

Representa a configuração principal da aplicação.

Pode configurar:

* Tema.
* Rotas.
* Tela inicial.
* Navegação.
* Idioma.

---

### `Scaffold`

Fornece a estrutura básica de uma tela.

Pode possuir:

* `AppBar`
* `body`
* `drawer`
* `bottomNavigationBar`
* `floatingActionButton`

---

### `AppBar`

Cria a barra superior da aplicação.

```dart
AppBar(
  title: const Text('Meu Aplicativo'),
)
```

---

### `Text`

Utilizado para exibir textos.

```dart
Text('Olá, Flutter!');
```

---

# 🌙 Dark Theme no Flutter

O **Dark Theme** é um tema visual baseado em cores escuras.

Exemplo de configuração:

```dart
ThemeData(
  brightness: Brightness.dark,
)
```

O tema escuro pode proporcionar:

* Menor luminosidade visual.
* Melhor conforto em ambientes escuros.
* Interfaces modernas.
* Personalização para diferentes preferências.
* Redução do brilho emitido pela tela.

---

# 🌙 Aplicação utilizando apenas Tema Escuro

```dart
import 'package:flutter/material.dart';

void main() {
  runApp(const MeuApp());
}

class MeuApp extends StatelessWidget {
  const MeuApp({super.key});

  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      theme: ThemeData(
        brightness: Brightness.dark,
        useMaterial3: true,
      ),
      home: const HomePage(),
    );
  }
}

class HomePage extends StatelessWidget {
  const HomePage({super.key});

  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(
        title: const Text('Flutter Dark'),
      ),
      body: const Center(
        child: Text(
          'Aplicativo utilizando Tema Escuro',
        ),
      ),
    );
  }
}
```

---

# ☀️🌙 Tema Claro e Tema Escuro

É possível configurar os dois temas.

```dart
MaterialApp(
  theme: ThemeData(
    brightness: Brightness.light,
    useMaterial3: true,
  ),

  darkTheme: ThemeData(
    brightness: Brightness.dark,
    useMaterial3: true,
  ),

  themeMode: ThemeMode.system,

  home: const HomePage(),
)
```

---

## 🎯 `theme`

Representa o tema claro.

```dart
theme: ThemeData(
  brightness: Brightness.light,
),
```

---

## 🌙 `darkTheme`

Representa o tema escuro.

```dart
darkTheme: ThemeData(
  brightness: Brightness.dark,
),
```

---

## ⚙️ `themeMode`

Define qual tema será utilizado.

Principais opções:

```dart
ThemeMode.light
```

Sempre utiliza o tema claro.

```dart
ThemeMode.dark
```

Sempre utiliza o tema escuro.

```dart
ThemeMode.system
```

Utiliza a configuração definida pelo sistema operacional.

---

# 🎨 ColorScheme

O `ColorScheme` permite organizar e definir as cores utilizadas pela aplicação.

Exemplo:

```dart
ThemeData(
  colorScheme: ColorScheme.fromSeed(
    seedColor: Colors.deepPurple,
    brightness: Brightness.dark,
  ),
)
```

Utilizando `ColorScheme.fromSeed()`, o Flutter gera uma combinação de cores baseada em uma cor principal.

Exemplo completo:

```dart
MaterialApp(
  theme: ThemeData(
    useMaterial3: true,

    colorScheme: ColorScheme.fromSeed(
      seedColor: Colors.blue,
      brightness: Brightness.light,
    ),
  ),

  darkTheme: ThemeData(
    useMaterial3: true,

    colorScheme: ColorScheme.fromSeed(
      seedColor: Colors.blue,
      brightness: Brightness.dark,
    ),
  ),

  themeMode: ThemeMode.system,

  home: const HomePage(),
)
```

---

# 🎨 Material Design e Material 3

O **Material Design** é um sistema de design utilizado para criar interfaces consistentes e modernas.

O Flutter possui widgets que seguem esse padrão visual.

O **Material 3** representa uma evolução do Material Design, trazendo melhorias relacionadas a:

* Cores.
* Tipografia.
* Componentes.
* Acessibilidade.
* Interfaces adaptáveis.
* Personalização.

No Flutter moderno, o Material 3 é o padrão de design utilizado pelos componentes Material.

Podemos deixar a configuração explícita:

```dart
ThemeData(
  useMaterial3: true,
)
```

Exemplo:

```dart
MaterialApp(
  theme: ThemeData(
    useMaterial3: true,

    colorScheme: ColorScheme.fromSeed(
      seedColor: Colors.deepPurple,
    ),
  ),

  home: const HomePage(),
)
```

---

# 🧩 Widgets Fundamentais

---

## 📱 MaterialApp

Configura a aplicação.

Principais propriedades:

* `home`
* `theme`
* `darkTheme`
* `themeMode`
* `routes`

Exemplo:

```dart
MaterialApp(
  home: const HomePage(),
)
```

---

## 🏗️ Scaffold

Fornece a estrutura básica da tela.

Exemplo:

```dart
Scaffold(
  appBar: AppBar(),
  body: const Center(),
)
```

---

## 📊 SafeArea

Evita que o conteúdo fique atrás de elementos do sistema.

```dart
SafeArea(
  child: Text('Conteúdo seguro'),
)
```

---

## 📦 Container

Cria uma área configurável.

```dart
Container(
  padding: const EdgeInsets.all(20),
  child: const Text('Container'),
)
```

Pode ser utilizado para:

* Espaçamento.
* Tamanho.
* Decoração.
* Cor.
* Bordas.

---

## 📏 Padding

Adiciona espaçamento interno.

```dart
Padding(
  padding: const EdgeInsets.all(16),
  child: Text('Texto'),
)
```

---

## 🎯 Center

Centraliza um widget.

```dart
Center(
  child: Text('Centralizado'),
)
```

---

## 📐 SizedBox

Pode criar espaços ou definir dimensões.

```dart
SizedBox(
  width: 200,
  height: 100,
  child: Container(),
)
```

Para espaçamento:

```dart
const SizedBox(height: 20)
```

---

## ↔️ Row

Organiza widgets horizontalmente.

```dart
Row(
  children: [
    Icon(Icons.home),
    SizedBox(width: 10),
    Text('Início'),
  ],
)
```

---

## ↕️ Column

Organiza widgets verticalmente.

```dart
Column(
  children: [
    Text('Primeiro'),
    Text('Segundo'),
    Text('Terceiro'),
  ],
)
```

---

## 📈 Expanded

Permite que um widget ocupe o espaço disponível.

```dart
Row(
  children: [
    Expanded(
      child: Container(
        height: 100,
      ),
    ),
  ],
)
```

---

## 🗂️ Stack

Permite sobrepor widgets.

```dart
Stack(
  children: [
    Container(
      height: 200,
    ),

    Positioned(
      top: 20,
      left: 20,
      child: Text('Texto sobreposto'),
    ),
  ],
)
```

---

## 🃏 Card

Cria cartões para organizar informações.

```dart
Card(
  child: Padding(
    padding: const EdgeInsets.all(16),
    child: Text('Conteúdo do Card'),
  ),
)
```

---

## ➖ Divider

Cria uma linha divisória.

```dart
const Divider()
```

---

# 📝 Widgets de Texto

O principal widget para exibir texto é:

```dart
Text()
```

Exemplo simples:

```dart
Text('Olá, Flutter!')
```

---

## 🎨 TextStyle

Permite personalizar o texto.

```dart
Text(
  'Texto personalizado',
  style: TextStyle(
    fontSize: 24,
    fontWeight: FontWeight.bold,
  ),
)
```

---

## 📐 TextAlign

Define o alinhamento.

```dart
Text(
  'Texto centralizado',
  textAlign: TextAlign.center,
)
```

---

## 💪 FontWeight

Define o peso da fonte.

```dart
fontWeight: FontWeight.bold
```

Outros exemplos:

```dart
FontWeight.normal
FontWeight.w500
FontWeight.w700
FontWeight.bold
```

---

## ✂️ TextOverflow

Define o comportamento quando o texto é muito grande.

```dart
Text(
  'Um texto muito longo',
  overflow: TextOverflow.ellipsis,
)
```

---

# 🔘 Botões no Flutter

O Flutter possui diversos tipos de botões.

Principais exemplos:

* `ElevatedButton`
* `FilledButton`
* `OutlinedButton`
* `TextButton`
* `IconButton`
* `FloatingActionButton`

---

## ElevatedButton

```dart
ElevatedButton(
  onPressed: () {
    print('Botão clicado');
  },
  child: const Text('Clique aqui'),
)
```

---

## FilledButton

```dart
FilledButton(
  onPressed: () {
    print('Ação executada');
  },
  child: const Text('Continuar'),
)
```

---

## OutlinedButton

```dart
OutlinedButton(
  onPressed: () {},
  child: const Text('Cancelar'),
)
```

---

## TextButton

```dart
TextButton(
  onPressed: () {},
  child: const Text('Saiba mais'),
)
```

---

## IconButton

```dart
IconButton(
  onPressed: () {},
  icon: const Icon(Icons.favorite),
)
```

---

## FloatingActionButton

```dart
FloatingActionButton(
  onPressed: () {
    print('Botão flutuante');
  },

  child: const Icon(Icons.add),
)
```

---

# 🎨 Botão Estilizado

```dart
ElevatedButton(
  onPressed: () {},

  style: ElevatedButton.styleFrom(
    padding: const EdgeInsets.symmetric(
      horizontal: 24,
      vertical: 16,
    ),
  ),

  child: const Text('Botão Estilizado'),
)
```

---

# 🖼️ Imagens no Flutter

Existem diferentes formas de trabalhar com imagens.

As principais são:

* `Image.asset()`
* `Image.network()`

---

# 📁 Imagem Local

Primeiro, crie a estrutura:

```text
assets/
└── images/
    └── imagem.png
```

Depois configure o `pubspec.yaml`:

```yaml
flutter:
  assets:
    - assets/images/
```

Agora utilize a imagem:

```dart
Image.asset(
  'assets/images/imagem.png',
)
```

Exemplo com tamanho:

```dart
Image.asset(
  'assets/images/logo.png',
  width: 150,
  height: 150,
  fit: BoxFit.contain,
)
```

---

# 🌐 Imagem da Internet

Para carregar uma imagem da internet:

```dart
Image.network(
  'https://exemplo.com/imagem.jpg',
)
```

Exemplo completo:

```dart
Image.network(
  'https://picsum.photos/400',

  width: 300,
  height: 200,

  fit: BoxFit.cover,
)
```

---

## 📐 BoxFit

Controla como a imagem ocupa o espaço.

Principais opções:

```dart
BoxFit.cover
BoxFit.contain
BoxFit.fill
BoxFit.fitWidth
BoxFit.fitHeight
```

---

# 🔗 Links no Flutter

Para abrir links externos, uma solução comum é utilizar o pacote:

```text
url_launcher
```

Adicione a dependência:

```bash
flutter pub add url_launcher
```

Importe o pacote:

```dart
import 'package:url_launcher/url_launcher.dart';
```

Crie uma URL:

```dart
final Uri url = Uri.parse(
  'https://docs.flutter.dev/',
);
```

Depois:

```dart
FilledButton(
  onPressed: () async {
    if (await canLaunchUrl(url)) {
      await launchUrl(url);
    }
  },

  child: const Text('Abrir documentação'),
)
```

A função `launchUrl()` é responsável por solicitar a abertura da URL utilizando uma aplicação adequada no dispositivo.

---

# 🧭 Navegação Entre Telas

A navegação no Flutter normalmente é realizada utilizando o:

```dart
Navigator
```

Uma aplicação pode possuir várias telas.

Exemplo:

```text
Tela Inicial
     ↓
Tela de Perfil
     ↓
Tela de Configurações
```

---

## ➡️ Navigator.push()

Para abrir uma nova tela:

```dart
Navigator.push(
  context,

  MaterialPageRoute(
    builder: (context) => const PerfilPage(),
  ),
);
```

---

## 📄 Tela Inicial

```dart
class HomePage extends StatelessWidget {
  const HomePage({super.key});

  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(
        title: const Text('Início'),
      ),

      body: Center(
        child: ElevatedButton(
          onPressed: () {
            Navigator.push(
              context,

              MaterialPageRoute(
                builder: (context) => const PerfilPage(),
              ),
            );
          },

          child: const Text('Abrir Perfil'),
        ),
      ),
    );
  }
}
```

---

## 👤 Tela de Perfil

```dart
class PerfilPage extends StatelessWidget {
  const PerfilPage({super.key});

  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(
        title: const Text('Perfil'),
      ),

      body: Center(
        child: ElevatedButton(
          onPressed: () {
            Navigator.push(
              context,

              MaterialPageRoute(
                builder: (context) => const ConfiguracoesPage(),
              ),
            );
          },

          child: const Text('Configurações'),
        ),
      ),
    );
  }
}
```

---

# 🔙 Voltar para a Última Tela

Para voltar para a tela anterior:

```dart
Navigator.pop(context);
```

O `Navigator` trabalha com uma estrutura semelhante a uma pilha.

Exemplo:

```text
Home
  ↓
Perfil
  ↓
Configurações
```

Ao executar:

```dart
Navigator.pop(context);
```

A tela atual é removida.

Resultado:

```text
Home
  ↓
Perfil
```

---

## Exemplo

```dart
ElevatedButton.icon(
  onPressed: () {
    Navigator.pop(context);
  },

  icon: const Icon(Icons.arrow_back),

  label: const Text('Voltar'),
)
```

---

# 🗺️ Rotas Nomeadas

Rotas nomeadas ajudam a organizar aplicações maiores.

Exemplo:

```dart
MaterialApp(
  initialRoute: '/',

  routes: {
    '/': (context) => const HomePage(),

    '/perfil': (context) => const PerfilPage(),

    '/configuracoes': (context) =>
        const ConfiguracoesPage(),
  },
)
```

Para navegar:

```dart
Navigator.pushNamed(
  context,
  '/perfil',
);
```

Para voltar:

```dart
Navigator.pop(context);
```

Rotas nomeadas são úteis quando existem diversas telas e você deseja centralizar a organização da navegação.

---

# 📱 NavigationBar

A `NavigationBar` é o componente moderno do Material 3 para navegação entre destinos principais.

Exemplo:

```text
🏠 Início
📚 Estudos
👤 Perfil
⚙️ Configurações
```

---

## Exemplo completo

```dart
class HomePage extends StatefulWidget {
  const HomePage({super.key});

  @override
  State<HomePage> createState() => _HomePageState();
}

class _HomePageState extends State<HomePage> {
  int selectedIndex = 0;

  final List<Widget> pages = const [
    Center(child: Text('Início')),
    Center(child: Text('Estudos')),
    Center(child: Text('Perfil')),
    Center(child: Text('Configurações')),
  ];

  @override
  Widget build(BuildContext context) {
    return Scaffold(
      body: pages[selectedIndex],

      bottomNavigationBar: NavigationBar(
        selectedIndex: selectedIndex,

        onDestinationSelected: (index) {
          setState(() {
            selectedIndex = index;
          });
        },

        destinations: const [
          NavigationDestination(
            icon: Icon(Icons.home),
            label: 'Início',
          ),

          NavigationDestination(
            icon: Icon(Icons.menu_book),
            label: 'Estudos',
          ),

          NavigationDestination(
            icon: Icon(Icons.person),
            label: 'Perfil',
          ),

          NavigationDestination(
            icon: Icon(Icons.settings),
            label: 'Configurações',
          ),
        ],
      ),
    );
  }
}
```

---

## 🔢 selectedIndex

Armazena o índice da tela selecionada.

```dart
int selectedIndex = 0;
```

---

## 🔄 onDestinationSelected

É executado quando o usuário seleciona um item.

```dart
onDestinationSelected: (index) {
  setState(() {
    selectedIndex = index;
  });
}
```

---

## 📍 NavigationDestination

Representa cada destino da barra.

```dart
NavigationDestination(
  icon: Icon(Icons.home),
  label: 'Início',
)
```

---

# 📱 NavigationBar x BottomNavigationBar

### NavigationBar

É a opção moderna alinhada ao Material 3.

```dart
NavigationBar()
```

### BottomNavigationBar

É um componente tradicional para navegação inferior.

```dart
BottomNavigationBar()
```

Para projetos novos utilizando Material 3, é recomendado conhecer e considerar a utilização da `NavigationBar`.

---

# ☰ Menu de Navegação com Drawer

O `Drawer` permite criar um menu lateral.

Exemplo:

```dart
Drawer(
  child: ListView(
    children: [
      const DrawerHeader(
        child: Column(
          children: [
            Icon(
              Icons.school,
              size: 50,
            ),

            Text(
              'Flutter Dark',
            ),
          ],
        ),
      ),

      ListTile(
        leading: const Icon(Icons.home),

        title: const Text('Início'),

        onTap: () {},
      ),

      ListTile(
        leading: const Icon(Icons.settings),

        title: const Text('Configurações'),

        onTap: () {},
      ),
    ],
  ),
)
```

---

# 🖼️ Logo do Aplicativo

Uma logo pode ser armazenada em:

```text
assets/
└── images/
    └── logo.png
```

Exemplo:

```dart
Center(
  child: Image.asset(
    'assets/images/logo.png',

    width: 120,
    height: 120,

    fit: BoxFit.contain,
  ),
)
```

---

# 🎯 Ícones

Flutter possui diversos ícones através da classe:

```dart
Icons
```

Exemplos:

```dart
Icons.home
Icons.person
Icons.settings
Icons.menu
Icons.arrow_back
Icons.dark_mode
Icons.light_mode
```

---

## Ícone em botão

```dart
IconButton(
  onPressed: () {},

  icon: const Icon(
    Icons.settings,
  ),
)
```

---

## Ícone no AppBar

```dart
AppBar(
  title: const Text('Aplicativo'),

  actions: [
    IconButton(
      onPressed: () {},

      icon: const Icon(
        Icons.dark_mode,
      ),
    ),
  ],
)
```

---

# 🃏 Cards

O widget `Card` é utilizado para apresentar conteúdos organizados.

Exemplo:

```dart
Card(
  child: Padding(
    padding: const EdgeInsets.all(16),

    child: Column(
      crossAxisAlignment: CrossAxisAlignment.start,

      children: [
        const Icon(
          Icons.menu_book,
        ),

        const SizedBox(height: 10),

        const Text(
          'Flutter',
        ),

        const SizedBox(height: 10),

        ElevatedButton(
          onPressed: () {},

          child: const Text('Estudar'),
        ),
      ],
    ),
  ),
)
```

Os cards podem apresentar:

* Informações.
* Imagens.
* Botões.
* Links.
* Cursos.
* Conteúdos.

---

# 📋 Listas

---

## ListView

Cria uma lista rolável.

```dart
ListView(
  children: const [
    ListTile(
      title: Text('Flutter'),
    ),

    ListTile(
      title: Text('Dart'),
    ),
  ],
)
```

---

## ListView.builder

Ideal para criar listas maiores.

```dart
ListView.builder(
  itemCount: 10,

  itemBuilder: (context, index) {
    return ListTile(
      title: Text(
        'Item ${index + 1}',
      ),
    );
  },
)
```

---

## ListTile

Representa um item de lista.

```dart
ListTile(
  leading: const Icon(
    Icons.menu_book,
  ),

  title: const Text(
    'Flutter',
  ),

  subtitle: const Text(
    'Estudo de desenvolvimento mobile',
  ),

  trailing: const Icon(
    Icons.arrow_forward,
  ),

  onTap: () {
    print('Item clicado');
  },
)
```

---

# 🔄 Componentes Reutilizáveis

Criar widgets reutilizáveis evita repetição de código.

Exemplos:

```text
BotaoPersonalizado
CardPersonalizado
Cabecalho
MenuItem
```

---

## 🔘 BotaoPersonalizado

```dart
class BotaoPersonalizado extends StatelessWidget {
  final String texto;
  final VoidCallback onPressed;

  const BotaoPersonalizado({
    super.key,
    required this.texto,
    required this.onPressed,
  });

  @override
  Widget build(BuildContext context) {
    return FilledButton(
      onPressed: onPressed,

      child: Text(texto),
    );
  }
}
```

Utilização:

```dart
BotaoPersonalizado(
  texto: 'Continuar',

  onPressed: () {
    print('Botão clicado');
  },
)
```

---

## 🃏 CardPersonalizado

```dart
class CardPersonalizado extends StatelessWidget {
  final String titulo;
  final String descricao;
  final IconData icone;

  const CardPersonalizado({
    super.key,
    required this.titulo,
    required this.descricao,
    required this.icone,
  });

  @override
  Widget build(BuildContext context) {
    return Card(
      child: ListTile(
        leading: Icon(icone),

        title: Text(titulo),

        subtitle: Text(descricao),
      ),
    );
  }
}
```

---

# 📁 Organização do Projeto

Uma possível organização:

```text
lib/
│
├── main.dart
│
├── pages/
│   ├── home_page.dart
│   ├── estudos_page.dart
│   ├── perfil_page.dart
│   └── configuracoes_page.dart
│
├── widgets/
│   ├── custom_button.dart
│   ├── custom_card.dart
│   └── app_logo.dart
│
├── themes/
│   └── app_theme.dart
│
└── routes/
    └── app_routes.dart
```

---

## 📄 pages/

Contém as telas da aplicação.

---

## 🧩 widgets/

Contém componentes reutilizáveis.

---

## 🎨 themes/

Contém configurações relacionadas aos temas.

Exemplo:

```text
app_theme.dart
```

---

## 🧭 routes/

Contém a organização das rotas da aplicação.

---

# 🚀 Projeto Prático — Aplicativo Flutter Dark

A proposta é criar um aplicativo de estudos.

Estrutura:

```text
📱 Aplicativo de Estudos

🏠 Home
│
├── 🖼️ Logo
├── 📚 Cards de conteúdo
├── 🔘 Botões
├── 🔗 Links
│
├── 📚 Estudos
│
├── 👤 Perfil
│
└── ⚙️ Configurações
```

---

# 📄 `main.dart`

```dart
import 'package:flutter/material.dart';

void main() {
  runApp(const FlutterDarkApp());
}

class FlutterDarkApp extends StatelessWidget {
  const FlutterDarkApp({super.key});

  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      debugShowCheckedModeBanner: false,

      title: 'Flutter Dark',

      theme: ThemeData(
        useMaterial3: true,

        colorScheme: ColorScheme.fromSeed(
          seedColor: Colors.blue,
          brightness: Brightness.light,
        ),
      ),

      darkTheme: ThemeData(
        useMaterial3: true,

        colorScheme: ColorScheme.fromSeed(
          seedColor: Colors.blue,
          brightness: Brightness.dark,
        ),
      ),

      themeMode: ThemeMode.dark,

      home: const MainPage(),
    );
  }
}
```

---

# 🏠 Página Principal com NavigationBar

```dart
class MainPage extends StatefulWidget {
  const MainPage({super.key});

  @override
  State<MainPage> createState() => _MainPageState();
}

class _MainPageState extends State<MainPage> {
  int selectedIndex = 0;

  final List<Widget> pages = const [
    HomePage(),
    EstudosPage(),
    PerfilPage(),
    ConfiguracoesPage(),
  ];

  @override
  Widget build(BuildContext context) {
    return Scaffold(
      body: pages[selectedIndex],

      bottomNavigationBar: NavigationBar(
        selectedIndex: selectedIndex,

        onDestinationSelected: (index) {
          setState(() {
            selectedIndex = index;
          });
        },

        destinations: const [
          NavigationDestination(
            icon: Icon(Icons.home_outlined),
            selectedIcon: Icon(Icons.home),
            label: 'Início',
          ),

          NavigationDestination(
            icon: Icon(Icons.menu_book_outlined),
            selectedIcon: Icon(Icons.menu_book),
            label: 'Estudos',
          ),

          NavigationDestination(
            icon: Icon(Icons.person_outline),
            selectedIcon: Icon(Icons.person),
            label: 'Perfil',
          ),

          NavigationDestination(
            icon: Icon(Icons.settings_outlined),
            selectedIcon: Icon(Icons.settings),
            label: 'Configurações',
          ),
        ],
      ),
    );
  }
}
```

---

# 🏠 `home_page.dart`

```dart
class HomePage extends StatelessWidget {
  const HomePage({super.key});

  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(
        title: const Text(
          'Flutter Dark',
        ),
      ),

      body: SafeArea(
        child: ListView(
          padding: const EdgeInsets.all(16),

          children: [
            Center(
              child: Icon(
                Icons.flutter_dash,
                size: 100,
              ),
            ),

            const SizedBox(height: 20),

            Text(
              'Bem-vindo!',
              textAlign: TextAlign.center,

              style: Theme.of(context)
                  .textTheme
                  .headlineMedium,
            ),

            const SizedBox(height: 20),

            Card(
              child: ListTile(
                leading: const Icon(
                  Icons.menu_book,
                ),

                title: const Text(
                  'Aprenda Flutter',
                ),

                subtitle: const Text(
                  'Estude widgets e desenvolvimento mobile.',
                ),
              ),
            ),

            Card(
              child: ListTile(
                leading: const Icon(
                  Icons.dark_mode,
                ),

                title: const Text(
                  'Dark Theme',
                ),

                subtitle: const Text(
                  'Aprenda a criar interfaces modernas.',
                ),
              ),
            ),

            const SizedBox(height: 20),

            FilledButton.icon(
              onPressed: () {
                Navigator.push(
                  context,

                  MaterialPageRoute(
                    builder: (context) =>
                        const DetalhesPage(),
                  ),
                );
              },

              icon: const Icon(
                Icons.arrow_forward,
              ),

              label: const Text(
                'Ver detalhes',
              ),
            ),
          ],
        ),
      ),
    );
  }
}
```

---

# 📚 Página de Estudos

```dart
class EstudosPage extends StatelessWidget {
  const EstudosPage({super.key});

  final List<String> estudos = const [
    'Widgets',
    'Layouts',
    'Dark Theme',
    'Navigation',
    'Imagens',
    'Botões',
  ];

  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(
        title: const Text('Estudos'),
      ),

      body: ListView.builder(
        itemCount: estudos.length,

        itemBuilder: (context, index) {
          return ListTile(
            leading: const Icon(
              Icons.school,
            ),

            title: Text(
              estudos[index],
            ),

            trailing: const Icon(
              Icons.arrow_forward,
            ),

            onTap: () {},
          );
        },
      ),
    );
  }
}
```

---

# 👤 Página de Perfil

```dart
class PerfilPage extends StatelessWidget {
  const PerfilPage({super.key});

  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(
        title: const Text('Perfil'),
      ),

      body: const Center(
        child: Column(
          mainAxisAlignment:
              MainAxisAlignment.center,

          children: [
            CircleAvatar(
              radius: 50,

              child: Icon(
                Icons.person,
                size: 50,
              ),
            ),

            SizedBox(height: 20),

            Text(
              'Estudante Flutter',
            ),
          ],
        ),
      ),
    );
  }
}
```

---

# ⚙️ Página de Configurações

```dart
class ConfiguracoesPage extends StatelessWidget {
  const ConfiguracoesPage({super.key});

  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(
        title: const Text(
          'Configurações',
        ),
      ),

      body: ListView(
        children: const [
          ListTile(
            leading: Icon(
              Icons.dark_mode,
            ),

            title: Text(
              'Tema Escuro',
            ),
          ),

          ListTile(
            leading: Icon(
              Icons.notifications,
            ),

            title: Text(
              'Notificações',
            ),
          ),

          ListTile(
            leading: Icon(
              Icons.info,
            ),

            title: Text(
              'Sobre o aplicativo',
            ),
          ),
        ],
      ),
    );
  }
}
```

---

# 📄 Página de Detalhes e Botão Voltar

```dart
class DetalhesPage extends StatelessWidget {
  const DetalhesPage({super.key});

  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(
        title: const Text(
          'Detalhes',
        ),
      ),

      body: Center(
        child: FilledButton.icon(
          onPressed: () {
            Navigator.pop(context);
          },

          icon: const Icon(
            Icons.arrow_back,
          ),

          label: const Text(
            'Voltar',
          ),
        ),
      ),
    );
  }
}
```

---

# 💻 Como Executar o Projeto

## Criar um novo projeto

```bash
flutter create nome_do_projeto
```

Cria uma nova aplicação Flutter.

---

## Entrar na pasta

```bash
cd nome_do_projeto
```

Acessa a pasta do projeto.

---

## Instalar dependências

```bash
flutter pub get
```

Baixa e configura as dependências declaradas no `pubspec.yaml`.

---

## Executar a aplicação

```bash
flutter run
```

Inicia a aplicação em um dispositivo ou emulador disponível.

---

# 📚 Principais Widgets Estudados

| Widget                  | Função                              |
| ----------------------- | ----------------------------------- |
| `MaterialApp`           | Configuração principal da aplicação |
| `Scaffold`              | Estrutura básica da tela            |
| `AppBar`                | Barra superior                      |
| `SafeArea`              | Área segura da tela                 |
| `Text`                  | Exibir textos                       |
| `Container`             | Criar áreas personalizadas          |
| `Padding`               | Adicionar espaçamento interno       |
| `Center`                | Centralizar widgets                 |
| `SizedBox`              | Criar espaços ou definir tamanho    |
| `Row`                   | Organizar horizontalmente           |
| `Column`                | Organizar verticalmente             |
| `Expanded`              | Ocupar espaço disponível            |
| `Stack`                 | Sobrepor widgets                    |
| `Image.asset`           | Exibir imagem local                 |
| `Image.network`         | Exibir imagem da internet           |
| `ElevatedButton`        | Botão elevado                       |
| `FilledButton`          | Botão preenchido                    |
| `OutlinedButton`        | Botão com contorno                  |
| `TextButton`            | Botão de texto                      |
| `IconButton`            | Botão com ícone                     |
| `FloatingActionButton`  | Botão flutuante                     |
| `Card`                  | Cartão de conteúdo                  |
| `ListView`              | Lista rolável                       |
| `ListView.builder`      | Lista dinâmica                      |
| `ListTile`              | Item de lista                       |
| `Navigator`             | Navegação                           |
| `NavigationBar`         | Barra de navegação                  |
| `NavigationDestination` | Destino da NavigationBar            |
| `Drawer`                | Menu lateral                        |
| `Icon`                  | Exibir ícones                       |
| `Divider`               | Linha divisória                     |
| `CircleAvatar`          | Avatar circular                     |

---

# 🧠 Boas Práticas

Durante o desenvolvimento de aplicações Flutter:

* ✅ Crie widgets reutilizáveis.
* 📁 Separe as telas em arquivos.
* 📦 Evite arquivos muito grandes.
* 🎨 Utilize temas globais.
* 🖼️ Organize os assets.
* 📝 Utilize nomes claros.
* 💬 Comente apenas quando necessário.
* 🧹 Mantenha o código organizado.
* 🔄 Evite duplicação de código.
* 🎨 Utilize Material 3.
* 📱 Crie interfaces responsivas.
* 🧩 Divida componentes complexos em widgets menores.
* 📂 Organize o projeto por responsabilidade.
* 🎯 Mantenha uma navegação clara para o usuário.

---

# 🎓 Objetivos de Aprendizagem

Ao finalizar este projeto, o estudante deverá ser capaz de:

* Criar um aplicativo Flutter.
* Trabalhar com Dart.
* Criar múltiplas telas.
* Trabalhar com widgets.
* Criar interfaces modernas.
* Criar Dark Theme.
* Trabalhar com tema claro.
* Trabalhar com imagens.
* Adicionar logos.
* Criar botões.
* Trabalhar com links.
* Navegar entre telas.
* Retornar para a tela anterior.
* Criar uma NavigationBar.
* Utilizar ícones.
* Criar componentes reutilizáveis.
* Organizar um projeto Flutter.

---

# 🔗 Documentação Oficial

## 📱 Flutter

* [Site oficial do Flutter](https://flutter.dev/?utm_source=chatgpt.com)
* [Documentação oficial do Flutter](https://docs.flutter.dev/?utm_source=chatgpt.com)
* [Catálogo de Widgets](https://docs.flutter.dev/ui/widgets?utm_source=chatgpt.com)
* [Widgets Material](https://docs.flutter.dev/ui/widgets/material?source=post_page-----67d1d0a684f0----------------------&utm_source=chatgpt.com)

## 🎯 Dart

* [Site oficial do Dart](https://dart.dev/?utm_source=chatgpt.com)
* [Documentação do Dart](https://dart.dev/docs?utm_source=chatgpt.com)
* [Introdução à linguagem Dart](https://dart.dev/language?lang=en&utm_source=chatgpt.com)
* [API do Dart](https://api.dart.dev/?utm_source=chatgpt.com)

## 🎨 Material Design

* [Material Design no Flutter](https://docs.flutter.dev/ui/design/material?utm_source=chatgpt.com)
* [Documentação oficial do Material Design](https://m3.material.io/?utm_source=chatgpt.com)

## 🧩 Widgets

* [Catálogo oficial de Widgets](https://docs.flutter.dev/ui/widgets?utm_source=chatgpt.com)
* [Assets, imagens e ícones](https://docs.flutter.dev/ui/widgets/assets?utm_source=chatgpt.com)
* [Widgets de estilo e temas](https://docs.flutter.dev/ui/widgets/styling?utm_source=chatgpt.com)

## 📱 NavigationBar

* [Documentação da NavigationBar](https://api.flutter.dev/flutter/material/NavigationBar-class.html?utm_source=chatgpt.com)
* [Personalização da NavigationBar](https://api.flutter.dev/flutter/material/NavigationBarThemeData-class.html?utm_source=chatgpt.com)

## 📦 Temas

* [ThemeData API](https://api.flutter.dev/flutter/material/ThemeData-class.html?utm_source=chatgpt.com)
* [Material 3 como padrão no Flutter](https://docs.flutter.dev/release/breaking-changes/material-3-default?utm_source=chatgpt.com)

---

# 📚 Recursos para Estudo

Para aprofundar os conhecimentos, utilize principalmente os recursos oficiais:

* [Documentação do Flutter](https://docs.flutter.dev/?utm_source=chatgpt.com)
* [Catálogo de Widgets do Flutter](https://docs.flutter.dev/ui/widgets?utm_source=chatgpt.com)
* [Widgets Material](https://docs.flutter.dev/ui/widgets/material?source=post_page-----67d1d0a684f0----------------------&utm_source=chatgpt.com)
* [Documentação do Dart](https://dart.dev/docs?utm_source=chatgpt.com)
* [Introdução ao Dart](https://dart.dev/language?lang=en&utm_source=chatgpt.com)
* [Assets, imagens e ícones no Flutter](https://docs.flutter.dev/ui/widgets/assets?utm_source=chatgpt.com)
* [Material Design no Flutter](https://docs.flutter.dev/ui/design/material?utm_source=chatgpt.com)
* [NavigationBar no Flutter](https://api.flutter.dev/flutter/material/NavigationBar-class.html?utm_source=chatgpt.com)

---

# 🚀 Próximos Passos

Depois de dominar os conceitos apresentados neste projeto, continue estudando:

* Gerenciamento de estado.
* Formulários.
* Validação de dados.
* Consumo de APIs.
* Programação assíncrona.
* `Future` e `async/await`.
* Banco de dados local.
* Firebase.
* Autenticação.
* Animações.
* Responsividade.
* Testes.
* Arquitetura de aplicações.

---

# 🎯 Conclusão

Flutter permite criar aplicações modernas e multiplataforma utilizando uma única base de código.

Durante este projeto foram estudados conceitos importantes como:

* Widgets.
* Material 3.
* Dark Theme.
* Layouts.
* Botões.
* Imagens.
* Links.
* Navegação.
* Rotas.
* NavigationBar.
* Drawer.
* Ícones.
* Cards.
* Listas.
* Componentes reutilizáveis.
* Organização de projetos.

A melhor forma de aprender Flutter é praticando.

Experimente modificar os exemplos, criar novas telas, alterar os temas, adicionar imagens e desenvolver novas funcionalidades.

> 📱 **Aprender desenvolvimento mobile é um processo contínuo. Quanto mais projetos você construir, mais experiência terá com Flutter e Dart.**

---

## ⭐ Projeto Educacional

Este repositório possui finalidade educacional e foi desenvolvido para auxiliar no aprendizado e na prática de:

```text
Flutter
+
Dart
+
Material 3
+
Dark Theme
+
Desenvolvimento Mobile
```

**Bons estudos e bom desenvolvimento! 🚀📱🌙**
