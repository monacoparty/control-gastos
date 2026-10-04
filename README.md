# Mis Gastos (PWA · GitHub + Vercel + Firestore)

## 1. Firebase
1. console.firebase.google.com → crear proyecto → añadir app **Web** → copiar `firebaseConfig`.
2. Pegarlo en `index.html` (constante `firebaseConfig`).
3. **Authentication → Sign-in method → Google** → activar.
4. **Firestore Database** → crear base de datos (modo producción) → pestaña **Reglas** → pegar `firestore.rules` → Publicar.

## 2. GitHub
```bash
git init && git add . && git commit -m "app gastos"
git branch -M main
git remote add origin https://github.com/TU_USUARIO/control-gastos.git
git push -u origin main
```

## 3. Vercel
vercel.com → Add New Project → importar el repo → Framework "Other" → Deploy (sin build, es estático).

## 4. Dominio autorizado
Firebase → Authentication → Settings → **Authorized domains** → añadir tu `xxx.vercel.app`.

## 5. Móvil
Abre la URL en el móvil → menú del navegador → **Añadir a pantalla de inicio**.

## Notas
- Presupuesto de gastos variables mensual = 4 × (entre semana + fin de semana) = 640 €, como en tu hoja.
- "Fin de semana" = vie, sáb, dom (constante `WEEKEND` en `index.html`).
- Importes y presupuestos se editan en la pestaña Ajustes.
