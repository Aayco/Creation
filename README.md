# ID Creation Date Estimator

This is an experimental tool to **estimate the creation date of Telegram user IDs** using a linear approximation model. The project is based on the idea that most newer Telegram user IDs are timestamp-based, and with enough known ID–date pairs, we can approximate other users' creation dates.

> ⚠️ This is still a **work in progress**, and the estimation may not always be 100% accurate. However, it generally provides a **very close** approximation for most IDs — especially newer ones.

---

## 🔍 How It Works

- The tool uses **math and a linear equation** to estimate the creation date from the Telegram user ID.
- A cached set of ID–date pairs (provided manually or through DMs) helps build the model.
- Older IDs (e.g., short ones like `25`) are not timestamp-based, so they might return inaccurate results.
- As more accurate ID–date pairs are collected, the model improves.

---

## 🧠 Why?

Many people have asked about the creation date of their Telegram ID. While Telegram does not provide this information directly, **IDs based on timestamps can be reverse-engineered** to estimate their creation time. This script is a small step toward that.

---

## 🧪 Try It Out

### Python Example

```python
from create import creation

date = creation(id)
await event.reply(date)
```

### JavaScript Example

```javascript
import { creation } from './create.js';

const userId = 6101607245;
console.log(creation(userId));
```

```warn⚠️
**These scripts are based on early versions and may give results that differ from the official bot. They need updating.**
```

---

## 🚧 Disclaimer
**This is a test tool for educational and experimental purposes. It's not guaranteed to be accurate, especially for very old Telegram IDs. Consider it as a "math experiment" — sometimes sick, sometimes smart.**
