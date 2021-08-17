# Pushover Client

A simple lightweight client for Pushover notifications.

# Installation

```bash
npm install @hyperlink/pushover
```

# Usage

```typescript
import { Pushover } from '@hyperlink/pushover';

async function sendMessage() {
  const pushover = new Pushover('<YOUR TOKEN>', '<USER TOKEN>');
  await pushover.sendMessage({
    message: 'Test message',
    title: 'Test title',
  });
}

sendMessage();
```

### Message Format

```typeScript
interface PushoverMessage {
    message: string;
    title?: string;
    sound?: string;
    device?: string;
    priority?: number;
    url?: string;
    url_title?: string;
    attachment?: string; // path to the file
    timestamp?: string;
}
```
