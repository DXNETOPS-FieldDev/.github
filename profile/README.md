<p align="center">
  <img src="images/broadcom-logo.png" alt="Broadcom" width="80" />
</p>

<h1 align="center">DX NetOps Field Development</h1>

<p align="center">
  Enhancements and customizations for <strong>DX NetOps</strong>, built by the Broadcom field team —
  <br />
  App Views for the NetOps Portal, Grafana dashboards, and operational utilities.
</p>

<p align="center">
  <a href="#public-projects">Public projects</a> ·
  <a href="#internal-projects">Internal projects</a> ·
  <a href="#using-these-projects">Using these projects</a>
</p>

---

## Public projects

**Everything in this section is public — browse it, clone it, and run it in your own
environment.** Each repository carries its own installation and configuration guide.

### App Views for the DX NetOps Portal

Self-contained App Views that deploy into the NetOps Portal and run against its own
services — no separate backend to stand up.

| Project | What it does |
|---|---|
| **[WeatherMap](https://github.com/DXNETOPS-FieldDev/WeatherMap)** | Puts the network on a map — devices, SD-WAN tunnels, AppNeta paths, Spectrum alarms, weather and power-grid events in one geographic view, so an operator can see *where* something is going wrong at a glance. |
| **[ThresholdReport](https://github.com/DXNETOPS-FieldDev/ThresholdReport)** | A searchable view of every DX NetOps Performance Management threshold profile, its event rules, and the devices each rule applies to — including rules whose devices have no polled items, which the standard DA UI does not surface. CSV export. |
| **[Device-Geo-Editor](https://github.com/DXNETOPS-FieldDev/Device-Geo-Editor)** | View and edit the geographic coordinates of managed devices from inside the Portal — address geocoding, a draggable map pin, and a one-click write back to the DA REST API. |

### Grafana dashboards

Dashboard libraries that query DX NetOps directly, with the generators and deployment
tooling used to build and install them.

| Project | What it does |
|---|---|
| **[grafana-operational-reports](https://github.com/DXNETOPS-FieldDev/grafana-operational-reports)** | The CABI Operational Reports for DX NetOps Spectrum, rebuilt as Grafana dashboards — alarm log, alarm activity by user, alarm count trend and more, with a per-report import guide and a catalog of screenshots. |
| **[grafana-netops-flow-reports](https://github.com/DXNETOPS-FieldDev/grafana-netops-flow-reports)** | Flow and conversation reporting for DX NetOps Performance Center, queried live through PC's OData4 API with no ingestion or caching layer in between. Ships the Python generators that build the dashboard JSON. |

---

## Internal projects

These are **maintained by the Broadcom field team and are not publicly cloneable.** They
are listed here so it is clear what exists; if one of them is relevant to your
environment, get in touch and we will tell you where it stands.

| Project | What it does | Access |
|---|---|---|
| **netops-dashboard-studio** | Self-service Grafana dashboards for DX NetOps: describe a monitoring or troubleshooting need in plain language and get a live dashboard assembled from measured inventory. Also curates dashboards contributed by field SEs onto a shared demo estate. | On request |

<!-- Add further internal projects here, same three columns. Keep the "Access" column
     honest -- "On request" means someone will actually answer. -->

---

## Using these projects

**Start with the repository's own README.** Each one documents its prerequisites, how to
install it, and how to configure it against your environment — App Views ship as a
deployable zip, the Grafana repositories ship importable dashboard JSON plus a deployment
script.

**Check the `LICENSE` file before you reuse anything.** This page does not itself grant
any usage rights, and the terms differ between repositories. If a repository you need is
missing a license, open an issue on it and we will clarify the terms.

**Questions, bugs, or a request?** Open an issue on the relevant repository — that is the
fastest way to reach the people who built it.

---

<p align="center">
  <sub>Built by the DX NetOps field team at Broadcom.</sub>
</p>
