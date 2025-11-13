📇 Lista de Contatos — Supabase

Projeto simples utilizando Supabase + HTML + JavaScript para criar uma lista de contatos com nome e e-mail, consumindo um banco de dados Postgres online.

🚀 Tecnologias usadas

Supabase (Postgres + API + RLS)


HTML5


JavaScript

GitHub Pages (deploy)

📌 Funcionalidades

✔ Adicionar contatos (nome e e-mail)

✔ Listar contatos cadastrados

✔ Conexão direta com banco via Supabase

✔ Estrutura mínima para estudo de CRUD

✔ Página leve, simples e totalmente estática

🗄 Estrutura da Tabela no Supabase

create table public.contatos (

  id uuid primary key default gen_random_uuid(),
  
  nome text not null,
  
  email text not null,
  
  created_at timestamp with time zone default now()
  
);

alter table public.contatos enable row level security;

create policy "Allow read for anon"

  on public.contatos for select
  
  using (true);

create policy "Allow insert for anon"

  on public.contatos for insert
  
  with check (true);

🌐 Deploy do Projeto

A página está disponível em:
➡️ https://guiszax.github.io/Lista_Contatos/
