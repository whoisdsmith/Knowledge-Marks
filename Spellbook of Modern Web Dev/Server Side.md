## Server Side

### Network

* HTTP
  * Intro
    * [An overview of HTTP](https://developer.mozilla.org/en-US/docs/Web/HTTP/Overview), \
      [Introduction to HTTP](https://launchschool.com/books/http)
    * [Evolution of HTTP](https://developer.mozilla.org/en-US/docs/Web/HTTP/Basics_of_HTTP/Evolution_of_HTTP)
    * [Identifying resources on the Web](https://developer.mozilla.org/en-US/docs/Web/HTTP/Basics_of_HTTP/Identifying_resources_on_the_Web) / \
      [Understanding URIs](http://medialize.github.io/URI.js/about-uris.html)
    * [Architecture of the World Wide Web: Identification](https://www.w3.org/TR/webarch/#identification)
    * [MIME types](https://developer.mozilla.org/en-US/docs/Web/HTTP/Basics_of_HTTP/MIME_Types)
    * [HTTP Messages](https://developer.mozilla.org/en-US/docs/Web/HTTP/Messages)
    * [Connection management in HTTP/1.x](https://developer.mozilla.org/en-US/docs/Web/HTTP/Connection_management_in_HTTP_1.x)
    * [Redirections in HTTP](https://developer.mozilla.org/en-US/docs/Web/HTTP/Redirections)
  * Reference
    * [HTTP headers](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers)
    * [HTTP response status codes](https://developer.mozilla.org/en-US/docs/Web/HTTP/Status) / [httpstatuses.com](https://httpstatuses.com/)
  * [Same-origin policy](https://developer.mozilla.org/en-US/docs/Web/Security/Same-origin_policy)
    * [HTTP access control (CORS)](https://developer.mozilla.org/en-US/docs/Web/HTTP/Access_control_CORS) / [Using CORS](https://www.html5rocks.com/en/tutorials/cors/)
    * Content Security Policy (CSP) - [Google](https://developers.google.com/web/fundamentals/security/csp/) / [Mozilla](https://developer.mozilla.org/en-US/docs/Web/HTTP/CSP)
  * Performance
    * [High Performance Browser Networking](https://hpbn.co/), \
      [Ideal HTTP Performance](https://www.mnot.net/blog/2016/04/22/ideal-http)
    * HTTP Caching - [Google](https://developers.google.com/web/fundamentals/performance/optimizing-content-efficiency/http-caching), [Mozilla](https://developer.mozilla.org/en-US/docs/Web/HTTP/Caching)
    * [Compression in HTTP](https://developer.mozilla.org/en-US/docs/Web/HTTP/Compression)
  * HTTPS
    * [Why HTTPS Matters](https://developers.google.com/web/fundamentals/security/encrypt-in-transit/why-https)
    * [Is TLS Fast Yet?](https://istlsfastyet.com/) / [HTTP vs HTTPS Test](https://www.httpvshttps.com/)
    * [HTTP Strict-Transport-Security (HSTS)](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Strict-Transport-Security)
    * [What Is Mixed Content?](https://developers.google.com/web/fundamentals/security/prevent-mixed-content/what-is-mixed-content), [Preventing Mixed Content](https://developers.google.com/web/fundamentals/security/prevent-mixed-content/fixing-mixed-content)
  * HTTP/2
    * [http2 explained](https://www.gitbook.com/book/bagder/http2-explained/details) / \
      [Introduction to HTTP/2](https://developers.google.com/web/fundamentals/performance/http2/)
    * [HTTP/2 FAQ](https://http2.github.io/faq/)
    * [A Comprehensive Guide To HTTP/2 Server Push](https://www.smashingmagazine.com/2017/04/guide-http2-server-push/)
  * [gRPC](http://www.grpc.io/docs/quickstart/node.html)
    * [What is gRPC?](http://www.grpc.io/docs/guides/)
    * [Protocol Buffers](https://developers.google.com/protocol-buffers/)
* TCP
  * [Writing WebSocket servers](https://developer.mozilla.org/en-US/docs/Web/API/WebSockets_API/Writing_WebSocket_servers)
* UDP
  * [QUIC](https://www.chromium.org/quic)

\>\> Return to [Table of Contents](#table-of-contents)

### Server-side Best Practices

* SaaS
  * [The Twelve-Factor App](https://12factor.net/)
* Restful API
  * Heroku's [HTTP API Design Guide](https://geemus.gitbooks.io/http-api-design/content/en/), \
    Microsoft's [API Design Best Practices](https://docs.microsoft.com/en-us/azure/architecture/best-practices/api-design), [REST API Guidelines](https://github.com/Microsoft/api-guidelines/blob/master/Guidelines.md), \
    [Best Practices for Designing a Pragmatic RESTful API](http://www.vinaysahni.com/best-practices-for-a-pragmatic-restful-api), \
    [Principles of good RESTful API Design](https://codeplanet.io/principles-good-restful-api-design/)
  * [REST API Error Codes 101](http://blog.restcase.com/rest-api-error-codes-101/)
  * [Introducing JSON](http://json.org/)
* Microservices
  * [A pattern language for microservices](http://microservices.io/patterns/index.html)
    * [Microservice Architecture](http://microservices.io/patterns/microservices.html), [Monolithic Architecture](http://microservices.io/patterns/monolithic.html)
    * Decompose by [business capability](http://microservices.io/patterns/decomposition/decompose-by-business-capability.html), [subdomain](http://microservices.io/patterns/decomposition/decompose-by-subdomain.html)
    * [Service instance per container](http://microservices.io/patterns/deployment/service-per-container.html), [Service deployment platform](http://microservices.io/patterns/deployment/service-deployment-platform.html)
    * [Externalized configuration](http://microservices.io/patterns/externalized-configuration.html), [Microservice chassis](http://microservices.io/patterns/microservice-chassis.html)
    * Service discovery ([Server-side](http://microservices.io/patterns/server-side-discovery.html), [Client-side](http://microservices.io/patterns/client-side-discovery.html)), [Service registry](http://microservices.io/patterns/service-registry.html), [Remote Procedure Invocation](http://microservices.io/patterns/communication-style/rpi.html)
    * [Database per service](http://microservices.io/patterns/data/database-per-service.html), [Shared database](http://microservices.io/patterns/data/shared-database.html)
  * [Microservices: From Design to Deployment](https://www.nginx.com/blog/introduction-to-microservices/)
  * [Microservices Resource Guide](https://martinfowler.com/microservices/)
  * API Gateway
    * [Pattern: API Gateway / Backend for Front-End](http://microservices.io/patterns/apigateway.html)
    * [Why an API Gateway?](https://www.nginx.com/blog/microservices-api-gateways-part-1-why-an-api-gateway/)
    * [Moving from REST to GraphQL](https://medium.com/@frikille/moving-from-rest-to-graphql-e3650b6f5247) / [From REST to GraphQL](https://0x2a.sh/from-rest-to-graphql-b4e95e94c26b) / [GraphQL vs. REST](https://dev-blog.apollodata.com/graphql-vs-rest-5d425123e34b)
    * [Serverless and GraphQL: A Perfect Match for the New Cloud Paradigm](https://thenewstack.io/serverless-graphql-perfect-match-new-cloud-paradigm/)
  * Serverless
    * [Pattern: Serverless deployment](http://microservices.io/patterns/deployment/serverless-deployment.html)
    * [Microservices without the Servers](https://aws.amazon.com/blogs/compute/microservices-without-the-servers/)
    * [The Next Layer of Abstraction in Cloud Computing is Serverless](https://read.acloud.guru/iaas-paas-serverless-the-next-big-deal-in-cloud-computing-34b8198c98a2)
    * [The essential guide to serverless technologies and architectures](https://techbeacon.com/essential-guide-serverless-technologies-architectures), \
      [An essential guide to the serverless ecosystem](https://techbeacon.com/essential-guide-serverless-ecosystem)
    * [Serverless Architecture: Five Design Patterns](https://thenewstack.io/serverless-architecture-five-design-patterns/), \
      [Serverless Code Patterns](https://serverless.com/blog/serverless-architecture-code-patterns/)
* Cloud / Distributed
  * Architecture
    * [AWS Well-Architected](https://aws.amazon.com/architecture/well-architected/)
    * Azure's Cloud Fundamentals - [Architecture styles](https://docs.microsoft.com/en-us/azure/architecture/guide/architecture-styles/), [Pillars of software quality](https://docs.microsoft.com/en-us/azure/architecture/guide/pillars), [Design principles](https://docs.microsoft.com/en-us/azure/architecture/guide/design-principles/index)
  * Static
    * [Static Content Hosting](https://docs.microsoft.com/en-us/azure/architecture/patterns/static-content-hosting), [Valet Key](https://docs.microsoft.com/en-us/azure/architecture/patterns/valet-key), [Content Delivery Network](https://docs.microsoft.com/en-us/azure/architecture/best-practices/cdn)
  * Queue / Jobs
    * [Queue-Based Load Leveling](https://docs.microsoft.com/en-us/azure/architecture/patterns/queue-based-load-leveling), [Competing Consumers](https://docs.microsoft.com/en-us/azure/architecture/patterns/competing-consumers), [Priority Queue](https://docs.microsoft.com/en-us/azure/architecture/patterns/priority-queue)
    * [Background jobs](https://docs.microsoft.com/en-us/azure/architecture/best-practices/background-jobs)
  * Decompose
    * [Federated Identity](https://docs.microsoft.com/en-us/azure/architecture/patterns/federated-identity)
    * [Pipes and Filters](https://docs.microsoft.com/en-us/azure/architecture/patterns/pipes-and-filters)
    * [Compute Resource Consolidation](https://docs.microsoft.com/en-us/azure/architecture/patterns/compute-resource-consolidation)
  * Configuration
    * [External Configuration Store](https://docs.microsoft.com/en-us/azure/architecture/patterns/external-configuration-store), [Runtime Reconfiguration](https://docs.microsoft.com/en-us/azure/architecture/patterns/runtime-reconfiguration)
  * Storage / Querying
    * [Cache-Aside](https://docs.microsoft.com/en-us/azure/architecture/patterns/cache-aside), [Caching](https://docs.microsoft.com/en-us/azure/architecture/best-practices/caching)
    * [CQRS](https://docs.microsoft.com/en-us/azure/architecture/patterns/cqrs), [Event Sourcing](https://docs.microsoft.com/en-us/azure/architecture/patterns/event-sourcing)
    * [Index Table](https://docs.microsoft.com/en-us/azure/architecture/patterns/index-table), [Materialized View](https://docs.microsoft.com/en-us/azure/architecture/patterns/materialized-view)
    * [Data partitioning](https://docs.microsoft.com/en-us/azure/architecture/best-practices/data-partitioning), [Sharding](https://docs.microsoft.com/en-us/azure/architecture/patterns/sharding)
  * [Resiliency](https://docs.microsoft.com/en-us/azure/architecture/resiliency/) / [Availability](https://docs.microsoft.com/en-us/azure/architecture/checklist/availability)
    * [Retry](https://docs.microsoft.com/en-us/azure/architecture/patterns/retry), [Circuit Breaker](https://docs.microsoft.com/en-us/azure/architecture/patterns/circuit-breaker), [Transient fault handling](https://docs.microsoft.com/en-us/azure/architecture/best-practices/transient-faults)
    * [Compensating Transaction](https://docs.microsoft.com/en-us/azure/architecture/patterns/compensating-transaction)
    * [Health Endpoint Monitoring](https://docs.microsoft.com/en-us/azure/architecture/patterns/health-endpoint-monitoring), [Leader Election](https://docs.microsoft.com/en-us/azure/architecture/patterns/leader-election), [Scheduler Agent Supervisor](https://docs.microsoft.com/en-us/azure/architecture/patterns/scheduler-agent-supervisor)
    * [The Reactive Manifesto](http://www.reactivemanifesto.org/)
  * Multitenant
    * [Manage Identity in Multitenant Applications](https://docs.microsoft.com/en-us/azure/architecture/multitenant-identity/)
* Old-fashioned Web Hosting / Non-distributed
  * [Ultimate Guide to Web Hosting](http://www.whoishostingthis.com/resources/web-hosting/) / [Web Hosting Beginner Guide](http://www.webhostingsecretrevealed.net/web-hosting-beginner-guide/)
* Authentication / Authorization
  * [Cookies vs Tokens: The Definitive Guide](https://auth0.com/blog/cookies-vs-tokens-definitive-guide/), \
    [The Ins and Outs of Token Based Authentication](https://scotch.io/tutorials/the-ins-and-outs-of-token-based-authentication)
  * [Introduction to JSON Web Tokens](https://jwt.io/introduction/)
  * [An Introduction to OAuth 2](https://www.digitalocean.com/community/tutorials/an-introduction-to-oauth-2), [Understanding OAuth2](http://www.bubblecode.net/en/2016/01/22/understanding-oauth2/)
    * [The OAuth Bible](http://oauthbible.com/)
  * [Tokens used by Auth0](https://auth0.com/docs/tokens)
    * [Understanding Refresh Tokens](https://auth0.com/learn/refresh-tokens/)
  * [How To Safely Store A Password](https://codahale.com/how-to-safely-store-a-password/), \
    [You Wouldn't Base64 a Password - Cryptography Decoded](https://paragonie.com/blog/2015/08/you-wouldnt-base64-a-password-cryptography-decoded), \
    [How to securely hash passwords?](https://security.stackexchange.com/a/31846)
  * [Weak Signature Algorithm](https://developer.mozilla.org/en-US/docs/Web/Security/Weak_Signature_Algorithm)
* Security
  * [Security Guide for Developers](https://github.com/FallibleInc/security-guide-for-developers)
    * [Understanding CSRF](https://github.com/pillarjs/understanding-csrf), [CSRF Demystified](http://www.gnucitizen.org/blog/csrf-demystified/)
    * [Cross-site Scripting (XSS) Attack](https://www.acunetix.com/websitesecurity/cross-site-scripting/)
  * [OWASP Top Ten Cheat Sheet](https://www.owasp.org/index.php/OWASP_Top_Ten_Cheat_Sheet)
  * [WebAppSec/Secure Coding Guidelines](https://wiki.mozilla.org/WebAppSec/Secure_Coding_Guidelines)
  * [Node.js Security Checklist](https://blog.risingstack.com/node-js-security-checklist/)
  * Tools - see _[Tooling > Testing](#testing) > Analysis_
* Logging / Monitoring
  * [Logging The Ultimate Guide](https://www.loggly.com/ultimate-guide/category/node/)
  * [The Definitive Guide for Monitoring Node.js Applications](https://blog.risingstack.com/monitoring-nodejs-applications-nodejs-at-scale/)
  * [Monitoring and diagnostics](https://docs.microsoft.com/en-us/azure/architecture/best-practices/monitoring)
  * Tools - see _[Tooling > Workflow](#workflow) > Monitoring_
* DevOps
  * [Deployments Best Practices](http://guides.beanstalkapp.com/deployments/best-practices.html)
  * [Start your DevOps journey](https://www.atlassian.com/devops/start-your-journey)
  * [The Practical DevOps Playbook](https://www.shippable.com/devops-playbook.html)
  * Tools - see _[Tooling > Workflow](#workflow) > Deployment > DevOps_

\>\> Return to [Table of Contents](#table-of-contents)

### Microservices / API Services (Node.js)

* Frameworks
  * RESTful API
    * Middleware Framework
      * [Express](http://expressjs.com/) / [Koa](http://koajs.com/)
      * Express Middlewares
        * Logger
          * [morgan](https://www.npmjs.com/package/morgan), [express-winston](https://www.npmjs.com/package/express-winston), [errorhandler](https://www.npmjs.com/package/errorhandler), [response-time](https://www.npmjs.com/package/response-time)
        * HTTP Parser
          * [body-parser](https://www.npmjs.com/package/body-parser), [multer](https://www.npmjs.com/package/multer), [raw-body](https://www.npmjs.com/package/raw-body), [cookie-parser](https://www.npmjs.com/package/cookie-parser)
        * HTTP Headers and Verbs
          * [cors](https://www.npmjs.com/package/cors), [method-override](https://www.npmjs.com/package/method-override)
        * Performance
          * [compression](https://www.npmjs.com/package/compression) , [connect-timeout](https://www.npmjs.com/package/connect-timeout)
        * Security
          * [helmet](https://www.npmjs.com/package/helmet), [express-validator](https://www.npmjs.com/package/express-validator)
        * Auth
          * [express-jwt](https://www.npmjs.com/package/express-jwt) / [passport.js](http://passportjs.org/)
        * Proxy
          * [http-proxy-middleware](https://www.npmjs.com/package/http-proxy-middleware) / [rocky](https://www.npmjs.com/package/rocky)
        * GraphQL
          * [apollo-server-express](https://www.apollographql.com/docs/apollo-server/servers/express.html) / [express-graphql](https://www.npmjs.com/package/express-graphql)
    * Rich Framework
      * Configuration - [Hapi](https://hapijs.com/)
      * Realtime - [Feathers](https://feathersjs.com/)
  * Microservices
    * [Micro](https://www.npmjs.com/package/micro) / [Seneca](http://senecajs.org/) / [StdLib](https://stdlib.com/)
  * Serverless
    * [Serverless Framework](https://github.com/serverless/serverless)
    * [IronFunctions](https://github.com/iron-io/functions)
  * Bots
    * [Botkit](https://www.npmjs.com/package/botkit)
* GraphQL
  * [Schemas and Types](http://graphql.org/learn/schema/)
    * [GraphQL Schema Language Cheat Sheet](https://wehavefaces.net/graphql-shorthand-notation-cheatsheet-17cd715861b6)
  * [The Fullstack Tutorial for GraphQL](https://www.howtographql.com/)
  * Server
    * [Apollo Server](https://www.apollographql.com/docs/apollo-server/)
    * [graphql-tools](http://dev.apollodata.com/tools/graphql-tools/index.html)
  * Resolvers
    * [graphql-resolvers](https://github.com/lucasconstantino/graphql-resolvers)
* DocGen + CodeGen
  * [API Blueprint](https://apiblueprint.org/) / [Swagger](http://swagger.io/) / [RAML](http://raml.org/)
    * Parser - [Protagonist](https://www.npmjs.com/package/protagonist) / [Drafter](https://www.npmjs.com/package/drafter)
      * Renderer - [Aglio](https://www.npmjs.com/package/aglio)
    * Validator - [Dredd](https://www.npmjs.com/package/dredd)
  * [JSON Schema](http://json-schema.org/)
    * [Understanding JSON Schema](https://spacetelescope.github.io/understanding-json-schema/)
    * [JSON Schema Based Editor](https://github.com/jdorn/json-editor)
  * See _[Tooling > Documentation](#documentation)_
* Scaffold / Boilerplate / Generator
  * [Nodal](https://github.com/keithwhor/nodal)
  * [Fuge](http://fuge.io/)
  * [Botpress](https://github.com/botpress/botpress)
  * [nodecube](https://github.com/dexteryy/Project-WebCube) (Author's own project)

\>\> Return to [Table of Contents](#table-of-contents)

### Server-side Libraries (Node.js)

* Configuration
  * [dotenv](https://www.npmjs.com/package/dotenv)
  * [jsonfile](https://www.npmjs.com/package/jsonfile)
* Debugging
  * [winston](https://www.npmjs.com/package/winston)
  * [verror](https://www.npmjs.com/package/verror)
  * [longjohn](https://www.npmjs.com/package/longjohn), [stackman](https://www.npmjs.com/package/stackman)
  * [why-is-node-running](https://www.npmjs.com/package/why-is-node-running)
* Protocols
  * [form-data](https://www.npmjs.com/package/form-data), [formidable](https://www.npmjs.com/package/formidable)
  * [iconv-lite](https://www.npmjs.com/package/iconv-lite)
* Network
  * WebSocket - [ws](https://www.npmjs.com/package/ws) / [Socket.IO](https://www.npmjs.com/package/socket.io) / [Engine.IO](https://www.npmjs.com/package/engine.io) / [SockJS-node](https://www.npmjs.com/package/sockjs)
  * Server-Sent Event - [faye-websocket](https://www.npmjs.com/package/faye-websocket)
  * HTTP/2 - [spdy](https://www.npmjs.com/package/spdy)
  * gRPC - [grpc](https://www.npmjs.com/package/grpc)
  * AMQP - [amqplib](https://www.npmjs.com/package/amqplib)
  * [download](https://www.npmjs.com/package/download)
  * Email - [Nodemailer](https://nodemailer.com/)
    * Email HTML - [mailgen](https://www.npmjs.com/package/mailgen)
* Crypto
  * [hasha](https://www.npmjs.com/package/hasha)
  * [md5](https://www.npmjs.com/package/md5)
  * [bcrypt](https://www.npmjs.com/package/bcrypt)
* Auth
  * JWT - [jsonwebtoken](https://www.npmjs.com/package/jsonwebtoken)
  * [passwordless](https://passwordless.net/)
  * [oauth](https://www.npmjs.com/package/oauth)
  * OAuth Providers - [hello.js](http://adodson.com/hello.js/) / [grant](https://www.npmjs.com/package/grant)
  * [svg-captcha](https://github.com/lemonce/svg-captcha)
* Storage
  * NOSQL
    * Redis Client - [ioredis](https://github.com/luin/ioredis)
    * MongoDB ORM - [Mongooose](http://mongoosejs.com/)
    * DynamoDB ORM - [vogels](https://www.npmjs.com/package/vogels)
    * HBase Client - [hbase](https://www.npmjs.com/package/hbase)
  * RDS
    * RDS ORM - [Sequelize](http://docs.sequelizejs.com/)
    * SQL Builder - [Knex.js](http://knexjs.org/)
* Jobs
  * Parallel - [webworker-threads](https://www.npmjs.com/package/webworker-threads)
  * Queue - [kue](https://www.npmjs.com/package/kue) / [bull](https://www.npmjs.com/package/bull)
  * Scheduler - [node-schedule](https://www.npmjs.com/package/node-schedule)
* Scraping
  * HTML Traversing - [cheerio](https://www.npmjs.com/package/cheerio), [jsdom](https://www.npmjs.com/package/jsdom)
  * HTML Parsing - [parse5](http://inikulin.github.io/parse5/index.html) / [htmlparser2](https://www.npmjs.com/package/htmlparser2)
  * Extract Article - [read-art](https://www.npmjs.com/package/read-art) / [node-readability](https://www.npmjs.com/package/node-readability)
  * Extract Metadata - [url-unshort](https://www.npmjs.com/package/url-unshort) / [embedza](https://www.npmjs.com/package/embedza)
  * Web Crawler - [simplecrawler](https://www.npmjs.com/package/simplecrawler) / [x-ray](https://www.npmjs.com/package/x-ray) / [scrape-it](https://www.npmjs.com/package/scrape-it) / [Headless Chrome Crawler](https://github.com/yujiosaka/headless-chrome-crawler)
  * Headless Browsers Automation - see _[Tooling > Testing](#testing) > Web Testing > Functional Testing > Headless Browser Automation_
* Images
  * Canvas / WebGL API - [node-canvas](https://www.npmjs.com/package/canvas) / [gl](https://www.npmjs.com/package/gl)
  * Image Manipulation - [gm](https://www.npmjs.com/package/gm) / [sharp](http://sharp.dimens.io/)
  * Capture Screenshots - [pageres](https://github.com/sindresorhus/pageres)
  * QR Code / Barcode - [qr-image](https://www.npmjs.com/package/qr-image)
  * Computer Vision - [tracking.js](https://trackingjs.com) / [opencv](https://www.npmjs.com/package/opencv)
* Parsing / Generating
  * Text - [unified](https://www.npmjs.com/package/unified)
    * Markdown - [remark](http://remark.js.org/)
  * [PDFKit](https://www.npmjs.com/package/pdfkit)
  * [csv](https://www.npmjs.com/package/csv)
  * [xml2js](https://www.npmjs.com/package/xml2js)
* NLP
  * [natural](https://github.com/NaturalNode/natural) / [retext](https://github.com/wooorm/retext) / [NodeJieba](https://github.com/yanyiwu/nodejieba)

\>\> Return to [Table of Contents](#table-of-contents)

### Cloud Services (Global)

* Compute
  * FaaS / Serverless / WebHook
    * [AWS Lambda](https://aws.amazon.com/lambda/) / [Google Cloud Functions](https://cloud.google.com/functions/)
    * [webtask](https://webtask.io/) / [hook.io](https://hook.io/)
    * [Graphcool Functions](https://www.graph.cool/docs/reference/functions/overview-boo6uteemo/)
    * [Amazon API Gateway](https://aws.amazon.com/api-gateway/)
  * PaaS
    * See _[Tooling > Workflow](#workflow) > Deployment > DevOps > PaaS_
  * CaaS
    * [Amazon ECS](https://aws.amazon.com/ecs/) / [Google Container Engine](https://cloud.google.com/container-engine/)
* Storage
  * Object Storage
    * [Amazon S3](https://aws.amazon.com/s3/) / [Google Cloud Storage](https://cloud.google.com/storage/)
    * [imgix](https://www.imgix.com)
  * DBaaS
    * In-Memory Key-Value NoSQL - [Amazon ElastiCache](https://aws.amazon.com/elasticache/)
      * Redis - [Compose](https://www.compose.com/redis) / [Redise Cloud](https://redislabs.com/products/redis-cloud/) / [Heroku Redis](https://www.heroku.com/redis)
    * Document NoSQL - [Amazon DynamoDB](https://aws.amazon.com/dynamodb/) / [Google Cloud Datastore](https://cloud.google.com/datastore/)
      * MongoDB - [Compose](https://www.compose.com/mongodb) / [mLab](https://mlab.com/) / [MongoDB Atlas](https://www.mongodb.com/cloud/atlas)
      * CouchDB - [Couchbase](https://www.couchbase.com/products/server) / [Cloudant](https://www.ibm.com/analytics/us/en/technology/cloud-data-services/cloudant/)
    * Wide Column NoSQL - [Google Bigtable](https://cloud.google.com/bigtable/)
    * SQL - [Amazon RDS](https://aws.amazon.com/rds/) / [Google Cloud SQL](https://cloud.google.com/sql/)
      * PostgreSQL - [Compose](https://www.compose.com/postgresql) / [Heroku Postgres](https://www.heroku.com/postgres)
      * MySQL - [Compose](https://www.compose.com/mysql)
    * NewSQL - [Google Cloud Spanner](https://cloud.google.com/spanner/)
    * Queue - [Amazon SQS](https://aws.amazon.com/sqs/) / [Amazon Kinesis](https://aws.amazon.com/kinesis/) / [Google Cloud Pub/Sub](https://cloud.google.com/pubsub/)
      * Kafka - [Heroku Kafka](https://www.heroku.com/kafka)
      * RabbitMQ - [Compose](https://www.compose.com/rabbitmq)
    * Analytics - [Amazon CloudSearch](https://aws.amazon.com/cloudsearch/)
      * Elasticsearch - [Amazon Elasticsearch Service](https://aws.amazon.com/elasticsearch-service/) / [Elastic Cloud](https://www.elastic.co/cloud) / [Bonsai](https://bonsai.io/)
    * Warehouse - [Amazon Redshift](https://aws.amazon.com/redshift/) / [Google BigQuery](https://cloud.google.com/bigquery/)
* BaaS
  * CRUD
    * Realtime
      * [Firebase Realtime Database](https://firebase.google.com/products/database/)
    * GraphQL
      * [Graphcool](https://www.graph.cool/) / [Scaphold](https://scaphold.io/)
    * CMS
      * [WordPress.com REST API](https://developer.wordpress.com/docs/api/) / [Contentful](https://www.contentful.com/) / [DatoCMS](https://www.datocms.com/) / [GraphCMS](https://graphcms.com/) / [Baasic](http://www.baasic.com/)
  * Auth
    * [Auth0](https://auth0.com/) / [Amazon Cognito](https://aws.amazon.com/cognito/) / [Firebase Authentication](https://firebase.google.com/products/auth/)
    * [OAuth.io](https://oauth.io/)
    * CAPTCHA
      * [reCAPTCHA](https://www.google.com/recaptcha/)
  * Search - [Algolia](https://www.algolia.com/)
  * Email - [SendGrid](https://sendgrid.com/) / [Mailgun](https://www.mailgun.com/) / [Mandrill](http://www.mandrill.com/) / [Amazon SES](https://aws.amazon.com/ses/)
  * SMS - [Nexmo](https://www.nexmo.com/) / [Twilio](https://www.twilio.com/) / [Amazon SNS](https://aws.amazon.com/sns/)
  * Payment - [Stripe](https://stripe.com/)
  * Maps - [Mapbox](https://www.mapbox.com/)
  * Customer Support - [Intercom](https://developers.intercom.com/) / [Zendesk](https://developer.zendesk.com/)
  * IM - [Discord](https://discordapp.com/developers/)
  * Form - [Typeform.io](http://docs.typeform.io/) / [Form.io](https://form.io/)
* AIaaS / BDaaS
  * Natural Language
    * NLP - [Google Natural Language API](https://cloud.google.com/natural-language/)
    * Speech Recognition / Speech Synthesis
      * [Amazon Lex](https://aws.amazon.com/lex/) / [Google Cloud Speech API](https://cloud.google.com/speech/)
      * [Amazon Polly](https://aws.amazon.com/polly/)
    * Translation - [Google Cloud Translation API](https://cloud.google.com/translate/)
  * Computer Vision
    * [Amazon Rekognition](https://aws.amazon.com/rekognition/) / [Google Cloud Vision API](https://cloud.google.com/vision/)
    * [Google Cloud Video Intelligence API](https://cloud.google.com/video-intelligence/)

\>\> Return to [Table of Contents](#table-of-contents)

### Cloud Services (China)

> The evil twins inside [the Great Firewall of China](https://github.com/dexteryy/spellbook-of-modern-webdev/pull/4)

* Compute
  * FaaS / Serverless / WebHook
    * [阿里云-函数计算](https://www.aliyun.com/product/fc) / [腾讯云-无服务器云函数 SCF](https://www.qcloud.com/product/scf)
    * [阿里云-API 网关](https://www.aliyun.com/product/apigateway)
  * PaaS
    * See _[Tooling > Workflow](#workflow) > Deployment > DevOps > PaaS_
  * CaaS
    * [阿里云-容器服务](https://www.aliyun.com/product/containerservice) / [腾讯云-容器服务 CCS](https://www.qcloud.com/product/ccs) / [DaoCloud](https://www.daocloud.io/dcs)
* Storage
  * Object Storage
    * [阿里云-对象存储 OSS](https://www.aliyun.com/product/oss) / [腾讯云-对象存储 COS](https://www.qcloud.com/product/cos)
  * DBaaS
    * In-Memory Key-Value NoSQL
      * Redis - [阿里云-云数据库 Redis 版](https://www.aliyun.com/product/kvstore) / [腾讯云-云存储 Redis](https://www.qcloud.com/product/crs)
    * Document NoSQL
      * MongoDB - [阿里云-云数据库 MongoDB版](https://www.aliyun.com/product/mongodb) / [腾讯云-文档数据库 MongoDB](https://www.qcloud.com/product/mongodb)
    * Wide Column NoSQL - [阿里云-表格存储 OTS](https://www.aliyun.com/product/ots)
      * HBase - [阿里云-云数据库 HBase 版](https://cn.aliyun.com/product/hbase) / [腾讯云-列式数据库 HBase](https://www.qcloud.com/product/HBase)
    * SQL
      * PostgreSQL - [阿里云-云数据库 PostgreSQL 版](https://www.aliyun.com/product/rds/postgresql) / [腾讯云-云数据库 CDB for PostgreSQL](https://www.qcloud.com/product/postgresql)
      * MySQL - [阿里云-云数据库 MySQL 版](https://www.aliyun.com/product/rds/mysql) / [腾讯云-云数据库 CDB for MySQL](https://www.qcloud.com/product/cdb)
    * Queue - [阿里云-消息服务 MNS](https://www.aliyun.com/product/mns) / [腾讯云-消息服务 CMQ](https://www.qcloud.com/product/cmq)
      * Kafka - [腾讯云-消息服务 CKAFKA](https://www.qcloud.com/product/CKafka)
    * Analytics - [阿里云-开放搜索 OpenSearch](https://www.aliyun.com/product/opensearch) / [腾讯云搜 TCS](https://www.qcloud.com/product/tcs)
    * Warehouse - [阿里云-MaxCompute (ODPS)](https://www.aliyun.com/product/odps) / [腾讯云-大数据处理套件TBDS](https://www.qcloud.com/product/tbds)
* BaaS
  * CRUD
    * [LeanCloud-数据存储](https://leancloud.cn/docs/storage_overview.html)
    * Realtime
      * [野狗-实时通信引擎](https://www.wilddog.com/product/sync-overview) / [LeanCloud-实时通信](https://leancloud.cn/docs/realtime_v2.html)
  * Auth
    * [野狗-身份认证](https://www.wilddog.com/product/auth-overview)
    * CAPTCHA
      * [极验](http://www.geetest.com/) / [腾讯云-验证码服务 YY](https://www.qcloud.com/product/yy)
  * Search -
  * Email - [阿里云-邮件推送](https://www.aliyun.com/product/directmail) / [SendCloud](http://sendcloud.sohu.com/)
  * SMS - [阿里云-短信服务](https://www.aliyun.com/product/sms) / [腾讯云-短信 SMS](https://www.qcloud.com/product/sms) / [云片](https://www.yunpian.com/) / [野狗-短信](https://www.wilddog.com/product/message-overview)
  * Payment - [Ping++](https://www.pingxx.com/products)
  * Maps - [高德开放平台](https://lbs.amap.com/getting-started/map/) / [百度地图开放平台](http://lbsyun.baidu.com/)
  * Customer Support - [美洽](https://meiqia.com/) / [微金小云客服](https://www.qcloud.com/product/ICS)
  * IM - [野狗-即时通讯](https://www.wilddog.com/product/im-overview) / [腾讯云-云通信 IM](https://www.qcloud.com/product/im)
  * Form - [金数据](https://help.jinshuju.net/articles/api-intro)
* AIaaS / BDaaS
  * Natural Language
    * NLP
      * [腾讯云-文智自然语言处理 NLP](https://www.qcloud.com/product/nlp)
      * [阿里云-机器学习PAI-文本分析](https://help.aliyun.com/document_detail/42747.html)
    * Speech Recognition / Speech Synthesis
      * [阿里云-智能语音交互](https://data.aliyun.com/product/nls) / [腾讯云-智能语音服务 AAI](https://www.qcloud.com/product/aai)
    * Translation - [腾讯云-机器翻译](https://www.qcloud.com/product/tmt)
  * Computer Vision
    * [腾讯云-万象优图 CI](https://www.qcloud.com/product/ci)
    * [阿里云-印刷文字识别](https://data.aliyun.com/product/ocr)
  * Graphs / Networks / Clusters
    * [阿里云-推荐引擎](https://data.aliyun.com/product/re) / [腾讯云-云推荐引擎 CRE](https://www.qcloud.com/product/cre)
    * [阿里云-关系网络分析](https://data.aliyun.com/product/graphanalytics)
    * [阿里云-机器学习PAI-网络分析](https://help.aliyun.com/document_detail/42750.html)
  * Persona
    * [阿里云-画像分析](https://data.aliyun.com/product/porana) / [腾讯云-智能推荐 IR](https://www.qcloud.com/product/ir)

\>\> Return to [Table of Contents](#table-of-contents)