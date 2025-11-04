# Contributing to Quest Crossfire Chatbot

Thank you for your interest in contributing to the Multi-Persona Chatbot!

## 🎯 Project Overview

This is a Streamlit-based multi-persona chatbot developed as part of the OutSkill AI Engineering Bootcamp 2025. It demonstrates AI integration, session management, and file export capabilities.

## 🚀 Quick Start

### Prerequisites
- Python 3.8+
- OpenAI API key
- Git
- Basic understanding of Streamlit and OpenAI API

### Development Setup

1. **Clone the repository**
   ```bash
   git clone https://github.com/AsheeshSrivastava/quest-crossfire-chatbot.git
   cd quest-crossfire-chatbot
   ```

2. **Create virtual environment**
   ```bash
   python -m venv venv
   source venv/bin/activate  # Windows: venv\Scripts\activate
   ```

3. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

4. **Configure API key**
   ```bash
   mkdir .streamlit
   # Create .streamlit/secrets.toml with your OpenAI API key
   echo 'OPENAI_API_KEY = "sk-your_key_here"' > .streamlit/secrets.toml
   ```

5. **Run the application**
   ```bash
   streamlit run app.py
   ```

## 📐 Code Standards

### Python Style
- Follow PEP 8 guidelines
- Use type hints where appropriate
- Maximum line length: 100 characters
- Use docstrings for functions and classes

Example:
```python
def export_chat_to_txt(chat_data: dict) -> str:
    """Export chat history to plain text format.

    Args:
        chat_data: Dictionary containing chat messages and metadata

    Returns:
        Formatted string suitable for TXT export
    """
    pass
```

### Streamlit Conventions
- Use `st.session_state` for persistent data
- Implement proper error handling with try/except
- Use `st.error()`, `st.warning()`, `st.success()` for user feedback
- Test streaming responses thoroughly

### File Organization
```
quest-crossfire-chatbot/
├── app.py                  # Main application logic
├── requirements.txt        # Python dependencies
├── .streamlit/            # Streamlit configuration
│   └── secrets.toml       # API keys (gitignored)
├── chat_history/          # Saved chats (gitignored)
└── session_logs/          # Development documentation
```

## 🔧 Pull Request Process

1. **Create feature branch**
   ```bash
   git checkout -b feature/your-feature-name
   ```

2. **Make changes**
   - Write clean, documented code
   - Test thoroughly with multiple personas
   - Verify export functionality works

3. **Test locally**
   ```bash
   streamlit run app.py

   # Test checklist:
   # - Create new chat
   # - Switch personas
   # - Send messages
   # - Export to all formats (TXT, JSON, CSV)
   # - Load saved chat
   # - Delete chat
   ```

4. **Commit changes**
   ```bash
   git add .
   git commit -m "feat: brief description of changes"
   ```

   **Commit message format:**
   - `feat:` - New feature
   - `fix:` - Bug fix
   - `docs:` - Documentation only
   - `style:` - Formatting changes
   - `refactor:` - Code refactoring
   - `test:` - Adding tests
   - `chore:` - Maintenance

5. **Push and create PR**
   ```bash
   git push origin feature/your-feature-name
   ```

   **In your Pull Request:**
   - Clear title describing change
   - Screenshots of new features (if UI changes)
   - Test results
   - Explanation of why the change is needed

## 🐛 Bug Reports

Include:
- Steps to reproduce the bug
- Expected vs actual behavior
- Screenshots or error messages
- Python version
- Streamlit version
- Operating system

**Example Bug Report:**
```markdown
**Bug:** Chat export fails with special characters

**Steps to reproduce:**
1. Create a new chat
2. Send message with emoji: "Hello 👋"
3. Click "Export as TXT"
4. Error appears: "UnicodeEncodeError"

**Expected:** Export succeeds with emoji preserved
**Actual:** Export fails with encoding error

**Environment:**
- Python: 3.9.7
- Streamlit: 1.28.0
- OS: Windows 11
```

## 💡 Feature Requests

For new features, please:
1. Check if it already exists in "Future Enhancements" (README.md)
2. Explain the use case (who benefits and how)
3. Provide implementation ideas if possible
4. Consider impact on existing functionality

**Good Feature Request Example:**
```markdown
**Feature:** Conversation search functionality

**Use case:**
Users with many saved chats need to find specific conversations quickly.

**Proposal:**
- Add search bar in sidebar
- Search through chat titles and message content
- Show matching chats with highlighted keywords
- Filter by persona type

**Implementation idea:**
- Use Python's `re` module for keyword matching
- Update sidebar to show only matching chats
- Add "Clear search" button
```

## 🧪 Testing

### Manual Testing Checklist

Before submitting PR:
- [ ] Create new chat works
- [ ] All 4 personas respond correctly
- [ ] Persona switching works mid-conversation
- [ ] Chat auto-saves after each message
- [ ] Loading saved chats works
- [ ] Deleting chats works
- [ ] Export to TXT works
- [ ] Export to JSON works
- [ ] Export to CSV works
- [ ] No errors in console
- [ ] UI looks good on different screen sizes

### Persona Testing

Test each persona separately:
- [ ] **General Assistant**: Helpful and informative tone
- [ ] **Creative Poet**: Uses metaphors and artistic language
- [ ] **Technical Coder**: Precise, code-focused responses
- [ ] **Sarcastic Robot**: Humorous but correct answers

## 🎨 UI/UX Guidelines

### Streamlit Best Practices
- Use emojis consistently (🤖, 💬, 📤, etc.)
- Provide clear user feedback for actions
- Show loading states for API calls
- Use columns for better layout
- Implement error handling gracefully

### Design Principles
- Keep it simple and intuitive
- Minimize clicks for common actions
- Provide clear labels and instructions
- Use consistent spacing and formatting

## 🔐 Security

### API Key Management
- ⚠️ **NEVER commit API keys** to Git
- Use `.streamlit/secrets.toml` (gitignored)
- Verify `.gitignore` includes secrets file
- Test with invalid API keys to ensure proper error handling

### Data Privacy
- Chat history stored locally (not sent to external servers except OpenAI)
- No user tracking or analytics
- Export functionality should not expose sensitive data

## 📚 Documentation

When adding features:
- Update README.md if user-facing
- Add docstrings to new functions
- Include usage examples
- Update "Features" section if applicable

## 🏷️ Trademark Notice

**QUEST AND CROSSFIRE™** is a trademark (Filed - awaiting certification).

When contributing:
- ✅ You may contribute code improvements
- ✅ You may fork and modify (with attribution)
- ❌ You may NOT claim ownership of QUEST AND CROSSFIRE™ trademark
- ❌ You may NOT use the trademark for your own projects without permission

## 📄 License

By contributing, you agree that your contributions will be licensed under **AGPL-3.0**.

This means:
- Your code remains open source
- Derivative works must also be AGPL-3.0
- Network use triggers source disclosure requirement
- Commercial use is allowed (with license compliance)

## ❓ Questions & Support

- **Issues:** [GitHub Issues](https://github.com/AsheeshSrivastava/quest-crossfire-chatbot/issues)
- **Email:** asheeshsrivastava9@gmail.com
- **Documentation:** Check README.md and code comments

## 🙏 Acknowledgments

Contributions welcome from:
- **Developers** - Code improvements, bug fixes
- **Designers** - UI/UX enhancements
- **Writers** - Documentation improvements
- **Testers** - Bug reports, feature suggestions

---

**Built with Streamlit and OpenAI**

**Part of OutSkill AI Engineering Bootcamp 2025**

**© 2025 QUEST AND CROSSFIRE™. Licensed under AGPL-3.0.**
