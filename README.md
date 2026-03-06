# Survey Data Analysis Toolkit

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.XXXXXXX.svg)](https://doi.org/10.5281/zenodo.XXXXXXX)

This repository contains the results for the Practical Exercises 1 and 2 of the "Scientific Paper of the Future" training.

## Practical Exercise 1: Software Preservation and Citation

This repository is documented following best practices for software sharing:
- **License**: MIT License.
- **Metadata**: [codemeta.json](codemeta.json) provides machine-readable metadata.
- **Citation**: See the Citation section below.
- **DOI**: A DOI will be assigned by Zenodo upon the first tagged release.

## Practical Exercise 2: Representing Provenance

The provenance of the survey results is represented in the [provenance.prov](provenance.prov) file and the diagram below.

### Provenance Diagram (Mermaid)

```mermaid
graph TD
    subgraph Agents
        Laura[Laura: Researcher]
        Jack[Jack: Surveyor]
        Jill[Jill: Surveyor]
        Peter[Peter: Surveyor]
        Paula[Paula: Surveyor]
        Zack[Zack: Analyst]
    end

    subgraph Entities
        SurveyV1[Survey v1]
        SurveyV2[Survey v2]
        Data1[Survey Data 1]
        Data2[Survey Data 2]
        Results[Statistical Analysis Results]
        Paper[Published Paper]
    end

    subgraph Activities
        DesigningV1[Designing the survey]
        Conducting1[Conducting survey 1]
        Revising[Revising the survey]
        Conducting2[Conducting survey 2]
        Analyzing[Analyzing data]
        Publishing[Writing and publishing]
    end

    Laura --> DesigningV1
    DesigningV1 --> SurveyV1
    SurveyV1 --> Conducting1
    Jack --> Conducting1
    Jill --> Conducting1
    Conducting1 --> Data1
    SurveyV1 --> Revising
    Laura --> Revising
    Revising --> SurveyV2
    SurveyV2 --> Conducting2
    Peter --> Conducting2
    Paula --> Conducting2
    Conducting2 --> Data2
    Data1 --> Analyzing
    Data2 --> Analyzing
    Zack --> Analyzing
    Analyzing --> Results
    Results --> Publishing
    Zack --> Publishing
    Laura --> Publishing
    Publishing --> Paper
```

## Citation

To cite this software, please use the following metadata:

Sami Abar. (2026). Survey Data Analysis Toolkit (v1.0.0). Zenodo. https://doi.org/10.5281/zenodo.XXXXXXX
