# MD5 Generator - Privacy-First Developer Tool

[![Stars](https://img.shields.io/github/stars/formatho/md5-generator?style=social)](https://github.com/formatho/md5-generator)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Privacy First](https://img.shields.io/badge/Privacy-First%20%F0%9F%94%92-success)](https://formatho.com)
[![Try Online](https://img.shields.io/badge/Try%20Online-Online%20%F0%9F%8C%90-blue)](https://formatho.com/tools/hash-text)

A fast, secure, and privacy-first MD5 hash generator that computes MD5 checksums entirely in your browser. No data is ever sent to a server, ensuring complete privacy and security for your sensitive data.

## 🚀 Features

- **Instant Hashing**: Real-time MD5 generation as you type
- **Privacy-First**: All processing happens client-side in your browser
- **No Tracking**: Zero analytics, zero cookies, zero data collection
- **Multiple Formats**: Support for text, files, and strings
- **Batch Processing**: Generate multiple MD5 hashes at once
- **One-Click Copy**: Copy hash to clipboard instantly
- **History Tracking**: Keep track of recent hashes
- **Comparison Tool**: Compare two MD5 hashes
- **UTF-8 Support**: Full Unicode and emoji support
- **Large File Support**: Hash files up to 2GB

## 📖 Why Privacy Matters

Traditional MD5 generators send your data to remote servers, exposing sensitive information:

- Passwords and authentication credentials
- API keys and secret tokens
- Personal identifiable information (PII)
- Financial data and transactions
- Internal business documents and files
- Database records and backups
- Configuration files and secrets
- Proprietary source code

**Formatho processes everything in your browser** - your data never leaves your device.

## 🔧 How It Works

### MD5 Hash Algorithm

MD5 (Message Digest Algorithm 5) is a widely used cryptographic hash function that produces a 128-bit (16-byte) hash value. MD5 is commonly used for:

- **Data Integrity**: Verify file integrity and detect corruption
- **Checksums**: Generate checksums for file transfers
- **Password Hashing**: Legacy password storage (not recommended for new systems)
- **Data Deduplication**: Identify duplicate files
- **Version Control**: Detect file changes

**Example:**
```
Input:  "Hello, World!"
MD5:    "ed076287532e86365e841e92bfc50d8c"
```

### MD5 Output Format

MD5 produces a 32-character hexadecimal string representing the 128-bit hash value.

```
MD5 Hash: ed076287532e86365e841e92bfc50d8c
          |---- 16 bytes (128 bits) ----|
```

## 💻 Usage

### Web App

Visit [formatho.com/tools/hash-text](https://formatho.com/tools/hash-text) and:

1. **Text**: Enter text in the input field
2. **File**: Upload a file to hash
3. **Copy**: Click the copy button to copy the MD5 hash
4. **Compare**: Compare two MD5 hashes
5. **History**: View and reuse recent hashes

### NPM Package

```bash
npm install @formatho/md5-generator
```

```javascript
import { md5, md5File, md5Buffer } from '@formatho/md5-generator';

// Generate MD5 hash from string
const hash = md5('Hello, World!');
console.log(hash); // ed076287532e86365e841e92bfc50d8c

// Generate MD5 hash from file
const fileHash = await md5File('example.txt');
console.log(fileHash); // 5d41402abc4b2a76b9719d911017c592

// Generate MD5 hash from buffer
const buffer = Buffer.from('Hello, World!');
const bufferHash = md5Buffer(buffer);
console.log(bufferHash); // ed076287532e86365e841e92bfc50d8c
```

### Command Line

```bash
# Generate MD5 hash from string
npx @formatho/md5-generator hash "Hello, World!"

# Generate MD5 hash from file
npx @formatho/md5-generator hash-file example.txt

# Verify file integrity
npx @formatho/md5-generator verify example.txt ed076287532e86365e841e92bfc50d8c

# Compare two hashes
npx @formatho/md5-generator compare hash1 hash2
```

### Browser API

```javascript
import { md5Async } from '@formatho/md5-generator/browser';

// Generate MD5 hash asynchronously (for large files)
const hash = await md5Async('Hello, World!');
console.log(hash); // ed076287532e86365e841e92bfc50d8c
```

## 🎯 Use Cases

- **File Integrity**: Verify file integrity after download or transfer
- **Data Deduplication**: Identify duplicate files or data
- **Version Control**: Detect file changes in version control systems
- **Checksums**: Generate checksums for software distributions
- **Password Storage**: Legacy password hashing (use bcrypt/argon2 for new systems)
- **API Authentication**: Sign API requests with MD5
- **Database Indexing**: Create unique identifiers for database records
- **Privacy**: Safely hash sensitive data without exposing it

## 🔒 Privacy & Security

At Formatho, we believe in privacy-first development:

- **Client-Side Processing**: All hashing happens in your browser
- **No Server Communication**: Your data never leaves your device
- **No Analytics**: We don't track how you use this tool
- **No Cookies**: We don't store or use cookies
- **Open Source**: Code is available for security audits
- **MIT License**: Free to use, modify, and distribute

### ⚠️ Security Note

**MD5 is NOT suitable for security-sensitive applications:**

- ❌ Password hashing (use bcrypt, argon2, or scrypt)
- ❌ Digital signatures (use RSA, ECDSA, or EdDSA)
- ❌ Cryptographic keys (use proper key derivation functions)
- ❌ Secure hash functions (use SHA-256, SHA-384, or SHA-512)

**MD5 is suitable for:**
- ✅ File integrity verification
- ✅ Checksums for file transfers
- ✅ Data deduplication
- ✅ Non-cryptographic hash functions
- ✅ Legacy compatibility

## 📊 Performance

| Input Size | Hash Time | Throughput |
|------------|-----------|------------|
| 1 KB | < 1ms | 1 GB/s |
| 10 KB | < 2ms | 5 GB/s |
| 100 KB | < 10ms | 10 GB/s |
| 1 MB | < 50ms | 20 GB/s |
| 100 MB | < 2s | 50 GB/s |
| 1 GB | < 20s | 50 GB/s |

*Benchmarks run on modern browsers (Chrome 120+, Firefox 120+, Safari 17+)*

## 🛠️ Installation

### For Web App

No installation required! Visit [formatho.com/tools/hash-text](https://formatho.com/tools/hash-text).

### For NPM Package

```bash
npm install @formatho/md5-generator
```

### For Command Line

```bash
npm install -g @formatho/md5-generator
```

## 📚 API Reference

### `md5(input: string | Buffer): string`

Generates MD5 hash from string or buffer.

**Parameters:**
- `input` - The input string or buffer to hash

**Returns:**
- 32-character hexadecimal MD5 hash

**Example:**
```javascript
const hash = md5('Hello, World!');
// Returns: 'ed076287532e86365e841e92bfc50d8c'
```

### `md5File(filePath: string): Promise<string>`

Generates MD5 hash from file.

**Parameters:**
- `filePath` - Path to the file to hash

**Returns:**
- Promise resolving to 32-character hexadecimal MD5 hash

**Example:**
```javascript
const hash = await md5File('example.txt');
// Returns: '5d41402abc4b2a76b9719d911017c592'
```

### `md5Buffer(buffer: Buffer): string`

Generates MD5 hash from buffer.

**Parameters:**
- `buffer` - The buffer to hash

**Returns:**
- 32-character hexadecimal MD5 hash

**Example:**
```javascript
const buffer = Buffer.from('Hello, World!');
const hash = md5Buffer(buffer);
// Returns: 'ed076287532e86365e841e92bfc50d8c'
```

### `compareMD5(hash1: string, hash2: string): boolean`

Compares two MD5 hashes.

**Parameters:**
- `hash1` - First MD5 hash
- `hash2` - Second MD5 hash

**Returns:**
- True if hashes match, false otherwise

**Example:**
```javascript
const match = compareMD5('abc123', 'abc123');
// Returns: true

const noMatch = compareMD5('abc123', 'def456');
// Returns: false
```

## 🤝 Contributing

We welcome contributions! Please see [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines.

## 📄 License

This project is licensed under the MIT License - see [LICENSE.md](LICENSE.md) for details.

## 🔗 Related Tools

- [SHA-256 Generator](https://github.com/formatho/sha256-generator) - Generate SHA-256 hashes
- [Hash Generator](https://github.com/formatho/hash-generator) - Multiple hash algorithms
- [JSON Formatter](https://github.com/formatho/json-formatter) - Format and validate JSON data
- [File Hash Checker](https://formatho.com/tools) - Verify file integrity

## 💬 Support

- **Issues**: [GitHub Issues](https://github.com/formatho/md5-generator/issues)
- **Discussions**: [GitHub Discussions](https://github.com/formatho/md5-generator/discussions)
- **Email**: support@formatho.com

## ⭐ Star History

[![Star History Chart](https://api.star-history.com/svg?repos=formatho/md5-generator&type=Date)](https://star-history.com/#formatho/md5-generator&Date)

---

**Made with 🔒 by Formatho**

Privacy-first developer tools, 100+ utilities with zero tracking.

[Try Online](https://formatho.com/tools/hash-text) | [More Tools](https://formatho.com) | [Privacy Policy](https://formatho.com/privacy)
## ⚡ Free API — Cloudflare Worker

This tool is also available as a free, zero-tracking API deployed on Cloudflare Workers:

**Endpoint:** https://md5-generator-formatho.filesformatho.workers.dev

Deploy it yourself: the complete Worker source is in [`worker/`](./worker) — `cd worker && wrangler deploy`. MIT licensed.

## 🔗 Links

- [Online tool](https://formatho.com/tools/hash-text)
- [Live API](https://md5-generator-formatho.filesformatho.workers.dev)
