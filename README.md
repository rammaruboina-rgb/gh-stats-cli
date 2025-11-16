# 🦀 gh-stats-cli

![Rust](https://img.shields.io/badge/rust-%23000000.svg?style=for-the-badge&logo=rust&logoColor=white)
![GitHub API](https://img.shields.io/badge/GitHub_API-181717?style=for-the-badge&logo=github&logoColor=white)
![License](https://img.shields.io/badge/License-MIT-yellow.svg?style=for-the-badge)

A blazing-fast Rust CLI tool to fetch, analyze, and visualize GitHub profile statistics, contributions, and repository insights using async/await patterns and the GitHub REST API.

## ✨ Features

- 📊 **Profile Analytics**: View detailed GitHub profile statistics
- 🔥 **Contribution Heatmap**: Visualize contribution patterns
- 📦 **Repository Insights**: Analyze languages, stars, forks, and more
- ⚡ **Async Performance**: Built with Tokio for lightning-fast API calls
- 🎨 **Beautiful CLI**: Colorful terminal output using `colored` crate
- 🔒 **Secure**: Token-based authentication with GitHub Personal Access Tokens

## 🚀 Installation

### From Source

```bash
# Clone the repository
git clone https://github.com/rammaruboina-rgb/gh-stats-cli.git
cd gh-stats-cli

# Build and install
cargo install --path .
```

### From Cargo (Coming Soon)

```bash
cargo install gh-stats-cli
```

## 📖 Usage

### Basic Commands

```bash
# View your own profile stats
gh-stats-cli profile --user rammaruboina-rgb

# Analyze a specific repository
gh-stats-cli repo --owner rust-lang --name rust

# View contribution stats for the year
gh-stats-cli contributions --user rammaruboina-rgb --year 2025

# Export stats to JSON
gh-stats-cli profile --user rammaruboina-rgb --format json > stats.json
```

### Authentication

Set your GitHub Personal Access Token:

```bash
export GITHUB_TOKEN=your_token_here
```

Or pass it directly:

```bash
gh-stats-cli profile --user rammaruboina-rgb --token your_token_here
```

## 🛠️ Tech Stack

- **Language**: Rust 2021 Edition
- **Async Runtime**: [tokio](https://tokio.rs/)
- **HTTP Client**: [reqwest](https://docs.rs/reqwest/)
- **CLI Framework**: [clap](https://docs.rs/clap/)
- **JSON Parsing**: [serde](https://serde.rs/) & [serde_json](https://docs.rs/serde_json/)
- **Terminal Colors**: [colored](https://docs.rs/colored/)
- **Error Handling**: [anyhow](https://docs.rs/anyhow/)

## 📦 Project Structure

```
gh-stats-cli/
├── src/
│   ├── main.rs           # Entry point
│   ├── cli.rs            # CLI argument parsing
│   ├── api/
│   │   ├── mod.rs        # API module
│   │   ├── client.rs     # GitHub API client
│   │   └── models.rs     # Data models
│   ├── commands/
│   │   ├── mod.rs
│   │   ├── profile.rs    # Profile command
│   │   ├── repo.rs       # Repository command
│   │   └── contributions.rs
│   └── utils/
│       ├── mod.rs
│       └── formatter.rs  # Output formatting
├── tests/
│   └── integration_tests.rs
├── Cargo.toml
├── Cargo.lock
├── .gitignore
├── LICENSE
└── README.md
```

## 🧪 Testing

```bash
# Run all tests
cargo test

# Run with output
cargo test -- --nocapture

# Run specific test
cargo test test_profile_fetch
```

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📝 Roadmap

- [ ] Basic profile statistics
- [ ] Repository analysis
- [ ] Contribution visualization
- [ ] Export to multiple formats (JSON, CSV, Markdown)
- [ ] GitHub Actions integration
- [ ] Caching for improved performance
- [ ] Compare multiple profiles
- [ ] Star history visualization

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- Built with ❤️ using Rust
- Powered by [GitHub REST API](https://docs.github.com/en/rest)
- Inspired by the Rust community

## 👤 Author

**Rama Krishnnudu**
- GitHub: [@rammaruboina-rgb](https://github.com/rammaruboina-rgb)
- LinkedIn: [ram-maruboina](https://linkedin.com/in/ram-maruboina-932597235)

---

⭐ Star this repository if you find it helpful!
