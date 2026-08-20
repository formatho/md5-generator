# Contributing to Formatho Tools

Thank you for your interest in contributing to Formatho's privacy-first developer tools! We welcome contributions from developers of all skill levels.

## About Formatho

Formatho provides privacy-first developer tools that process all data client-side in your browser. No tracking, no analytics, no data collection. All tools are open source and completely free to use.

## Our Principles

- **Privacy First**: All data processing happens client-side
- **Zero Tracking**: No analytics, no user tracking
- **Open Source**: All code is transparent and auditable
- **User-Focused**: Tools built for developers, by developers
- **Accessibility**: Tools should be usable by everyone

## How to Contribute

### Reporting Bugs

Before creating bug reports, please check existing issues to avoid duplicates.

When creating a bug report, include:
- **Title**: Clear and descriptive
- **Description**: Detailed explanation of the bug
- **Steps to Reproduce**: Step-by-step instructions
- **Expected Behavior**: What should happen
- **Actual Behavior**: What actually happens
- **Screenshots**: If applicable
- **Environment**: Browser, OS, device info

### Suggesting Features

Feature suggestions are welcome! When suggesting a feature:
- **Title**: Clear and concise
- **Problem**: What problem does this solve?
- **Solution**: How should it work?
- **Alternatives**: What alternatives have you considered?
- **Additional Context**: Any other relevant information

### Pull Requests

We accept pull requests for:
- Bug fixes
- New features
- Performance improvements
- Documentation updates
- Accessibility improvements

#### Pull Request Process

1. **Fork the repository**
2. **Create a branch**: `git checkout -b feature/your-feature-name`
3. **Make your changes**: Follow our coding standards
4. **Test thoroughly**: Ensure all existing tests pass
5. **Commit**: Use clear, descriptive commit messages
6. **Push**: `git push origin feature/your-feature-name`
7. **Create PR**: Describe your changes and link to related issues

#### PR Checklist

- [ ] Code follows our style guidelines
- [ ] Tests pass locally
- [ ] Documentation updated (if needed)
- [ ] PR description is clear and descriptive
- [ ] Linked to related issues
- [ ] No personal data or tracking added
- [ ] Privacy-first architecture maintained

## Coding Standards

### Privacy-First Development

**CRITICAL**: All Formatho tools must maintain privacy-first architecture:

- ✅ **Client-side processing only**: No data sent to servers
- ✅ **No analytics**: No Google Analytics or tracking scripts
- ✅ **No data collection**: No local storage of user data (except preferences)
- ✅ **No external requests**: No API calls to third-party services
- ✅ **Open source**: All code must be transparent and auditable

### Code Style

- Use descriptive variable and function names
- Add comments for complex logic
- Follow existing code formatting
- Keep functions small and focused
- Avoid code duplication

### Testing

- Write tests for new features
- Test on multiple browsers (Chrome, Firefox, Safari, Edge)
- Test on mobile devices
- Test accessibility (screen readers, keyboard navigation)
- Test privacy features (no network requests)

### Documentation

- Update README.md for user-facing changes
- Add inline code comments for complex logic
- Update CHANGELOG.md for version changes
- Create or update API documentation

## Development Setup

### Prerequisites

- Node.js 18+ (for tools with NPM packages)
- Git
- Modern web browser

### Local Development

1. **Clone the repository**
```bash
git clone https://github.com/formatho/repository-name.git
cd repository-name
```

2. **Install dependencies** (if applicable)
```bash
npm install
```

3. **Start development server** (if applicable)
```bash
npm run dev
```

4. **Run tests** (if applicable)
```bash
npm test
```

## Accessibility

Formatho tools must be accessible to all users:

- **Keyboard Navigation**: All features accessible via keyboard
- **Screen Readers**: Proper ARIA labels and semantic HTML
- **Color Contrast**: WCAG AA compliant (4.5:1 minimum)
- **Focus Indicators**: Visible focus states for all interactive elements
- **Error Messages**: Clear, descriptive error messages
- **Forms**: Proper labels and error handling

## Performance

Tools should be fast and efficient:

- **Load Time**: < 2 seconds initial load
- **Runtime**: Instant feedback for user actions
- **File Size**: Minimize JavaScript bundle size
- **Optimization**: Lazy loading, code splitting where appropriate

## Security

- **No eval()**: Never use eval() or similar functions
- **Input Sanitization**: Sanitize all user inputs
- **XSS Prevention**: Proper escaping and sanitization
- **HTTPS**: Deploy with HTTPS (when applicable)
- **Dependencies**: Keep dependencies updated

## Communication

- **GitHub Issues**: For bug reports and feature requests
- **Discord**: For community discussions
- **Email**: For security issues (security@formatho.com)

## License

By contributing, you agree that your contributions will be licensed under the MIT License.

## Recognition

Contributors are recognized in:
- README.md (Contributors section)
- CHANGELOG.md (for each release)
- GitHub's contributors list

## Questions?

- 📧 Email: support@formatho.com
- 💬 Discord: [Formatho Discord](https://discord.gg/formatho)
- 🐛 GitHub Issues: [Report an issue](https://github.com/formatho/repository-name/issues)

---

**Thank you for contributing to Formatho! 🎉**

**Made with 🔒 by Formatho - Privacy-first developer tools, 100+ utilities with zero tracking.**