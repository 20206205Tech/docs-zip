# Tài liệu hướng dẫn cài đặt dự án

## Cấu hình các biến bí mật trong Doppler

Trong Doppler 4 dự án `infra, kong-api-gateway,  supabase,  20206205tech` để chia nhỏ theo từng mục đích khác nhau

### Cấu hình về infra

Trong dự án infra sử dụng cấu hình:

<!-- - AIVEN_TOKEN=example
- CLOUDFLARE_ACCOUNT_ID=example
- CLOUDFLARE_API_TOKEN=example
- DIGITALOCEAN_TOKEN=example
- GOOGLE_CLIENT_ID=example
- GOOGLE_CLIENT_SECRET=example
- HEROKU_API_KEY=example
- LANGSMITH_API_KEY=example
- NEON_API_KEY=example
- OCI_FINGERPRINT=example
- OCI_PRIVATE_KEY=example
- OCI_SSH_PUBLIC_KEY=example
- OCI_USER_OCID=example
- SMTP_PASSWORD=example
- SMTP_USERNAME=example
- SUPABASE_ACCESS_TOKEN=example
- SUPABASE_DB_PASSWORD=example
- TF_API_TOKEN=example
- UPSTASH_API_KEY=example -->

Trong repo github `infra-by-terraform`, GitHub Actions chạy terraform tạo các hạ tầng cần thiết của dự án.

### Cấu hình về kong-api-gateway

Trong dự án `kong-api-gateway` sử dụng cấu hình:

<!-- - KONG_DATABASE=example
- KONG_PG_DATABASE=example
- KONG_PG_HOST=example
- KONG_PG_PASSWORD=example
- KONG_PG_PORT=example
- KONG_PG_SSL=example
- KONG_PG_SSL_VERIFY=example
- KONG_PG_USER=example -->

Vì Render bản miễn phí không hỗ trợ terraform nên sẽ thực hiện triển khai thủ công Kong API Gateway trên giao diện Web.

### Cấu hình về http-log

Trong Doppler tạo dự án `kong-api-gateway` với cấu hình http-log:

<!-- - API_GATEWAY_HTTP_LOG_BEARER=example
- API_GATEWAY_HTTP_LOG_DATABASE_URL=example
- CLOUDFLARE_API_TOKEN=example
- CLOUDFLARE_ZONE_ID=example
- CODECOV_TOKEN=example
- VERCEL_CNAME=example
- VERCEL_TOKEN=example -->

Trong repo github `api-gateway-http-log`, GitHub Actions sẽ tự động chạy kiểm thử đẩy kết quả lên CodeCov, cấu hình dự án api-gateway-http-log trong Vercel và cấu hình domain trong Cloudflare.

### Cấu hình về 20206205tech

Trong dự án 20206205tech sử dụng cấu hình:

<!-- - BREVO_API_KEY=example
- CLOUDFLARE_ACCOUNT_ID=example
- CLOUDFLARE_API_TOKEN=example
- CLOUDFLARE_ZONE_ID=example
- CODECOV_TOKEN=example
- DATA_PIPELINE_PHAP_DIEN_DATABASE_URL=exampletech/neondb?sslmode=example
- DATA_PIPELINE_USER_DOCUMENTS_DATABASE_URL=exampleneon.tech/neondb?sslmode=example
- DATA_PIPELINE_VBPLNEW_DATABASE_URL=exampleondigitalocean.com:25060/defaultdb?sslmode=example
- DATA_PIPELINE_VBPL_DATABASE_URL=exampleneondb?sslmode=example
- DEEPGRAM_API_KEY=example
- DOCKERHUB_TOKEN=example
- DOCKERHUB_USERNAME=example
- DOCKER_REGISTRY_CONFIG=example
- ELEVENLABS_API_KEY=example
- ENVIRONMENT=example
- GEMINI_API_KEY=example
- GOOGLE_DRIVE_FOLDER_ID_DATA_PIPELINE_PHAP_DIEN=example
- GOOGLE_DRIVE_FOLDER_ID_DATA_PIPELINE_VBPL=example
- GOOGLE_DRIVE_FOLDER_ID_DATA_PIPELINE_VBPLNEW=example
- GOOGLE_DRIVE_TOKEN=example
- GROQ_API_KEY=example
- HF_TOKEN=example
- HONEYCOMB_API_KEY=example
- JINA_API_KEY=example
- KAFKA_BROKER=example
- KAFKA_PASSWORD=example
- KAFKA_SSL_CA=example
- KAFKA_SSL_CERT=example
- KAFKA_SSL_KEY=example
- KAFKA_USERNAME=example
- LANGFUSE_BASE_URL=example
- LANGFUSE_PUBLIC_KEY=example
- LANGFUSE_SECRET_KEY=example
- LANGSMITH_API_KEY=example
- LIVEKIT_API_KEY=example
- LIVEKIT_API_SECRET=example
- LIVEKIT_URL=example
- MICROSERVICE_CHATBOT_SERVICE_DATABASE_URL=example
- MICROSERVICE_CHAT_HISTORY_DATABASE_URL=example
- MICROSERVICE_CONVERSATION_SERVICE_DATABASE_URL=example
- MICROSERVICE_DOCUMENT_SERVICE_DATABASE_URL=example
- MICROSERVICE_PAYMENT_SERVICE_DATABASE_URL=example
- MICROSERVICE_PERSONA_SERVICE_DATABASE_URL=example
- MILVUS_TOKEN=example
- MILVUS_URI=example
- NAME_TEST=example
- NPM_TOKEN=example
- NVIDIA_API_KEY=example
- OLLAMA_API_KEY=example
- OPENROUTER_API_KEY=example
- PAT=example
- PAYMENT_DEFAULT_PROVIDER=example
- PAYMENT_MOMO_ACCESS_KEY=example
- PAYMENT_MOMO_ENDPOINT=example
- PAYMENT_MOMO_PARTNER_CODE=example
- PAYMENT_MOMO_SECRET_KEY=example
- PAYMENT_SEPAY_MERCHANT_ID=example
- PAYMENT_SEPAY_SECRET_KEY=example
- PAYMENT_VNPAY_API_URL=example
- PAYMENT_VNPAY_HASH_SECRET_KEY=example
- PAYMENT_VNPAY_PAYMENT_URL=example
- PAYMENT_VNPAY_TMN_CODE=example
- PAYMENT_ZALOPAY_APP_ID=example
- PAYMENT_ZALOPAY_ENDPOINT=example
- PAYMENT_ZALOPAY_KEY1=example
- PAYMENT_ZALOPAY_KEY2=example
- PERSONA_API_KEY=example
- PINECONE_API_KEY=example
- PYPI_TOKEN=example
- QDRANT_API_KEY=example
- QDRANT_URL=example
- QWEN_API_KEY=example
- R2_ACCESS_KEY_ID=example
- R2_SECRET_ACCESS_KEY=example
- REDIS_URL=example
- REQUEST_KONG_SECRET=example
- SONAR_TOKEN=example
- SUPABASE_ANON_KEY=example
- SUPABASE_DB_PASSWORD=example
- SUPABASE_PROJECT_ID=example
- SUPABASE_SERVICE_ROLE_KEY=example
- TAVILY_API_KEY=example
- TELEGRAM_ALERT_CHAT_ID=example
- TELEGRAM_BOT_TOKEN=example
- VERCEL_CNAME=example
- VERCEL_TOKEN=example -->

Các biến bí mật này dùng cho các dịch vụ trong hệ thống.

### Cấu hình về supabase

Trong dự án supabase sử dụng cấu hình:

<!--
- SUPABASE_ACCESS_TOKEN=example
- SUPABASE_ANON_KEY=example
- SUPABASE_PROJECT_ID=example -->

Trong repo github `code-supabase-manager`, GitHub Actions sẽ tự động chạy cấu hình tạo bảng admin_whitelist, profiles và tạo bucket avatars, persona_avatars, persona_audios.

## Thông tin các repo mã nguồn khác

### Đường ống dữ liệu Data pipeline

Trong repo github `data-pipeline-vbplnew, data-pipeline-phapdien`, GitHub Actions sẽ tự động chạy thu thập dữ liệu, xử lý dữ liệu, thực hiện vector hóa dữ liệu và lưu và vector database.

Trong repo github `data-pipeline-phapdien-service, data-pipeline-vbplnew-service`, GitHub Actions sẽ tự động cấu hình dự án trong Vercel và cấu hình domain trong Cloudflare tương tự như api-gateway-http-log.
