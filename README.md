# 👁 Log & Metrics Explorer

A smart and minimal data explorer for logs, metrics, traces, and time-series data, developed with React and JavaScript.

## Features

**Data Sources Settings**
- URL and Headers
- Basic Authentication
- Quick Settings
- Shared configuration across data sources

**Data Browsers**
- Logs
- Metrics
- Traces
- Flux (experimental)

**Display & Visualization**
- Logs and Charts
- Traces View
- Table View
- Link Logs with Traces
- Split Data Views
- Multi-query Execution
- Time Range Selector
- Query History
- Mobile Responsive View
- 100% Client-Side Processing

---

## Usage

**Local Development**

Install dependencies:

```bash
pnpm install
```

**Local Build**

Build the application:

```bash
pnpm run build
```

Install and run a static server:

```bash
sudo npm install -g serve
serve -s ./packages/main/dist
```

---

## Environment Variables

| Variable | Default |
|---|---|
| host | `0.0.0.0` |
| port | `5173` |

Example:

```bash
pnpm dev -- --host localhost --port 8080
```

---

## Available Routes

The application uses hash-based routing for flexible static deployments.

| Route | Description |
|---|---|
| `/#/datasources` | Data source settings |
| `/#/search` | Main search interface |
| `/#/users` | Reserved users route |
| `/#/plugins` | Custom plugins |

---

## URL Parameters

The application can be controlled through URL parameters.

| Parameter | Description | Default |
|---|---|---|
| `start` | Start timestamp (Ns) | now |
| `stop` | End timestamp (Ns) | — |
| `isEmbed` | Embedded mode | false |
| `theme` | Application theme | dark |
| `left` | Left panel query details | — |
| `right` | Right panel query details | — |

---

## Query Configuration

Queries can be configured inside the left or right panel using JSON-encoded URL parameters.

- `id` — Query ID
- `idRef` — Query title
- `expr` — Query expression
- `limit` — Query result limit
- `dataSourceType` — Data source type (`logs`, `metrics`, `traces`, `flux`)
- `dataSourceURL` — Data source API URL
- `dataSourceId` — Data source identifier

---

## Local Proxy

For local experimentation, configure the following environment variable:

```env
VITE_API_BASE_URL=http://localhost:3100
```

Use the same protocol as the application instance.

---

## License

See the project's license file for licensing information.
