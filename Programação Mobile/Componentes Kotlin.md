# Principais Componentes do Jetpack Compose

Esta documentação reúne os componentes essenciais que você deve conhecer para a prova, com exemplos práticos de como utilizá-los.

---

## LazyColumn e LazyRow

**Descrição:**  
Utilizados para exibir listas de forma eficiente, carregando os itens sob demanda.

### Exemplo com LazyColumn:
```kotlin
@Composable
fun ExemploLazyColumn() {
    val itens = (1..20).toList()
    LazyColumn {
        items(itens) { item ->
            Text(
                text = "Item $item",
                modifier = Modifier
                    .fillMaxWidth()
                    .padding(16.dp)
            )
        }
    }
}
```
### Exemplo com LazyRow:

```kotlin
@Composable
fun ExemploLazyRow() {
    val letras = listOf("A", "B", "C", "D", "E")
    LazyRow {
        items(letras) { letra ->
            Text(
                text = "Letra $letra",
                modifier = Modifier
                    .padding(16.dp)
                    .border(1.dp, Color.Gray)
                    .padding(8.dp)
            )
        }
    }
}
```
---
## Text

**Descrição:**  
Exibe textos com várias opções de estilização, como fonte, cor e tamanho.

### Exemplo:
```kotlin
@Composable
fun ExemploText() {
    Text(
        text = "Olá, Jetpack Compose!",
        fontSize = 20.sp,
        color = Color.Blue,
        modifier = Modifier.padding(16.dp)
    )
}
```

---

## Image

**Descrição:**  
Utilizado para exibir imagens, seja a partir de recursos bitmap ou vetoriais.

### Exemplo:
```kotlin
@Composable
fun ExemploImage() {
    Image(
        painter = painterResource(id = R.drawable.exemplo_imagem),
        contentDescription = "Exemplo de Imagem",
        modifier = Modifier
            .size(100.dp)
            .padding(16.dp)
    )
}
```

---

## InputText (TextField)

**Descrição:**  
Componente para entrada de texto do usuário. Em Compose, utiliza-se o `TextField`.

### Exemplo:
```kotlin
@Composable
fun ExemploTextField() {
    var texto by remember { mutableStateOf("") }
    TextField(
        value = texto,
        onValueChange = { novoTexto -> texto = novoTexto },
        label = { Text("Digite algo") },
        modifier = Modifier.padding(16.dp)
    )
}
```

---

## Button

**Descrição:**  
Botão que executa uma ação quando clicado.

### Exemplo:
```kotlin
@Composable
fun ExemploButton() {
    Button(
        onClick = { /* Executa alguma ação */ },
        modifier = Modifier.padding(16.dp)
    ) {
        Text("Clique Aqui")
    }
}
```

---

## Row

**Descrição:**  
Organiza os componentes horizontalmente, alinhando-os em uma linha.

### Exemplo:
```kotlin
@Composable
fun ExemploRow() {
    Row(
        modifier = Modifier
            .fillMaxWidth()
            .padding(16.dp),
        horizontalArrangement = Arrangement.SpaceBetween
    ) {
        Text("Item 1")
        Text("Item 2")
        Text("Item 3")
    }
}
```

---

## Column

**Descrição:**  
Organiza os componentes verticalmente, empilhando-os em uma coluna.

### Exemplo:
```kotlin
@Composable
fun ExemploColumn() {
    Column(
        modifier = Modifier
            .fillMaxWidth()
            .padding(16.dp),
        verticalArrangement = Arrangement.spacedBy(8.dp)
    ) {
        Text("Item A")
        Text("Item B")
        Text("Item C")
    }
}
```

---

## Box

**Descrição:**  
Container flexível que permite sobrepor componentes, possibilitando layouts customizados.

### Exemplo:
```kotlin
@Composable
fun ExemploBox() {
    Box(
        modifier = Modifier
            .size(150.dp)
            .padding(16.dp)
    ) {
        // Imagem de fundo
        Image(
            painter = painterResource(id = R.drawable.exemplo_imagem),
            contentDescription = null,
            modifier = Modifier.fillMaxSize()
        )
        // Texto sobreposto
        Text(
            text = "Sobreposto",
            modifier = Modifier.align(Alignment.Center),
            color = Color.White,
            fontWeight = FontWeight.Bold
        )
    }
}
```

---

Estude e pratique cada um desses exemplos para se familiarizar com os componentes essenciais do Jetpack Compose e garantir um bom desempenho na prova!
