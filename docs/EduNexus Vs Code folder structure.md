EDUNEXUS/

│

├── backend/

│   │

│   ├── src/

│   │   │

│   │   ├── config/

│   │   │   ├── db.js

│   │   │   ├── redis.js

│   │   │   ├── env.js

│   │   │   └── payments.config.js

│   │   │

│   │   ├── routes/

│   │   │   ├── auth.routes.js

│   │   │   ├── user.routes.js

│   │   │   ├── school.routes.js

│   │   │   ├── academic.routes.js

│   │   │   ├── finance.routes.js

│   │   │   ├── library.routes.js

│   │   │   ├── hostel.routes.js

│   │   │   ├── ai.routes.js

│   │   │   ├── opportunet.routes.js

│   │   │   ├── communication.routes.js

│   │   │   └── workflow.routes.js

│   │   │

│   │   ├── controllers/

│   │   │   ├── auth.controller.js

│   │   │   ├── user.controller.js

│   │   │   ├── school.controller.js

│   │   │   ├── finance.controller.js

│   │   │   ├── payment.controller.js   ⭐

│   │   │   ├── ai.controller.js

│   │   │   └── workflow.controller.js

│   │   │

│   │   ├── services/

│   │   │   ├── auth.service.js

│   │   │   ├── user.service.js

│   │   │   ├── payment.service.js      ⭐ (card + bank transfer logic)

│   │   │   ├── ai.service.js

│   │   │   └── workflow.service.js

│   │   │

│   │   ├── models/

│   │   │   ├── user.model.js

│   │   │   ├── school.model.js

│   │   │   ├── finance.model.js

│   │   │   └── payment.model.js

│   │   │

│   │   ├── middleware/

│   │   │   ├── auth.middleware.js   ⭐ (your login protection layer)

│   │   │   ├── role.middleware.js

│   │   │   ├── error.middleware.js

│   │   │   └── rateLimit.middleware.js

│   │   │

│   │   ├── utils/

│   │   │   ├── password.utils.js

│   │   │   ├── jwt.utils.js

│   │   │   ├── logger.js

│   │   │   └── validator.js

│   │   │

│   │   ├── payments/

│   │   │   ├── card.payments.js        ⭐ Stripe/Mpesa abstraction

│   │   │   ├── bank.transfer.js        ⭐ manual + webhook verification

│   │   │   └── payment.gateway.js

│   │   │

│   │   ├── ai/

│   │   │   ├── engine.js

│   │   │   ├── recommender.js

│   │   │   ├── risk.model.js

│   │   │   └── opportunet.engine.js

│   │   │

│   │   ├── workflows/

│   │   │   ├── engine.js

│   │   │   ├── executor.js

│   │   │   └── scheduler.js

│   │   │

│   │   ├── app.js

│   │   └── server.js

│   │

│   ├── tests/

│   ├── package.json

│   ├── .env

│   └── README.md

│

│

├── frontend/

│   │

│   ├── public/

│   │   ├── login.html

│   │   ├── signup.html

│   │   ├── dashboard.html

│   │   ├── assets/

│   │   │   ├── images/

│   │   │   ├── css/

│   │   │   └── js/

│   │

│   ├── src/

│   │   ├── pages/

│   │   ├── components/

│   │   ├── services/

│   │   └── router/

│   │


│   └── package.json

│

│

├── database/

│   │

│   ├── postgres/

│   │   ├── layer1_core.sql

│   │   ├── layer2_academic.sql

│   │   ├── layer3_communication.sql

│   │   ├── layer4_finance.sql

│   │   ├── layer5_library.sql

│   │   ├── layer6_hostel.sql

│   │   ├── layer7_activities.sql

│   │   ├── layer8_opportunet.sql

│   │   ├── layer9_ai.sql

│   │   └── layer10_security.sql

│   │

│   ├── seeds/

│   │   ├── roles.seed.sql

│   │   ├── permissions.seed.sql

│   │   └── sample_school.seed.sql

│   │

│   └── migrations/

│

│

├── integrations/

│   ├── mpesa/

│   ├── stripe/

│   ├── email/

│   ├── sms/

│   └── whatsapp/

│

│

├── ai-engine/

│   ├── models/

│   ├── training/

│   ├── inference/

│   └── datasets/

│

│

├── devops/

│   ├── docker/

│   ├── nginx/

│   ├── ci-cd/

│   └── deployment-scripts/

│

│

├── docs/

│   ├── architecture.md

│   ├── database-design.md

│   ├── api-specs.md


│   └── system-flow.md

│

│

├── .gitignore

├── README.md

└── docker-compose.yml
