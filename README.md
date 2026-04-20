# 🐾 Pet Shop Dev - Landing Page

Bem-vindo ao repositório da Landing Page do **Pet Shop Dev**! Este projeto foi desenvolvido com **Next.js**, **React**, **Tailwind CSS** e utiliza **AOS (Animate On Scroll)** para animações.

## 🚀 Tecnologias Utilizadas

- **Next.js** - Framework React para aplicações modernas
- **React** - Biblioteca para construção de interfaces
- **Tailwind CSS** - Framework de estilização
- **AOS (Animate On Scroll)** - Biblioteca de animação
- **Lucide-react** e **Phosphor Icons** - Ícones personalizados
- **Next/Image** - Otimização de imagens

## 📂 Estrutura do Projeto

```
📁 src/
 ├── _components/      # Componentes reutilizáveis
 │   ├── hero.tsx      # Seção Hero
 │   ├── about.tsx     # Seção Sobre
 │   ├── services.tsx  # Seção Serviços
 │   ├── testimonials.tsx # Seção Depoimentos
 │   ├── footer.tsx    # Rodapé
 │   ├── aos-init.tsx  # Inicialização de animações
 │
 ├── page.tsx          # Página principal
 ├── layout.tsx        # Layout base da aplicação
 ├── globals.css       # Estilização global
```

## 📌 Passo a Passo do Código

### 1️⃣ **Estrutura Base da Página**

O arquivo **`page.tsx`** monta a página principal, importando e organizando os componentes principais.

```tsx
export default function Home() {
  return (
    <main>
      <Hero />
      <About />
      <Services />
      <Testimonials />
      <Footer />
    </main>
  );
}
```

### 2️⃣ **Configuração do Layout**

No **`layout.tsx`**, configuramos a estrutura base da aplicação, incluindo metadados e fontes personalizadas:

```tsx
export default function RootLayout({
  children,
}: {
  children: React.ReactNode;
}) {
  return (
    <html lang="en">
      <body className="antialiased">
        {children}
        <AosInit />
      </body>
    </html>
  );
}
```

### 3️⃣ **Seção "Sobre"**

No **`about.tsx`**, utilizamos **Next/Image** para otimização de imagens e **Lucide-react** para ícones personalizados.

```tsx
<ul className="space-y-4">
  <li className="flex items-center gap-2">
    <Check className="text-red-500" />
    Aberto desde 2006.
  </li>
</ul>
```

### 4️⃣ **Animações com AOS**

O **`aos-init.tsx`** inicializa o **AOS** para aplicar animações de rolagem:

```tsx
useEffect(() => {
  Aos.init({ duration: 800, once: true });
}, []);
```

### 5️⃣ **Rodapé com Marcas**

O **`footer.tsx`** exibe marcas de produtos e links sociais com **Phosphor Icons**.

```tsx
<div className="flex gap-4">
  <FacebookLogo className="w-8 h-8" />
  <InstagramLogo className="w-8 h-8" />
  <YoutubeLogo className="w-8 h-8" />
</div>
```

Feito com ❤️ para o seu pet! 🐶🐱
