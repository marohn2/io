View additional fields: [OpenEPD spreadsheet](https://docs.google.com/spreadsheets/d/1q2TW0GlLlK7yH3k5TSsWGmXyL94KPI9VUWWv9vid63A/edit) - [How to Get an EPD](https://buildingtransparency.org/ec3/creator-contacts/epds) - [EPD Guide](https://www.oneclicklca.com/simple-epd-guide/)

<br>**Applied Sciences 2021 - Article Draft**

## International Impact Labels for Communities and Individuals using Environmental Product Declarations (EPD) with YAML

Environmental Impact Profiles published using the user-friendly [YMAL syntax](https://docs.ansible.com/ansible/latest/reference_appendices/YAMLSyntax.html) allow scenarios and entity profiles to be easily shared and compared for communities, companies and individuals when combined with international standards created for Environmental Product Declarations (EPDs) by organizations like the Smart Built Environment Innovation Program in Europe and <a href="https://buildingtransparency.org" target="_blank">Building&nbsp;Transparency</a> in the United States.

Standardized international data practices have emerged for Life Cycle Assessment (LCA) interoperability based on common units of flow when measuring the activities of agents within a comparable range of time.<sup>1</sup>  Large backend databases like USEEIO<sup>2</sup>, Ecoinvent<sup>3</sup> and Bonsai<sup>4</sup> now make the output of flow analysis broadly accessible through API calls which aggregate results into small, pre-processed files that can be output to CSV, JSON or YAML for use in fast-loading, static website displays &ndash; which are increasingly hosted for free using Content Delivery Networks (CDN) in conjunction with collaborative editing sites like GitHub.

<div class="text-highlight">
Currently, most EPD reporting is still done via <a href="https://www.nrmca.org/association-resources/sustainability/epd-program/epd-ready-mix-usa-materials-lookup/">PDF</a>.<br>
A Ready Mix USA cement PDF example is downloadable at <a href="https://www.nrmca.org/association-resources/sustainability/epd-program/epd-ready-mix-usa-materials-lookup/">nrmca.org</a>.
</div>

An opportunity exists to improve entity data sharing by extending machine readable Environmental Product Declaration (EPD) formats to also describe community impacts and individual footprints.  Using YAML (an easy-to-read superset of JSON), entity reports can be compared visually or formatted as summaries for a variety of entities, with layouts similar to nutritional labels. (Figure 1)

Expanding research by the Carbon Leadership Forum to align analysis methods around a common standard for conveying estimates of embodied carbon in construction from extracting, manufacturing and installing materials<sup>5</sup> strategies are being developed to document sources and overcome uncertainty.

An EPD file is a short version of an entity's Life Cycle Assessment (LCA) report. An LCA report must be performed before an EPD can be created. The LCA report can be stored privately to protect sensitive info. The EPD format avoids sensitive details and can therefore be shared without exposing company secrets.  

Storing editable scenario configuration files as YAML allows for faster editing by humans since YAML uses a simple outline format. Subsequently there are fewer opportunities for errors. YAML is also less intimidating than JSON to new editors. 

To automate the exchange of impact files, Building Transparency has extended the popular ILCD+EPD standard<sup>6</sup> to include guarantees for the uniqueness of agents, dated version control and precise Product Category Rules (PCR).  In the [OpenEPD Interchange Format](https://docs.google.com/document/d/1rvWl0W2nmCohaaHXG1P-uX5cDKHv_vD9zfTV5A6qM7A/edit#), each sector's classifications are defined independently by industry groups extending base properties.<sup>7</sup>  

The resulting classifications may be output as JSON or converted to YAML <span style="white-space: nowrap;">(a superset of JSON).</span>

**AS JSON**  

~~~
“concrete” : {
   “compressive_strength_28d” : 35.5,
   “compressive_strength_3d” : 25,
   “exposure_F” : “F0”,
}
~~~

**As YAML**

~~~
concrete:  
 compressive_strength_28d: 35.5  
 compressive_strength_3d: 25  
 exposure_F: F0
~~~





**Advantage of YAML for entity data sharing**  

JSON is well suited for data interchange since the structure is rigid.  
YAML based on JSON standards has the advantage of being both slim and easier to read/edit.  

- Machine-Readable - A significant advantage of both JSON and YAML over PDF files  
- Human-Editable - Fewer errors likely when editing YAML compared to JSON scenario files   
- Modular for CI/CD settings - Stand-alone files are not dependant on an API for transfer   
- Equitable - Allows for static file comparisons without database access requirements
- Inclusive - Universally accessible to developers, designers and machine learning   

Samples of profile templates using YAML and JSON may be viewed online at:
<a href="https://model.earth/io/template/">model.earth/io/template</a>


**Enhancements to the International ILCD+EPD+ Standard provided by openEPD**

- Guarantees for the uniqueness of agents
- Dated version control
- Precise Product Category Rules (PCR)
- New sector classifications defined independently

[Plus codes](https://9to5google.com/2018/03/13/google-plus-codes-maps/), also known as Open Location Code, were developed by Google in 2015 for locations without streetnames. Plus codes represent regions using 100-meter and 14-meter squares. An additional character can be added for 3 square meter precision - like the location of a loading dock.

<img src="img/google-plus-codes-how-it-works.jpg" style="width:100%; max-width:800px">


**Additional advantages of YAML when outputting HTML for PDF files**

- Ability to self reference 
- Support for complex datatypes 
- Embedded block literals 
- Storage of comments

**Machine Learning Applications**

Indexes of Machine-Readable APIs and detail files allow for graph analysis and imputation for missing data to further reduce uncertainties in the evaluation of local impacts.

---
<br>

**Conclusion**

Basing new inflow-outflow summaries for communities on existing EPD standards developed for product impacts, will simplify the ease with which impacts are compared and mitigated for locations, workforces and schools. Including YAML file links in environmental product directories will allow for easier sharing of metadata for scenario configuration and web services such as impact labels and heatmaps, while providing a human-readable format that works equally well for machine learning analysis. 

A frontend YAML editing interface is being developed by Code for America<sup>8</sup> to update community impact scenario files directly using GitHub Actions. The new work extends the metadata editing interface created by the government of Italy to manage public code repositories. The same process could update individual footprint estimates using a community's unique baseline mix of industries and commute times.

Possible next steps: Set up GitHub Actions using [Futura's scenario analysis tool for LCA](https://futura.readthedocs.io/en/latest/)<sup>9</sup> to preprocess foreground model data using Wurst library Python functions and the Brightway2 framework with background database systems like Ecoinvent.  
<br>



## References:
1. Janowicz, K.; Krisnadhi, A.A.; Hu, Y.; Suh, S.; Weidema, P.; Rivela, B.; Tiv, J.; Meyer, D.E.; Hitzler, P.; Ingwersen, W.; Kuczenski, B. [A minimal ontology pattern for life cycle assessment data](https://www.researchgate.net/publication/281685710_A_Minimal_Ontology_Pattern_for_Life_Cycle_Assessment_Data). Proceedings of the Workshop on Ontology and Semantic Web Patterns (6th edition) **2015**, WOP2015.
2. USEEIO citation.
3. Ecoinvent citation.
4. Ghose, A., Hose, K.; Lissandrini, M.; Weidema, B.P. [An open source dataset and ontology for product footprinting](https://people.cs.aau.dk/~matteo/pdf/eswc19-bonsai.pdf). In European Semantic Web Conference (pp. 75-79). Springer, Cham. **2019**, June
5. Simonen, K.; Droguett, B.R.; Strain, L.; McDade, E. [Embodied carbon benchmark study: LCA for low carbon construction](https://digital.lib.washington.edu/researchworks/handle/1773/38017). University of Washington. **2017**
6. [Increased availability of machine-readable EPDs in the ILCD+EPD+ format](https://www.diva-portal.org/smash/get/diva2:1549561/FULLTEXT01.pdf)  
7. [OpenEPD](https://www.buildingtransparency.org/openepd/) by Building Transparency
8. Code for America project citation.
9. Joyce, P.J.; Björklund, A. [Futura: A new tool for transparent and shareable scenario analysis in prospective life cycle assessment](https://onlinelibrary.wiley.com/doi/full/10.1111/jiec.13115). Journal of Industrial Ecology. **2021**


##Notes:

[Applied Sciences citation style](https://www.mdpi.com/journal/applsci/instructions) - Prep steps: start with Harvard citation style in [Google Scholar](https://scholar.google.com). Convert commas between names to semi-colons. Remove "and". Move year after the journal/conference name and make it bold.

