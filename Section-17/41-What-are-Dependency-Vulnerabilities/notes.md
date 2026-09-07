# 🔐 What are Dependency Vulnerabilities?

### 📌 What is a Dependency Vulnerability?

A **dependency vulnerability** is a security weakness in a third-party package/library that your application uses.

For example:

```text
Your App
   ↓
Express
   ↓
Some vulnerable dependency
   ↓
Security vulnerability ⚠️
```

Even if your own code is secure, a vulnerable dependency can make your application vulnerable.

### 🔹 Example

Suppose your project uses:

```bash
npm install some-package
```

That package may internally depend on another package containing a known security vulnerability.

This creates a **transitive dependency vulnerability**.

### 🔹 Common Risks

Vulnerable dependencies can lead to:

- **XSS**
- **Prototype pollution**
- **Remote Code Execution (RCE)**
- **Denial of Service (DoS)**
- **Data leakage**
- Authentication/security bypasses

### 🔍 How to Check

For Node.js projects:

```bash
npm audit
```

To automatically fix compatible dependency updates:

```bash
npm audit fix
```

### 🛡️ Prevention

- Keep dependencies updated.
- Regularly run `npm audit`.
- Remove unused packages.
- Review security advisories.
- Use trusted and maintained packages.
- Lock dependency versions with `package-lock.json`.

### 🧠 Remember

> **Dependency vulnerability = Security weakness in a package your application depends on.**

### 🎤 Interview Point

> **A dependency vulnerability occurs when a third-party library used by an application contains a known security weakness that can potentially be exploited.**
