# 🎯 Funcionalidade: Ocultar Cores e Tamanhos Esgotados

## 📋 Descrição
Esta funcionalidade permite ocultar automaticamente cores, tamanhos e outras variantes de produtos que estão esgotadas, mostrando apenas as opções disponíveis para o cliente.

## ⚙️ Como Ativar

### 1. Via Painel Administrativo (Recomendado)
1. Acesse **Admin → Temas**
2. Clique em **Personalizar** no tema ativo
3. Vá para **Configurações do tema → Produtos**
4. Procure por **"Variantes Esgotadas"**
5. Marque a opção **"Ocultar cores e tamanhos esgotados"**
6. Clique em **Salvar**

### 2. Via Código (Para desenvolvedores)
No arquivo `config/settings_data.json`, adicione:
```json
{
  "current": {
    "hide_sold_out_variants": true
  }
}
```

## 🔧 Como Funciona

### Comportamento Padrão (Desativado)
- ❌ Mostra TODAS as cores e tamanhos
- ❌ Opções esgotadas aparecem mas ficam desabilitadas
- ❌ Cliente pode tentar selecionar opções indisponíveis

### Comportamento Ativado
- ✅ Mostra APENAS cores e tamanhos disponíveis
- ✅ Opções esgotadas são completamente ocultadas
- ✅ Cliente só vê o que pode realmente comprar
- ✅ Interface mais limpa e intuitiva

## 📍 Onde Funciona
A funcionalidade é aplicada em:
- ✅ Página individual do produto
- ✅ Listagem de produtos (grades de coleção)
- ✅ Quick view (visualização rápida)
- ✅ Todos os tipos de seletor: cores, blocos, dropdown

## 🎨 Tipos de Seletor Suportados
- **Cores (Color Swatches)**: Círculos coloridos
- **Variantes com Imagem**: Miniaturas das variantes
- **Blocos (Block Swatches)**: Botões retangulares
- **Dropdown**: Listas suspensas

## 🧪 Como Testar

### Teste Básico
1. Escolha um produto com múltiplas cores/tamanhos
2. No admin, marque algumas variantes como "Esgotado"
3. Ative a funcionalidade
4. Vá à página do produto
5. Verifique se as opções esgotadas sumiram

### Teste com Snippet de Debug
Adicione temporariamente ao template do produto:
```liquid
{% render 'test-hide-variants' %}
```

### Teste Avançado
1. Crie um produto com 3 cores e 3 tamanhos (9 variantes)
2. Deixe apenas 2-3 variantes disponíveis
3. Ative a funcionalidade
4. Verifique se apenas as cores/tamanhos com estoque aparecem

## 🔍 Resolução de Problemas

### Problema: Funcionalidade não está funcionando
**Soluções:**
1. Verifique se a configuração está salva
2. Limpe o cache do navegador (Ctrl+F5)
3. Verifique se o produto tem variantes configuradas
4. Confirme se algumas variantes estão realmente esgotadas

### Problema: Todas as opções sumiram
**Causa:** Todas as variantes estão esgotadas
**Solução:** Marque pelo menos uma variante como disponível

### Problema: Não funciona em produtos específicos
**Verificar:**
1. Se o produto tem variantes (não apenas produto simples)
2. Se as variantes têm estoque configurado corretamente
3. Se o template do produto está usando os snippets corretos

## 📁 Arquivos Modificados
- `config/settings_schema.json` - Configuração no admin
- `snippets/filter-available-variants.liquid` - Lógica de filtro
- `snippets/product-info.liquid` - Página do produto
- `snippets/product-item.liquid` - Listagem de produtos

## 🚀 Benefícios para a Loja
- **Melhor UX**: Cliente não perde tempo com opções indisponíveis
- **Menos Frustração**: Evita tentativas de compra de produtos esgotados
- **Interface Limpa**: Mostra apenas o que importa
- **Conversão**: Foco nas opções disponíveis

## 🔄 Reversão
Para desativar:
1. Vá em **Personalizar → Produtos**
2. Desmarque **"Ocultar cores e tamanhos esgotados"**
3. Salve as alterações

## 💡 Dicas Avançadas
- Use em conjunto com notificações de "Voltar ao estoque"
- Combine com badges de "Últimas unidades"
- Monitore o impacto na conversão via Google Analytics
- Considere mostrar quantas opções foram ocultadas

## 📞 Suporte
Para dúvidas ou problemas:
- Verifique este documento primeiro
- Teste com o snippet de debug
- Documente o comportamento observado vs esperado