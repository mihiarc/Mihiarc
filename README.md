# Hi, I'm Chris Mihiar

I'm a **Research Economist** at the USDA Forest Service, Southern Research Station, where I develop open-source software tools that make environmental and natural resource research more accessible and reproducible.

My work lives at the intersection of **economics, ecology, and data science**. I build tools that help researchers, land managers, and policymakers understand our forests better — from analyzing national forest inventories to projecting how land use will change under different climate scenarios. I was a key contributor to the [USDA Forest Service 2020 RPA Assessment](https://research.fs.usda.gov/understory/2020-resources-planning-act-assessment), which provides long-range strategic planning for America's renewable resources.

<table>
<tr>
<td><strong>Education</strong></td>
<td>Ph.D. Applied Economics, Oregon State University</td>
</tr>
<tr>
<td><strong>Location</strong></td>
<td>Research Triangle Park, NC</td>
</tr>
</table>

[![Google Scholar](https://img.shields.io/badge/Google%20Scholar-183%20citations-4285F4?style=for-the-badge&logo=googlescholar&logoColor=white)](https://scholar.google.com/citations?user=buI4HUIAAAAJ)
[![ORCID](https://img.shields.io/badge/ORCID-0000--0002--9832--5262-A6CE39?style=for-the-badge&logo=orcid&logoColor=white)](https://orcid.org/0000-0002-9832-5262)

<p>
<a href="mailto:chris.mihiar@gmail.com">Email</a> ·
<a href="https://research.fs.usda.gov/about/people/christopher.mihiar">USFS Profile</a> ·
<a href="https://www.linkedin.com/in/chris-mihiar">LinkedIn</a> ·
<a href="https://www.researchgate.net/profile/Chris-Mihiar">ResearchGate</a> ·
<a href="https://www.nber.org/people/christopher_mihiar">NBER</a>
</p>

---

## GitHub Stats

<p>
<img src="https://github-readme-stats.vercel.app/api?username=mihiarc&show_icons=true&theme=default&hide_border=true&count_private=true" alt="GitHub Stats" height="165" />
<img src="https://github-readme-stats.vercel.app/api/top-langs/?username=mihiarc&layout=compact&theme=default&hide_border=true&langs_count=8" alt="Top Languages" height="165" />
</p>

<img src="https://github-readme-streak-stats.herokuapp.com/?user=mihiarc&theme=default&hide_border=true" alt="GitHub Streak" />

---

## Featured Projects

### pyfia — Forest Inventory Analysis Toolkit

[![PyPI](https://img.shields.io/pypi/v/pyfia?color=blue)](https://pypi.org/project/pyfia/)
[![Downloads](https://img.shields.io/pypi/dm/pyfia.svg)](https://pypi.org/project/pyfia/)
[![GitHub](https://img.shields.io/github/stars/mihiarc/pyfia?style=social)](https://github.com/mihiarc/pyfia)

The [USDA Forest Inventory and Analysis (FIA)](https://www.fia.fs.usda.gov/) program is the nation's continuous forest census, monitoring trees on over 300,000 plots across the United States. **pyfia** makes this massive dataset accessible to Python users with a clean API built on modern tools like Polars and DuckDB.

The library implements proper design-based statistical estimation with variance calculations that match the official FIA EVALIDator tool, so researchers can trust their results. Whether you need state-level timber volume estimates, county carbon stocks, or custom spatial analyses, pyfia handles the complexity of FIA's stratified sampling design.

**Key features:** Design-based estimation with proper variance · DuckDB backend for fast queries · Spatial filtering with arbitrary geometries · Exact statistical compatibility with FIA EVALIDator

---

### pyfvs — Forest Vegetation Simulator

[![GitHub](https://img.shields.io/github/stars/mihiarc/pyfvs?style=social)](https://github.com/mihiarc/pyfvs)

The Forest Vegetation Simulator (FVS) is the USDA Forest Service's standard tool for predicting forest growth and yield — it's been used for decades to plan timber harvests, model carbon sequestration, and simulate forest management scenarios. **pyfvs** brings this capability to Python with a clean, modern implementation of the Southern variant.

The simulator models the growth dynamics of four southern yellow pine species (loblolly, shortleaf, longleaf, and slash pine) that dominate commercial forestry in the southeastern United States. Given initial stand conditions, pyfvs projects tree growth, mortality, and yield over time, enabling researchers and forest managers to evaluate different management strategies.

**Key features:** Individual-tree growth models · Mortality and regeneration simulation · Yield projections for southern pines · Python-native implementation

---

### gridfia — Spatial Forest Biomass Analysis

[![GitHub](https://img.shields.io/github/stars/mihiarc/gridfia?style=social)](https://github.com/mihiarc/gridfia)

Forest inventory data is collected at discrete plot locations, but many applications need continuous spatial estimates — maps of biomass, carbon density, or timber volume across a landscape. **gridfia** bridges this gap by providing tools to create gridded estimates from FIA plot data.

The library handles the statistical challenges of spatial interpolation while respecting the design-based nature of FIA sampling. It's designed to work seamlessly with pyfia for data access and produces outputs compatible with standard geospatial tools.

**Key features:** Gridded biomass estimates · Spatial interpolation methods · Integration with pyfia · GeoTIFF and Zarr output formats

---

### rpa-landuse — AI-Powered Land Use Analytics

[![GitHub](https://img.shields.io/github/stars/mihiarc/rpa-landuse?style=social)](https://github.com/mihiarc/rpa-landuse)

The RPA Assessment projects how American lands will change over the coming decades under different climate and socioeconomic scenarios — tracking shifts between forest, cropland, pasture, urban, and range across every county in the contiguous US. **rpa-landuse** makes this complex dataset queryable through natural language.

Built with LangChain and Claude, the tool lets users ask questions like "How much forestland is projected to be lost in Georgia by 2070 under the high-growth scenario?" and get accurate answers backed by the underlying data. It's designed to make RPA projections accessible to policymakers, journalists, and researchers who may not be comfortable writing SQL queries.

**Key features:** Natural language queries · DuckDB backend for fast analytics · Multiple climate scenarios · County-level resolution

---

### socialmapper — Community Accessibility Analysis

[![GitHub](https://img.shields.io/github/stars/mihiarc/socialmapper?style=social)](https://github.com/mihiarc/socialmapper)

Understanding community accessibility requires combining geographic data (where are grocery stores, hospitals, parks?) with demographic data (who lives where, and can they reach these services?). **socialmapper** bridges OpenStreetMap POI data and US Census demographics to analyze accessibility patterns.

The toolkit calculates travel-time based metrics — not just straight-line distances — to understand how well different communities are served by essential services. It's useful for urban planning, public health research, and equity analysis.

**Key features:** OpenStreetMap POI integration · US Census demographic data · Travel-time isochrones · Community accessibility scoring

---

### esri-converter — Open Format Conversion

[![GitHub](https://img.shields.io/github/stars/mihiarc/esri-converter?style=social)](https://github.com/mihiarc/esri-converter)

ESRI's proprietary geodatabase format (GDB) is ubiquitous in government and enterprise GIS, but it creates barriers to data sharing and reproducible research. **esri-converter** provides robust tools for converting GDB files to open formats like GeoParquet.

Built for production workloads, the library handles multi-gigabyte datasets through streaming and chunking, with comprehensive validation and progress tracking via Rich. The output files are OGC GeoParquet compliant and readable by all standard geospatial tools.

**Key features:** GDB to GeoParquet conversion · Streaming for large datasets · OGC compliant output · Beautiful Rich progress UI

---

## Tech Stack

| Category | Tools |
|----------|-------|
| **Languages** | Python, R, TypeScript, SQL |
| **Data Processing** | Polars, DuckDB, Apache Arrow, Parquet, Zarr |
| **Geospatial** | GDAL, pyogrio, rioxarray, GeoPandas |
| **Web Development** | Next.js, React, Tailwind CSS |
| **AI/ML** | LangChain, LangGraph, Claude, Claude Code |
| **Infrastructure** | Google Cloud, uv, Ruff, pytest |

---

## Research Focus

### Forest Inventory & Analysis
I develop statistical methods and software for analyzing large-scale forest inventory data. The FIA program generates terabytes of data each year, and my tools help researchers extract meaningful insights while respecting the complex sampling design.

### Land-Use Change Modeling
My research projects how land use will evolve under different climate and socioeconomic futures. This work informs national policy through the RPA Assessment and helps land managers anticipate and adapt to change.

### Natural Capital Accounting
Forests provide enormous value through carbon storage, timber production, water filtration, and recreation — but this value rarely appears in economic accounts. I develop methods to quantify these ecosystem services using frameworks like the UN SEEA.

### Climate Adaptation
Climate change is already affecting American forests through more frequent wildfires, drought stress, and shifting species ranges. My research develops tools and projections that help managers and policymakers plan for these changes.

---

## Selected Publications

### First-Author Publications

**Mihiar, C.** & Lewis, D.J. (2021). Climate, adaptation, and the value of forestland: A national Ricardian analysis of the United States. *Land Economics*, 97(4), 911-932.
> This paper estimates how climate affects forest land values across the US, finding that forests are already adapting to local climate conditions. The results suggest forestland values are more resilient to climate change than previously thought. **[15 citations]**

**Mihiar, C.**, Lewis, D.J. & Coulston, J.W. (2023). County-level land-use projections for the conterminous United States, 2020-2070, used in the 2020 RPA Assessment.
> The official land-use projections for the 2020 RPA Assessment, covering six land-use categories across 3,000+ counties under multiple climate and socioeconomic scenarios. **[4 citations]**

**Mihiar, C.** & Lewis, D.J. (2023). An empirical analysis of US land-use change under multiple climate change scenarios. *Journal of the Agricultural and Applied Economics Association*, 2(3), 597-611.
> Analyzes how US land use is projected to change through 2070, finding that climate effects on land use are generally smaller than socioeconomic drivers but significant in particular regions. **[3 citations]**

### Co-Authored Publications

Cavender-Bares, J., Nelson, E., Meireles, J.E., ... **Mihiar, C.**, et al. (2022). The hidden value of trees: Quantifying the ecosystem services of tree lineages and their major threats across the contiguous US. *PLOS Sustainability and Transformation*, 1(4).
> A comprehensive assessment of tree ecosystem services across evolutionary lineages, revealing which tree groups provide the most value and face the greatest threats. **[44 citations]**

Caldwell, P.V., Martin, K.L., Vose, J.M., ... **Mihiar, C.**, et al. (2023). Forested watersheds provide the highest water quality among all land cover types, but the benefit of this ecosystem service depends on landscape context. *Science of the Total Environment*, 882.
> Demonstrates that forests are critical for water quality, but the value of forest cover depends on what other land uses surround it. **[43 citations]**

---

*Building tools that empower researchers, policymakers, and communities to understand and protect our natural resources.*
