---
title: Principles for interoperable Information Packages
---
# 3. Principles for interoperable Information Packages
At the heart of any standardisation activity has to be a clear understanding of the needs and aims to be addressed. This is the goal of this Section which presents a series of high level principles to be applied to the detailed requirements delivered in Part II of this specification.

Most of the principles are motivated by the aim of interoperability, that is to say Information Packages should be easy to exchange, identify, validate and (re)use by a wide variety of software tools and systems.

Another crucial factor is long-term sustainability. Technical and semantic interoperability is possible only when a specific set of technologies have been agreed upon, implemented and tested. However, any technology will eventually become obsolete meaning previously agreed approaches have to be updated to accommodate emerging technologies and standards. Because of this, the developers of this Common Specification for Information Packages have endeavoured to reuse existing powerful, standardised and well-established best practices for the implementation of an Information Package (Part II of this document). This does not mean that the technical implementation details will not be subject to change in the future, but we anticipate that this will not happen in the immediate future. To achieve long-term sustainability of the Common Specification for Information Packages, we present a set of principles which must be followed when updating any specific implementation details.

The principles present a conceptual view of an Information Package, including a data model, and the use of data and metadata. An implementation that adheres to these principles is presented in Part II of this document.

Each principle has a number and a short description. The descriptions include a MoSCoW (MUST/MUST NOT, SHOULD/SHOULD NOT, COULD, WOULD) statement. The  description includes a rationale documenting the background and motivation for the principle.

## 3.1. General principles

### Principle 1.1
*It MUST be possible to include any data or metadata, regardless of its type or format, in a CS IP Information Package.*

This is one of the most crucial principles of the CS IP. In order to be truly “common”, technical implementations of the CS IP MUST NOT introduce limitations or restrictions which are only applicable to certain data or metadata types. If an Information Package implementation fails to meet this principle it is not possible to use it across different sectors and tools, thereby limiting practical interoperability.

### Principle 1.2:
*A CS IP Information Package MUST NOT restrict the means, methods or tools for exchanging it.*

Tools and methods for transferring Information Packages between locations are constantly evolving. It is also possible that different methods are preferred for packages of varying sizes. In order to achieve that a CS IP Information Package is truly interoperable across different platforms it therefore MUST NOT introduce limitations or restrictions which would be impossible to be met by specific information exchange tools or channels.

As such the CS IP does also not define the principle to use a particular transfer package or envelope. The scope of the CS IP is limited to the structure and requirements for data and metadata within the package. Different implementers are welcome to choose their own methods on top of the CS IP.

### Principle 1.3
*The CS IP MUST NOT define the scope of data and metadata which constitutes an Information Package.*

One of the fundamental principles of the CS IP is that it MUST allow each individual repository to define the (intellectual) scope of an Information Package and its relations to real life entities. As such, any implementation of the CS IP MUST be equally usable for packaging, for example, the whole content of an ERMS as an single IP; or for extracting each record and its metadata from the ERMS individually and packaging each as a separate IP.

Out of the previous we can also derive that a CS IP specification MUST NOT define that, for example, a SIP should conform to exactly one AIP. Instead the CS IP MUST allow for the inclusion of “anything that the implementer wants to define as a SIP, AIP or DIP” and allow for “any relationships (1-1; 1-n; n-1; n-m) between SIPs, AIPs and DIPs".

### Principle 1.4:
*A CS IP Information Package SHOULD be scalable.*

One of the practical concerns for Information Packages is their size. Many digital repositories have problems with data objects and metadata of increasing sizes, making it especially difficult to carry out tasks related to data or metadata validation, and identification and modification. For example, Information Packages including relational databases or born-digital 3D movies can easily reach TB sizes.

Consequently, any current or future implementation of the CS IP is required to provide for appropriate scalability mechanisms (for example: mechanisms for splitting large-scale data or metadata).

### Principle 1.5:
*A CS IP Information Package MUST be machine-readable*

To support the goal of automating ingest, preservation and access workflows each of the implementations of the CS IP must be machine-actionable. This means that decisions about the use of metadata syntax and semantics as well as the physical structure must be expressed explicitly and in a clear way. This, in turn, allows the specification to be implemented in the same way across different tools and environments.

### Principle 1.6:
*A CS IP Information Package SHOULD be human-readable*

In long-term preservation we also need to take into account that “forgotten” Information Packages might be found long after details about the implementation are gone and no tools to access the package are available. For these scenarios it is crucial to ensure that the structure and metadata of the Information Package are understandable with minimal effort by using simple tools like text editors and file viewers.

In practice this means that any implementation of the CS IP should ensure that folder and file naming conventions allow for the human identification of package components, and that the semantics of the package is explicit.

### Principle 1.7:
*A CS IP Information Package MUST support the preservation method best suited for the data.*

Different preservation institutions and different types of data need to use different methods for long-term preservation; migration and emulation being the most usual choices. A CS IP Information Package implementation MUST NOT prescribe the use of a specific preservation method but instead allow to document and/or add any data or metadata which is needed for any method.

## 3.2. Identification of the Information Package

### Principle 2.1:
*The Information Package type (SIP, AIP or DIP) MUST be clearly indicated.*

One of the first tasks in analysing any Information Package is to identify its current status in the overall archival process. Therefore, any Information Package must explicitly and uniformly include metadata which identifies it as a SIP, AIP or DIP.

### Principle 2.2:
*Any CS IP Information Package MUST clearly identify the Content Information Type(s) of its data and metadata.*

As stated in Principle 1.1 any CS IP Information Package MUST be able to include any kind of data and metadata. At the same time we have introduced in earlier Sections the concept of Content Information Types which allow users to achieve more detailed control and fine-grained interoperability. As such, any CS IP Information Package MUST include a statement about which Content Information Type specification(s) has been followed within the Information Package, or on the contrary, indicate clearly that no specific Content Information Type Specification has been followed.

The practical implication of principles 1.1, 2.1 and 2.2 is that, once these have been followed in implementations, we can in fact develop modular identification and validation tools and workflows. While generic components can carry out high level tasks regardless of the Content Information Type, it is possible to detect automatically which additional content-aware modules need to be executed.

### Principle 2.3:
*Any CS IP Information Package MUST bear an identifier which is unique and persistent within the repository.*

In order to manage a digital repository and provide access services each Information Package stored in the repository MUST be identified uniquely at least within the repository. At the same time a CS IP implementation MUST NOT limit the choice of the exact identification mechanism, as long as the mechanism is implemented consistently throughout the repository.

### Principle 2.4:
*Any CS IP Information Package SHOULD bear an identifier which is globally unique and persistent.*

In addition to the previous principle, it is recommended that the identification mechanism used at the repository provides for global uniqueness and persistence of Information Package IDs. The application of globally unique and persistent identifiers allows repositories to participate more easily in cross-institutional information exchange and reuse scenarios (for example participation in national or international portals, or cross-repository duplication of AIP preservation). However, the CS IP MUST NOT limit the choice of the exact identification mechanism.

### Principle 2.5:
*All components of a CS IP Information Package MUST bear an identifier which is unique and persistent within the repository.*

As stated above, a CS IP Information Package MUST be flexible enough to allow for the inclusion of any data or metadata depending on the needs of the repository and its users. As well, an Information Package might include additional support documentation like metadata schemas, user guidelines, contextual documentation etc. Regardless of which and how many components constitute a full Information Package, all components MUST bear a unique and persistent identifier which allows for the appropriate linking of data, metadata and all other components. This, in turn, is one of the most crucial aspects towards achieving an interoperable way towards maintaining package integrity.

It is also worth mentioning that in any implementation it is only necessary to achieve identifier uniqueness and persistence within an individual Information Package. If this is the case, repository-wide uniqueness is easily achieved when combining the package ID (unique according to principle 2.3) and the component ID.

The components of a CS IP Information Package are explained in more detail in the following section.

## 3.3 Structure of the Information Package

### Principle 3.1:
*A Common Specification Information Package MUST be built in such a way that its data and metadata can be logically separated from one another.*

At the highest level each Information Package can be divided into data and metadata. In order to minimise the effort needed for the identification and validation of both, and to simplify long-term preservation actions it is reasonable to clearly separate data and metadata. This allows, for example, ingest tools to streamline and separate metadata identification and validation tasks, and file format identification and normalisation. Throughout long-term preservation such a separation allows also The most crucial (MUST) aspect of such separation is that it is achieved on the logical level of the Information Package.

### Principle 3.2:
*A Common Specification Information Package SHOULD be structured so that data and metadata are separate from each other.*

In addition to the logical separation of components it is beneficial to have data and metadata physically separated (i.e. formatted as individual computer files or clearly separated bitstreams). This allows digital preservation tools and systems to update respective data or metadata portions of an Information Package without endangering the integrity of the whole package.

### Principle 3.3:
*The structure of an Information Package SHOULD allow for the separation of different types of metadata*

In addition to the previous principle it is recommended to explicitly divide metadata into more specific components. While the definitions of metadata types vary a lot between implementations it is our recommendation to divide metadata logically and physically at least into descriptive and preservation metadata.

### Principle 3.4:
*The structure of an Information Package MUST allow for the separation of data and/or metadata representations.*

The concept of representations is one of the fundamental building blocks in digital preservation. As technologies become obsolete, data and metadata is updated to ensure long-term accessibility, creating new versions and/or representations of the data and metadata as necessary.

Expressing representations within an Information Package helps institutions to understand the various states of the information throughout its lifecycle, therefore facilitating long-term management and reuse of the information.

### Principle 3.5:
*The structure of an Information Package MUST be freely extensible, allowing for additional components within the Information Package.*

In addition to data and metadata, institutions may wish to include additional components within an Information Package. The IP shouldn't restrict which components can constitute an Information Package. It must offer well defined extension points for the inclusion of additional components, which shouldn't affect other components (i.e. the extension points must be clearly separated from other components within the IP).

### Principle 3.6:
*An Information Package MUST follow a common conceptual structure regardless of its technical implementation.*

Based on principles 3.1 – 3.5 we now present a common structure for any CS IP Information Package ([Figure 7](#fig7)).

<a name="fig7"></a>
![Conceptual Structure](fig_7_cs_con_struct.png "Conceptual structure of the Common Specification")

**Figure 7:** Conceptual structure of the Common Specification

Principle 3.1 states that the package must include a high-level structural component for metadata. Representations must internally separate data and metadata. Note that the CSIP does not mandate that both data and metadata must be present in all representations.

Principle 3.2 recommends the separation of data and metadata.

Principle 3.3 recommends dividing the metadata in an Information Package by category.

Principle 3.4 separates the representations of data and metadata into separate components.

Principle 3.5 allows repositories and their users the possibility of adding additional components, e.g. schemas and supplementary documentation.

### Principle 3.7:
**TODO: Review and remove?**

*An Information Package MUST be expressed using only a single CSIP Implementation.*

The conceptual structure can be implemented in various ways – for example the components might be defined by accompanying package metadata or explicitly through a physical structure. However, it is not reasonable to have multiple implementations available at once as this would lead to unnecessary complexity in developing interoperable tools for creating, processing and managing Information Packages.

At the same time it is clear that any given technical implementation will become obsolete in time, for example as new transfer methods and storage solutions emerge. As such this requirement does not prohibit the take-up of any emerging logical of physical technical solutions but merely requires to have one and only one of these to be implemented at any given point in time.

At the time being, the CS IP  mandates a fixed physical folder structure (see Section 4) as the implementation of this and the previous requirements.

## 3.4 Information Package Metadata

### Principle 4.1:
*Metadata in an Information Package MUST be based on standards.*

In order to exchange, validate, process and reuse Information Packages in an interoperable and automated way we need to standardise how crucial metadata are presented in the package. “Crucial metadata”, is defined in this specification as the core information about how the package content has been created and managed (administrative and preservation metadata), explicit descriptions about of the structure of the package (structural metadata) and the technical details of the data themselves (technical metadata).

In order to ensure that these metadata are understood and implemented in a common and interoperable way in any Information Package, the use of established and widely used metadata standards is highly recommended. In the current implementation a large proportion of such metadata is covered by the widely used METS and PREMIS standards (see Section 5).

### Principle 4.2:
*Metadata standards used in an Information Package MUST be used consistently.*

Many metadata standards support multiple options for describing specific details of an Information Package. However, such interpretation possibilities can also lead to different implementations and ultimately to the loss of interoperability.

To overcome this risk the CS IP requires that, while developing a specific implementation, the chosen metadata standard MUST be reviewed in regard to potential ambiguity. If needed, the selected metadata standard MUST be further refined to meet the needs of interoperability and automation.

### Principle 4.3:
*An Information Package MUST allow the addition of supplementary metadata.*

The previous principles state the importance of strictly controlled administrative, preservation, structural and technical metadata for interoperability. This applies for other types of metadata, most prominently for resource discovery or specific technical and structural metadata. To encourage widespread adoption of the CSIP it must be possible for implementers to add arbitary metadata alongside the mandatory metadata components.

To summarise the requirements above from a more technical perspective, the CS IP adopts a modular approach towards Information Package metadata:

- All Information Packages share a common core of metadata which allows for the common development of high-level package creation, validation, identification and reuse tools;

- Further metadata in the Information Package might follow additional conventions. Metadata transferred to support specific tools, for example, tools to manage archival descriptions in EAD, or for specific Content Information Types like relational databases in the SIARD2 format.
