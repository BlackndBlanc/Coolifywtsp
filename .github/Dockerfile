# استخدم صورة Node الرسمية
FROM node:18

# تثبيت المتطلبات الخاصة بـ puppeteer/chromium
RUN apt-get update && apt-get install -y \
    wget \
    ca-certificates \
    fonts-liberation \
    libappindicator3-1 \
    libasound2 \
    libatk-bridge2.0-0 \
    libatk1.0-0 \
    libcups2 \
    libdbus-1-3 \
    libgdk-pixbuf2.0-0 \
    libnspr4 \
    libnss3 \
    libx11-xcb1 \
    libxcomposite1 \
    libxdamage1 \
    libxrandr2 \
    xdg-utils \
    --no-install-recommends && \
    rm -rf /var/lib/apt/lists/*

# مجلد العمل داخل الحاوية
WORKDIR /app

# نسخ كل الملفات
COPY . .

# تثبيت الحزم
RUN npm install

# بدء التطبيق
CMD ["node", "server.js"]
