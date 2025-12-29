<h1>🚀 Cloud-Native CRM SaaS Platform (NestJS + Prisma + PostgreSQL)</h1>

<p>
A <strong>production-ready, cloud-native CRM SaaS backend</strong> built with
<strong>NestJS</strong>, <strong>Prisma v7</strong>, and <strong>PostgreSQL</strong>,
designed using <strong>clean architecture</strong>, <strong>multi-tenant SaaS principles</strong>,
and <strong>enterprise-grade authentication & billing workflows</strong>.
</p>

<p>
This project demonstrates real-world backend engineering skills expected from
<strong>software engineers in New Zealand and global tech companies</strong>.
</p>

<hr />

<h2>✨ Key Features</h2>
<ul>
  <li>🧱 Modular NestJS Architecture</li>
  <li>🏢 Multi-Tenant SaaS Design</li>
  <li>🔐 JWT Authentication with Refresh Tokens</li>
  <li>👤 Role-Based Access Control (Admin / User)</li>
  <li>📦 Prisma ORM (v7) with PostgreSQL</li>
  <li>🧪 Swagger API Documentation</li>
  <li>💳 Stripe Subscription Billing (Test Mode)</li>
  <li>🔄 Database Migrations with Shadow Database</li>
  <li>🌱 Seeded Admin User</li>
  <li>⚙️ Production-Ready Config Structure</li>
</ul>

<hr />

<h2>🛠️ Tech Stack</h2>
<table>
  <thead>
    <tr>
      <th>Layer</th>
      <th>Technology</th>
    </tr>
  </thead>
  <tbody>
    <tr><td>Backend</td><td>NestJS (TypeScript)</td></tr>
    <tr><td>ORM</td><td>Prisma v7</td></tr>
    <tr><td>Database</td><td>PostgreSQL</td></tr>
    <tr><td>Authentication</td><td>JWT + Refresh Tokens</td></tr>
    <tr><td>Payments</td><td>Stripe (Subscriptions)</td></tr>
    <tr><td>Documentation</td><td>Swagger / OpenAPI</td></tr>
    <tr><td>Runtime</td><td>Node.js</td></tr>
    <tr><td>OS</td><td>Linux (Kali / Ubuntu compatible)</td></tr>
  </tbody>
</table>

<hr />

<h2>📁 Project Structure</h2>
<pre>
backend/
├── prisma/
│   ├── schema.prisma
│   └── migrations/
├── src/
│   ├── auth/
│   ├── users/
│   ├── admin/
│   ├── organizations/
│   ├── billing/
│   ├── common/
│   ├── app.module.ts
│   └── main.ts
├── prisma.config.ts
├── .env
├── package.json
└── README.md
</pre>

<hr />

<h2>🔐 Authentication Flow</h2>
<ol>
  <li>User registers or logs in</li>
  <li>Server issues:
    <ul>
      <li>Access Token (short-lived)</li>
      <li>Refresh Token (secure)</li>
    </ul>
  </li>
  <li>Access token expires → refresh token generates a new one</li>
  <li>Role guards protect admin routes</li>
</ol>

<hr />

<h2>💳 Billing (Stripe – Test Mode)</h2>
<ul>
  <li>Subscription-based billing model</li>
  <li>Monthly plans</li>
  <li>Stripe test keys only</li>
  <li>Webhook-ready structure</li>
</ul>

<hr />

<h2>📘 API Documentation (Swagger)</h2>
<p>
After starting the server, access Swagger UI at:
</p>
<pre>
http://localhost:3000/api
</pre>

<hr />

<h2>⚙️ Environment Variables</h2>
<pre>
DATABASE_URL="postgresql://crm_user:password@localhost:5432/crm_db"
SHADOW_DATABASE_URL="postgresql://crm_user:password@localhost:5432/crm_shadow_db"

JWT_SECRET="supersecretjwt"
JWT_REFRESH_SECRET="supersecretrefresh"
JWT_EXPIRES_IN="15m"
JWT_REFRESH_EXPIRES_IN="7d"

STRIPE_SECRET_KEY="sk_test_..."
STRIPE_WEBHOOK_SECRET="whsec_..."
</pre>

<hr />

<h2>🗄️ Database Setup</h2>
<h3>Create Databases</h3>
<pre>
sudo -u postgres createdb crm_db
sudo -u postgres createdb crm_shadow_db
</pre>

<h3>Grant Permissions</h3>
<pre>
ALTER ROLE crm_user CREATEDB;
GRANT ALL PRIVILEGES ON DATABASE crm_db TO crm_user;
GRANT ALL PRIVILEGES ON DATABASE crm_shadow_db TO crm_user;
</pre>

<hr />

<h2>🔄 Run Migrations</h2>
<pre>
npx prisma migrate dev --name init
</pre>

<hr />

<h2>▶️ Run the Application</h2>
<pre>
npm run start:dev
</pre>

<p>
Server runs at:
</p>
<pre>
http://localhost:3000
</pre>

<hr />

<h2>🌱 Seed Admin User</h2>
<pre>
npx prisma db seed
</pre>

<p>
<strong>Development credentials:</strong>
</p>
<pre>
Email: admin@crm.local
Password: Admin@123
Role: ADMIN
</pre>

<hr />

<h2>📈 Why This Project Matters</h2>
<ul>
  <li>Real SaaS backend architecture</li>
  <li>Secure authentication patterns</li>
  <li>Production-grade database migrations</li>
  <li>Stripe subscription billing</li>
  <li>Clean, scalable NestJS codebase</li>
</ul>

<hr />

<h2>📜 License</h2>
<p>MIT License — free to use, modify, and extend.</p>

<hr />

<h2>👨‍💻 Author</h2>
<p>
<strong>Ravindu Prabashwara</strong><br />
Software Engineer<br />
New Zealand 🇳🇿
</p>
