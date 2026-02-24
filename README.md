
https://github.com/user-attachments/assets/c68db4b1-d187-4d0a-abdf-129da1147918
aiesec-onboarding/
 ├─ pages/
 │   ├─ index.js
 │   ├─ parte1.js
 │   ├─ parte2.js
 │   ├─ parte3.js
 │   └─ prova.js
 ├─ lib/
 │   └─ progresso.js
 ├─ styles/
 │   └─ globals.css
 └─ package.json
 export function getProgresso() {
  if (typeof window === "undefined") return 0;
  return Number(localStorage.getItem("progresso")) || 0;
}

export function setProgresso(valor) {
  localStorage.setItem("progresso", valor);
}import Link from "next/link";
import { getProgresso } from "../lib/progresso";
import { useEffect, useState } from "react";

export default function Home() {
  const [progresso, setProgressoState] = useState(0);

  useEffect(() => {
    setProgressoState(getProgresso());
  }, []);

  return (
    <div className="container">
      <h1>AIESEC Onboarding Journey</h1>
      <p>Progresso: {progresso}%</p>

      <Link href="/parte1">
        <button>Começar</button>
      </Link>
    </div>
  );
}import { setProgresso } from "../lib/progresso";
import Link from "next/link";

export default function Parte1() {
  return (
    <div className="container">
      <h2>Parte 1</h2>
      <p>Edite aqui o conteúdo da Parte 1.</p>

      <button onClick={() => setProgresso(33)}>
        Concluir módulo
      </button>

      <Link href="/parte2">
        <button>Ir para Parte 2</button>
      </Link>
    </div>
  );
}import { setProgresso } from "../lib/progresso";
import Link from "next/link";

export default function Parte1() {
  return (
    <div className="container">
      <h2>Parte 1</h2>
      <p>Edite aqui o conteúdo da Parte 1.</p>

      <button onClick={() => setProgresso(33)}>
        Concluir módulo
      </button>

      <Link href="/parte2">
        <button>Ir para Parte 2</button>
      </Link>
    </div>
  );
}import { setProgresso } from "../lib/progresso";
import Link from "next/link";

export default function Parte1() {
  return (
    <div className="container">
      <h2>Parte 1</h2>
      <p>Edite aqui o conteúdo da Parte 1.</p>

      <button onClick={() => setProgresso(33)}>
        Concluir módulo
      </button>

      <Link href="/parte2">
        <button>Ir para Parte 2</button>
      </Link>
    </div>
  );
}import { setProgresso } from "../lib/progresso";
import Link from "next/link";

export default function Parte1() {
  return (
    <div className="container">
      <h2>Parte 1</h2>
      <p>Edite aqui o conteúdo da Parte 1.</p>

      <button onClick={() => setProgresso(33)}>
        Concluir módulo
      </button>

      <Link href="/parte2">
        <button>Ir para Parte 2</button>
      </Link>
    </div>
  );
}body {
  font-family: Arial, sans-serif;
  background: #f4f4f4;
}

.container {
  max-width: 600px;
  margin: auto;
  padding: 40px;
  background: white;
  margin-top: 50px;
  border-radius: 10px;
}

button {
  display: block;
  margin-top: 15px;
  padding: 10px;
  border-radius: 8px;
  border: none;
  background: orange;
  color: white;
  cursor: pointer;
}        
