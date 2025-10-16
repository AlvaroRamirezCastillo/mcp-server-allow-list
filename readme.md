sequenceDiagram
  actor U as Usuario
  participant FE as Frontend
  participant API as Auth API
  participant IdP
  U->>FE: Ingresa OTP
  FE->>API: /exchange-otp
  API->>IdP: verify(otp)
  IdP-->>API: OK
  API-->>FE: tokens