# 📍 ONDE ENCONTRAR A CONFIGURAÇÃO

## 🎯 LOCALIZAÇÃO EXATA

### Passo a Passo:
1. **Admin Shopify** → **Temas**
2. **Personalizar** (no tema ativo)
3. **Configurações do tema** (ícone de engrenagem no canto inferior esquerdo)
4. **Produtos** (na lista de configurações)
5. Procure por: **"🔥 Ocultar cores e tamanhos esgotados"**

### 📱 Localização Visual:
```
Personalizar
├── Seções (páginas)
└── Configurações do tema ← CLIQUE AQUI
    ├── Cores
    ├── Layout
    ├── Produtos ← CLIQUE AQUI
    │   ├── Frete Grátis Personalizado
    │   ├── Estrelas  
    │   ├── Imagem Natalina
    │   ├── Outros
    │   │   ├── Mostrar vendedor
    │   │   ├── Mostrar imagem secundária
    │   │   ├── Mostrar desconto
    │   │   ├── Mostrar amostra de cores
    │   │   ├── Mostrar inventário
    │   │   ├── 🔥 Ocultar cores e tamanhos esgotados ← AQUI!
    │   │   ├── Limite de estoque baixo
    │   │   └── Mostrar selo de comentários
    ├── Bloqueadores
    ├── Parcelamentos
    └── ...
```

## 🔍 SE NÃO APARECER:

### Solução 1: Recarregar
1. **Feche** o painel de personalização
2. **Reabra**: Admin → Temas → Personalizar
3. **Vá novamente** em Configurações → Produtos

### Solução 2: Limpar Cache
1. **Ctrl + F5** (Windows) ou **Cmd + Shift + R** (Mac)
2. **Reabra** o painel de personalização

### Solução 3: Verificar se Salvou
1. **Verifique** se você salvou as alterações no código
2. **Aguarde** 1-2 minutos para o Shopify processar
3. **Reabra** o painel

## 🧪 TESTE SE ESTÁ FUNCIONANDO

### Método 1: Visual
Adicione temporariamente ao template do produto:
```liquid
{% render 'test-config-visibility' %}
```

### Método 2: Comportamento
1. **Ative** a configuração
2. **Vá** a um produto com variantes esgotadas
3. **Verifique** se as cores/tamanhos esgotados sumiram

## 🎨 COMO DEVE APARECER:
- **Título**: 🔥 Ocultar cores e tamanhos esgotados
- **Tipo**: Checkbox (caixinha para marcar)
- **Descrição**: "NOVA FUNCIONALIDADE: Quando ativado, cores e tamanhos sem estoque não aparecerão nas opções do produto"
- **Posição**: Logo após "Mostrar inventário"

## ⚠️ PROBLEMAS COMUNS:

### "Não vejo a opção"
- **Causa**: Cache do navegador ou Shopify não atualizou
- **Solução**: Recarregue a página (Ctrl+F5) e reabra o painel

### "A opção aparece mas não funciona"
- **Causa**: Todas as variantes estão esgotadas
- **Solução**: Adicione estoque a pelo menos uma variante

### "Funciona mas oculta tudo"
- **Causa**: Produto sem variantes disponíveis
- **Solução**: Já corrigi o código para evitar isso

## 📞 PRÓXIMO PASSO:
1. **Siga** o passo a passo acima
2. **Procure** pela opção com 🔥 no nome
3. **Teste** ativando/desativando
4. **Me informe** se encontrou!