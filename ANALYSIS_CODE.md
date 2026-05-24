# Mermaid packages/ TypeScript ファイル分析

> 生成日: 2026-05-24  
> 対象: `packages/` 下のソース TypeScript ファイル（dist・.d.ts・テストを除く）

---

## 目次

- [packages/examples](#packagesexamples)
  - [packages/examples/src/examples/architecture.ts](#packagesexamplessrcexamplesarchitecturets)
  - [packages/examples/src/examples/block.ts](#packagesexamplessrcexamplesblockts)
  - [packages/examples/src/examples/c4.ts](#packagesexamplessrcexamplesc4ts)
  - [packages/examples/src/examples/class.ts](#packagesexamplessrcexamplesclassts)
  - [packages/examples/src/examples/cynefin.ts](#packagesexamplessrcexamplescynefints)
  - [packages/examples/src/examples/er.ts](#packagesexamplessrcexampleserts)
  - [packages/examples/src/examples/eventmodeling.ts](#packagesexamplessrcexampleseventmodelingts)
  - [packages/examples/src/examples/flowchart.ts](#packagesexamplessrcexamplesflowchartts)
  - [packages/examples/src/examples/gantt.ts](#packagesexamplessrcexamplesganttts)
  - [packages/examples/src/examples/git.ts](#packagesexamplessrcexamplesgitts)
  - [packages/examples/src/examples/ishikawa.ts](#packagesexamplessrcexamplesishikawats)
  - [packages/examples/src/examples/kanban.ts](#packagesexamplessrcexampleskanbants)
  - [packages/examples/src/examples/mindmap.ts](#packagesexamplessrcexamplesmindmapts)
  - [packages/examples/src/examples/packet.ts](#packagesexamplessrcexamplespacketts)
  - [packages/examples/src/examples/pie.ts](#packagesexamplessrcexamplespiets)
  - [packages/examples/src/examples/quadrant-chart.ts](#packagesexamplessrcexamplesquadrant-chartts)
  - [packages/examples/src/examples/radar.ts](#packagesexamplessrcexamplesradarts)
  - [packages/examples/src/examples/railroad-abnf.ts](#packagesexamplessrcexamplesrailroad-abnfts)
  - [packages/examples/src/examples/railroad-ebnf.ts](#packagesexamplessrcexamplesrailroad-ebnfts)
  - [packages/examples/src/examples/railroad-peg.ts](#packagesexamplessrcexamplesrailroad-pegts)
  - [packages/examples/src/examples/railroad.ts](#packagesexamplessrcexamplesrailroadts)
  - [packages/examples/src/examples/requirement.ts](#packagesexamplessrcexamplesrequirementts)
  - [packages/examples/src/examples/sankey.ts](#packagesexamplessrcexamplessankeyts)
  - [packages/examples/src/examples/sequence.ts](#packagesexamplessrcexamplessequencets)
  - [packages/examples/src/examples/state.ts](#packagesexamplessrcexamplesstatets)
  - [packages/examples/src/examples/timeline.ts](#packagesexamplessrcexamplestimelinets)
  - [packages/examples/src/examples/tree-view.ts](#packagesexamplessrcexamplestree-viewts)
  - [packages/examples/src/examples/treemap.ts](#packagesexamplessrcexamplestreemapts)
  - [packages/examples/src/examples/user-journey.ts](#packagesexamplessrcexamplesuser-journeyts)
  - [packages/examples/src/examples/venn.ts](#packagesexamplessrcexamplesvennts)
  - [packages/examples/src/examples/wardley.ts](#packagesexamplessrcexampleswardleyts)

- [packages/mermaid-example-diagram](#packagesmermaid-example-diagram)
  - [packages/mermaid-example-diagram/src/diagram-definition.ts](#packagesmermaid-example-diagramsrcdiagram-definitionts)
  - [packages/mermaid-example-diagram/src/detector.ts](#packagesmermaid-example-diagramsrcdetectorts)
  - [packages/mermaid-example-diagram/src/mermaidUtils.ts](#packagesmermaid-example-diagramsrcmermaidutilsts)

- [packages/mermaid-zenuml](#packagesmermaid-zenuml)
  - [packages/mermaid-zenuml/src/detector.ts](#packagesmermaid-zenumlsrcdetectorts)
  - [packages/mermaid-zenuml/src/mermaidUtils.ts](#packagesmermaid-zenumlsrcmermaidutilsts)
  - [packages/mermaid-zenuml/src/parser.ts](#packagesmermaid-zenumlsrcparserts)
  - [packages/mermaid-zenuml/src/zenuml-definition.ts](#packagesmermaid-zenumlsrczenuml-definitionts)
  - [packages/mermaid-zenuml/src/zenumlRenderer.ts](#packagesmermaid-zenumlsrczenumlrendererts)

- [packages/mermaid-layout-tidy-tree](#packagesmermaid-layout-tidy-tree)
  - [packages/mermaid-layout-tidy-tree/src/layouts.ts](#packagesmermaid-layout-tidy-treesrclayoutsts)
  - [packages/mermaid-layout-tidy-tree/src/layout.ts](#packagesmermaid-layout-tidy-treesrclayoutts)
  - [packages/mermaid-layout-tidy-tree/src/render.ts](#packagesmermaid-layout-tidy-treesrcrenderts)
  - [packages/mermaid-layout-tidy-tree/src/types.ts](#packagesmermaid-layout-tidy-treesrctypests)
  - [packages/mermaid-layout-tidy-tree/src/index.ts](#packagesmermaid-layout-tidy-treesrcindexts)

- [packages/mermaid-layout-elk](#packagesmermaid-layout-elk)
  - [packages/mermaid-layout-elk/src/index.ts](#packagesmermaid-layout-elksrcindexts)

- [packages/parser](#packagesparser)
  - [packages/parser/src/parse.ts](#packagesparsersrcparsets)
  - [packages/parser/src/index.ts](#packagesparsersrcindexts)
  - [packages/parser/scripts/prepack.ts](#packagesparserscriptsprepackts)
  - [packages/parser/tests/test-util.ts](#packagesparserteststest-utilts)
  - [packages/parser/tests/eventmodeling.test.ts](#packagesparsertestseventmodelingtestts)
  - [packages/parser/tests/radar.test.ts](#packagesparsertestsradartestts)
  - [packages/parser/tests/treeViewValueConverter.test.ts](#packagesparserteststreeviewvalueconvertertestts)
  - [packages/parser/tests/pie.test.ts](#packagesparsertestspietestts)
  - [packages/parser/tests/railroad.test.ts](#packagesparsertestsrailroadtestts)
  - [packages/parser/tests/architecture.test.ts](#packagesparsertestsarchitecturetestts)
  - [packages/parser/tests/packet.test.ts](#packagesparsertestspackettestts)
  - [packages/parser/tests/treeView.test.ts](#packagesparserteststreeviewtestts)
  - [packages/parser/tests/gitGraph.test.ts](#packagesparsertestsgitgraphtestts)
  - [packages/parser/tests/info.test.ts](#packagesparsertestsinfotestts)
  - [packages/parser/src/language/generated/ast.ts](#packagesparsersrclanguagegeneratedastts)
  - [packages/parser/src/language/generated/grammar.ts](#packagesparsersrclanguagegeneratedgrammarts)
  - [packages/parser/src/language/generated/module.ts](#packagesparsersrclanguagegeneratedmodulets)
  - [packages/parser/src/language/index.ts](#packagesparsersrclanguageindexts)
  - [packages/parser/src/language/common/matcher.ts](#packagesparsersrclanguagecommonmatcherts)
  - [packages/parser/src/language/common/tokenBuilder.ts](#packagesparsersrclanguagecommontokenbuilderts)
  - [packages/parser/src/language/common/valueConverter.ts](#packagesparsersrclanguagecommonvalueconverterts)
  - [packages/parser/src/language/architecture/module.ts](#packagesparsersrclanguagearchitecturemodulets)
  - [packages/parser/src/language/architecture/tokenBuilder.ts](#packagesparsersrclanguagearchitecturetokenbuilderts)
  - [packages/parser/src/language/architecture/valueConverter.ts](#packagesparsersrclanguagearchitecturevalueconverterts)
  - [packages/parser/src/language/cynefin/module.ts](#packagesparsersrclanguagecynefinmodulets)
  - [packages/parser/src/language/cynefin/tokenBuilder.ts](#packagesparsersrclanguagecynefintokenbuilderts)
  - [packages/parser/src/language/eventmodeling/event-modeling-validator.ts](#packagesparsersrclanguageeventmodelingevent-modeling-validatorts)
  - [packages/parser/src/language/eventmodeling/module.ts](#packagesparsersrclanguageeventmodelingmodulets)
  - [packages/parser/src/language/eventmodeling/tokenBuilder.ts](#packagesparsersrclanguageeventmodelingtokenbuilderts)
  - [packages/parser/src/language/gitGraph/module.ts](#packagesparsersrclanguagegitgraphmodulets)
  - [packages/parser/src/language/gitGraph/tokenBuilder.ts](#packagesparsersrclanguagegitgraphtokenbuilderts)
  - [packages/parser/src/language/info/module.ts](#packagesparsersrclanguageinfomodulets)
  - [packages/parser/src/language/packet/module.ts](#packagesparsersrclanguagepacketmodulets)
  - [packages/parser/src/language/pie/module.ts](#packagesparsersrclanguagepiemodulets)
  - [packages/parser/src/language/pie/valueConverter.ts](#packagesparsersrclanguagepievalueconverterts)
  - [packages/parser/src/language/radar/module.ts](#packagesparsersrclanguageradarmodulets)
  - [packages/parser/src/language/radar/tokenBuilder.ts](#packagesparsersrclanguageradartokenbuilderts)
  - [packages/parser/src/language/railroad/module.ts](#packagesparsersrclanguagerailroadmodulets)
  - [packages/parser/src/language/railroad/valueConverter.ts](#packagesparsersrclanguagerailroadvalueconverterts)
  - [packages/parser/src/language/railroad-ebnf/module.ts](#packagesparsersrclanguagerailroad-ebnfmodulets)
  - [packages/parser/src/language/railroad-ebnf/valueConverter.ts](#packagesparsersrclanguagerailroad-ebnfvalueconverterts)
  - [packages/parser/src/language/railroad-abnf/module.ts](#packagesparsersrclanguagerailroad-abnfmodulets)
  - [packages/parser/src/language/railroad-abnf/valueConverter.ts](#packagesparsersrclanguagerailroad-abnfvalueconverterts)
  - [packages/parser/src/language/railroad-peg/module.ts](#packagesparsersrclanguagerailroad-pegmodulets)
  - [packages/parser/src/language/railroad-peg/valueConverter.ts](#packagesparsersrclanguagerailroad-pegvalueconverterts)
  - [packages/parser/src/language/treeView/module.ts](#packagesparsersrclanguagetreeviewmodulets)
  - [packages/parser/src/language/treeView/tokenBuilder.ts](#packagesparsersrclanguagetreeviewtokenbuilderts)
  - [packages/parser/src/language/treeView/valueConverter.ts](#packagesparsersrclanguagetreeviewvalueconverterts)
  - [packages/parser/src/language/treemap/module.ts](#packagesparsersrclanguagetreemapmodulets)
  - [packages/parser/src/language/treemap/valueConverter.ts](#packagesparsersrclanguagetreemapvalueconverterts)
  - [packages/parser/src/language/treemap/treemap-validator.ts](#packagesparsersrclanguagetreemaptreemap-validatorts)
  - [packages/parser/src/language/wardley/module.ts](#packagesparsersrclanguagewardleymodulets)
  - [packages/parser/src/language/wardley/valueConverter.ts](#packagesparsersrclanguagewardleyvalueconverterts)

- [packages/mermaid — コア](#packagesmermaid-コア)
  - [packages/mermaid/src/Diagram.ts](#packagesmermaidsrcdiagramts)
  - [packages/mermaid/src/**mocks**/mermaidAPI.ts](#packagesmermaidsrcmocksmermaidapits)
  - [packages/mermaid/src/accessibility.ts](#packagesmermaidsrcaccessibilityts)
  - [packages/mermaid/src/assignWithDepth.ts](#packagesmermaidsrcassignwithdepthts)
  - [packages/mermaid/src/config.ts](#packagesmermaidsrcconfigts)
  - [packages/mermaid/src/config.type.ts](#packagesmermaidsrcconfigtypets)
  - [packages/mermaid/src/defaultConfig.ts](#packagesmermaidsrcdefaultconfigts)
  - [packages/mermaid/src/errors.ts](#packagesmermaidsrcerrorsts)
  - [packages/mermaid/src/interactionDb.ts](#packagesmermaidsrcinteractiondbts)
  - [packages/mermaid/src/internals.ts](#packagesmermaidsrcinternalsts)
  - [packages/mermaid/src/logger.ts](#packagesmermaidsrcloggerts)
  - [packages/mermaid/src/mermaid.ts](#packagesmermaidsrcmermaidts)
  - [packages/mermaid/src/mermaidAPI.ts](#packagesmermaidsrcmermaidapits)
  - [packages/mermaid/src/preprocess.ts](#packagesmermaidsrcpreprocessts)
  - [packages/mermaid/src/styles.ts](#packagesmermaidsrcstylests)
  - [packages/mermaid/src/types.ts](#packagesmermaidsrctypests)
  - [packages/mermaid/src/utils.ts](#packagesmermaidsrcutilsts)

- [packages/mermaid — diagram-api](#packagesmermaid-diagram-api)
  - [packages/mermaid/src/diagram-api/comments.ts](#packagesmermaidsrcdiagram-apicommentsts)
  - [packages/mermaid/src/diagram-api/detectType.ts](#packagesmermaidsrcdiagram-apidetecttypets)
  - [packages/mermaid/src/diagram-api/diagram-orchestration.ts](#packagesmermaidsrcdiagram-apidiagram-orchestrationts)
  - [packages/mermaid/src/diagram-api/diagramAPI.ts](#packagesmermaidsrcdiagram-apidiagramapits)
  - [packages/mermaid/src/diagram-api/frontmatter.ts](#packagesmermaidsrcdiagram-apifrontmatterts)
  - [packages/mermaid/src/diagram-api/loadDiagram.ts](#packagesmermaidsrcdiagram-apiloaddiagramts)
  - [packages/mermaid/src/diagram-api/regexes.ts](#packagesmermaidsrcdiagram-apiregexests)
  - [packages/mermaid/src/diagram-api/types.ts](#packagesmermaidsrcdiagram-apitypests)

- [packages/mermaid — dagre-wrapper](#packagesmermaid-dagre-wrapper)
  - [packages/mermaid/src/dagre-wrapper/blockArrowHelper.ts](#packagesmermaidsrcdagre-wrapperblockarrowhelperts)
  - [packages/mermaid/src/dagre-wrapper/edgeMarker.ts](#packagesmermaidsrcdagre-wrapperedgemarkerts)

- [packages/mermaid — diagrams/common](#packagesmermaid-diagramscommon)
  - [packages/mermaid/src/diagrams/common/common.ts](#packagesmermaidsrcdiagramscommoncommonts)
  - [packages/mermaid/src/diagrams/common/commonDb.ts](#packagesmermaidsrcdiagramscommoncommondbts)
  - [packages/mermaid/src/diagrams/common/commonTypes.ts](#packagesmermaidsrcdiagramscommoncommontypests)
  - [packages/mermaid/src/diagrams/common/populateCommonDb.ts](#packagesmermaidsrcdiagramscommonpopulatecommondbts)
  - [packages/mermaid/src/diagrams/common/svgDrawCommon.ts](#packagesmermaidsrcdiagramscommonsvgdrawcommonts)
  - [packages/mermaid/src/diagrams/globalStyles.ts](#packagesmermaidsrcdiagramsglobalstylests)

- [packages/mermaid — diagrams/architecture](#packagesmermaid-diagramsarchitecture)
  - [packages/mermaid/src/diagrams/architecture/architectureDb.ts](#packagesmermaidsrcdiagramsarchitecturearchitecturedbts)
  - [packages/mermaid/src/diagrams/architecture/architectureDetector.ts](#packagesmermaidsrcdiagramsarchitecturearchitecturedetectorts)
  - [packages/mermaid/src/diagrams/architecture/architectureDiagram.ts](#packagesmermaidsrcdiagramsarchitecturearchitecturediagramts)
  - [packages/mermaid/src/diagrams/architecture/architectureIcons.ts](#packagesmermaidsrcdiagramsarchitecturearchitectureiconsts)
  - [packages/mermaid/src/diagrams/architecture/architectureParser.ts](#packagesmermaidsrcdiagramsarchitecturearchitectureparserts)
  - [packages/mermaid/src/diagrams/architecture/architectureRenderer.ts](#packagesmermaidsrcdiagramsarchitecturearchitecturerendererts)
  - [packages/mermaid/src/diagrams/architecture/architectureStyles.ts](#packagesmermaidsrcdiagramsarchitecturearchitecturestylests)
  - [packages/mermaid/src/diagrams/architecture/architectureTypes.ts](#packagesmermaidsrcdiagramsarchitecturearchitecturetypests)
  - [packages/mermaid/src/diagrams/architecture/svgDraw.ts](#packagesmermaidsrcdiagramsarchitecturesvgdrawts)

- [packages/mermaid — diagrams/block](#packagesmermaid-diagramsblock)
  - [packages/mermaid/src/diagrams/block/blockDB.ts](#packagesmermaidsrcdiagramsblockblockdbts)
  - [packages/mermaid/src/diagrams/block/blockDetector.ts](#packagesmermaidsrcdiagramsblockblockdetectorts)
  - [packages/mermaid/src/diagrams/block/blockDiagram.ts](#packagesmermaidsrcdiagramsblockblockdiagramts)
  - [packages/mermaid/src/diagrams/block/blockRenderer.ts](#packagesmermaidsrcdiagramsblockblockrendererts)
  - [packages/mermaid/src/diagrams/block/blockTypes.ts](#packagesmermaidsrcdiagramsblockblocktypests)
  - [packages/mermaid/src/diagrams/block/blockUtils.ts](#packagesmermaidsrcdiagramsblockblockutilsts)
  - [packages/mermaid/src/diagrams/block/layout.ts](#packagesmermaidsrcdiagramsblocklayoutts)
  - [packages/mermaid/src/diagrams/block/renderHelpers.ts](#packagesmermaidsrcdiagramsblockrenderhelpersts)
  - [packages/mermaid/src/diagrams/block/styles.ts](#packagesmermaidsrcdiagramsblockstylests)

- [packages/mermaid — diagrams/c4](#packagesmermaid-diagramsc4)
  - [packages/mermaid/src/diagrams/c4/c4Detector.ts](#packagesmermaidsrcdiagramsc4c4detectorts)
  - [packages/mermaid/src/diagrams/c4/c4Diagram.ts](#packagesmermaidsrcdiagramsc4c4diagramts)

- [packages/mermaid — diagrams/class](#packagesmermaid-diagramsclass)
  - [packages/mermaid/src/diagrams/class/classDb.ts](#packagesmermaidsrcdiagramsclassclassdbts)
  - [packages/mermaid/src/diagrams/class/classDetector-V2.ts](#packagesmermaidsrcdiagramsclassclassdetector-v2ts)
  - [packages/mermaid/src/diagrams/class/classDetector.ts](#packagesmermaidsrcdiagramsclassclassdetectorts)
  - [packages/mermaid/src/diagrams/class/classDiagram-v2.ts](#packagesmermaidsrcdiagramsclassclassdiagram-v2ts)
  - [packages/mermaid/src/diagrams/class/classDiagram.ts](#packagesmermaidsrcdiagramsclassclassdiagramts)
  - [packages/mermaid/src/diagrams/class/classRenderer-v2.ts](#packagesmermaidsrcdiagramsclassclassrenderer-v2ts)
  - [packages/mermaid/src/diagrams/class/classRenderer-v3-unified.ts](#packagesmermaidsrcdiagramsclassclassrenderer-v3-unifiedts)
  - [packages/mermaid/src/diagrams/class/classTypes.ts](#packagesmermaidsrcdiagramsclassclasstypests)
  - [packages/mermaid/src/diagrams/class/shapeUtil.ts](#packagesmermaidsrcdiagramsclassshapeutilts)

- [packages/mermaid — diagrams/cynefin](#packagesmermaid-diagramscynefin)
  - [packages/mermaid/src/diagrams/cynefin/cynefinBoundaries.ts](#packagesmermaidsrcdiagramscynefincynefinboundariests)
  - [packages/mermaid/src/diagrams/cynefin/cynefinDb.ts](#packagesmermaidsrcdiagramscynefincynefindbts)
  - [packages/mermaid/src/diagrams/cynefin/cynefinDetector.ts](#packagesmermaidsrcdiagramscynefincynefindetectorts)
  - [packages/mermaid/src/diagrams/cynefin/cynefinDiagram.ts](#packagesmermaidsrcdiagramscynefincynefindiagramts)
  - [packages/mermaid/src/diagrams/cynefin/cynefinParser.ts](#packagesmermaidsrcdiagramscynefincynefinparserts)
  - [packages/mermaid/src/diagrams/cynefin/cynefinRenderer.ts](#packagesmermaidsrcdiagramscynefincynefinrendererts)
  - [packages/mermaid/src/diagrams/cynefin/styles.ts](#packagesmermaidsrcdiagramscynefinstylests)
  - [packages/mermaid/src/diagrams/cynefin/types.ts](#packagesmermaidsrcdiagramscynefintypests)

- [packages/mermaid — diagrams/er](#packagesmermaid-diagramser)
  - [packages/mermaid/src/diagrams/er/erDb.ts](#packagesmermaidsrcdiagramsererdbts)
  - [packages/mermaid/src/diagrams/er/erDetector.ts](#packagesmermaidsrcdiagramsererdetectorts)
  - [packages/mermaid/src/diagrams/er/erDiagram.ts](#packagesmermaidsrcdiagramsererdiagramts)
  - [packages/mermaid/src/diagrams/er/erRenderer-unified.ts](#packagesmermaidsrcdiagramsererrenderer-unifiedts)
  - [packages/mermaid/src/diagrams/er/erTypes.ts](#packagesmermaidsrcdiagramserertypests)
  - [packages/mermaid/src/diagrams/er/styles.ts](#packagesmermaidsrcdiagramserstylests)

- [packages/mermaid — diagrams/error](#packagesmermaid-diagramserror)
  - [packages/mermaid/src/diagrams/error/errorDiagram.ts](#packagesmermaidsrcdiagramserrorerrordiagramts)
  - [packages/mermaid/src/diagrams/error/errorRenderer.ts](#packagesmermaidsrcdiagramserrorerrorrendererts)

- [packages/mermaid — diagrams/eventmodeling](#packagesmermaid-diagramseventmodeling)
  - [packages/mermaid/src/diagrams/eventmodeling/db.ts](#packagesmermaidsrcdiagramseventmodelingdbts)
  - [packages/mermaid/src/diagrams/eventmodeling/detector.ts](#packagesmermaidsrcdiagramseventmodelingdetectorts)
  - [packages/mermaid/src/diagrams/eventmodeling/diagram.ts](#packagesmermaidsrcdiagramseventmodelingdiagramts)
  - [packages/mermaid/src/diagrams/eventmodeling/parser.ts](#packagesmermaidsrcdiagramseventmodelingparserts)
  - [packages/mermaid/src/diagrams/eventmodeling/renderer.ts](#packagesmermaidsrcdiagramseventmodelingrendererts)
  - [packages/mermaid/src/diagrams/eventmodeling/types.ts](#packagesmermaidsrcdiagramseventmodelingtypests)

- [packages/mermaid — diagrams/flowchart](#packagesmermaid-diagramsflowchart)
  - [packages/mermaid/src/diagrams/flowchart/elk/detector.ts](#packagesmermaidsrcdiagramsflowchartelkdetectorts)
  - [packages/mermaid/src/diagrams/flowchart/flowDb.ts](#packagesmermaidsrcdiagramsflowchartflowdbts)
  - [packages/mermaid/src/diagrams/flowchart/flowDetector-v2.ts](#packagesmermaidsrcdiagramsflowchartflowdetector-v2ts)
  - [packages/mermaid/src/diagrams/flowchart/flowDetector.ts](#packagesmermaidsrcdiagramsflowchartflowdetectorts)
  - [packages/mermaid/src/diagrams/flowchart/flowDiagram.ts](#packagesmermaidsrcdiagramsflowchartflowdiagramts)
  - [packages/mermaid/src/diagrams/flowchart/flowRenderer-v3-unified.ts](#packagesmermaidsrcdiagramsflowchartflowrenderer-v3-unifiedts)
  - [packages/mermaid/src/diagrams/flowchart/parser/flowParser.ts](#packagesmermaidsrcdiagramsflowchartparserflowparserts)
  - [packages/mermaid/src/diagrams/flowchart/styles.ts](#packagesmermaidsrcdiagramsflowchartstylests)
  - [packages/mermaid/src/diagrams/flowchart/types.ts](#packagesmermaidsrcdiagramsflowcharttypests)

- [packages/mermaid — diagrams/gantt](#packagesmermaid-diagramsgantt)
  - [packages/mermaid/src/diagrams/gantt/ganttDetector.ts](#packagesmermaidsrcdiagramsganttganttdetectorts)
  - [packages/mermaid/src/diagrams/gantt/ganttDiagram.ts](#packagesmermaidsrcdiagramsganttganttdiagramts)

- [packages/mermaid — diagrams/git](#packagesmermaid-diagramsgit)
  - [packages/mermaid/src/diagrams/git/gitGraphAst.ts](#packagesmermaidsrcdiagramsgitgitgraphastts)
  - [packages/mermaid/src/diagrams/git/gitGraphDetector.ts](#packagesmermaidsrcdiagramsgitgitgraphdetectorts)
  - [packages/mermaid/src/diagrams/git/gitGraphDiagram.ts](#packagesmermaidsrcdiagramsgitgitgraphdiagramts)
  - [packages/mermaid/src/diagrams/git/gitGraphParser.ts](#packagesmermaidsrcdiagramsgitgitgraphparserts)
  - [packages/mermaid/src/diagrams/git/gitGraphRenderer.ts](#packagesmermaidsrcdiagramsgitgitgraphrendererts)
  - [packages/mermaid/src/diagrams/git/gitGraphTypes.ts](#packagesmermaidsrcdiagramsgitgitgraphtypests)

- [packages/mermaid — diagrams/info](#packagesmermaid-diagramsinfo)
  - [packages/mermaid/src/diagrams/info/infoDb.ts](#packagesmermaidsrcdiagramsinfoinfodbts)
  - [packages/mermaid/src/diagrams/info/infoDetector.ts](#packagesmermaidsrcdiagramsinfoinfodetectorts)
  - [packages/mermaid/src/diagrams/info/infoDiagram.ts](#packagesmermaidsrcdiagramsinfoinfodiagramts)
  - [packages/mermaid/src/diagrams/info/infoParser.ts](#packagesmermaidsrcdiagramsinfoinfoparserts)
  - [packages/mermaid/src/diagrams/info/infoRenderer.ts](#packagesmermaidsrcdiagramsinfoinforendererts)
  - [packages/mermaid/src/diagrams/info/infoTypes.ts](#packagesmermaidsrcdiagramsinfoinfotypests)

- [packages/mermaid — diagrams/ishikawa](#packagesmermaid-diagramsishikawa)
  - [packages/mermaid/src/diagrams/ishikawa/ishikawaDb.ts](#packagesmermaidsrcdiagramsishikawaishikawadbts)
  - [packages/mermaid/src/diagrams/ishikawa/ishikawaDetector.ts](#packagesmermaidsrcdiagramsishikawaishikawadetectorts)
  - [packages/mermaid/src/diagrams/ishikawa/ishikawaDiagram.ts](#packagesmermaidsrcdiagramsishikawaishikawadiagramts)
  - [packages/mermaid/src/diagrams/ishikawa/ishikawaRenderer.ts](#packagesmermaidsrcdiagramsishikawaishikawarendererts)
  - [packages/mermaid/src/diagrams/ishikawa/ishikawaStyles.ts](#packagesmermaidsrcdiagramsishikawaishikawastylests)
  - [packages/mermaid/src/diagrams/ishikawa/ishikawaTypes.ts](#packagesmermaidsrcdiagramsishikawaishikawatypests)

- [packages/mermaid — diagrams/kanban](#packagesmermaid-diagramskanban)
  - [packages/mermaid/src/diagrams/kanban/detector.ts](#packagesmermaidsrcdiagramskanbandetectorts)
  - [packages/mermaid/src/diagrams/kanban/kanban-definition.ts](#packagesmermaidsrcdiagramskanbankanban-definitionts)
  - [packages/mermaid/src/diagrams/kanban/kanbanDb.ts](#packagesmermaidsrcdiagramskanbankanbandbts)
  - [packages/mermaid/src/diagrams/kanban/kanbanRenderer.ts](#packagesmermaidsrcdiagramskanbankanbanrendererts)
  - [packages/mermaid/src/diagrams/kanban/kanbanTypes.ts](#packagesmermaidsrcdiagramskanbankanbantypests)
  - [packages/mermaid/src/diagrams/kanban/styles.ts](#packagesmermaidsrcdiagramskanbanstylests)

- [packages/mermaid — diagrams/mindmap](#packagesmermaid-diagramsmindmap)
  - [packages/mermaid/src/diagrams/mindmap/detector.ts](#packagesmermaidsrcdiagramsmindmapdetectorts)
  - [packages/mermaid/src/diagrams/mindmap/mindmap-definition.ts](#packagesmermaidsrcdiagramsmindmapmindmap-definitionts)
  - [packages/mermaid/src/diagrams/mindmap/mindmapDb.ts](#packagesmermaidsrcdiagramsmindmapmindmapdbts)
  - [packages/mermaid/src/diagrams/mindmap/mindmapRenderer.ts](#packagesmermaidsrcdiagramsmindmapmindmaprendererts)
  - [packages/mermaid/src/diagrams/mindmap/mindmapTypes.ts](#packagesmermaidsrcdiagramsmindmapmindmaptypests)
  - [packages/mermaid/src/diagrams/mindmap/styles.ts](#packagesmermaidsrcdiagramsmindmapstylests)
  - [packages/mermaid/src/diagrams/mindmap/svgDraw.ts](#packagesmermaidsrcdiagramsmindmapsvgdrawts)

- [packages/mermaid — diagrams/packet](#packagesmermaid-diagramspacket)
  - [packages/mermaid/src/diagrams/packet/db.ts](#packagesmermaidsrcdiagramspacketdbts)
  - [packages/mermaid/src/diagrams/packet/detector.ts](#packagesmermaidsrcdiagramspacketdetectorts)
  - [packages/mermaid/src/diagrams/packet/diagram.ts](#packagesmermaidsrcdiagramspacketdiagramts)
  - [packages/mermaid/src/diagrams/packet/parser.ts](#packagesmermaidsrcdiagramspacketparserts)
  - [packages/mermaid/src/diagrams/packet/renderer.ts](#packagesmermaidsrcdiagramspacketrendererts)
  - [packages/mermaid/src/diagrams/packet/styles.ts](#packagesmermaidsrcdiagramspacketstylests)
  - [packages/mermaid/src/diagrams/packet/types.ts](#packagesmermaidsrcdiagramspackettypests)

- [packages/mermaid — diagrams/pie](#packagesmermaid-diagramspie)
  - [packages/mermaid/src/diagrams/pie/pieDb.ts](#packagesmermaidsrcdiagramspiepiedbts)
  - [packages/mermaid/src/diagrams/pie/pieDetector.ts](#packagesmermaidsrcdiagramspiepiedetectorts)
  - [packages/mermaid/src/diagrams/pie/pieDiagram.ts](#packagesmermaidsrcdiagramspiepiediagramts)
  - [packages/mermaid/src/diagrams/pie/pieParser.ts](#packagesmermaidsrcdiagramspiepieparserts)
  - [packages/mermaid/src/diagrams/pie/pieRenderer.ts](#packagesmermaidsrcdiagramspiepierendererts)
  - [packages/mermaid/src/diagrams/pie/pieStyles.ts](#packagesmermaidsrcdiagramspiepiestylests)
  - [packages/mermaid/src/diagrams/pie/pieTypes.ts](#packagesmermaidsrcdiagramspiepietypests)

- [packages/mermaid — diagrams/quadrant-chart](#packagesmermaid-diagramsquadrant-chart)
  - [packages/mermaid/src/diagrams/quadrant-chart/quadrantBuilder.ts](#packagesmermaidsrcdiagramsquadrant-chartquadrantbuilderts)
  - [packages/mermaid/src/diagrams/quadrant-chart/quadrantDb.ts](#packagesmermaidsrcdiagramsquadrant-chartquadrantdbts)
  - [packages/mermaid/src/diagrams/quadrant-chart/quadrantDetector.ts](#packagesmermaidsrcdiagramsquadrant-chartquadrantdetectorts)
  - [packages/mermaid/src/diagrams/quadrant-chart/quadrantDiagram.ts](#packagesmermaidsrcdiagramsquadrant-chartquadrantdiagramts)
  - [packages/mermaid/src/diagrams/quadrant-chart/quadrantRenderer.ts](#packagesmermaidsrcdiagramsquadrant-chartquadrantrendererts)
  - [packages/mermaid/src/diagrams/quadrant-chart/utils.ts](#packagesmermaidsrcdiagramsquadrant-chartutilsts)

- [packages/mermaid — diagrams/radar](#packagesmermaid-diagramsradar)
  - [packages/mermaid/src/diagrams/radar/db.ts](#packagesmermaidsrcdiagramsradardbts)
  - [packages/mermaid/src/diagrams/radar/detector.ts](#packagesmermaidsrcdiagramsradardetectorts)
  - [packages/mermaid/src/diagrams/radar/diagram.ts](#packagesmermaidsrcdiagramsradardiagramts)
  - [packages/mermaid/src/diagrams/radar/parser.ts](#packagesmermaidsrcdiagramsradarparserts)
  - [packages/mermaid/src/diagrams/radar/renderer.ts](#packagesmermaidsrcdiagramsradarrendererts)
  - [packages/mermaid/src/diagrams/radar/styles.ts](#packagesmermaidsrcdiagramsradarstylests)
  - [packages/mermaid/src/diagrams/radar/types.ts](#packagesmermaidsrcdiagramsradartypests)

- [packages/mermaid — diagrams/railroad](#packagesmermaid-diagramsrailroad)
  - [packages/mermaid/src/diagrams/railroad/abnfDetector.ts](#packagesmermaidsrcdiagramsrailroadabnfdetectorts)
  - [packages/mermaid/src/diagrams/railroad/abnfDiagram.ts](#packagesmermaidsrcdiagramsrailroadabnfdiagramts)
  - [packages/mermaid/src/diagrams/railroad/ebnfDetector.ts](#packagesmermaidsrcdiagramsrailroadebnfdetectorts)
  - [packages/mermaid/src/diagrams/railroad/ebnfDiagram.ts](#packagesmermaidsrcdiagramsrailroadebnfdiagramts)
  - [packages/mermaid/src/diagrams/railroad/parser/abnfParser.ts](#packagesmermaidsrcdiagramsrailroadparserabnfparserts)
  - [packages/mermaid/src/diagrams/railroad/parser/ebnfParser.ts](#packagesmermaidsrcdiagramsrailroadparserebnfparserts)
  - [packages/mermaid/src/diagrams/railroad/parser/pegParser.ts](#packagesmermaidsrcdiagramsrailroadparserpegparserts)
  - [packages/mermaid/src/diagrams/railroad/parser/railroadParser.ts](#packagesmermaidsrcdiagramsrailroadparserrailroadparserts)
  - [packages/mermaid/src/diagrams/railroad/pegDetector.ts](#packagesmermaidsrcdiagramsrailroadpegdetectorts)
  - [packages/mermaid/src/diagrams/railroad/pegDiagram.ts](#packagesmermaidsrcdiagramsrailroadpegdiagramts)
  - [packages/mermaid/src/diagrams/railroad/railroadDb.ts](#packagesmermaidsrcdiagramsrailroadrailroaddbts)
  - [packages/mermaid/src/diagrams/railroad/railroadDetector.ts](#packagesmermaidsrcdiagramsrailroadrailroaddetectorts)
  - [packages/mermaid/src/diagrams/railroad/railroadDiagram.ts](#packagesmermaidsrcdiagramsrailroadrailroaddiagramts)
  - [packages/mermaid/src/diagrams/railroad/railroadRenderer.ts](#packagesmermaidsrcdiagramsrailroadrailroadrendererts)
  - [packages/mermaid/src/diagrams/railroad/railroadTypes.ts](#packagesmermaidsrcdiagramsrailroadrailroadtypests)
  - [packages/mermaid/src/diagrams/railroad/styles.ts](#packagesmermaidsrcdiagramsrailroadstylests)

- [packages/mermaid — diagrams/requirement](#packagesmermaid-diagramsrequirement)
  - [packages/mermaid/src/diagrams/requirement/requirementDb.ts](#packagesmermaidsrcdiagramsrequirementrequirementdbts)
  - [packages/mermaid/src/diagrams/requirement/requirementDetector.ts](#packagesmermaidsrcdiagramsrequirementrequirementdetectorts)
  - [packages/mermaid/src/diagrams/requirement/requirementDiagram.ts](#packagesmermaidsrcdiagramsrequirementrequirementdiagramts)
  - [packages/mermaid/src/diagrams/requirement/requirementRenderer.ts](#packagesmermaidsrcdiagramsrequirementrequirementrendererts)
  - [packages/mermaid/src/diagrams/requirement/types.ts](#packagesmermaidsrcdiagramsrequirementtypests)

- [packages/mermaid — diagrams/sankey](#packagesmermaid-diagramssankey)
  - [packages/mermaid/src/diagrams/sankey/sankeyDB.ts](#packagesmermaidsrcdiagramssankeysankeydbts)
  - [packages/mermaid/src/diagrams/sankey/sankeyDetector.ts](#packagesmermaidsrcdiagramssankeysankeydetectorts)
  - [packages/mermaid/src/diagrams/sankey/sankeyDiagram.ts](#packagesmermaidsrcdiagramssankeysankeydiagramts)
  - [packages/mermaid/src/diagrams/sankey/sankeyRenderer.ts](#packagesmermaidsrcdiagramssankeysankeyrendererts)
  - [packages/mermaid/src/diagrams/sankey/sankeyUtils.ts](#packagesmermaidsrcdiagramssankeysankeyutilsts)

- [packages/mermaid — diagrams/sequence](#packagesmermaid-diagramssequence)
  - [packages/mermaid/src/diagrams/sequence/sequenceDb.ts](#packagesmermaidsrcdiagramssequencesequencedbts)
  - [packages/mermaid/src/diagrams/sequence/sequenceDetector.ts](#packagesmermaidsrcdiagramssequencesequencedetectorts)
  - [packages/mermaid/src/diagrams/sequence/sequenceDiagram.ts](#packagesmermaidsrcdiagramssequencesequencediagramts)
  - [packages/mermaid/src/diagrams/sequence/sequenceRenderer.ts](#packagesmermaidsrcdiagramssequencesequencerendererts)
  - [packages/mermaid/src/diagrams/sequence/types.ts](#packagesmermaidsrcdiagramssequencetypests)

- [packages/mermaid — diagrams/state](#packagesmermaid-diagramsstate)
  - [packages/mermaid/src/diagrams/state/dataFetcher.ts](#packagesmermaidsrcdiagramsstatedatafetcherts)
  - [packages/mermaid/src/diagrams/state/stateCommon.ts](#packagesmermaidsrcdiagramsstatestatecommonts)
  - [packages/mermaid/src/diagrams/state/stateDb.ts](#packagesmermaidsrcdiagramsstatestatedbts)
  - [packages/mermaid/src/diagrams/state/stateDetector-V2.ts](#packagesmermaidsrcdiagramsstatestatedetector-v2ts)
  - [packages/mermaid/src/diagrams/state/stateDetector.ts](#packagesmermaidsrcdiagramsstatestatedetectorts)
  - [packages/mermaid/src/diagrams/state/stateDiagram-v2.ts](#packagesmermaidsrcdiagramsstatestatediagram-v2ts)
  - [packages/mermaid/src/diagrams/state/stateDiagram.ts](#packagesmermaidsrcdiagramsstatestatediagramts)
  - [packages/mermaid/src/diagrams/state/stateRenderer-v3-unified.ts](#packagesmermaidsrcdiagramsstatestaterenderer-v3-unifiedts)

- [packages/mermaid — diagrams/timeline](#packagesmermaid-diagramstimeline)
  - [packages/mermaid/src/diagrams/timeline/detector.ts](#packagesmermaidsrcdiagramstimelinedetectorts)
  - [packages/mermaid/src/diagrams/timeline/timeline-definition.ts](#packagesmermaidsrcdiagramstimelinetimeline-definitionts)
  - [packages/mermaid/src/diagrams/timeline/timelineRenderer.ts](#packagesmermaidsrcdiagramstimelinetimelinerendererts)
  - [packages/mermaid/src/diagrams/timeline/timelineRendererVertical.ts](#packagesmermaidsrcdiagramstimelinetimelinerendererverticalts)

- [packages/mermaid — diagrams/treeView](#packagesmermaid-diagramstreeview)
  - [packages/mermaid/src/diagrams/treeView/boxDrawingPreprocessor.ts](#packagesmermaidsrcdiagramstreeviewboxdrawingpreprocessorts)
  - [packages/mermaid/src/diagrams/treeView/db.ts](#packagesmermaidsrcdiagramstreeviewdbts)
  - [packages/mermaid/src/diagrams/treeView/detector.ts](#packagesmermaidsrcdiagramstreeviewdetectorts)
  - [packages/mermaid/src/diagrams/treeView/diagram.ts](#packagesmermaidsrcdiagramstreeviewdiagramts)
  - [packages/mermaid/src/diagrams/treeView/icons.ts](#packagesmermaidsrcdiagramstreeviewiconsts)
  - [packages/mermaid/src/diagrams/treeView/parser.ts](#packagesmermaidsrcdiagramstreeviewparserts)
  - [packages/mermaid/src/diagrams/treeView/renderer.ts](#packagesmermaidsrcdiagramstreeviewrendererts)
  - [packages/mermaid/src/diagrams/treeView/styles.ts](#packagesmermaidsrcdiagramstreeviewstylests)
  - [packages/mermaid/src/diagrams/treeView/types.ts](#packagesmermaidsrcdiagramstreeviewtypests)

- [packages/mermaid — diagrams/treemap](#packagesmermaid-diagramstreemap)
  - [packages/mermaid/src/diagrams/treemap/db.ts](#packagesmermaidsrcdiagramstreemapdbts)
  - [packages/mermaid/src/diagrams/treemap/detector.ts](#packagesmermaidsrcdiagramstreemapdetectorts)
  - [packages/mermaid/src/diagrams/treemap/diagram.ts](#packagesmermaidsrcdiagramstreemapdiagramts)
  - [packages/mermaid/src/diagrams/treemap/parser.ts](#packagesmermaidsrcdiagramstreemapparserts)
  - [packages/mermaid/src/diagrams/treemap/renderer.ts](#packagesmermaidsrcdiagramstreemaprendererts)
  - [packages/mermaid/src/diagrams/treemap/styles.ts](#packagesmermaidsrcdiagramstreemapstylests)
  - [packages/mermaid/src/diagrams/treemap/types.ts](#packagesmermaidsrcdiagramstreemaptypests)
  - [packages/mermaid/src/diagrams/treemap/utils.ts](#packagesmermaidsrcdiagramstreemaputilsts)

- [packages/mermaid — diagrams/user-journey](#packagesmermaid-diagramsuser-journey)
  - [packages/mermaid/src/diagrams/user-journey/journeyDetector.ts](#packagesmermaidsrcdiagramsuser-journeyjourneydetectorts)
  - [packages/mermaid/src/diagrams/user-journey/journeyDiagram.ts](#packagesmermaidsrcdiagramsuser-journeyjourneydiagramts)
  - [packages/mermaid/src/diagrams/user-journey/journeyRenderer.ts](#packagesmermaidsrcdiagramsuser-journeyjourneyrendererts)

- [packages/mermaid — diagrams/venn](#packagesmermaid-diagramsvenn)
  - [packages/mermaid/src/diagrams/venn/styles.ts](#packagesmermaidsrcdiagramsvennstylests)
  - [packages/mermaid/src/diagrams/venn/vennDB.ts](#packagesmermaidsrcdiagramsvennvenndbts)
  - [packages/mermaid/src/diagrams/venn/vennDetector.ts](#packagesmermaidsrcdiagramsvennvenndetectorts)
  - [packages/mermaid/src/diagrams/venn/vennDiagram.ts](#packagesmermaidsrcdiagramsvennvenndiagramts)
  - [packages/mermaid/src/diagrams/venn/vennRenderer.ts](#packagesmermaidsrcdiagramsvennvennrendererts)
  - [packages/mermaid/src/diagrams/venn/vennTypes.ts](#packagesmermaidsrcdiagramsvennvenntypests)

- [packages/mermaid — diagrams/wardley](#packagesmermaid-diagramswardley)
  - [packages/mermaid/src/diagrams/wardley/styles.ts](#packagesmermaidsrcdiagramswardleystylests)
  - [packages/mermaid/src/diagrams/wardley/wardleyBuilder.ts](#packagesmermaidsrcdiagramswardleywardleybuilderts)
  - [packages/mermaid/src/diagrams/wardley/wardleyDb.ts](#packagesmermaidsrcdiagramswardleywardleydbts)
  - [packages/mermaid/src/diagrams/wardley/wardleyDetector.ts](#packagesmermaidsrcdiagramswardleywardleydetectorts)
  - [packages/mermaid/src/diagrams/wardley/wardleyDiagram.ts](#packagesmermaidsrcdiagramswardleywardleydiagramts)
  - [packages/mermaid/src/diagrams/wardley/wardleyParser.ts](#packagesmermaidsrcdiagramswardleywardleyparserts)
  - [packages/mermaid/src/diagrams/wardley/wardleyRenderer.ts](#packagesmermaidsrcdiagramswardleywardleyrendererts)
  - [packages/mermaid/src/diagrams/wardley/wardleyTypes.ts](#packagesmermaidsrcdiagramswardleywardleytypests)

- [packages/mermaid — diagrams/xychart](#packagesmermaid-diagramsxychart)
  - [packages/mermaid/src/diagrams/xychart/chartBuilder/components/axis/bandAxis.ts](#packagesmermaidsrcdiagramsxychartchartbuildercomponentsaxisbandaxists)
  - [packages/mermaid/src/diagrams/xychart/chartBuilder/components/axis/baseAxis.ts](#packagesmermaidsrcdiagramsxychartchartbuildercomponentsaxisbaseaxists)
  - [packages/mermaid/src/diagrams/xychart/chartBuilder/components/axis/index.ts](#packagesmermaidsrcdiagramsxychartchartbuildercomponentsaxisindexts)
  - [packages/mermaid/src/diagrams/xychart/chartBuilder/components/axis/linearAxis.ts](#packagesmermaidsrcdiagramsxychartchartbuildercomponentsaxislinearaxists)
  - [packages/mermaid/src/diagrams/xychart/chartBuilder/components/chartTitle.ts](#packagesmermaidsrcdiagramsxychartchartbuildercomponentscharttitlets)
  - [packages/mermaid/src/diagrams/xychart/chartBuilder/components/plot/barPlot.ts](#packagesmermaidsrcdiagramsxychartchartbuildercomponentsplotbarplotts)
  - [packages/mermaid/src/diagrams/xychart/chartBuilder/components/plot/index.ts](#packagesmermaidsrcdiagramsxychartchartbuildercomponentsplotindexts)
  - [packages/mermaid/src/diagrams/xychart/chartBuilder/components/plot/linePlot.ts](#packagesmermaidsrcdiagramsxychartchartbuildercomponentsplotlineplotts)
  - [packages/mermaid/src/diagrams/xychart/chartBuilder/index.ts](#packagesmermaidsrcdiagramsxychartchartbuilderindexts)
  - [packages/mermaid/src/diagrams/xychart/chartBuilder/interfaces.ts](#packagesmermaidsrcdiagramsxychartchartbuilderinterfacests)
  - [packages/mermaid/src/diagrams/xychart/chartBuilder/orchestrator.ts](#packagesmermaidsrcdiagramsxychartchartbuilderorchestratorts)
  - [packages/mermaid/src/diagrams/xychart/chartBuilder/textDimensionCalculator.ts](#packagesmermaidsrcdiagramsxychartchartbuildertextdimensioncalculatorts)
  - [packages/mermaid/src/diagrams/xychart/xychartDb.ts](#packagesmermaidsrcdiagramsxychartxychartdbts)
  - [packages/mermaid/src/diagrams/xychart/xychartDetector.ts](#packagesmermaidsrcdiagramsxychartxychartdetectorts)
  - [packages/mermaid/src/diagrams/xychart/xychartDiagram.ts](#packagesmermaidsrcdiagramsxychartxychartdiagramts)
  - [packages/mermaid/src/diagrams/xychart/xychartRenderer.ts](#packagesmermaidsrcdiagramsxychartxychartrendererts)

- [packages/mermaid — rendering-util](#packagesmermaid-rendering-util)
  - [packages/mermaid/src/rendering-util/createText.ts](#packagesmermaidsrcrendering-utilcreatetextts)
  - [packages/mermaid/src/rendering-util/handle-markdown-text.ts](#packagesmermaidsrcrendering-utilhandle-markdown-textts)
  - [packages/mermaid/src/rendering-util/icons.ts](#packagesmermaidsrcrendering-utiliconsts)
  - [packages/mermaid/src/rendering-util/labelTransform.ts](#packagesmermaidsrcrendering-utillabeltransformts)
  - [packages/mermaid/src/rendering-util/layout-algorithms/cose-bilkent/cytoscape-setup.ts](#packagesmermaidsrcrendering-utillayout-algorithmscose-bilkentcytoscape-setupts)
  - [packages/mermaid/src/rendering-util/layout-algorithms/cose-bilkent/index.ts](#packagesmermaidsrcrendering-utillayout-algorithmscose-bilkentindexts)
  - [packages/mermaid/src/rendering-util/layout-algorithms/cose-bilkent/layout.ts](#packagesmermaidsrcrendering-utillayout-algorithmscose-bilkentlayoutts)
  - [packages/mermaid/src/rendering-util/layout-algorithms/cose-bilkent/render.ts](#packagesmermaidsrcrendering-utillayout-algorithmscose-bilkentrenderts)
  - [packages/mermaid/src/rendering-util/layout-algorithms/cose-bilkent/types.ts](#packagesmermaidsrcrendering-utillayout-algorithmscose-bilkenttypests)
  - [packages/mermaid/src/rendering-util/render.ts](#packagesmermaidsrcrendering-utilrenderts)
  - [packages/mermaid/src/rendering-util/rendering-elements/edgeMarker.ts](#packagesmermaidsrcrendering-utilrendering-elementsedgemarkerts)
  - [packages/mermaid/src/rendering-util/rendering-elements/nodes.ts](#packagesmermaidsrcrendering-utilrendering-elementsnodests)
  - [packages/mermaid/src/rendering-util/rendering-elements/shapes.ts](#packagesmermaidsrcrendering-utilrendering-elementsshapests)
  - [packages/mermaid/src/rendering-util/rendering-elements/shapes/anchor.ts](#packagesmermaidsrcrendering-utilrendering-elementsshapesanchorts)
  - [packages/mermaid/src/rendering-util/rendering-elements/shapes/bang.ts](#packagesmermaidsrcrendering-utilrendering-elementsshapesbangts)
  - [packages/mermaid/src/rendering-util/rendering-elements/shapes/bowTieRect.ts](#packagesmermaidsrcrendering-utilrendering-elementsshapesbowtierectts)
  - [packages/mermaid/src/rendering-util/rendering-elements/shapes/card.ts](#packagesmermaidsrcrendering-utilrendering-elementsshapescardts)
  - [packages/mermaid/src/rendering-util/rendering-elements/shapes/choice.ts](#packagesmermaidsrcrendering-utilrendering-elementsshapeschoicets)
  - [packages/mermaid/src/rendering-util/rendering-elements/shapes/circle.ts](#packagesmermaidsrcrendering-utilrendering-elementsshapescirclets)
  - [packages/mermaid/src/rendering-util/rendering-elements/shapes/classBox.ts](#packagesmermaidsrcrendering-utilrendering-elementsshapesclassboxts)
  - [packages/mermaid/src/rendering-util/rendering-elements/shapes/cloud.ts](#packagesmermaidsrcrendering-utilrendering-elementsshapescloudts)
  - [packages/mermaid/src/rendering-util/rendering-elements/shapes/crossedCircle.ts](#packagesmermaidsrcrendering-utilrendering-elementsshapescrossedcirclets)
  - [packages/mermaid/src/rendering-util/rendering-elements/shapes/curlyBraceLeft.ts](#packagesmermaidsrcrendering-utilrendering-elementsshapescurlybraceleftts)
  - [packages/mermaid/src/rendering-util/rendering-elements/shapes/curlyBraceRight.ts](#packagesmermaidsrcrendering-utilrendering-elementsshapescurlybracerightts)
  - [packages/mermaid/src/rendering-util/rendering-elements/shapes/curlyBraces.ts](#packagesmermaidsrcrendering-utilrendering-elementsshapescurlybracests)
  - [packages/mermaid/src/rendering-util/rendering-elements/shapes/curvedTrapezoid.ts](#packagesmermaidsrcrendering-utilrendering-elementsshapescurvedtrapezoidts)
  - [packages/mermaid/src/rendering-util/rendering-elements/shapes/cylinder.ts](#packagesmermaidsrcrendering-utilrendering-elementsshapescylinderts)
  - [packages/mermaid/src/rendering-util/rendering-elements/shapes/datastore.ts](#packagesmermaidsrcrendering-utilrendering-elementsshapesdatastorets)
  - [packages/mermaid/src/rendering-util/rendering-elements/shapes/defaultMindmapNode.ts](#packagesmermaidsrcrendering-utilrendering-elementsshapesdefaultmindmapnodets)
  - [packages/mermaid/src/rendering-util/rendering-elements/shapes/dividedRect.ts](#packagesmermaidsrcrendering-utilrendering-elementsshapesdividedrectts)
  - [packages/mermaid/src/rendering-util/rendering-elements/shapes/document.ts](#packagesmermaidsrcrendering-utilrendering-elementsshapesdocumentts)
  - [packages/mermaid/src/rendering-util/rendering-elements/shapes/doubleCircle.ts](#packagesmermaidsrcrendering-utilrendering-elementsshapesdoublecirclets)
  - [packages/mermaid/src/rendering-util/rendering-elements/shapes/drawRect.ts](#packagesmermaidsrcrendering-utilrendering-elementsshapesdrawrectts)
  - [packages/mermaid/src/rendering-util/rendering-elements/shapes/erBox.ts](#packagesmermaidsrcrendering-utilrendering-elementsshapeserboxts)
  - [packages/mermaid/src/rendering-util/rendering-elements/shapes/filledCircle.ts](#packagesmermaidsrcrendering-utilrendering-elementsshapesfilledcirclets)
  - [packages/mermaid/src/rendering-util/rendering-elements/shapes/flippedTriangle.ts](#packagesmermaidsrcrendering-utilrendering-elementsshapesflippedtrianglets)
  - [packages/mermaid/src/rendering-util/rendering-elements/shapes/forkJoin.ts](#packagesmermaidsrcrendering-utilrendering-elementsshapesforkjoints)
  - [packages/mermaid/src/rendering-util/rendering-elements/shapes/halfRoundedRectangle.ts](#packagesmermaidsrcrendering-utilrendering-elementsshapeshalfroundedrectanglets)
  - [packages/mermaid/src/rendering-util/rendering-elements/shapes/handDrawnShapeStyles.ts](#packagesmermaidsrcrendering-utilrendering-elementsshapeshanddrawnshapestylests)
  - [packages/mermaid/src/rendering-util/rendering-elements/shapes/hexagon.ts](#packagesmermaidsrcrendering-utilrendering-elementsshapeshexagonts)
  - [packages/mermaid/src/rendering-util/rendering-elements/shapes/hourglass.ts](#packagesmermaidsrcrendering-utilrendering-elementsshapeshourglassts)
  - [packages/mermaid/src/rendering-util/rendering-elements/shapes/icon.ts](#packagesmermaidsrcrendering-utilrendering-elementsshapesiconts)
  - [packages/mermaid/src/rendering-util/rendering-elements/shapes/iconCircle.ts](#packagesmermaidsrcrendering-utilrendering-elementsshapesiconcirclets)
  - [packages/mermaid/src/rendering-util/rendering-elements/shapes/iconRounded.ts](#packagesmermaidsrcrendering-utilrendering-elementsshapesiconroundedts)
  - [packages/mermaid/src/rendering-util/rendering-elements/shapes/iconSquare.ts](#packagesmermaidsrcrendering-utilrendering-elementsshapesiconsquarets)
  - [packages/mermaid/src/rendering-util/rendering-elements/shapes/imageSquare.ts](#packagesmermaidsrcrendering-utilrendering-elementsshapesimagesquarets)
  - [packages/mermaid/src/rendering-util/rendering-elements/shapes/insertPolygonShape.ts](#packagesmermaidsrcrendering-utilrendering-elementsshapesinsertpolygonshapets)
  - [packages/mermaid/src/rendering-util/rendering-elements/shapes/invertedTrapezoid.ts](#packagesmermaidsrcrendering-utilrendering-elementsshapesinvertedtrapezoidts)
  - [packages/mermaid/src/rendering-util/rendering-elements/shapes/kanbanItem.ts](#packagesmermaidsrcrendering-utilrendering-elementsshapeskanbanitemts)
  - [packages/mermaid/src/rendering-util/rendering-elements/shapes/labelImageUtils.ts](#packagesmermaidsrcrendering-utilrendering-elementsshapeslabelimageutilsts)
  - [packages/mermaid/src/rendering-util/rendering-elements/shapes/labelRect.ts](#packagesmermaidsrcrendering-utilrendering-elementsshapeslabelrectts)
  - [packages/mermaid/src/rendering-util/rendering-elements/shapes/leanLeft.ts](#packagesmermaidsrcrendering-utilrendering-elementsshapesleanleftts)
  - [packages/mermaid/src/rendering-util/rendering-elements/shapes/leanRight.ts](#packagesmermaidsrcrendering-utilrendering-elementsshapesleanrightts)
  - [packages/mermaid/src/rendering-util/rendering-elements/shapes/lightningBolt.ts](#packagesmermaidsrcrendering-utilrendering-elementsshapeslightningboltts)
  - [packages/mermaid/src/rendering-util/rendering-elements/shapes/linedCylinder.ts](#packagesmermaidsrcrendering-utilrendering-elementsshapeslinedcylinderts)
  - [packages/mermaid/src/rendering-util/rendering-elements/shapes/linedWaveEdgedRect.ts](#packagesmermaidsrcrendering-utilrendering-elementsshapeslinedwaveedgedrectts)
  - [packages/mermaid/src/rendering-util/rendering-elements/shapes/mindmapCircle.ts](#packagesmermaidsrcrendering-utilrendering-elementsshapesmindmapcirclets)
  - [packages/mermaid/src/rendering-util/rendering-elements/shapes/multiRect.ts](#packagesmermaidsrcrendering-utilrendering-elementsshapesmultirectts)
  - [packages/mermaid/src/rendering-util/rendering-elements/shapes/multiWaveEdgedRectangle.ts](#packagesmermaidsrcrendering-utilrendering-elementsshapesmultiwaveedgedrectanglets)
  - [packages/mermaid/src/rendering-util/rendering-elements/shapes/note.ts](#packagesmermaidsrcrendering-utilrendering-elementsshapesnotets)
  - [packages/mermaid/src/rendering-util/rendering-elements/shapes/question.ts](#packagesmermaidsrcrendering-utilrendering-elementsshapesquestionts)
  - [packages/mermaid/src/rendering-util/rendering-elements/shapes/rectLeftInvArrow.ts](#packagesmermaidsrcrendering-utilrendering-elementsshapesrectleftinvarrowts)
  - [packages/mermaid/src/rendering-util/rendering-elements/shapes/rectWithTitle.ts](#packagesmermaidsrcrendering-utilrendering-elementsshapesrectwithtitlets)
  - [packages/mermaid/src/rendering-util/rendering-elements/shapes/requirementBox.ts](#packagesmermaidsrcrendering-utilrendering-elementsshapesrequirementboxts)
  - [packages/mermaid/src/rendering-util/rendering-elements/shapes/roundedRect.ts](#packagesmermaidsrcrendering-utilrendering-elementsshapesroundedrectts)
  - [packages/mermaid/src/rendering-util/rendering-elements/shapes/roundedRectPath.ts](#packagesmermaidsrcrendering-utilrendering-elementsshapesroundedrectpathts)
  - [packages/mermaid/src/rendering-util/rendering-elements/shapes/shadedProcess.ts](#packagesmermaidsrcrendering-utilrendering-elementsshapesshadedprocessts)
  - [packages/mermaid/src/rendering-util/rendering-elements/shapes/slopedRect.ts](#packagesmermaidsrcrendering-utilrendering-elementsshapesslopedrectts)
  - [packages/mermaid/src/rendering-util/rendering-elements/shapes/squareRect.ts](#packagesmermaidsrcrendering-utilrendering-elementsshapessquarerectts)
  - [packages/mermaid/src/rendering-util/rendering-elements/shapes/stadium.ts](#packagesmermaidsrcrendering-utilrendering-elementsshapesstadiumts)
  - [packages/mermaid/src/rendering-util/rendering-elements/shapes/state.ts](#packagesmermaidsrcrendering-utilrendering-elementsshapesstatets)
  - [packages/mermaid/src/rendering-util/rendering-elements/shapes/stateEnd.ts](#packagesmermaidsrcrendering-utilrendering-elementsshapesstateendts)
  - [packages/mermaid/src/rendering-util/rendering-elements/shapes/stateStart.ts](#packagesmermaidsrcrendering-utilrendering-elementsshapesstatestartts)
  - [packages/mermaid/src/rendering-util/rendering-elements/shapes/subroutine.ts](#packagesmermaidsrcrendering-utilrendering-elementsshapessubroutinets)
  - [packages/mermaid/src/rendering-util/rendering-elements/shapes/taggedRect.ts](#packagesmermaidsrcrendering-utilrendering-elementsshapestaggedrectts)
  - [packages/mermaid/src/rendering-util/rendering-elements/shapes/taggedWaveEdgedRectangle.ts](#packagesmermaidsrcrendering-utilrendering-elementsshapestaggedwaveedgedrectanglets)
  - [packages/mermaid/src/rendering-util/rendering-elements/shapes/text.ts](#packagesmermaidsrcrendering-utilrendering-elementsshapestextts)
  - [packages/mermaid/src/rendering-util/rendering-elements/shapes/tiltedCylinder.ts](#packagesmermaidsrcrendering-utilrendering-elementsshapestiltedcylinderts)
  - [packages/mermaid/src/rendering-util/rendering-elements/shapes/trapezoid.ts](#packagesmermaidsrcrendering-utilrendering-elementsshapestrapezoidts)
  - [packages/mermaid/src/rendering-util/rendering-elements/shapes/trapezoidalPentagon.ts](#packagesmermaidsrcrendering-utilrendering-elementsshapestrapezoidalpentagonts)
  - [packages/mermaid/src/rendering-util/rendering-elements/shapes/triangle.ts](#packagesmermaidsrcrendering-utilrendering-elementsshapestrianglets)
  - [packages/mermaid/src/rendering-util/rendering-elements/shapes/util.ts](#packagesmermaidsrcrendering-utilrendering-elementsshapesutilts)
  - [packages/mermaid/src/rendering-util/rendering-elements/shapes/waveEdgedRectangle.ts](#packagesmermaidsrcrendering-utilrendering-elementsshapeswaveedgedrectanglets)
  - [packages/mermaid/src/rendering-util/rendering-elements/shapes/waveRectangle.ts](#packagesmermaidsrcrendering-utilrendering-elementsshapeswaverectanglets)
  - [packages/mermaid/src/rendering-util/rendering-elements/shapes/windowPane.ts](#packagesmermaidsrcrendering-utilrendering-elementsshapeswindowpanets)
  - [packages/mermaid/src/rendering-util/selectSvgElement.ts](#packagesmermaidsrcrendering-utilselectsvgelementts)
  - [packages/mermaid/src/rendering-util/setupViewPortForSVG.ts](#packagesmermaidsrcrendering-utilsetupviewportforsvgts)
  - [packages/mermaid/src/rendering-util/splitText.ts](#packagesmermaidsrcrendering-utilsplittextts)
  - [packages/mermaid/src/rendering-util/types.ts](#packagesmermaidsrcrendering-utiltypests)
  - [packages/mermaid/src/rendering-util/uid.ts](#packagesmermaidsrcrendering-utiluidts)

- [packages/mermaid — docs/.vitepress](#packagesmermaid-docsvitepress)
  - [packages/mermaid/src/docs/.vitepress/canonical-config.ts](#packagesmermaidsrcdocsvitepresscanonical-configts)
  - [packages/mermaid/src/docs/.vitepress/canonical-urls.ts](#packagesmermaidsrcdocsvitepresscanonical-urlsts)
  - [packages/mermaid/src/docs/.vitepress/config.ts](#packagesmermaidsrcdocsvitepressconfigts)
  - [packages/mermaid/src/docs/.vitepress/contributors.ts](#packagesmermaidsrcdocsvitepresscontributorsts)
  - [packages/mermaid/src/docs/.vitepress/headerDomainRules.ts](#packagesmermaidsrcdocsvitepressheaderdomainrulests)
  - [packages/mermaid/src/docs/.vitepress/homepageHeroCopy.ts](#packagesmermaidsrcdocsvitepresshomepageherocopyts)
  - [packages/mermaid/src/docs/.vitepress/mermaid-markdown-all.ts](#packagesmermaidsrcdocsvitepressmermaid-markdown-allts)
  - [packages/mermaid/src/docs/.vitepress/ossHeroClass.ts](#packagesmermaidsrcdocsvitepressossheroclassts)
  - [packages/mermaid/src/docs/.vitepress/scripts/fetch-avatars.ts](#packagesmermaidsrcdocsvitepressscriptsfetch-avatarsts)
  - [packages/mermaid/src/docs/.vitepress/scripts/fetch-contributors.ts](#packagesmermaidsrcdocsvitepressscriptsfetch-contributorsts)
  - [packages/mermaid/src/docs/.vitepress/teamMembers.ts](#packagesmermaidsrcdocsvitepressteammembersts)
  - [packages/mermaid/src/docs/.vitepress/theme/OssHomeHeroNameClipApplier.ts](#packagesmermaidsrcdocsvitepressthemeosshomeheronameclipapplierts)
  - [packages/mermaid/src/docs/.vitepress/theme/index.ts](#packagesmermaidsrcdocsvitepressthemeindexts)
  - [packages/mermaid/src/docs/.vitepress/theme/mermaid.ts](#packagesmermaidsrcdocsvitepressthememermaidts)
  - [packages/mermaid/src/docs/.vitepress/theme/plausible.ts](#packagesmermaidsrcdocsvitepressthemeplausiblets)
  - [packages/mermaid/src/docs/.vitepress/theme/redirect.ts](#packagesmermaidsrcdocsvitepressthemeredirectts)
  - [packages/mermaid/src/docs/vite.config.ts](#packagesmermaidsrcdocsviteconfigts)

- [packages/mermaid — その他ユーティリティ](#packagesmermaid-その他ユーティリティ)
  - [packages/mermaid/src/utils/base64.ts](#packagesmermaidsrcutilsbase64ts)
  - [packages/mermaid/src/utils/imperativeState.ts](#packagesmermaidsrcutilsimperativestatets)
  - [packages/mermaid/src/utils/lineWithOffset.ts](#packagesmermaidsrcutilslinewithoffsetts)
  - [packages/mermaid/src/utils/sanitizeDirective.ts](#packagesmermaidsrcutilssanitizedirectivets)
  - [packages/mermaid/src/utils/subGraphTitleMargins.ts](#packagesmermaidsrcutilssubgraphtitlemarginsts)
  - [packages/mermaid/src/themes/erDiagram-oldHardcodedValues.ts](#packagesmermaidsrcthemeserdiagram-oldhardcodedvaluests)
  - [packages/mermaid/src/tests/util.ts](#packagesmermaidsrctestsutilts)

---

## packages/examples

### packages/examples/src/examples/architecture.ts

`DiagramMetadata` 型を満たすオブジェクトをエクスポートするファイル。ID は `architecture`、名前は「Architecture Diagram」。クラウドグループ内にデータベース・ストレージ・サーバーを配置し、それらを接続する1つのサンプルコードを定義している。`architecture-beta` 記法を使ったシステム構成図のデフォルト例を提供する。

### packages/examples/src/examples/block.ts

ID `block` のブロック図サンプルを定義するファイル。`block-beta` 記法を使い、DBノード・矢印・ブロックグループ・スタイルを含む1例を提供する。`isDefault: true` が設定されたシンプルなブロックレイアウトのデモ。

### packages/examples/src/examples/c4.ts

C4モデル（Context / Container / Component / Codeの4層）によるソフトウェアアーキテクチャ図のサンプルファイル。インターネットバンキングシステムのコンテキスト図を例として定義しており、エンタープライズ境界・人物・システム・キューなどの構成要素を網羅している。

### packages/examples/src/examples/class.ts

UMLクラス図のサンプルを定義するファイル。ID は `classDiagram`。`Animal` を親クラスとして `Duck`・`Fish`・`Zebra` が継承するシンプルな継承関係を記述した1つのデフォルト例を提供する。

### packages/examples/src/examples/cynefin.ts

Cynefin フレームワーク図のサンプルを定義するファイル（ID: `cynefin`）。インシデントレスポンスを題材に、`complex`・`complicated`・`clear`・`chaotic`・`confusion` の各ドメインにアクションを配置し、ドメイン間の遷移を示す `cynefin-beta` 記法の例を提供する。

### packages/examples/src/examples/er.ts

ER図（Entity Relationship Diagram）のサンプルを定義するファイル（ID: `er`）。`CUSTOMER`・`ORDER`・`PRODUCT`・`ORDER_ITEM` の4エンティティとその関連（多対一、一対多など）を `erDiagram` 記法で記述したデフォルト例を1つ提供する。

### packages/examples/src/examples/eventmodeling.ts

イベントモデリング図のサンプルを定義するファイル（ID: `eventmodeling`）。`eventmodeling` 記法を使い、UI・コマンド・イベント・Read Model Outputを時系列に並べた最小限の例を1つ提供する。

### packages/examples/src/examples/flowchart.ts

フローチャートのサンプルを定義するファイル（ID: `flowchart-v2`）。`flowchart TD` 記法を使った上から下方向のフロー例（クリスマスの買い物判断フロー）を1つ提供する。Font Awesome アイコンの使用例も含まれている。

### packages/examples/src/examples/gantt.ts

ガントチャートのサンプルを定義するファイル（ID: `gantt`）。`gantt` 記法で日付フォーマット・セクション・タスク・依存関係を定義した基本的なプロジェクトタイムラインの例を1つ提供する。

### packages/examples/src/examples/git.ts

Gitグラフのサンプルを定義するファイル（ID: `gitGraph`）。`main` ブランチから `develop` と `feature` ブランチを作成してマージする基本的な Git フローを `gitGraph` 記法で記述した例を1つ提供する。

### packages/examples/src/examples/ishikawa.ts

石川ダイアグラム（フィッシュボーン図）のサンプルを定義するファイル（ID: `ishikawa`）。「ぼやけた写真」の原因をプロセス・ユーザー・機材・環境の4カテゴリで整理した `ishikawa-beta` 記法の例を1つ提供する。

### packages/examples/src/examples/kanban.ts

カンバンボードのサンプルを定義するファイル（ID: `kanban`）。フロントマターで `ticketBaseUrl` を設定し、Todo・In progress・Ready for deploy・Done など複数カラムにチケット・担当者・優先度付きのアイテムを配置した詳細な例を提供する。

### packages/examples/src/examples/mindmap.ts

マインドマップのサンプルを定義するファイル（ID: `mindmap`）。`mindmap` 記法でルートから「Origins」「Research」「Tools」の3ブランチを展開し、Font Awesome アイコンの使用例も含む基本的なマインドマップ1例を提供する。

### packages/examples/src/examples/packet.ts

パケット図のサンプルを定義するファイル（ID: `packet`）。TCP パケットのヘッダーフィールドをビット範囲（0–255）で定義した `packet` 記法の例を1つ提供する。ネットワークプロトコルのビットレベル構造の可視化に使用される。

### packages/examples/src/examples/pie.ts

円グラフのサンプルを定義するファイル（ID: `pie`）。ボランティアに引き取られたペット（犬・猫・ネズミ）の割合を示す `pie` 記法の最小限の例を1つ提供する。

### packages/examples/src/examples/quadrant-chart.ts

クォードラントチャートのサンプルを定義するファイル（ID: `quadrantChart`）。X軸をリーチ・Y軸をエンゲージメントとしてキャンペーンの位置を2×2マトリクスに配置した `quadrantChart` 記法の例を1つ提供する。

### packages/examples/src/examples/radar.ts

レーダーチャートのサンプルを定義するファイル（ID: `radar`）。`radar-beta` 記法を使い、数学・理科・英語・歴史・地理・美術の6軸に対して Alice と Bob の成績を表示する例を1つ提供する。`max`/`min` の指定も含まれている。

### packages/examples/src/examples/railroad-abnf.ts

ABNF（RFC 5234）記法によるレールロード図のサンプルを定義するファイル（ID: `railroadAbnf`）。メールアドレスの文法規則（`address`・`local-part`・`domain`・`label`）を `railroad-abnf` 記法で記述した例を1つ提供する。

### packages/examples/src/examples/railroad-ebnf.ts

EBNF記法（W3CおよびISO 14977対応）によるレールロード図のサンプルを定義するファイル（ID: `railroadEbnf`）。算術式の文法（`expression`・`term`・`factor`・`number`・`digit`）を `railroad-ebnf` 記法で記述した例を1つ提供する。

### packages/examples/src/examples/railroad-peg.ts

PEG（Parsing Expression Grammar）記法によるレールロード図のサンプルを定義するファイル（ID: `railroadPeg`）。計算機の文法（`Expression`・`Term`・`Factor`・`Number`・`Digit`）を `railroad-peg` 記法で記述した例を1つ提供する。

### packages/examples/src/examples/railroad.ts

レールロード図の中間表現（IR）を直接記述するサンプルを定義するファイル（ID: `railroad`）。`railroad-diagram` 記法で `sequence`・`choice`・`zeroOrMore`・`nonterminal`・`terminal` などのプリミティブを使い、算術式文法とJSON文法の2例を提供する。

### packages/examples/src/examples/requirement.ts

要求図のサンプルを定義するファイル（ID: `requirement`）。`requirementDiagram` 記法でリスク・検証方法を持つ要求と要素を定義し、`satisfies` 関係で結んだ最小限の例を1つ提供する。

### packages/examples/src/examples/sankey.ts

サンキー図のサンプルを定義するファイル（ID: `sankey`）。`sankey-beta` 記法で農業廃棄物・石炭・核エネルギー・再生可能エネルギーなど多数のエネルギーフローを定義した大規模な英国エネルギーフローの実例を1つ提供する。`showValues: false` のフロントマター設定付き。

### packages/examples/src/examples/sequence.ts

シーケンス図のサンプルを定義するファイル（ID: `sequence`）。`sequenceDiagram` 記法で Alice と John 間の同期・非同期メッセージをやり取りするシンプルな会話例を1つ提供する。

### packages/examples/src/examples/state.ts

状態遷移図のサンプルを定義するファイル（ID: `stateDiagram`）。`stateDiagram-v2` 記法で初期状態・`Still`・`Moving`・`Crash`・終了状態の間の遷移を記述した基本的な例を1つ提供する。

### packages/examples/src/examples/timeline.ts

タイムライン図のサンプルを定義するファイル（ID: `timeline`）。`timeline` 記法で2002年〜2006年のソーシャルメディアプラットフォームの歴史（LinkedIn・Facebook・Google・YouTube・Twitter）を年表形式で表した例を1つ提供する。

### packages/examples/src/examples/tree-view.ts

ツリービューのサンプルを定義するファイル（ID: `treeView`）。`treeView-beta` 記法でディレクトリ構造を表す3種類の例（基本・アイコン付き・アノテーション付き）を提供する。アノテーション例では `:::highlight`・`icon()`・`##コメント` の記法も示している。

### packages/examples/src/examples/treemap.ts

ツリーマップのサンプルを定義するファイル（ID: `treemap`）。`treemap-beta` 記法でセクションとリーフノードに数値を持つ階層的な矩形分割図の最小例を1つ提供する。

### packages/examples/src/examples/user-journey.ts

ユーザージャーニー図のサンプルを定義するファイル（ID: `journey`）。`journey` 記法で「仕事の一日」を題材に、出勤・在宅ワーク・帰宅の各セクションにアクションとスコア・担当者を記述した例を1つ提供する。

### packages/examples/src/examples/venn.ts

ベン図のサンプルを定義するファイル（ID: `venn`）。`venn-beta` 記法で3つの集合 A・B・C とその交差領域（AB・BC・AC・ABC）を定義し、各領域にラベルと塗りつぶし色を設定した例を1つ提供する。

### packages/examples/src/examples/wardley.ts

ウォードリーマップのサンプルを定義するファイル（ID: `wardley-beta`）。`wardley-beta` 記法でビジネス戦略・バリューチェーンを可視化する4つの例（紅茶店・データパイプライン・ケトルパイプライン・GPTトークナイザー）を提供する。アンカー・コンポーネント・進化・パイプライン・アノテーション等の記法を網羅している。

---

## packages/mermaid-example-diagram

### packages/mermaid-example-diagram/src/diagram-definition.ts

サンプルカスタムダイアグラムの定義をまとめてエクスポートするファイル。Jison パーサー・DB・レンダラー・スタイル・`injectUtils` を1つの `diagram` オブジェクトとしてまとめる。Mermaid の外部ダイアグラムプラグイン開発のリファレンス実装として機能する。

### packages/mermaid-example-diagram/src/detector.ts

`example-diagram` という外部ダイアグラムプラグインの検出・遅延ロードロジックを定義するファイル。テキストが `/^\s*example-diagram/` にマッチするかで判定し、マッチ時に `diagram-definition.ts` を動的インポートする `ExternalDiagramDefinition` オブジェクトをエクスポートする。

### packages/mermaid-example-diagram/src/mermaidUtils.ts

Mermaid コアから外部プラグインへユーティリティ関数（ロガー・`setLogLevel`・`getConfig`・`sanitizeText`・`setupGraphViewbox`・`commonDb`）を注入するためのモジュール。初期化前は警告関数をデフォルトとして使用し、`injectUtils` 呼び出し時に実際の関数で上書きする。

---

## packages/mermaid-zenuml

### packages/mermaid-zenuml/src/detector.ts

ZenUML ダイアグラムの外部プラグイン検出・遅延ロードを定義するファイル。テキストが `/^\s*zenuml/` にマッチするかで判定し、`zenuml-definition.ts` を動的インポートする `ExternalDiagramDefinition` をエクスポートする。構造は `mermaid-example-diagram` の `detector.ts` と同一パターン。

### packages/mermaid-zenuml/src/mermaidUtils.ts

`mermaid-example-diagram` の同名ファイルとほぼ同等。Mermaid コアからのユーティリティ注入モジュール。異なる点は `commonDb` の注入引数がなく、`getConfig` の戻り値が `MermaidConfig` 型として厳密に型付けされている。

### packages/mermaid-zenuml/src/parser.ts

ZenUML は内部で Antlr4 パーサー（`vue-sequence` ライブラリ）を使用するため、Mermaid の API 仕様を満たすための「何もしない（no-op）」ダミーパーサーを定義する。`parse()` メソッドが空実装のオブジェクトをエクスポートするのみ。

### packages/mermaid-zenuml/src/zenuml-definition.ts

ZenUML ダイアグラムの定義をまとめてエクスポートするファイル。DB（`clear` のみの no-op）・`parser`（ダミー）・`renderer`（`zenumlRenderer`）・`styles`（no-op）・`injectUtils` を1つの `diagram` オブジェクトとして組み合わせる。

### packages/mermaid-zenuml/src/zenumlRenderer.ts

ZenUML ダイアグラムのレンダリングロジックを実装するファイル。`@zenuml/core` の `renderToSvg` を呼び出して SVG を生成し、セキュリティレベル（sandbox 対応）を考慮した `selectSvgElement` でターゲット SVG 要素を取得して innerSVG・サイズ・viewBox を設定する。`useMaxWidth` オプションによるレスポンシブ対応も含む。

---

## packages/mermaid-layout-tidy-tree

### packages/mermaid-layout-tidy-tree/src/layouts.ts

Tidy-tree レイアウトプラグインのエントリポイント定義ファイル。`render.js` を遅延ロードする `LayoutLoaderDefinition` を1つ（`name: 'tidy-tree'`、`algorithm: 'tidy-tree'`）エクスポートする。配列形式で Mermaid のレイアウトシステムに登録される。

### packages/mermaid-layout-tidy-tree/src/layout.ts

非層型 Tidy-tree レイアウトアルゴリズムの実装本体。ノードとエッジの `LayoutData` を受け取り、ルートの子ノードを左右交互に振り分けて2つのサブツリーを構築（双方向レイアウト）、`non-layered-tidy-tree-layout` ライブラリで各ツリーの座標を計算した後、ノードとエッジの最終座標を返す。エッジの境界交差計算（矩形・円形）も含む大規模なファイル。

### packages/mermaid-layout-tidy-tree/src/render.ts

Tidy-tree レイアウトの SVG レンダリング処理を実装するファイル。「ノードを DOM に挿入して実寸を取得 → Tidy-tree レイアウト計算 → ノードと辺を SVG に配置」の3ステップを実行する。ELK や Dagre と同じ統一レンダリングパターンに従い、`insertNode`・`insertEdge`・`positionEdgeLabel` などの `InternalHelpers` を使用する。

### packages/mermaid-layout-tidy-tree/src/types.ts

Tidy-tree レイアウトパッケージで使用する型定義ファイル。`PositionedNode`（`section: 'root'|'left'|'right'` 付き）・`PositionedEdge`・`LayoutResult`・`TidyTreeNode`・`TidyTreeLayoutConfig` の5インターフェースを定義する。

### packages/mermaid-layout-tidy-tree/src/index.ts

Tidy-tree レイアウトパッケージの公開エントリポイント。モジュールの概要コメント（双方向ツリーレイアウトの構造説明）を含み、`layouts.ts`・`types.ts`・`layout.ts`・`render.ts` の全エクスポートを再エクスポートする。

---

## packages/mermaid-layout-elk

### packages/mermaid-layout-elk/src/index.ts

ELK（Eclipse Layout Kernel）レイアウトプラグインのエントリポイント定義ファイル。`elk`（`elk.layered`）をデフォルトに、`elk.stress`・`elk.force`・`elk.mrtree`・`elk.sporeOverlap` の計5種類のレイアウトアルゴリズムを `LayoutLoaderDefinition` 配列としてエクスポートし、Mermaid のレイアウトシステムに登録する。

---

## packages/parser

### packages/parser/src/parse.ts

Langium ベースのパーサーへの統一的なエントリポイント。15 種類の図タイプ（info、pie、gitGraph など）それぞれに対応した `LangiumParser` をレイジーに初期化・キャッシュする `parsers` レコードと `initializers` マップを保持する。公開 API の `parse(diagramType, text)` 関数はダイナミックインポートでパーサーを取得し、パース結果にエラーがあれば `MermaidParseError` をスローする。型オーバーロードにより `diagramType` 文字列から戻り値の AST 型を正しく推論できる。

### packages/parser/src/index.ts

パッケージ全体の公開 API を集約するバレルファイル。`./language/index.js` と `./parse.js` を再エクスポートする。独自のユーティリティ型 `RecursiveAstOmit<T>` を定義しており、Langium の `AstNode` 属性を再帰的に除去した純粋なデータ型を生成するために使用される。

### packages/parser/scripts/prepack.ts

npm パッケージ公開前の型定義バンドル生成スクリプト。`@microsoft/api-extractor` を使用して `dist/src/index.d.ts` に型をバンドルし、その後 `dist/**/*.d.ts` の不要なファイルと空ディレクトリを削除する。`node --experimental-strip-types` で直接実行できる形式になっている。

### packages/parser/tests/test-util.ts

テスト全体で共有されるヘルパー関数とパーサーインスタンスを定義するユーティリティ。`expectNoErrorsOrAlternatives` 関数はレキサー・パーサーエラーの不存在を検証し、info・architecture・pie・packet・radar・gitGraph・eventModeling・treeView の各図タイプに対してサービスとパース関数をシングルトンとして生成しエクスポートする。

### packages/parser/tests/eventmodeling.test.ts

イベントモデリング図パーサーのテストスイート。複雑なモデル構文（`tf`/`rf`/`entity`/`data`/`note`/`gwt` キーワード、クロスリファレンス、インライン/ブロックデータ）の正常解析を検証する。また `EventModelingValidator` の `registerValidationChecks` によるソースフレームタイプ制約の検証も含む。

### packages/parser/tests/radar.test.ts

レーダー図（`radar-beta`）パーサーのテストスイート。グローバル空白（スペース・タブ・改行）の有無に関わらず正しくパースできることを多様なインプットで検証する。`title`・`accDescr`・`accTitle` などのアクセシビリティメタデータの解析、セクション・軸・データポイントの解析、エラー時の `MermaidParseError` スローも検証する。

### packages/parser/tests/treeViewValueConverter.test.ts

`TreeViewValueConverter` の単体テスト。`runCustomConverter` を外部から呼び出せるテスト用サブクラスを定義し、`INDENTATION`・`QUOTED_NAME`・`CLASS_ANNOTATION`・`ICON_ANNOTATION`・`DESC_ANNOTATION` の各ルールの変換ロジックを検証する。

### packages/parser/tests/pie.test.ts

円グラフ（`pie`）パーサーのテストスイート。`pie`／`pie showData` の基本構文、`title`・`accDescr`・`accTitle` の同一行・次行での指定、パイセクション（ラベルと数値）の解析を多様な空白バリエーションで検証する。

### packages/parser/tests/railroad.test.ts

鉄道図（`railroad-diagram`）パーサーのテストスイート。タイトル・アクセシビリティメタデータ、IR 関数式（`sequence`・`terminal`・`nonterminal`・`choice`・`optional` など）の解析を詳細に検証する。`parse`（非同期）と直接パーサーの両方を用い、エラー時の `MermaidParseError` もテストする。

### packages/parser/tests/architecture.test.ts

アーキテクチャ図（`architecture-beta`）パーサーのテストスイート。基本構文の認識、`title`・`accDescr`・`accTitle` の同一行・次行解析、サービス・グループ・ジャンクション・エッジの各要素の構文解析を検証する。

### packages/parser/tests/packet.test.ts

パケット図（`packet-beta`／`packet`）パーサーの最小限のテストスイート。両キーワードとスペース・タブ・改行バリエーションで正しく `$type: 'Packet'` の AST が生成されることを確認する。

### packages/parser/tests/treeView.test.ts

ツリービュー（`treeView-beta`）パーサーのテストスイート。空のツリー、引用符付きノード、複数語ノード、子ノードのインデント階層、クラス・アイコン・説明アノテーションの解析、および様々な空白バリエーションに対する動作を検証する。

### packages/parser/tests/gitGraph.test.ts

GitGraph（`gitGraph`）パーサーのテストスイート。`commit`・`branch`・`merge`・`checkout`・`cherry-pick` の各ステートメントを詳細に検証する。コミット ID・メッセージ・タグ・タイプ、ブランチオーダー、マージオプション、チェリーピックの `parent` プロパティなども網羅的にテストする。

### packages/parser/tests/info.test.ts

Info 図（`info`）パーサーの最小テストスイート。`info` 単体と `info showInfo` の組み合わせを、先頭・末尾の空白や改行のバリエーションとともに検証する。

### packages/parser/src/language/generated/ast.ts

langium-cli 4.2.0 が自動生成した AST 型定義ファイル（手動編集禁止）。Architecture・Cynefin・EventModeling・GitGraph・Info・Packet・Pie・Radar・Railroad系・Treemap・TreeView・Wardley の全図タイプの AST ノード型・ターミナル定数・`is*` 型ガード関数・`MermaidAstReflection` クラスを定義する。

### packages/parser/src/language/generated/grammar.ts

langium-cli 4.2.0 が自動生成した文法定義ファイル（手動編集禁止）。各図タイプの文法を JSON シリアライズ形式で含み、`loadGrammarFromJson` で遅延ロードするファクトリ関数をエクスポートする。

### packages/parser/src/language/generated/module.ts

langium-cli 4.2.0 が自動生成したモジュール定義ファイル（手動編集禁止）。各言語の `LanguageMetaData` と、Langium の依存性注入で使用する `GeneratedModule` を定義する。共有サービス用の `MermaidGeneratedSharedModule`（`MermaidAstReflection` を登録）も含む。

### packages/parser/src/language/index.ts

`language/` ディレクトリ全体の公開 API をまとめるバレルファイル。`generated/ast.js` からの AST 型・型ガード、`generated/module.js` からの生成モジュール、各言語サブディレクトリの `index.js` をすべて再エクスポートする。

### packages/parser/src/language/common/matcher.ts

アクセシビリティメタデータとタイトルのパターンマッチング用正規表現を定義する共通ユーティリティ。`accessibilityDescrRegex`・`accessibilityTitleRegex`・`titleRegex` の3つの正規表現をエクスポートする。

### packages/parser/src/language/common/tokenBuilder.ts

全図タイプ共通の抽象トークンビルダー `AbstractMermaidTokenBuilder` を定義する。指定されたキーワードセットのトークンパターンに後続非空白制約を付加する。`CommonTokenBuilder` は追加ロジックなしでこのクラスを継承する。

### packages/parser/src/language/common/valueConverter.ts

全図タイプ共通の抽象値コンバーター `AbstractMermaidValueConverter` を定義する。`ACC_DESCR`・`ACC_TITLE`・`TITLE` ルールに対して `matcher.ts` の正規表現で共通変換を行う。サブクラスは `runCustomConverter` を実装して図タイプ固有の変換を追加する。

### packages/parser/src/language/architecture/module.ts

Architecture 図の Langium サービスを構成する DI モジュール。`ArchitectureTokenBuilder`・`ArchitectureValueConverter` を登録した `ArchitectureModule` と、`createArchitectureServices` 関数を提供する。

### packages/parser/src/language/architecture/tokenBuilder.ts

`AbstractMermaidTokenBuilder` を継承した `ArchitectureTokenBuilder`。キーワードリスト `['architecture']` をスーパークラスに渡して後続非空白制約を適用する。

### packages/parser/src/language/architecture/valueConverter.ts

Architecture 図固有の値変換を行う `ArchitectureValueConverter`。`ARCH_ICON`（括弧除去）・`ARCH_TEXT_ICON`（引用符・括弧除去）・`ARCH_TITLE`（角括弧と外側引用符除去・エスケープ解除）の3ルールを処理する。

### packages/parser/src/language/cynefin/module.ts

Cynefin 図の Langium サービスを構成する DI モジュール。`CynefinTokenBuilder` と共通の `CommonValueConverter` を登録し、`createCynefinServices` でサービスセットを生成する。

### packages/parser/src/language/cynefin/tokenBuilder.ts

`AbstractMermaidTokenBuilder` を継承した `CynefinTokenBuilder`。キーワードリスト `['cynefin-beta']` を使用する。

### packages/parser/src/language/eventmodeling/event-modeling-validator.ts

イベントモデリング図のカスタムバリデーターを実装。`EmTimeFrame`・`EmResetFrame` の `sourceFrames` に対して、entity タイプに応じた入力元制約を `checkSourceFrameTypes` で検証する。`registerValidationChecks` でサービスの ValidationRegistry に登録する。

### packages/parser/src/language/eventmodeling/module.ts

EventModeling 図の Langium サービスを構成する DI モジュール。`EventModelingTokenBuilder`・`CommonValueConverter`・`EventModelingValidator` を登録する。サービス生成後に `registerValidationChecks` を呼び出してバリデーションを有効化する。

### packages/parser/src/language/eventmodeling/tokenBuilder.ts

`AbstractMermaidTokenBuilder` を継承した `EventModelingTokenBuilder`。キーワードリスト `['eventmodeling']` を使用する。

### packages/parser/src/language/gitGraph/module.ts

GitGraph 図の Langium サービスを構成する DI モジュール。`GitGraphTokenBuilder` と `CommonValueConverter` を登録し、`createGitGraphServices` でサービスセットを生成する。

### packages/parser/src/language/gitGraph/tokenBuilder.ts

`AbstractMermaidTokenBuilder` を継承した `GitGraphTokenBuilder`。キーワードリスト `['gitGraph']` を使用する。

### packages/parser/src/language/info/module.ts

Info 図の Langium サービスを構成する DI モジュール。`InfoTokenBuilder` と `CommonValueConverter` を登録し、`createInfoServices` でサービスセットを生成する。

### packages/parser/src/language/packet/module.ts

Packet 図の Langium サービスを構成する DI モジュール。`PacketTokenBuilder` と `CommonValueConverter` を登録し、`createPacketServices` でサービスセットを生成する。

### packages/parser/src/language/pie/module.ts

Pie 図の Langium サービスを構成する DI モジュール。`PieTokenBuilder` と `PieValueConverter`（pie 固有の変換あり）を登録し、`createPieServices` でサービスセットを生成する。

### packages/parser/src/language/pie/valueConverter.ts

Pie 図固有の値変換を行う `PieValueConverter`。`PIE_SECTION_LABEL` ルールで引用符を除去してトリミングする。

### packages/parser/src/language/radar/module.ts

Radar 図の Langium サービスを構成する DI モジュール。`RadarTokenBuilder` と `CommonValueConverter` を登録し、`createRadarServices` でサービスセットを生成する。

### packages/parser/src/language/radar/tokenBuilder.ts

`AbstractMermaidTokenBuilder` を継承した `RadarTokenBuilder`。キーワードリスト `['radar-beta']` を使用する。

### packages/parser/src/language/railroad/module.ts

Railroad（IR 形式）図の Langium サービスを構成する DI モジュール。`RailroadTokenBuilder` と `RailroadValueConverter` を登録し、`createRailroadServices` でサービスセットを生成する。

### packages/parser/src/language/railroad/valueConverter.ts

Railroad 図固有の値変換を行う `RailroadValueConverter`。`decodeEscapedString` ヘルパーでエスケープシーケンス（`\n`・`\r`・`\t` など）を展開し、`RR_STRING` ルールおよびクォート付き `TITLE` に適用する。

### packages/parser/src/language/railroad-ebnf/module.ts

EBNF 形式の Railroad 図サービスを構成する DI モジュール。`RailroadEbnfTokenBuilder` と `RailroadEbnfValueConverter` を登録し、`createRailroadEbnfServices` でサービスセットを生成する。

### packages/parser/src/language/railroad-ebnf/valueConverter.ts

EBNF 形式固有の値変換。`EBNF_STRING`（エスケープ展開）と `EBNF_SPECIAL_SEQUENCE`（`?...?` の前後トリミング）を処理し、クォート付き `TITLE` にもエスケープ展開を適用する。

### packages/parser/src/language/railroad-abnf/module.ts

ABNF 形式の Railroad 図サービスを構成する DI モジュール。`RailroadAbnfTokenBuilder` と `RailroadAbnfValueConverter` を登録し、`createRailroadAbnfServices` でサービスセットを生成する。

### packages/parser/src/language/railroad-abnf/valueConverter.ts

ABNF 形式固有の値変換。`ABNF_STRING` ルールで引用符を除去（エスケープ展開なし）し、クォート付き `TITLE` も引用符を除去する。

### packages/parser/src/language/railroad-peg/module.ts

PEG 形式の Railroad 図サービスを構成する DI モジュール。`RailroadPegTokenBuilder` と `RailroadPegValueConverter` を登録し、`createRailroadPegServices` でサービスセットを生成する。

### packages/parser/src/language/railroad-peg/valueConverter.ts

PEG 形式固有の値変換。`PEG_STRING` ルールでエスケープシーケンスを展開し、クォート付き `TITLE` にも同様の変換を適用する。

### packages/parser/src/language/treeView/module.ts

TreeView 図の Langium サービスを構成する DI モジュール。`TreeViewTokenBuilder` と `TreeViewValueConverter` を登録し、`createTreeViewServices` でサービスセットを生成する。

### packages/parser/src/language/treeView/tokenBuilder.ts

`AbstractMermaidTokenBuilder` を継承した `TreeViewTokenBuilder`。キーワードリスト `['treeView-beta']` を使用する。

### packages/parser/src/language/treeView/valueConverter.ts

TreeView 図固有の値変換。`INDENTATION`（空白長を数値に変換）・`QUOTED_NAME`（外側引用符除去）・`CLASS_ANNOTATION`（`:::className` のパース）・`ICON_ANNOTATION`（`icon(name)` のパース）・`DESC_ANNOTATION`（`## description` のパース）の5ルールを処理する。

### packages/parser/src/language/treemap/module.ts

Treemap 図の Langium サービスを構成する DI モジュール。`TreemapTokenBuilder`・`TreemapValueConverter`・`TreemapValidator` を登録し、サービス生成後に `registerValidationChecks` を呼び出す。

### packages/parser/src/language/treemap/valueConverter.ts

Treemap 図固有の値変換。`NUMBER2`・`SEPARATOR`・`STRING2`・`INDENTATION`・`ClassDef` の各ルールを処理する。数値変換・引用符除去・インデント長の数値化・`classDef` 文のオブジェクト生成を担う。

### packages/parser/src/language/treemap/treemap-validator.ts

Treemap 図のカスタムバリデーター。`checkSingleRoot` で `TreemapRows` を走査し、インデントなしのルートノードが複数存在する場合にエラーを報告する。`registerValidationChecks` でサービスの ValidationRegistry に登録する。

### packages/parser/src/language/wardley/module.ts

Wardley マップの Langium サービスを構成する DI モジュール。`WardleyValueConverter` のみを登録（TokenBuilder はデフォルト使用）し、`createWardleyServices` でサービスセットを生成する。

### packages/parser/src/language/wardley/valueConverter.ts

Wardley マップ固有の値変換を行う `WardleyValueConverter`。`LINK_LABEL` ルールで先頭の `;` を除去してトリミングする。

---

## packages/mermaid — コア

### packages/mermaid/src/Diagram.ts

mermaid ダイアグラムの中核クラス `Diagram` を定義する。テキストからダイアグラムを非同期で生成する静的メソッド `fromText` を持ち、テキストの型検出・ローダー取得・パーサー呼び出しを行う。内部でダイアグラム種別の DB・パーサー・レンダラーを保持し、`render` メソッドで SVG として描画する。コンストラクターはプライベートで `fromText` 経由でのみインスタンス化される。

### packages/mermaid/src/**mocks**/mermaidAPI.ts

テスト用の `mermaidAPI` モックオブジェクトを提供する。本物の `mermaidAPI` は `Object.freeze` で凍結されているため `vi.spyOn` が使えないため、このモジュールで `vi.fn()` を使い `render` や `initialize` などをスパイ可能な関数に差し替えて提供している。

### packages/mermaid/src/accessibility.ts

SVG ダイアグラムに WAI-ARIA アクセシビリティ属性を付与するユーティリティ。`setA11yDiagramInfo` で SVG に `role` と `aria-roledescription` を設定し、`addSVGa11yTitleDescription` でアクセシブルタイトルや説明の `<title>`/`<desc>` 要素を SVG に挿入する。

### packages/mermaid/src/assignWithDepth.ts

`Object.assign` を拡張して任意の深さでオブジェクトを再帰的にマージする関数。型が異なるキーは `clobber` オプションが `false` のときに上書きしない。配列同士はマージして重複を除去する。mermaid の設定マージ処理全体で多用される基礎ユーティリティ。

### packages/mermaid/src/config.ts

mermaid のグローバル設定管理モジュール。`siteConfig`・`currentConfig`・`directives` の3層構造で設定を管理し、`setConfig`・`getConfig`・`setSiteConfig`・`reset`・`addDirective` などの API を提供する。XSS やプロトタイプ汚染を防ぐサニタイズ処理も含む。`defaultConfig` は `Object.freeze` で不変。

### packages/mermaid/src/config.type.ts

JSON Schema から自動生成された `MermaidConfig` インターフェースと全ダイアグラム種別の設定型定義ファイル。flowchart・sequence・gantt・class・state・er・c4・sankey・kanban・railroad など30以上のダイアグラム固有設定インターフェースを含む。手動で編集してはならないファイル。

### packages/mermaid/src/defaultConfig.ts

mermaid のデフォルト設定オブジェクトを定義する。YAML スキーマから自動生成されたデフォルト値に、`FontCalculator` 関数（sequence・c4 用）や `undefined` 値を追加している。`keyify` 関数で全設定キーのセット `configKeys` を生成し、サニタイズ処理で使用する。

### packages/mermaid/src/errors.ts

mermaid のカスタムエラークラスを定義する。現在は `UnknownDiagramError`（不明なダイアグラム種別が指定された際にスローされる）のみを含む。`Error` を継承し `name` プロパティを設定する最小実装。

### packages/mermaid/src/interactionDb.ts

ダイアグラム要素のクリックイベント等の操作関数を蓄積・実行するモジュール。`addFunction` でコールバック関数をキューに積み、`attachFunctions` でキュー内の全関数を実行してリセットする。レンダリング後に DOM ハンドラを遅延バインドするための仕組み。

### packages/mermaid/src/internals.ts

外部パッケージ向けに mermaid 内部ヘルパーをまとめて再エクスポートするモジュール。クラスター・エッジ・マーカー・ノード描画関数、設定取得、カーブ補間などを `internalHelpers` オブジェクトとして提供する。外部利用は非推奨で定義は予告なく変更される可能性がある。

### packages/mermaid/src/logger.ts

ログレベル管理ユーティリティ。`trace`・`debug`・`info`・`warn`・`error`・`fatal` の6段階を持つ `log` オブジェクトを提供し、`setLogLevel` でアクティブなレベルを動的に切り替える。デフォルトは `fatal` のみ有効。タイムスタンプ付きフォーマット文字列を `dayjs` で生成する。

### packages/mermaid/src/mermaid.ts

mermaid のブラウザ向け公開 API エントリポイント。`run`・`render`・`parse`・`init`（非推奨）・`initialize`・`registerExternalDiagrams`・`registerIconPacks` などを提供する。`render`/`parse` は実行キューで直列化される。ページロード時に `startOnLoad` が有効なら自動レンダリングする。

### packages/mermaid/src/mermaidAPI.ts

mermaid の内部 API 実装の核心部。SVG のレンダリング・スタイル適用・アクセシビリティ情報付与・セキュリティレベルに応じたサンドボックス処理などを担う `render` 関数と、設定初期化の `initialize` 関数を含む。`mermaidAPI` オブジェクトを `Object.freeze` してエクスポートする。

### packages/mermaid/src/preprocess.ts

ダイアグラムテキストの前処理を担う `preprocessDiagram` 関数を提供する。CRLF 正規化・HTML 属性クォート統一→フロントマター抽出→ディレクティブ抽出→コメント除去の4ステップを順に処理し、最終的なコード・タイトル・設定オブジェクトを返す。

### packages/mermaid/src/styles.ts

ダイアグラム種別ごとのスタイルプロバイダーを管理し、全ダイアグラム共通の CSS（エッジアニメーション・エラー表示・マーカー・neo スタイル等）を生成する `getStyles` 関数を提供する。`addStylesForDiagram` で各ダイアグラムのスタイル関数を登録する仕組みも持つ。

### packages/mermaid/src/types.ts

mermaid の公開 TypeScript 型定義ファイル。`NodeMetaData`・`EdgeData`・`ParseOptions`・`ParseResult`・`RenderResult`・`D3Element`・`D3Selection` などのインターフェースや型エイリアスを定義する。`RenderResult.bindFunctions` でレンダリング後のDOM バインド関数を渡す仕組みも定義。

### packages/mermaid/src/utils.ts

mermaid 全体で使われる多目的ユーティリティ集。テキスト寸法計算（`calculateTextDimensions`・メモ化）、ラベル折り返し（`wrapLabel`）、ディレクティブ検出（`detectInit`・`detectDirective`）、エンティティエンコード/デコード、カーブ名→d3 関数変換（`interpolateToCurve`）、ID生成など多数の汎用関数を含む。

---

## packages/mermaid — diagram-api

### packages/mermaid/src/diagram-api/comments.ts

mermaid テキストから `%%` で始まるコメント行（ただし `%%{` 始まりのディレクティブは除外）を除去する `cleanupComments` 関数を提供する。正規表現で1行マッチしてから `trimStart` で先頭空白を除去するシンプルな実装。

### packages/mermaid/src/diagram-api/detectType.ts

ダイアグラムテキストの種別を検出する `detectType` 関数と、ダイアグラム検出器の登録/取得 API を提供する。フロントマターやディレクティブを除去したテキストに対して登録済み `detector` 関数を順番に適用し、最初に `true` を返した種別を採用する。`registerLazyLoadedDiagrams` で遅延ロードダイアグラムも登録できる。

### packages/mermaid/src/diagram-api/diagram-orchestration.ts

mermaid が標準でサポートする全ダイアグラム種別の検出器・ローダーを一括登録する `addDiagrams` 関数を提供する。初回呼び出し時のみ実行（フラグ管理）し、`error` や `---` などの特殊ダイアグラムを直接登録、その他は `registerLazyLoadedDiagrams` で遅延登録する。

### packages/mermaid/src/diagram-api/diagramAPI.ts

外部ダイアグラムが mermaid コア機能にアクセスするための公開 API。`registerDiagram` で新しいダイアグラムを登録し、`getDiagram` で取得する。登録時にスタイルの追加や `injectUtils` でコア機能（設定・ログ・サニタイズ等）をダイアグラムに注入する。サードパーティ製カスタムダイアグラム向けの拡張ポイント。

### packages/mermaid/src/diagram-api/frontmatter.ts

mermaid テキストの先頭にある YAML フロントマター（`---`で囲まれたブロック）を解析する。`extractFrontMatter` 関数で `title`・`displayMode`・`config` を抽出し、残りのテキストと合わせて返す。インデントされたフロントマターにも対応（`js-yaml` の JSON スキーマを使用）。

### packages/mermaid/src/diagram-api/loadDiagram.ts

`loadRegisteredDiagrams` 関数で登録済みの全遅延ローダーを並列実行し、未ロードのダイアグラムを一括でロードする。ロード失敗したダイアグラムは検出器リストから削除し、すべての失敗をまとめてエラーとして報告する。

### packages/mermaid/src/diagram-api/regexes.ts

ダイアグラムテキスト解析に使う正規表現を定義するモジュール。フロントマター検出用 `frontMatterRegex`（インデント対応、バックリファレンスで開閉 `---` を同一インデントで対応）、ディレクティブ検出用 `directiveRegex`、コメント検出用 `anyCommentRegex` の3つのみをエクスポートする。

### packages/mermaid/src/diagram-api/types.ts

diagram-api 関連の TypeScript 型定義ファイル。`DiagramDB`・`DiagramDefinition`・`DiagramRenderer`・`DiagramDetector` など、mermaid のダイアグラムを実装するために必要なすべてのインターフェースを定義する。D3 の型ヘルパー（`SVG`・`SVGGroup`・`HTML`）や `DrawDefinition`・`ParserDefinition` も含む。

---

## packages/mermaid — dagre-wrapper

### packages/mermaid/src/dagre-wrapper/blockArrowHelper.ts

ブロック図で使用するブロック矢印形状の頂点座標を計算する `getArrowPoints` 関数を提供する。方向の組み合わせ（`x`/`y`/`up`/`down`/`left`/`right`）に応じて、四方向・三方向・二方向・一方向の矢印形状の多角形頂点リストを返す。

### packages/mermaid/src/dagre-wrapper/edgeMarker.ts

SVG パス要素にエッジの矢印マーカー（`marker-start`/`marker-end` 属性）を設定するユーティリティ。`arrowTypesMap` でエッジ矢印種別を内部 marker 名にマッピングし、`addEdgeMarkers` 関数で始端・終端に適切な SVG マーカー参照 URL を付与する。

---

## packages/mermaid — diagrams/common

### packages/mermaid/src/diagrams/common/common.ts

全ダイアグラム共通のユーティリティ関数群。DOMPurify を使ったテキストサニタイズ（`sanitizeText`）、`<br>` タグ処理、KaTeX 数式レンダリング、`getRows`・`getMin`・`getMax`、TypeScript ジェネリック型のパース（`parseGenericTypes`）などを提供する。セキュリティレベルに応じてサニタイズ方法を切り替える。

### packages/mermaid/src/diagrams/common/commonDb.ts

全ダイアグラム DB で共有されるアクセシビリティタイトル・説明・ダイアグラムタイトルの状態管理モジュール。`setAccTitle`・`getAccTitle`・`setAccDescription`・`getAccDescription`・`setDiagramTitle`・`getDiagramTitle`・`clear` を提供する。テキストはサニタイズ処理を通す。

### packages/mermaid/src/diagrams/common/commonTypes.ts

SVG 描画処理共通で使用する型定義ファイル。矩形データ（`RectData`）・境界（`Bound`）・テキストデータ（`TextData`・`TextObject`）などのインターフェースと、d3 の SVG 要素を型付けした `D3RectElement`・`D3TextElement` などの型エイリアスを定義する。

### packages/mermaid/src/diagrams/common/populateCommonDb.ts

パーサーが生成した `DiagramAST` からアクセシビリティ説明・タイトル・ダイアグラムタイトルを抽出し、`DiagramDB` に書き込む `populateCommonDb` 関数を提供する。新しい PEG.js 系パーサーを使うダイアグラムが共通処理として呼び出す。

### packages/mermaid/src/diagrams/common/svgDrawCommon.ts

d3 を使って SVG 要素（矩形・テキスト・画像・埋め込み画像・ツールチップ）を描画する共通ヘルパー関数群。`drawRect`・`drawBackgroundRect`・`drawText`・`drawImage`・`drawEmbeddedImage`・`createTooltip` など。URL は `sanitize-url` でサニタイズする。

### packages/mermaid/src/diagrams/globalStyles.ts

ノードに表示するアイコン（Font Awesome 等）のスタイルを返す `getIconStyles` 関数のみを持つ小さなモジュール。`label-icon` クラスと `.node .label-icon path` に対する CSS を文字列として返す。

---

## packages/mermaid — diagrams/architecture

### packages/mermaid/src/diagrams/architecture/architectureDb.ts

アーキテクチャ図のデータ管理クラス `ArchitectureDB`。サービス・ジャンクション・グループ・エッジを内部 Map/配列で管理し、追加・取得メソッドを提供する。ID の重複や不正な親子関係はエラーで弾く。`getDataStructures()` では隣接リストと BFS による空間マップを遅延生成し、切断グラフにも対応する。D3 要素の登録・参照、設定取得、アクセシビリティ情報も保持する。

### packages/mermaid/src/diagrams/architecture/architectureDetector.ts

`/^\s*architecture/` に一致するテキストを検知し、`architectureDiagram.js` を非同期でロードする軽量なディテクター/ローダー定義ファイル。

### packages/mermaid/src/diagrams/architecture/architectureDiagram.ts

パーサー・DB（`ArchitectureDB` の新インスタンスを `get db()` で都度生成）・レンダラー・スタイルをまとめた `DiagramDefinition` エクスポートファイル。

### packages/mermaid/src/diagrams/architecture/architectureIcons.ts

`mermaid-architecture` プレフィックスの Iconify アイコンセットを定義。`database`・`server`・`disk`・`internet`・`cloud`・`unknown`・`blank` の7種類のインラインSVGアイコンを80×80の青背景でラップして提供する。

### packages/mermaid/src/diagrams/architecture/architectureParser.ts

`@mermaid-js/parser` の `parse('architecture', ...)` で AST を得てから `ArchitectureDB` にグループ・サービス・ジャンクション・エッジを投入する `ParserDefinition`。`yy` が `ArchitectureDB` インスタンスでない場合はエラーを投げる。

### packages/mermaid/src/diagrams/architecture/architectureRenderer.ts

Cytoscape.js + fcose レイアウトを使ってアーキテクチャ図を SVG に描画するレンダラー。空間マップから整列制約・相対配置制約を生成し、XY 方向エッジを `layoutstop` 後に90度曲げに補正する。描画は `drawServices`・`drawJunctions`・`drawEdges`・`drawGroups` に委譲する。

### packages/mermaid/src/diagrams/architecture/architectureStyles.ts

アーキテクチャ図用 CSS を生成する `DiagramStylesProvider`。エッジ色・幅、矢印色、グループ境界線の破線スタイル、アイコンテキストの Flexbox レイアウトを `ArchitectureStyleOptions` から動的に生成する。

### packages/mermaid/src/diagrams/architecture/architectureTypes.ts

アーキテクチャ図全体の型定義モジュール。方向（L/R/T/B）・方向ペア・整列種別・サービス/ジャンクション/グループ/エッジのインターフェイス、Cytoscape オーバーライド型、方向ユーティリティ関数群を一括エクスポートする。

### packages/mermaid/src/diagrams/architecture/svgDraw.ts

Cytoscape コアと DB を受け取り、エッジ・グループ・サービス・ジャンクションを SVG に直接描画するユーティリティ群。エッジは方向と矢印に応じて始終端を補正し、ラベルは軸（X/Y/XY）に応じて回転・配置する。サービスはアイコン SVG または `iconText`（foreignObject）を挿入し、グループは破線枠＋ラベルを描く。

---

## packages/mermaid — diagrams/block

### packages/mermaid/src/diagrams/block/blockDB.ts

ブロック図のデータベース。ブロックを `Map<string, Block>` で管理し、エッジリスト・クラス定義も保持する。`setHierarchy()` でパーサー出力を受け取り `populateBlockDatabase()` が再帰的にブロックを正規化・登録する。シェイプ文字列→型変換やエッジ文字列のデコード関数も提供する。

### packages/mermaid/src/diagrams/block/blockDetector.ts

`/^\s*block(-beta)?/` に一致するテキストを検知し、`blockDiagram.js` を動的ロードするディテクター/ローダー定義ファイル。

### packages/mermaid/src/diagrams/block/blockDiagram.ts

Jison パーサー・DB・レンダラー・スタイルを組み合わせた `DiagramDefinition` エクスポートファイル。

### packages/mermaid/src/diagrams/block/blockRenderer.ts

ブロック図の描画エントリポイント。`calculateBlockSizes` でノードの実寸を計測し、`layout()` で座標を決定後、`insertBlocks` と `insertEdges` で SVG に挿入する。最終的に `viewBox` を計算して SVG サイズを確定させる。

### packages/mermaid/src/diagrams/block/blockTypes.ts

ブロック図の型定義。`BlockType`（20種超のシェイプ名 union）・`Block` インターフェイス（id/label/type/children/size/styles 等）・`ClassDef` インターフェイス・`Direction` 型を定義する。

### packages/mermaid/src/diagrams/block/blockUtils.ts

ブロック図パース前処理ユーティリティ。行頭・行末の余分な空白や重複した改行を除去して Jison パーサーに渡すテキストを正規化する `prepareTextForParsing` 関数のみを提供する。

### packages/mermaid/src/diagrams/block/layout.ts

ブロック図のレイアウトエンジン。`setBlockSizes()` でツリーを深さ優先探索して各ブロックの幅・高さを確定し、`layoutBlocks()` で列数と行ごとの最大高を考慮しながら x/y 座標を計算する。`findBounds()` で全ブロックの外接矩形を求め、最終的な `{x, y, width, height}` を返す。

### packages/mermaid/src/diagrams/block/renderHelpers.ts

ブロック図描画のヘルパー群。`calculateBlockSizes` で各ノードを DOM に一時挿入して BBox を取得し、`insertBlocks` で座標付きノードを配置し、`insertEdges` で各エッジをグラフライブラリ経由で描画する。エッジのスタイル（thick/dotted 等）も適切なクラスとして付与する。

### packages/mermaid/src/diagrams/block/styles.ts

ブロック図用 CSS を生成する `DiagramStylesProvider`。ノード形状・エッジ・ラベル・クラスタ・ツールチップ等のスタイルを `BlockChartStyleOptions` のテーマ変数から生成する。フローチャートとほぼ共通の CSS 構造を持つ。

---

## packages/mermaid — diagrams/c4

### packages/mermaid/src/diagrams/c4/c4Detector.ts

`C4Context`・`C4Container`・`C4Component`・`C4Dynamic`・`C4Deployment` のいずれかで始まるテキストを検知し、`c4Diagram.js` を動的ロードするディテクター/ローダー定義ファイル。

### packages/mermaid/src/diagrams/c4/c4Diagram.ts

C4図の `DiagramDefinition`。Jison パーサー・`c4Db`・`c4Renderer`・スタイルを結合し、`init` フックで `renderer.setConf(c4)` と `db.setWrap(wrap)` を設定する。

---

## packages/mermaid — diagrams/class

### packages/mermaid/src/diagrams/class/classDb.ts

クラス図のデータ管理クラス `ClassDB`。クラス・関係・ノート・インターフェイス・名前空間を保持し、メンバ追加・CSS クラス適用・ツールチップ・クリックイベント・リンク設定などのメソッドを提供する。`getData()` でレイアウト用 `{nodes, edges}` を構築し、階層/コンパクト名前空間モードにも対応する。

### packages/mermaid/src/diagrams/class/classDetector-V2.ts

`classDiagram-v2` または `classDiagram`（dagre-wrapper設定時）に一致するテキストを検知し、`classDiagram-v2.js` を動的ロードするディテクター/ローダー定義ファイル。

### packages/mermaid/src/diagrams/class/classDetector.ts

`classDiagram` に一致するテキストを検知するが、`dagre-wrapper` または `elk` 設定時は常に `false` を返すレガシー（v1）クラス図ディテクター。

### packages/mermaid/src/diagrams/class/classDiagram-v2.ts

`ClassDB` の新インスタンスを `get db()` で都度生成し、Jison パーサー・`classRenderer-v3-unified`・スタイルを組み合わせた v2 クラス図の `DiagramDefinition`。`init` フックで `arrowMarkerAbsolute` を設定する。

### packages/mermaid/src/diagrams/class/classDiagram.ts

`classDiagram-v2.ts` と内容が同一。同じ `DiagramDefinition` を `classDiagram.ts` の名前でもエクスポートしている（レガシー名称への対応）。

### packages/mermaid/src/diagrams/class/classRenderer-v2.ts

dagre-wrapper を使ったクラス図レンダラー（v2）。`addNamespaces`・`addClasses`・`addNotes`・`addRelations` で graphlib グラフを構築し、`render()` で SVG を生成する。階層/コンパクト名前空間モードの切り替え、エッジラベルの非HTMLモード対応なども含む。

### packages/mermaid/src/diagrams/class/classRenderer-v3-unified.ts

統合レンダリングパイプライン（`rendering-util/render.js`）を使う最新クラス図レンダラー。`getData()` からレイアウトデータを取得し、`getRegisteredLayoutAlgorithm` でレイアウトアルゴリズムを選択して `render()` に委譲する。

### packages/mermaid/src/diagrams/class/classTypes.ts

クラス図の型定義群。`ClassNode`・`ClassMember`（属性・メソッドのパース/表示ロジック付きクラス）・`ClassNote`・`ClassRelation`・`Interface`・`NamespaceNode`・`StyleClass` と対応する Map 型エイリアスを提供する。

### packages/mermaid/src/diagrams/class/shapeUtil.ts

クラス図ノードの SVG 描画ヘルパー `textHelper`。アノテーション・ラベル・メンバー・メソッドの各グループを順に生成・配置し、HTML/非HTMLラベル・KaTeX・画像に対応する。`addText` 内部関数で `createText()` を呼び出しフォント重みや HTML エンティティを補正する。

---

## packages/mermaid — diagrams/cynefin

### packages/mermaid/src/diagrams/cynefin/cynefinBoundaries.ts

Cynefin 図の境界線 SVG パス生成ユーティリティ。シード値付き擬似乱数（mulberry32）で決定論的な波線を生成する `generateFoldPath`・`generateHorizontalBoundary`・`generateCliffPath`・`generateConfusionPath` を提供する。`resolveSeed` でコンフィグのシードまたは SVG ID のハッシュを使い再現性を保証する。

### packages/mermaid/src/diagrams/cynefin/cynefinDb.ts

Cynefin 図のデータストア。ドメイン（`complex`/`complicated`/`clear`/`chaotic`/`confusion`）とトランジションを保持し、自己ループのトランジションをフィルタリングする。設定は `defaultConfig.cynefin` とユーザー設定をマージして提供する。

### packages/mermaid/src/diagrams/cynefin/cynefinDetector.ts

`/^\s*cynefin-beta/` に一致するテキストを検知し、`cynefinDiagram.js` を動的ロードするディテクター/ローダー定義ファイル。

### packages/mermaid/src/diagrams/cynefin/cynefinDiagram.ts

Cynefin 図の `DiagramDefinition`。パーサー・DB・レンダラー・スタイルを一括エクスポートする薄いアセンブリファイル。

### packages/mermaid/src/diagrams/cynefin/cynefinParser.ts

`@mermaid-js/parser` の `parse('cynefin', ...)` で AST を生成し、`db.setDomains()` と `db.setTransitions()` に投入する `ParserDefinition`。

### packages/mermaid/src/diagrams/cynefin/cynefinRenderer.ts

Cynefin フレームワーク図を SVG に描画するレンダラー。背景矩形→波線境界→崖ライン→混乱楕円→ドメインラベル→サブタイトル→アイテムバッジ→トランジション矢印→タイトルの順に描画する。アイテムバッジは `getBBox()` で実測幅を取得し、混乱ドメインは最大3件までに制限してオーバーフローバッジを表示する。

### packages/mermaid/src/diagrams/cynefin/styles.ts

Cynefin 図用 CSS を生成する `DiagramStylesProvider`。テーマ変数からフォントサイズ・境界線色・幅・矢印色などを取得し、ドメイン背景・ラベル・境界線・崖・矢印・アイテムバッジ等の各クラスにスタイルを適用する。

### packages/mermaid/src/diagrams/cynefin/types.ts

Cynefin 図の型定義。`DomainName` ユニオン、`CynefinItem`・`CynefinDomain`・`CynefinTransition` インターフェイス、DB インターフェイス `CynefinDB` を定義する。

---

## packages/mermaid — diagrams/er

### packages/mermaid/src/diagrams/er/erDb.ts

ER 図のデータ管理クラス `ErDB`。エンティティ（属性付き）・リレーションシップ・CSS クラスを保持し、`getData()` でレイアウト用ノード/エッジを構築する。カーディナリティ（ZERO_OR_ONE〜MD_PARENT）と識別関係/非識別関係に対応し、エッジのパターン（solid/dashed）をリレーションタイプから決定する。

### packages/mermaid/src/diagrams/er/erDetector.ts

`/^\s*erDiagram/` に一致するテキストを検知し、`erDiagram.js` を動的ロードするディテクター/ローダー定義ファイル。

### packages/mermaid/src/diagrams/er/erDiagram.ts

Jison パーサー・`ErDB` 新インスタンス（`get db()`）・`erRenderer-unified`・スタイルを組み合わせた ER 図の `DiagramDefinition`。

### packages/mermaid/src/diagrams/er/erRenderer-unified.ts

統合レンダリングパイプラインを使う ER 図レンダラー。ELK レイアウト時はエッジを前面に移動し、手書きスタイル用のバックグラウンドノードをオリジナルと同じ transform に配置するなど特殊処理を含む。

### packages/mermaid/src/diagrams/er/erTypes.ts

ER 図の型定義。`EntityNode`（属性・エイリアス・CSS スタイル付き）・`Attribute`（type/name/keys/comment）・`Relationship`・`RelSpec`（カーディナリティ・リレーション種別）・`EntityClass` インターフェイスを定義する。

### packages/mermaid/src/diagrams/er/styles.ts

ER 図用 CSS を生成する `DiagramStylesProvider`。`redux-color`/`redux-dark-color` テーマ時はカラーインデックスごとの動的セレクタを生成し、エンティティボックス・関係線・エッジラベル・マーカー等のスタイルをテーマ変数から組み立てる。

---

## packages/mermaid — diagrams/error

### packages/mermaid/src/diagrams/error/errorDiagram.ts

構文エラー時に表示するダミー図の `DiagramDefinition`。空の DB と何もしない `parse()` を持ち、レンダラーのみ実際の描画処理（`errorRenderer`）に委ねる。

### packages/mermaid/src/diagrams/error/errorRenderer.ts

mermaid の構文エラー時に「Syntax error in text」と mermaid バージョンを表示する SVG を描画するレンダラー。SVG の `viewBox` を `0 0 2412 512` に固定し、レンチ型アイコンの SVG パスと2行のテキストを描画する。

---

## packages/mermaid — diagrams/eventmodeling

### packages/mermaid/src/diagrams/eventmodeling/db.ts

イベントモデリング図のデータベース。CQRS/イベントソーシングパターン（decide→evolve→dispatch サイクル）でフレーム位置とリレーション位置を状態として蓄積する。スイムレーン（UI/Automation・Command/ReadModel・Events の3層）とボックスの座標を計算し、テキスト幅は `calculateTextDimensions` で推定する。

### packages/mermaid/src/diagrams/eventmodeling/detector.ts

`/^\s*eventmodeling/` に一致するテキストを検知し、`diagram.js` を動的ロードするディテクター/ローダー定義ファイル。

### packages/mermaid/src/diagrams/eventmodeling/diagram.ts

パーサー・DB・レンダラー・スタイルを組み合わせたイベントモデリング図の `DiagramDefinition`。

### packages/mermaid/src/diagrams/eventmodeling/parser.ts

`@mermaid-js/parser` の `parse('eventmodeling', ...)` で AST を生成し `db.setAst()` に渡す `ParserDefinition`。

### packages/mermaid/src/diagrams/eventmodeling/renderer.ts

イベントモデリング図の SVG 描画エントリポイント。スイムレーン背景→ボックス→リレーション矢印の順で D3 を使って描画する。矢印は上下方向を判定して Y 座標の付け根を変え、`foreignObject` でリッチテキストをボックス内に配置する。

### packages/mermaid/src/diagrams/eventmodeling/types.ts

イベントモデリング図の型定義群。`Box`・`Swimlane`・`Relation`・`Context`（状態）・コマンド・イベント・`Deciders`/`Evolvers` 型を定義する。

---

## packages/mermaid — diagrams/flowchart

### packages/mermaid/src/diagrams/flowchart/elk/detector.ts

`flowchart-elk` または `flowchart`/`graph` で `defaultRenderer=elk` の設定時に ELK レイアウトを選択するディテクター。`config.layout = 'elk'` を副作用として設定し `flowDiagram.js` をロードする。

### packages/mermaid/src/diagrams/flowchart/flowDb.ts

フローチャート図の最大規模データ管理クラス `FlowDB`。頂点（ノード）・エッジ・CSS クラス・サブグラフ・ツールチップ・クリックイベント・リンクを管理する。YAML メタデータからシェイプ/アイコン/画像などを取得し、`getData()` でレイアウト用 `{nodes, edges}` を構築する。Jison 向けに全メソッドをバインドしている。

### packages/mermaid/src/diagrams/flowchart/flowDetector-v2.ts

`flowchart` キーワードまたは `graph`+dagre-wrapper設定時を検知する v2 ディテクター。ELK 設定時は `config.layout='elk'` を設定する。`flowDiagram.js` をロードする。

### packages/mermaid/src/diagrams/flowchart/flowDetector.ts

`graph` キーワードを検知するレガシー（v1）フローチャートディテクター。`dagre-wrapper` または `elk` 設定時は `false` を返す。

### packages/mermaid/src/diagrams/flowchart/flowDiagram.ts

`FlowDB` 新インスタンス・flowParser・`flowRenderer-v3-unified`・スタイルを組み合わせたフローチャートの `DiagramDefinition`。`init` フックで `arrowMarkerAbsolute` と `layout` 設定を同期する。

### packages/mermaid/src/diagrams/flowchart/flowRenderer-v3-unified.ts

統合レンダリングパイプラインを使うフローチャートレンダラー（v3）。`getData()` からレイアウトデータを取得し、ELK レイアウトのフォールバック警告、方向・スペーシング・マーカー等を設定して `render()` に委譲する。タイトルと `setupViewPortForSVG` でビューポートを調整する。

### packages/mermaid/src/diagrams/flowchart/parser/flowParser.ts

Jison 生成の `flow.jison` パーサーをラップし、`}\s*\n` を `}\n` に正規化してから解析するカスタムパーサー定義。YAML メタデータ内の不要な空白を除去するための前処理が目的。

### packages/mermaid/src/diagrams/flowchart/styles.ts

フローチャート用 CSS を生成する `DiagramStylesProvider`。ノード形状・エッジ・ラベル・クラスタ・ツールチップ・アイコン形状・画像形状等のスタイルを `FlowChartStyleOptions` テーマ変数から組み立てる。

### packages/mermaid/src/diagrams/flowchart/types.ts

フローチャートの型定義。`FlowVertexTypeParam`（シェイプ名 union）・`FlowVertex`（アイコン/画像/制約など拡張済み）・`FlowText`・`FlowEdge`（アニメーション対応）・`FlowClass`・`FlowSubGraph`・`FlowLink` を定義する。

---

## packages/mermaid — diagrams/gantt

### packages/mermaid/src/diagrams/gantt/ganttDetector.ts

gantt ダイアグラムの検出器とローダーを定義するファイル。テキストが `/^\s*gantt/` にマッチするかで判定し、マッチした場合に `ganttDiagram.js` を動的インポートする `ExternalDiagramDefinition` としてエクスポートされる。

### packages/mermaid/src/diagrams/gantt/ganttDiagram.ts

gantt ダイアグラムの定義をまとめるファイル。JISON パーサー、`ganttDb`、`ganttRenderer`、`ganttStyles` を一つの `DiagramDefinition` オブジェクトに組み立てる。

---

## packages/mermaid — diagrams/git

### packages/mermaid/src/diagrams/git/gitGraphAst.ts

gitGraph ダイアグラムのデータベース（状態管理）本体。`ImperativeState` でコミット・ブランチ・HEAD などを管理し、`commit`・`branch`・`merge`・`cherryPick`・`checkout` などの操作を実装する。全操作はサニタイズ処理とバリデーションを通じて行われる。

### packages/mermaid/src/diagrams/git/gitGraphDetector.ts

`/^\s*gitGraph/` にマッチするかで gitGraph ダイアグラムを検出し、`gitGraphDiagram.js` を遅延ロードする標準的な Detector/Loader。

### packages/mermaid/src/diagrams/git/gitGraphDiagram.ts

gitGraph ダイアグラムの定義をまとめるファイル。パーサー・DB・レンダラー・スタイルを `DiagramDefinition` として組み立てる。

### packages/mermaid/src/diagrams/git/gitGraphParser.ts

Langium ベースのパーサーで gitGraph の AST を受け取り、DB 操作に変換する。`Commit`・`Branch`・`Merge`・`Checkout`・`CherryPicking` の各ステートメントを対応する DB メソッドに変換する `populate` 関数を持ち、in-source Vitest テストも含む。

### packages/mermaid/src/diagrams/git/gitGraphRenderer.ts

D3 を使って gitGraph を SVG に描画するレンダラー。ブランチの位置計算、コミットバレット（各種形状）の描画、コミットラベル・タグ、ブランチ間の矢印線、ブランチラベルを描画する。LR/TB/BT の3方向に対応し、redux/neo テーマの特殊処理も含む。

### packages/mermaid/src/diagrams/git/gitGraphTypes.ts

gitGraph ダイアグラムの全型定義ファイル。`commitType` 定数、`Commit`・`BranchDB`・`MergeDB`・`CherryPickDB` などのデータ型、`GitGraphDB`・`GitGraphDBParseProvider`・`GitGraphDBRenderProvider` の各インターフェース、および `DiagramOrientation` 型を定義する。

---

## packages/mermaid — diagrams/info

### packages/mermaid/src/diagrams/info/infoDb.ts

info ダイアグラムの DB。mermaid のバージョン文字列（`injected.version`）を保持し、`getVersion()` を提供する。非常にシンプルな read-only DB。

### packages/mermaid/src/diagrams/info/infoDetector.ts

`/^\s*info/` にマッチするかで info ダイアグラムを検出し、`infoDiagram.js` を遅延ロードする標準的な Detector/Loader。

### packages/mermaid/src/diagrams/info/infoDiagram.ts

info ダイアグラムの定義をまとめる。パーサー・DB・レンダラーを `DiagramDefinition` として組み立てる（スタイルは未定義）。

### packages/mermaid/src/diagrams/info/infoParser.ts

Langium の `parse('info', input)` を呼び出すだけのシンプルなパーサー。AST をログに出力するのみで DB への反映は行わない。

### packages/mermaid/src/diagrams/info/infoRenderer.ts

info ダイアグラムの SVG 描画。SVG に mermaid のバージョン番号をテキストとして表示するだけのシンプルなレンダラー。

### packages/mermaid/src/diagrams/info/infoTypes.ts

info ダイアグラムの型定義ファイル。`InfoFields`（`version` フィールド）と `InfoDB`（`getVersion` メソッド）を定義する最小限の型定義。

---

## packages/mermaid — diagrams/ishikawa

### packages/mermaid/src/diagrams/ishikawa/ishikawaDb.ts

石川（フィッシュボーン）ダイアグラムの DB クラス。テキスト行とインデントレベルを受け取り、スタックベースのツリー構造（`IshikawaNode`）を構築する `addNode` メソッドを持つ。最初の行が効果（頭）として `diagramTitle` に設定される。

### packages/mermaid/src/diagrams/ishikawa/ishikawaDetector.ts

`/^\s*ishikawa(-beta)?\b/i` にマッチするかで石川ダイアグラムを検出し、`ishikawaDiagram.js` を遅延ロードする。

### packages/mermaid/src/diagrams/ishikawa/ishikawaDiagram.ts

石川ダイアグラムの定義をまとめる。JISON パーサー、毎回インスタンス生成される `IshikawaDB`、レンダラー、スタイルを `DiagramDefinition` に組み立てる。

### packages/mermaid/src/diagrams/ishikawa/ishikawaRenderer.ts

石川（魚の骨）ダイアグラムの SVG レンダラー。脊椎（スパイン）・大骨（ブランチ）・小骨（サブブランチ）を D3 で描画し、handDrawn モードでは rough.js を使用してスケッチ風に描く。原因ノードの再帰的なツリー構造をフラット化して描画する工夫がある。

### packages/mermaid/src/diagrams/ishikawa/ishikawaStyles.ts

石川ダイアグラムの CSS スタイル定義。脊椎・骨・矢印・頭部・ラベルボックス・テキストの各スタイルをテーマ変数を用いて生成する。

### packages/mermaid/src/diagrams/ishikawa/ishikawaTypes.ts

石川ダイアグラムの型定義。`text: string` と `children: IshikawaNode[]` だけを持つシンプルな再帰ノード型 `IshikawaNode` を定義する。

---

## packages/mermaid — diagrams/kanban

### packages/mermaid/src/diagrams/kanban/detector.ts

`/^\s*kanban/` にマッチするかでカンバンダイアグラムを検出し、`kanban-definition.js` を遅延ロードする。

### packages/mermaid/src/diagrams/kanban/kanban-definition.ts

カンバンダイアグラムの定義をまとめる。JISON パーサー、DB、レンダラー、スタイルを `DiagramDefinition` に組み立てる。

### packages/mermaid/src/diagrams/kanban/kanbanDb.ts

カンバンダイアグラムの DB。セクション（列）とアイテムの2レベル構造を管理する。YAML メタデータ（アイコン・担当者・チケット・優先度等）を各ノードに付与し、`getData()` でレイアウトエンジン用のノード/エッジ配列を返す。

### packages/mermaid/src/diagrams/kanban/kanbanRenderer.ts

カンバンダイアグラムのレンダラー。各セクションを列として配置し、セクション内アイテムを縦に並べる。`insertCluster` でセクション枠を、`insertNode` で各アイテムを描画し、ラベル高さに応じて列高さを動的に調整する。

### packages/mermaid/src/diagrams/kanban/kanbanTypes.ts

カンバンダイアグラムの DB 型定義。`kanbanDb` の型を `typeof kanbanDb` でエクスポートする1行のシンプルな型ファイル。

### packages/mermaid/src/diagrams/kanban/styles.ts

カンバンダイアグラムの CSS スタイル定義。`THEME_COLOR_LIMIT` 分のセクション色（塗りつぶし・テキスト・エッジ）をループで生成し、アイコンコンテナのスタイルも含む。

---

## packages/mermaid — diagrams/mindmap

### packages/mermaid/src/diagrams/mindmap/detector.ts

`/^\s*mindmap/` にマッチするかでマインドマップダイアグラムを検出し、`mindmap-definition.js` を遅延ロードする。

### packages/mermaid/src/diagrams/mindmap/mindmap-definition.ts

マインドマップダイアグラムの定義。毎回 `new MindmapDB()` でインスタンス生成される DB と、JISON パーサー、レンダラー、スタイルを `DiagramDefinition` に組み立てる。

### packages/mermaid/src/diagrams/mindmap/mindmapDb.ts

マインドマップの DB クラス。ノードのツリー構造管理（`addNode`・`getParent`）、セクション番号の割り当て（`assignSections`）、フラット化（`flattenNodes`）、エッジ生成（`generateEdges`）を行い、`getData()` でレイアウトエンジン用の `LayoutData` を返す。デフォルトレイアウトは `cose-bilkent`。

### packages/mermaid/src/diagrams/mindmap/mindmapRenderer.ts

マインドマップのレンダラー。`getData()` でレイアウトデータを取得し、統合レンダリングシステム（`render()`）に渡す。neo テーマ用のリニアグラデーションを `<defs>` に追加し、`setupViewPortForSVG` でビューポートを設定する。

### packages/mermaid/src/diagrams/mindmap/mindmapTypes.ts

マインドマップノードの型定義。`id`・`level`・`descr`・`type`・`children` 等を持つ `MindmapNode` インターフェースと、全フィールドを必須化した `FilledMindMapNode` 型を定義する。

### packages/mermaid/src/diagrams/mindmap/styles.ts

マインドマップの CSS スタイル定義。`THEME_COLOR_LIMIT` 分のセクション色をループで生成し、neo テーマ用のグラデーション・ドロップシャドウ処理、redux/neutral テーマの特殊分岐も含む。

### packages/mermaid/src/diagrams/mindmap/svgDraw.ts

マインドマップノードの各形状（デフォルト・矩形・角丸矩形・円・クラウド・バング・六角形）を SVG に描画する関数群。`drawNode` がノードタイプに応じて形状を描画し、テキスト・アイコンを配置して高さを返す。`positionNode` でノードを座標に配置する。

---

## packages/mermaid — diagrams/packet

### packages/mermaid/src/diagrams/packet/db.ts

パケット（ネットワークパケット図）ダイアグラムの DB クラス。`PacketWord[]` のリストを管理し、設定（`showBits`・`bitsPerRow` 等）を提供する。`pushWord` と `getPacket` が主要メソッド。

### packages/mermaid/src/diagrams/packet/detector.ts

`/^\s*packet(-beta)?/` にマッチするかでパケットダイアグラムを検出し、`diagram.js` を遅延ロードする。

### packages/mermaid/src/diagrams/packet/diagram.ts

パケットダイアグラムの定義。毎回 `new PacketDB()` でインスタンス生成される DB、パーサー、レンダラー、スタイルを組み立てる。

### packages/mermaid/src/diagrams/packet/parser.ts

Langium パーサーで Packet AST を取得し、ブロックを行（`PacketWord`）に分割して DB に反映する。連続性チェック・ゼロビットチェック・最大パケット数制限を含む。

### packages/mermaid/src/diagrams/packet/renderer.ts

パケットダイアグラムのレンダラー。ビット数・行高さに基づいて SVG の viewBox を計算し、各ブロックを矩形＋ラベル＋ビット番号で描画する。`showBits` 設定でビット番号表示を切り替える。

### packages/mermaid/src/diagrams/packet/styles.ts

パケットダイアグラムの CSS スタイル定義。バイト番号・ラベル・タイトル・ブロックの各色・フォントサイズを設定オプションから生成する。

### packages/mermaid/src/diagrams/packet/types.ts

パケットダイアグラムの型定義。`PacketBlock`・`PacketWord`・`PacketDB`・`PacketStyleOptions`・`PacketData` インターフェースを定義する。

---

## packages/mermaid — diagrams/pie

### packages/mermaid/src/diagrams/pie/pieDb.ts

円グラフダイアグラムの DB。セクション名と値の `Map` を管理し、負の値を拒否する `addSection`、`showData` フラグの取得・設定、設定値の取得を提供する。

### packages/mermaid/src/diagrams/pie/pieDetector.ts

`/^\s*pie/` にマッチするかで円グラフダイアグラムを検出し、`pieDiagram.js` を遅延ロードする。

### packages/mermaid/src/diagrams/pie/pieDiagram.ts

円グラフダイアグラムの定義をまとめる。パーサー・DB・レンダラー・スタイルを `DiagramDefinition` に組み立てる。

### packages/mermaid/src/diagrams/pie/pieParser.ts

Langium の `parse('pie', input)` でAST取得後、`populateCommonDb` と `db.addSection`・`db.setShowData` で DB に反映する。

### packages/mermaid/src/diagrams/pie/pieRenderer.ts

D3 を使って円グラフを描画するレンダラー。スライス・パーセンテージラベル・凡例・タイトルを描画し、タイトル幅を考慮して viewBox を動的に調整する。1%未満のスライスはフィルタリングして除外する。

### packages/mermaid/src/diagrams/pie/pieStyles.ts

円グラフの CSS スタイル定義。スライス・外枠・タイトル・凡例テキストのスタイルをテーマ変数から生成する。

### packages/mermaid/src/diagrams/pie/pieTypes.ts

円グラフの型定義。`PieFields`・`PieStyleOptions`・`Sections`（`Map<string,number>`）・`D3Section`・`PieDB` インターフェースを定義する。

---

## packages/mermaid — diagrams/quadrant-chart

### packages/mermaid/src/diagrams/quadrant-chart/quadrantBuilder.ts

クワドラントチャートの座標計算ビルダークラス。軸ラベル・象限・データポイント・境界線・タイトルの座標を d3 の `scaleLinear` で計算し、`build()` で描画用データを返す。設定・テーマ設定・データを独立して管理する。

### packages/mermaid/src/diagrams/quadrant-chart/quadrantDb.ts

クワドラントチャートの DB。パーサーから呼ばれるセッター群（象限テキスト・軸テキスト・ポイント・クラス・サイズ）を持ち、`getQuadrantData()` で `QuadrantBuilder.build()` の結果を返す。

### packages/mermaid/src/diagrams/quadrant-chart/quadrantDetector.ts

`/^\s*quadrantChart/` にマッチするかでクワドラントチャートを検出し、`quadrantDiagram.js` を遅延ロードする。

### packages/mermaid/src/diagrams/quadrant-chart/quadrantDiagram.ts

クワドラントチャートの定義。JISON パーサー・DB・レンダラーを組み立てる。スタイルは空文字列を返す関数。

### packages/mermaid/src/diagrams/quadrant-chart/quadrantRenderer.ts

クワドラントチャートの SVG レンダラー。タイトル・境界線・象限・軸ラベル・データポイントをそれぞれ `<g>` グループに分けて D3 で描画する。

### packages/mermaid/src/diagrams/quadrant-chart/utils.ts

クワドラントチャートのバリデーションユーティリティ。16進カラーコード・数値・ピクセル値の検証関数と、カスタムエラークラス `InvalidStyleError` を提供する。

---

## packages/mermaid — diagrams/radar

### packages/mermaid/src/diagrams/radar/db.ts

レーダーチャートの DB。軸（`Axis[]`）・曲線（`Curve[]`）・オプション（表示設定）を管理する。曲線エントリは軸参照（unordered）と位置参照（ordered）の両形式をサポートし、軸順にソートして返す。

### packages/mermaid/src/diagrams/radar/detector.ts

`/^\s*radar-beta/` にマッチするかでレーダーチャートを検出し、`diagram.js` を遅延ロードする。

### packages/mermaid/src/diagrams/radar/diagram.ts

レーダーチャートの定義をまとめる。パーサー・DB・レンダラー・スタイルを `DiagramDefinition` に組み立てる。

### packages/mermaid/src/diagrams/radar/parser.ts

Langium の `parse('radar', input)` でAST取得後、`db.setAxes`・`db.setCurves`・`db.setOptions` で DB に反映する。

### packages/mermaid/src/diagrams/radar/renderer.ts

レーダーチャートのレンダラー。中心に座標系を置き、グラティキュール（円または多角形）・軸線・軸ラベル・曲線（Catmull-Rom スプライン）・凡例・タイトルを描画する。

### packages/mermaid/src/diagrams/radar/styles.ts

レーダーチャートの CSS スタイル定義。テーマの `cScale` 色配列を使って各曲線・凡例ボックスのインデックス別スタイルをループ生成し、タイトル・軸・グラティキュールのスタイルも出力する。

### packages/mermaid/src/diagrams/radar/types.ts

レーダーチャートの型定義。`RadarAxis`・`RadarCurve`・`RadarOptions`・`RadarDB`・`RadarStyleOptions`・`RadarData` インターフェースを定義する。

---

## packages/mermaid — diagrams/railroad

### packages/mermaid/src/diagrams/railroad/abnfDetector.ts

`/^\s*railroad-abnf/i` にマッチするかで ABNF 形式の鉄道図を検出し、`abnfDiagram.js` を遅延ロードする。

### packages/mermaid/src/diagrams/railroad/abnfDiagram.ts

ABNF 鉄道図の定義。ABNF パーサー・共通 DB・レンダラー・スタイルを `DiagramDefinition` に組み立てる。

### packages/mermaid/src/diagrams/railroad/ebnfDetector.ts

`/^\s*railroad-ebnf/i` にマッチするかで EBNF 形式の鉄道図を検出し、`ebnfDiagram.js` を遅延ロードする。

### packages/mermaid/src/diagrams/railroad/ebnfDiagram.ts

EBNF 鉄道図の定義。EBNF パーサー・共通 DB・レンダラー・スタイルを `DiagramDefinition` に組み立てる。

### packages/mermaid/src/diagrams/railroad/parser/abnfParser.ts

Langium で ABNF 文法をパースし、alternation/concatenation/element/primary の各ノードをレールロード共通 AST（terminal/nonterminal/sequence/choice/optional/repetition）に変換して DB に追加するパーサー。

### packages/mermaid/src/diagrams/railroad/parser/ebnfParser.ts

Langium で EBNF 文法をパースし、choice/sequence/primary/postfix ノードをレールロード共通 AST に変換して DB に追加するパーサー。例外記法（`-`）は sequence として変換する。

### packages/mermaid/src/diagrams/railroad/parser/pegParser.ts

Langium で PEG 文法をパースし、OrderedChoice/Sequence/Prefix（`&`・`!` 先読み）/Suffix（`?`・`*`・`+`）をレールロード共通 AST に変換して DB に追加するパーサー。

### packages/mermaid/src/diagrams/railroad/parser/railroadParser.ts

Langium でレールロード固有記法をパースし、Terminal/NonTerminal/Special/Sequence/Choice/Optional/OneOrMore/ZeroOrMore の各ノードを共通 AST に変換して DB に追加するパーサー。

### packages/mermaid/src/diagrams/railroad/pegDetector.ts

`/^\s*railroad-peg/i` にマッチするかで PEG 形式の鉄道図を検出し、`pegDiagram.js` を遅延ロードする。

### packages/mermaid/src/diagrams/railroad/pegDiagram.ts

PEG 鉄道図の定義。PEG パーサー・共通 DB・レンダラー・スタイルを `DiagramDefinition` に組み立てる。

### packages/mermaid/src/diagrams/railroad/railroadDb.ts

鉄道図の共通 DB。ルール（`RailroadRule`）をリストと Map で管理し、テキストのサニタイズを行う。タイトル・アクセシビリティタイトル/説明も管理する。複数のパーサー（ABNF/EBNF/PEG/railroad）が共有する。

### packages/mermaid/src/diagrams/railroad/railroadDetector.ts

`/^\s*railroad-diagram/i` にマッチするかで標準鉄道図を検出し、`railroadDiagram.js` を遅延ロードする。

### packages/mermaid/src/diagrams/railroad/railroadDiagram.ts

標準鉄道図の定義。鉄道パーサー・DB・レンダラー・スタイルを `DiagramDefinition` に組み立てる。

### packages/mermaid/src/diagrams/railroad/railroadRenderer.ts

鉄道図の SVG レンダラー。`RailroadRenderer` クラスが terminal（角丸矩形）・nonterminal（矩形）・sequence・choice・optional・repetition・special の各ノードを再帰的に描画する。`PathBuilder` ユーティリティで SVG パスを組み立て、各ルールをスタート/エンドマーカー付きで配置する。

### packages/mermaid/src/diagrams/railroad/railroadTypes.ts

鉄道図の型定義。AST ノード・`RailroadRule`・`RailroadStyleOptions`（レイアウト・色・フォント等の完全なオプション）・`DEFAULT_RAILROAD_CONFIG`・`RailroadDB` インターフェースを定義する。

### packages/mermaid/src/diagrams/railroad/styles.ts

鉄道図の CSS スタイル生成。テーマ変数から `buildRailroadStyleOptions()` でスタイル設定を組み立て、terminal・nonterminal・line・marker・comment・special・rule-name の各要素のスタイルを生成する。セキュリティのため色値・フォントファミリー・数値の入力値を正規表現で検証する。

---

## packages/mermaid — diagrams/requirement

### packages/mermaid/src/diagrams/requirement/requirementDb.ts

要求図（Requirement Diagram）の DB クラス。`Requirement`・`Element`・`Relation` の3種類のデータを管理し、`getData()` で統合レンダリングシステム用のノード/エッジ配列を返す。CSS クラス・スタイルの適用機能、方向設定も持つ。

### packages/mermaid/src/diagrams/requirement/requirementDetector.ts

`/^\s*requirement(Diagram)?/` にマッチするかで要求図を検出し、`requirementDiagram.js` を遅延ロードする。

### packages/mermaid/src/diagrams/requirement/requirementDiagram.ts

要求図の定義をまとめる。JISON パーサー、毎回インスタンス生成される `RequirementDB`、レンダラー、スタイルを `DiagramDefinition` に組み立てる。

### packages/mermaid/src/diagrams/requirement/requirementRenderer.ts

要求図のレンダラー。統合レンダリングシステム（`render()`）を使用し、`requirementBox` 形状ノードとリレーションシップエッジを描画する。neo テーマ用の専用マーカーを使い分け、`setupViewPortForSVG` でビューポートを設定する。

### packages/mermaid/src/diagrams/requirement/types.ts

要求図の型定義。`RequirementType`・`RiskLevel`・`VerifyType`・`Requirement`・`RelationshipType`・`Relation`・`Element`・`RequirementClass` を定義する。

---

## packages/mermaid — diagrams/sankey

### packages/mermaid/src/diagrams/sankey/sankeyDB.ts

Sankey ダイアグラムのデータストア。`SankeyNode` と `SankeyLink` のクラスを定義し、ノードの一意性を Map で管理する。`addLink` でリンクを追加し、`findOrCreateNode` でノードを取得または新規作成する。`getGraph` は d3-sankey に渡せる `{nodes, links}` 形式のオブジェクトを返す。

### packages/mermaid/src/diagrams/sankey/sankeyDetector.ts

`sankey(-beta)?` で始まるテキストを検出し、`sankeyDiagram.js` を動的インポートするプラグイン定義。

### packages/mermaid/src/diagrams/sankey/sankeyDiagram.ts

Sankey ダイアグラムの定義ファイル。JISON パーサーをラップし、`prepareTextForParsing` で前処理してから `parse` を実行する。`db`・`renderer`・`styles` を束ねた `DiagramDefinition` オブジェクトをエクスポートする。

### packages/mermaid/src/diagrams/sankey/sankeyRenderer.ts

D3 / d3-sankey を使用して Sankey ダイアグラムを SVG に描画する。ノードの矩形・ラベル（`legacy` と `outlined` の2スタイル）、リンクのパスとグラデーション着色を実装する。`findCentralNodeLayer` で最大値ノードのレイヤーを特定し、ラベル配置を最適化する。カスタムノードカラー設定もサポートする。

### packages/mermaid/src/diagrams/sankey/sankeyUtils.ts

Sankey テキスト前処理ユーティリティ。各行の前後スペース除去・連続改行の圧縮・トリムを行う `prepareTextForParsing` 関数のみを提供する小さなユーティリティファイル。

---

## packages/mermaid — diagrams/sequence

### packages/mermaid/src/diagrams/sequence/sequenceDb.ts

シーケンス図のデータベースクラス `SequenceDB`。アクター・メッセージ・ノート・ボックス・アクティベーションを管理し、LINETYPE / ARROWTYPE / PLACEMENT 定数を保持する。YAML メタデータのパースやボックスカラーの解析、アクターへのリンク・プロパティ追加も行う。`apply` メソッドがパーサーからのイベントを一括処理する。

### packages/mermaid/src/diagrams/sequence/sequenceDetector.ts

`sequenceDiagram` で始まるテキストを検出し、`sequenceDiagram.js` を動的インポートする軽量なプラグイン定義ファイル。

### packages/mermaid/src/diagrams/sequence/sequenceDiagram.ts

シーケンス図の `DiagramDefinition`。JISON パーサーと `SequenceDB` インスタンス（毎回 `new` で生成）、`renderer`、`styles` を束ねる。`init` で `wrap` 設定を `sequence` コンフィグに伝播する。

### packages/mermaid/src/diagrams/sequence/sequenceRenderer.ts

シーケンス図の SVG 描画エンジン（約2100行）。`bounds` オブジェクトで垂直位置を追跡しながら、アクター・メッセージ・ノート・ループ/alt/par/critical/break ブロック・アクティベーションを順次描画する。KaTeX 数式のサポート、シーケンス番号、中央接続矢印、bidirectional 矢印など多数の機能を実装する。

### packages/mermaid/src/diagrams/sequence/types.ts

シーケンス図の型定義ファイル。`Box`・`Actor`・`Message`・`Note`・`AddMessageParams` インターフェースを定義する。`AddMessageParams.type` は全パーサーイベント名のユニオン型として網羅的に定義されている。

---

## packages/mermaid — diagrams/state

### packages/mermaid/src/diagrams/state/dataFetcher.ts

ステート図のパース済み AST からノードとエッジのリストを構築するユーティリティ。`dataFetcher` 関数が各ステート項目の形状（start/end/fork/join 等）を決定し、ノート付きグループ構造を生成する。`setupDoc` は再帰的にドキュメントを処理し、`insertOrUpdateNode` で重複ノードをマージする。

### packages/mermaid/src/diagrams/state/stateCommon.ts

ステート図全体で共有される定数の定義ファイル。ダイアグラム方向・ステートメント種別・グラフエッジスタイル・形状名・CSS クラス名・DOM ID プレフィックスなど多数の定数をエクスポートする。

### packages/mermaid/src/diagrams/state/stateDb.ts

ステート図のデータベースクラス `StateDB`（v1/v2 共用）。ステート・遷移・スタイルクラス・クリックリンクを管理する。`setRootDoc` でパース済み AST を受け取り `extract` でノード/エッジに変換する。`docTranslator` で分岐（`[*]`）や divider を処理し、`getData` で描画エンジンが使う `LayoutData` 形式を返す。

### packages/mermaid/src/diagrams/state/stateDetector-V2.ts

`stateDiagram-v2` または `dagre-wrapper` 設定時の `stateDiagram` を検出し、v2 ダイアグラム (`stateDiagram-v2.js`) をロードするプラグイン定義。

### packages/mermaid/src/diagrams/state/stateDetector.ts

旧来の `stateDiagram` テキストを検出するプラグイン定義。`dagre-wrapper` が設定されている場合は false を返してレガシー実装を回避する。

### packages/mermaid/src/diagrams/state/stateDiagram-v2.ts

ステート図 v2 の `DiagramDefinition`。JISON パーサーと `StateDB(2)` インスタンス、統合レンダラー `stateRenderer-v3-unified`、スタイルを束ねる。

### packages/mermaid/src/diagrams/state/stateDiagram.ts

ステート図レガシー版の `DiagramDefinition`。`StateDB(1)` と `stateRenderer`（旧レンダラー）を使用する点が v2 との違い。

### packages/mermaid/src/diagrams/state/stateRenderer-v3-unified.ts

ステート図の統合レンダラー。`getData` で取得した `LayoutData` を `render` 関数に渡して描画する。ノードをクリックリンクでラップする後処理を実装しており、`getDir` でネスト文書の方向を決定するユーティリティも提供する。

---

## packages/mermaid — diagrams/timeline

### packages/mermaid/src/diagrams/timeline/detector.ts

`timeline` で始まるテキストを検出し、`timeline-definition.js` を動的インポートするタイムライン図用プラグイン定義。

### packages/mermaid/src/diagrams/timeline/timeline-definition.ts

タイムライン図の `DiagramDefinition`。`direction` が `TD` の場合は `timelineRendererVertical`、それ以外は `timelineRenderer` を選択して呼び出す `rendererSelector` を実装する。

### packages/mermaid/src/diagrams/timeline/timelineRenderer.ts

水平タイムライン図の描画実装（LR 方向）。セクション・タスク・イベントを左から右へ順に配置し、底部に水平な活動ライン（矢印付き）を描く。neo テーマ時のグラデーションサポートあり。

### packages/mermaid/src/diagrams/timeline/timelineRendererVertical.ts

垂直タイムライン図の描画実装（TD 方向）。中央に縦の活動ラインを引き、左側にタスク・右側にイベントを配置する。定数で各ノード幅・スペーシングを管理し、水平版と異なる座標計算を行う。

---

## packages/mermaid — diagrams/treeView

### packages/mermaid/src/diagrams/treeView/boxDrawingPreprocessor.ts

ツリービュー図のボックス描画文字（`├──`・`└──`・`│` 等）をインデントベースの書式に変換するプリプロセッサ。セグメント幅を自動推定し、ブランチ文字のカラム位置から深さを計算する。エラー行番号の逆マッピング機能も提供する。

### packages/mermaid/src/diagrams/treeView/db.ts

ツリービュー図のデータベース。`ImperativeState` でルートノードから始まるスタックベースのツリーを管理し、`addNode` が深さに応じて親ノードを動的に決定してツリーを構築する。

### packages/mermaid/src/diagrams/treeView/detector.ts

`treeView-beta` で始まるテキストを検出し、`diagram.js` を動的ロードするプラグイン定義。

### packages/mermaid/src/diagrams/treeView/diagram.ts

ツリービュー図の `DiagramDefinition`。Langium ベースのパーサー・db・renderer・styles を束ねる最小構成のエントリファイル。

### packages/mermaid/src/diagrams/treeView/icons.ts

ファイル名・拡張子に基づくアイコン解決ロジックとインラインSVGアイコンパスの定義。`resolveIcon` がファイル名→拡張子の順で検索し、ディレクトリはフォルダ、不明ファイルは `file` アイコンにフォールバックする。Material Design Icons のSVGパス数十種を `ICON_PATHS` マップで保持する。

### packages/mermaid/src/diagrams/treeView/parser.ts

Langium パーサーを使用したツリービュー図のパーサー定義。`preprocessBoxDrawing` で前処理後に AST を取得し、各ノードのインデント・名前・アイコン・CSS クラス・説明を解析して `db.addNode` に渡す。エラー時は行番号の逆マッピングを適用する。

### packages/mermaid/src/diagrams/treeView/renderer.ts

ツリービュー図の SVG レンダラー。`injectIconDefs` で使用アイコンを `<defs>` に注入し、再帰的な `processNode` でノード・水平ライン・垂直ラインを描画する。フェーズ2で説明テキストを整列配置し、フェーズ3でハイライト背景矩形の幅を全幅に調整する。

### packages/mermaid/src/diagrams/treeView/styles.ts

ツリービュー図のCSSスタイル定義。ノードラベル・ディレクトリ（太字）・接続ライン・アイコン・説明テキスト・ハイライト背景のスタイルをテーマ変数から生成して返す。

### packages/mermaid/src/diagrams/treeView/types.ts

ツリービュー図の型定義。`Node`・`TreeViewDB`・`TreeViewDiagramStyles`・`D3SVGElement` インターフェースを定義する。`NodeType` は `'file' | 'directory'` のユニオン型。

---

## packages/mermaid — diagrams/treemap

### packages/mermaid/src/diagrams/treemap/db.ts

Treemap 図のデータベースクラス `TreeMapDB`。フラットなノードリスト・深さマップ・外側ノード・スタイルクラスを管理する。`addNode` でレベル0をルートノードとして扱い、`getRoot` は外側ノードを子に持つ仮想ルートを返す。

### packages/mermaid/src/diagrams/treemap/detector.ts

`treemap` で始まるテキストを検出し、`diagram.js` を動的インポートする `ExternalDiagramDefinition` を `treemap` としてエクスポートする。

### packages/mermaid/src/diagrams/treemap/diagram.ts

Treemap 図の `DiagramDefinition`。Langium パーサー・`TreeMapDB` インスタンス（毎回 `new`）・レンダラー・スタイルを束ねる。

### packages/mermaid/src/diagrams/treemap/parser.ts

Langium を使用した Treemap 図のパーサー。AST の `TreemapRows` を走査して `ClassDefStatement` とデータ行を分離し、`buildHierarchy` でフラット配列を木構造に変換して `db.addNode` で登録する。

### packages/mermaid/src/diagrams/treemap/renderer.ts

D3 `treemap` レイアウトを使用した Treemap 図のレンダラー。セクション（ブランチ）ノードはヘッダー付き矩形で描画し、リーフノードは親カラーで色付けする。ラベル・値テキストのフォントサイズをノード面積に合わせて動的に縮小する機能を持つ。

### packages/mermaid/src/diagrams/treemap/styles.ts

Treemap 図の CSS スタイルプロバイダー。セクション・リーフ・ラベル・値・タイトルの色やフォントサイズをテーマ変数とユーザー設定からマージして生成する。

### packages/mermaid/src/diagrams/treemap/types.ts

Treemap 図の型定義。`TreemapNode`・`TreemapDB`・`TreemapStyleOptions`・`TreemapData`・`TreemapAst`・`TreemapDiagramConfig` など Treemap 関連の全インターフェースを集約する。

### packages/mermaid/src/diagrams/treemap/utils.ts

フラットなアイテム配列をレベル情報に基づいて階層ツリー (`TreemapNode[]`) に変換する `buildHierarchy` 関数のみを提供するユーティリティファイル。スタックで親子関係を追跡し、`Leaf` 型のみ値を持てる。

---

## packages/mermaid — diagrams/user-journey

### packages/mermaid/src/diagrams/user-journey/journeyDetector.ts

`journey` で始まるテキストを検出し、`journeyDiagram.js` を動的ロードするユーザージャーニー図プラグイン定義。

### packages/mermaid/src/diagrams/user-journey/journeyDiagram.ts

ユーザージャーニー図の `DiagramDefinition`。JISON パーサー・db・renderer・styles を束ね、`init` でレンダラーに設定を渡し db をクリアする。

### packages/mermaid/src/diagrams/user-journey/journeyRenderer.ts

ユーザージャーニー図のレンダラー。アクターの凡例（アイコン円＋テキスト）をサイドバーに描画し、セクション別に色分けされたタスクボックスを並べる。底部に水平な活動ライン（矢印付き）を引く。テキスト折り返しはKnuth-Plassアルゴリズム相当の実装で行う。

---

## packages/mermaid — diagrams/venn

### packages/mermaid/src/diagrams/venn/styles.ts

ベン図のCSS定義。タイトル・円テキスト・交差領域テキスト・テキストノードのフォントサイズ・色・フォントファミリーをテーマ変数から生成して返す。

### packages/mermaid/src/diagrams/venn/vennDB.ts

ベン図のデータベース。集合データ（`addSubsetData`）・テキストノード（`addTextData`）・スタイルデータ（`addStyleData`）を管理する。識別子の正規化（クォート除去）、未定義集合の検証、インデントモードのトグルを実装する。

### packages/mermaid/src/diagrams/venn/vennDetector.ts

`venn-beta` で始まるテキストを検出して `vennDiagram.js` をロードするプラグイン定義。

### packages/mermaid/src/diagrams/venn/vennDiagram.ts

ベン図の `DiagramDefinition`。JISON パーサー・`vennDB`・レンダラー・スタイルを束ねる最小構成ファイル。

### packages/mermaid/src/diagrams/venn/vennRenderer.ts

`@upsetjs/venn.js` を使用したベン図レンダラー。ダミー D3 要素上でVennレイアウトを計算し、テーマカラーで円を着色する。`handDrawn` テーマ時は `roughjs` でスケッチ風描画を行う。`foreignObject` によるHTMLテキストノード配置と `useDebugLayout` デバッグ機能も実装する。

### packages/mermaid/src/diagrams/venn/vennTypes.ts

ベン図の型定義。`VennData`・`VennTextData`・`VennStyleData`・`VennDB` インターフェースを定義する。`VennDB` は `DiagramDBBase` を継承し、集合・テキスト・スタイルの追加/取得メソッドを規定する。

---

## packages/mermaid — diagrams/wardley

### packages/mermaid/src/diagrams/wardley/styles.ts

ウォードリーマップのCSSスタイルプロバイダー。背景・軸・グリッド・ノード円・リンク・トレンドライン・アノテーション・パイプラインボックス・ノートの各要素のスタイルをテーマ変数からマージして生成する。

### packages/mermaid/src/diagrams/wardley/wardleyBuilder.ts

ウォードリーマップのデータ構造を組み立てる `WardleyBuilder` クラス。ノード・リンク・トレンド（進化矢印）・パイプライン・アノテーション・ノート・加速/減速要素を蓄積し、`build()` で最終的な `WardleyBuildResult` を返す。名前またはIDでのノード解決機能も提供する。

### packages/mermaid/src/diagrams/wardley/wardleyDb.ts

ウォードリーマップのデータベース。`WardleyBuilder` インスタンスをラップし、`addNode`・`addLink`・`addTrend`・`startPipeline` 等のメソッドをエクスポートする。`getWardleyData` で `builder.build()` を呼び出す。

### packages/mermaid/src/diagrams/wardley/wardleyDetector.ts

`wardley-beta` で始まるテキスト（大文字小文字不問）を検出して `wardleyDiagram.js` をロードするプラグイン定義。

### packages/mermaid/src/diagrams/wardley/wardleyDiagram.ts

ウォードリーマップの `DiagramDefinition`。Langium パーサー・db・renderer・スタイルを束ねる最小構成ファイル。

### packages/mermaid/src/diagrams/wardley/wardleyParser.ts

Langium ベースのウォードリーマップパーサー。AST をトラバースして可視性/進化値を0–100のパーセンテージ座標に変換し、コンポーネント・リンク（破線・フロー矢印）・パイプライン・アノテーション・アクセラレータなど全要素を `db` に登録する。

### packages/mermaid/src/diagrams/wardley/wardleyRenderer.ts

ウォードリーマップのSVGレンダラー（約1000行）。軸・グリッド・ステージラベル・パイプラインボックス・リンク・進化トレンド矢印・ノード円/矩形（ソース戦略別のオーバーレイ付き）・慣性インジケータ・アノテーションボックス・ノート・加速/減速矢印を描画する。

### packages/mermaid/src/diagrams/wardley/wardleyTypes.ts

`wardleyDb` のデフォルトエクスポートの型を `WardleyDB` として再エクスポートするだけの型ファイル。

---

## packages/mermaid — diagrams/xychart

### packages/mermaid/src/diagrams/xychart/chartBuilder/components/axis/bandAxis.ts

カテゴリ（文字列）軸を実装する `BandAxis` クラス。`d3.scaleBand` を使用し、`recalculateScale` で `paddingInner(1)` と `paddingOuter(0)` を設定してカテゴリ間の距離を計算する。

### packages/mermaid/src/diagrams/xychart/chartBuilder/components/axis/baseAxis.ts

XY チャート軸の抽象基底クラス。利用可能スペースを計算してタイトル/ラベル/ティック/軸線の表示可否を決定し、位置（left/bottom/top）に応じた `DrawableElem[]` を生成する。外側パディングの再計算でバーチャートの表示幅を調整する機能も持つ。

### packages/mermaid/src/diagrams/xychart/chartBuilder/components/axis/index.ts

`Axis` インターフェースと `getAxis` ファクトリ関数を定義するエクスポートファイル。`isBandAxisData` でデータ種別を判定し `BandAxis` または `LinearAxis` を返す。

### packages/mermaid/src/diagrams/xychart/chartBuilder/components/axis/linearAxis.ts

数値（線形）軸を実装する `LinearAxis` クラス。`d3.scaleLinear` を使用し、左軸の場合はドメインを反転（SVG の Y 軸が上から下のため）して scale を再計算する。

### packages/mermaid/src/diagrams/xychart/chartBuilder/components/chartTitle.ts

XY チャートのタイトルコンポーネント。利用可能スペース内にタイトルが収まる場合のみ描画し、中央揃えのテキスト要素を `DrawableElem` として返す。

### packages/mermaid/src/diagrams/xychart/chartBuilder/components/plot/barPlot.ts

棒グラフのプロットコンポーネント。X/Y 軸のスケール変換後に矩形要素を生成する。水平/垂直向きに対応し、各バーの幅をティック間距離とパディング率から計算する。

### packages/mermaid/src/diagrams/xychart/chartBuilder/components/plot/index.ts

プロットコンポーネントの `BasePlot` クラスと `getPlotComponent` ファクトリ。`chartData.plots` を走査して `LinePlot`/`BarPlot` を生成し、各描画要素を統合した `DrawableElem[]` を返す。

### packages/mermaid/src/diagrams/xychart/chartBuilder/components/plot/linePlot.ts

折れ線グラフのプロットコンポーネント。`d3.line` を使用してデータポイントをSVGパスに変換する。水平/垂直向きで X/Y 座標マッピングを切り替える。

### packages/mermaid/src/diagrams/xychart/chartBuilder/index.ts

`XYChartBuilder` クラス。`Orchestrator` を生成して `getDrawableElement()` を呼び出す静的ファクトリメソッド `build` を提供する薄いラッパー。

### packages/mermaid/src/diagrams/xychart/chartBuilder/interfaces.ts

XY チャートの全インターフェース・型定義集。テーマ設定・コンポーネントインターフェース・プロットデータ型（Line/Bar）・軸データ型（Band/Linear）・描画要素型（rect/text/path）・設定型 `XYChartConfig` 等を網羅的に定義する。

### packages/mermaid/src/diagrams/xychart/chartBuilder/orchestrator.ts

XY チャートのレイアウト計算を担う `Orchestrator` クラス。タイトル・X 軸・Y 軸・プロット領域の各コンポーネントに対してスペースを順次割り当て、縦横向きそれぞれの計算ロジックを実装する。最終的に全コンポーネントの `DrawableElem[]` を統合して返す。

### packages/mermaid/src/diagrams/xychart/chartBuilder/textDimensionCalculator.ts

SVG グループに不可視テキスト要素を一時的に追加し、`getBBox()` で実際のテキスト寸法を計測する `TextDimensionCalculatorWithFont` クラス。SVG 環境がない場合はフォントサイズ×文字数でフォールバック計算する。

### packages/mermaid/src/diagrams/xychart/xychartDb.ts

XY チャートのデータベース。設定・テーマ・チャートデータをモジュールレベル変数で管理し、X/Y 軸の設定（バンド/線形）・ライン/バーデータの追加・`XYChartBuilder.build` の呼び出しを行う。`setTmpSVGG` でテキスト計測用 SVG グループを受け取る。

### packages/mermaid/src/diagrams/xychart/xychartDetector.ts

`xychart(-beta)?` で始まるテキストを検出し、`xychartDiagram.js` を動的インポートするプラグイン定義。

### packages/mermaid/src/diagrams/xychart/xychartDiagram.ts

XY チャートの `DiagramDefinition`。JISON パーサー・db・renderer を束ねる最小構成ファイル（スタイル定義は含まない）。

### packages/mermaid/src/diagrams/xychart/xychartRenderer.ts

XY チャートのSVGレンダラー。`db.getDrawableElem()` で取得した `DrawableElem[]` を SVG要素（rect/text/path）に変換して描画する。バーチャートのデータラベル（水平/垂直向き別、フォントサイズ自動縮小）機能を実装する。

---

## packages/mermaid — rendering-util

### packages/mermaid/src/rendering-util/createText.ts

SVG ノードやエッジのラベルテキストを生成するメインユーティリティ。`useHtmlLabels` が true の場合は `<foreignObject>` + HTML span、false の場合は SVG `<text>` + `<tspan>` を使用してテキストを描画する。Markdown パース・KaTeX 数式・FontAwesome アイコン置換にも対応。幅制限に応じたテキスト折り返しも行う。

### packages/mermaid/src/rendering-util/handle-markdown-text.ts

Markdown テキストを SVG/HTML 用に変換するユーティリティ。`markdownToLines`（SVG テキスト向け）・`markdownToHTML`（HTML ラベル向け）・非 Markdown 用の `nonMarkdownToLines` / `nonMarkdownToHTML` の4関数を提供。太字・斜体・改行処理・`markdownAutoWrap` 設定をサポートする。

### packages/mermaid/src/rendering-util/icons.ts

Iconify ライブラリを使ったアイコン管理モジュール。`registerIconPacks` で同期/非同期のアイコンパックを登録し、`getIconSVG` で SVG 文字列を取得できる。未登録アイコンにはフォールバック用の「?」アイコンを返す。FontAwesome 等の外部アイコンセットを柔軟に扱えるよう設計されている。

### packages/mermaid/src/rendering-util/labelTransform.ts

ラベル要素を SVG グループの原点に中心揃えするための `translate` トランスフォーム文字列を計算するユーティリティ。HTML ラベル（`getBoundingClientRect` 使用）と SVG ラベル（`getBBox` 使用）で座標系が異なるため、`useHtmlLabels` フラグで処理を分岐する。

### packages/mermaid/src/rendering-util/layout-algorithms/cose-bilkent/cytoscape-setup.ts

Cytoscape インスタンスの生成・設定を担う。`addNodes`/`addEdges` でノード・エッジを追加し、`createCytoscapeInstance` で cose-bilkent レイアウトを実行する。レイアウト後に `extractPositionedNodes`/`extractPositionedEdges` でポジション情報を抽出する。

### packages/mermaid/src/rendering-util/layout-algorithms/cose-bilkent/index.ts

cose-bilkent レイアウトアルゴリズムのエントリポイント。`render.ts` の `render` 関数を再エクスポートするだけの薄いモジュールで、統一されたレイアウトアルゴリズム登録パターンに従っている。

### packages/mermaid/src/rendering-util/layout-algorithms/cose-bilkent/layout.ts

`executeCoseBilkentLayout` 関数を提供する。入力データのバリデーション後、`createCytoscapeInstance` でレイアウトを実行し、配置済みノード・エッジを返す。`validateLayoutData` でデータ構造の必須フィールドを検証する。

### packages/mermaid/src/rendering-util/layout-algorithms/cose-bilkent/render.ts

cose-bilkent レイアウトの SVG 描画処理。① DOM へのノード挿入で実寸取得 → ② cose-bilkent レイアウト実行 → ③ 計算済み座標への位置配置 → ④ エッジ描画の4ステップで動作する。dagre/ELK と同じ統一パターンに従う。

### packages/mermaid/src/rendering-util/layout-algorithms/cose-bilkent/types.ts

cose-bilkent レイアウト用の型定義ファイル。`PositionedNode`（id・x・y）・`PositionedEdge`（id・start/end座標）・`LayoutResult`（ノード・エッジ配列）・`CytoscapeLayoutConfig` の4インターフェースを定義する。

### packages/mermaid/src/rendering-util/render.ts

レイアウトアルゴリズムの登録・選択・実行を管理するコアモジュール。`registerLayoutLoaders` でアルゴリズムを登録（デフォルトは dagre、オプションで cose-bilkent）し、`render` 関数がアルゴリズムをレイジーロードして SVG へ描画する。ドロップシャドウフィルタやグラデーションなどの SVG 装飾も追加する。

### packages/mermaid/src/rendering-util/rendering-elements/edgeMarker.ts

エッジの矢印マーカーを SVG パス要素に付与するユーティリティ。`arrowTypesMap` で矢印種別（cross/point/barb 等）とフィルの有無を管理し、カラーマーカーはクローンして動的に生成する。`marker-start`/`marker-end` 属性を介してマーカーを適用する。

### packages/mermaid/src/rendering-util/rendering-elements/nodes.ts

ノードを SVG へ挿入・配置する関数群。`insertNode` はノードの `shape` に対応するハンドラを呼び出してノードを生成し、リンクがある場合は `<a>` でラップする。`positionNode` はレイアウト計算後の座標にノードを移動させる。

### packages/mermaid/src/rendering-util/rendering-elements/shapes.ts

すべての図形ハンドラをまとめた中央レジストリ。`shapesDefs` 配列に各形状の意味名・短縮名・エイリアス・ハンドラ関数を定義し、`generateShapeMap` でフラットな `shapes` マップを生成する。`isValidShape` で形状名の有効性を確認できる。

### packages/mermaid/src/rendering-util/rendering-elements/shapes/anchor.ts

フローチャートのアンカーポイント（極小の塗りつぶし円）を描画するシェイプ。半径1pxの黒塗り円を `roughjs` で生成する。`handDrawn` 以外は `roughness: 0` を設定してきれいな円を描く。

### packages/mermaid/src/rendering-util/rendering-elements/shapes/bang.ts

「bang」（爆発・吹き出し風の不規則な多角形）シェイプ。複数の円弧パスを組み合わせた複雑な閉じたパスを生成し、ラベルを内部に配置する。通常描画と `handDrawn` 両方をサポートする。

### packages/mermaid/src/rendering-util/rendering-elements/shapes/bowTieRect.ts

ボウタイ矩形（中央がくびれた形）シェイプ。左右端を楕円弧で構成し、データストア等に使用される「保存データ」の記号。サジタ（弧の膨らみ量）を計算して幅を補正する。

### packages/mermaid/src/rendering-util/rendering-elements/shapes/card.ts

カード形状（左上に切り欠きのある矩形）を描画するシェイプ。`NOTCH_SIZE = 12` のノッチを左上に入れた六角形ポリゴンを生成する。`handDrawn` モードでは `roughjs` でパスを描画する。

### packages/mermaid/src/rendering-util/rendering-elements/shapes/choice.ts

UML 状態図の疑似状態「choice」（菱形）シェイプ。ラベルなしの菱形（四角形を45度回転した形）を28×28px で描画する。`handDrawn` モードと通常モードの両方をサポートする。

### packages/mermaid/src/rendering-util/rendering-elements/shapes/circle.ts

円形シェイプ。ラベルテキストの幅に応じて半径を計算し、`handDrawn` モードでは `roughjs` の円を使用する。マインドマップでも流用できるよう `MindmapOptions` を受け付ける。

### packages/mermaid/src/rendering-util/rendering-elements/shapes/classBox.ts

クラス図専用のボックスシェイプ。アノテーション・クラス名・メンバー・メソッドの各テキストグループを垂直に配置し、区切り線（divider）を挿入する。グラデーションや手書き風など多くのテーマ変数に対応する複雑なシェイプ。

### packages/mermaid/src/rendering-util/rendering-elements/shapes/cloud.ts

雲形シェイプ。複数の円弧パスを組み合わせた雲のアウトラインを SVG パスで生成する。ラベルを内部中央に配置し、`handDrawn` モードと通常モードの両方をサポートする。

### packages/mermaid/src/rendering-util/rendering-elements/shapes/crossedCircle.ts

×印の付いた円（crossed circle）シェイプ。円に45度の交差した2本の線を重ねる。UML の「コンポーネント終了点」などに使用される。ラベルなしで固定サイズ。

### packages/mermaid/src/rendering-util/rendering-elements/shapes/curlyBraceLeft.ts

左向きの波括弧（`{`）シェイプ。複数の円弧点列を組み合わせて括弧の形を生成する。交差点計算用の不可視矩形も生成してエッジの接続判定に使用する。

### packages/mermaid/src/rendering-util/rendering-elements/shapes/curlyBraceRight.ts

右向きの波括弧（`}`）シェイプ。`curlyBraceLeft.ts` と同様のアプローチで右向きの括弧を生成する。生成する円弧点列の x 方向が左向きと逆転している。

### packages/mermaid/src/rendering-util/rendering-elements/shapes/curlyBraces.ts

両側に波括弧（`{}`）が付いたシェイプ。`curlyBraceLeft` と `curlyBraceRight` の両方を組み合わせた形状を生成する。コメントアノテーションに使用される。

### packages/mermaid/src/rendering-util/rendering-elements/shapes/curvedTrapezoid.ts

右端が半円の曲線付き台形（display シェイプ）。右側に半円の弧を付加した変形台形を生成する。モニターや表示デバイスを表す記号。

### packages/mermaid/src/rendering-util/rendering-elements/shapes/cylinder.ts

シリンダー（データベース）形状を描画するシェイプ。上下の楕円弧と縦のラインを組み合わせた SVG パスを生成する。`handDrawn` モードでは外枠と内部上部線を別々の `roughjs` パスで描く。

### packages/mermaid/src/rendering-util/rendering-elements/shapes/datastore.ts

データフロー図のデータストアシェイプ。`drawRect` をベースに、通常描画では `stroke-dasharray` で上下に横線を表現し、`handDrawn` モードでは roughjs の線を追加する。

### packages/mermaid/src/rendering-util/rendering-elements/shapes/defaultMindmapNode.ts

マインドマップのデフォルトノード（角丸矩形）シェイプ。`neo` ルックでは上部のみ角丸、通常は全周角丸の SVG パスを生成する。下辺に水平線を追加し、ノードの視覚的区切りを表現する。

### packages/mermaid/src/rendering-util/rendering-elements/shapes/dividedRect.ts

上部に区切り線を持つ矩形シェイプ（Divided Process）。矩形の上部20%を区切る横線を持つポリゴンを生成する。`roughjs` の polygon API を使用する。

### packages/mermaid/src/rendering-util/rendering-elements/shapes/document.ts

`cylinder.ts` のコピー相当のファイルで、`datastore` 形状向けに同じシリンダーパス関数を再定義している。実際の `document` シェイプとしては `waveEdgedRectangle` が使われており、内部実装上の重複と見られる。

### packages/mermaid/src/rendering-util/rendering-elements/shapes/doubleCircle.ts

二重円シェイプ（状態図の終了点など）。外円と内円の半径差でギャップ幅を制御する。`handDrawn` モードでは `roughjs` の円を2つ生成してグループ化する。

### packages/mermaid/src/rendering-util/rendering-elements/shapes/drawRect.ts

汎用的な矩形描画ヘルパー関数 `drawRect`。`RectOptions`（rx/ry・パディング）を受け取り、`handDrawn` では `roughjs`、通常では SVG `<rect>` で描画する。多くのシェイプが内部でこの関数を呼び出している基盤コンポーネント。

### packages/mermaid/src/rendering-util/rendering-elements/shapes/erBox.ts

ER 図のエンティティボックスシェイプ。属性がない場合は `drawRect` を使い、属性がある場合はタイプ・名前・キー・コメント列を持つ複数列テーブルを描画する。交互の行背景色・仕切り線・テーマに応じた配色など複雑なレイアウトを実装する。

### packages/mermaid/src/rendering-util/rendering-elements/shapes/filledCircle.ts

塗りつぶし円（junction point/状態遷移分岐点）シェイプ。半径7pxの小さな塗りつぶし円を `roughjs` で生成し、`nodeBorder` テーマ変数の色で塗る。ラベルなし固定サイズ。

### packages/mermaid/src/rendering-util/rendering-elements/shapes/flippedTriangle.ts

逆三角形（Manual File）シェイプ。頂点が下向きの三角形を生成する。幅・高さは `labelHelper` のバウンディングボックスを元に計算し、`handDrawn` モードでは `roughjs` を使用する。

### packages/mermaid/src/rendering-util/rendering-elements/shapes/forkJoin.ts

フォーク/ジョインシェイプ（状態図の同期バー）。方向 `LR` か TB かによって縦横を入れ替えた塗りつぶし矩形を生成する。`themeVariables.lineColor` を使って色を設定する。

### packages/mermaid/src/rendering-util/rendering-elements/shapes/halfRoundedRectangle.ts

片側半円の矩形（Delay シェイプ）。右端にのみ半円を持つ形状を生成する。`handDrawn` と通常の両モードをサポートする。

### packages/mermaid/src/rendering-util/rendering-elements/shapes/handDrawnShapeStyles.ts

手書き風スタイル（`handDrawn`/`neo` ルック）の設定を管理するユーティリティ。`styles2String` でノードスタイルをラベル/ノード/境界/背景の4カテゴリに分類し、`userNodeOverrides` で `roughjs` 向けのオプション（roughness・fill・stroke 等）を生成する。

### packages/mermaid/src/rendering-util/rendering-elements/shapes/hexagon.ts

六角形シェイプ（Prepare/Hexagon）。テキスト幅に応じた m 値（突起量）を計算して六角形の頂点を生成する。`insertPolygonShape` または `roughjs` パスで描画する。

### packages/mermaid/src/rendering-util/rendering-elements/shapes/hourglass.ts

砂時計シェイプ（Collate）。4点の多角形（対角交差）を生成して砂時計の形を表現する。ラベルなし固定サイズで `roughjs` を使用する。

### packages/mermaid/src/rendering-util/rendering-elements/shapes/icon.ts

アイコン付きのシェイプ（icon）。Iconify からアイコン SVG を取得してノードに埋め込む。ラベルはアイコンの上（`pos: 't'`）または下（デフォルト）に配置できる。外枠は透明な矩形で包む。

### packages/mermaid/src/rendering-util/rendering-elements/shapes/iconCircle.ts

円形背景付きのアイコンシェイプ。アイコンを内接正方形の外接円で囲み、ラベルは上下選択可能。`roughjs` の circle を背景に使用する。

### packages/mermaid/src/rendering-util/rendering-elements/shapes/iconRounded.ts

角丸矩形背景付きのアイコンシェイプ。`createRoundedRectPathD` でコーナー半径5の角丸矩形を背景に使用。アイコンの上下ラベル配置をサポートする。

### packages/mermaid/src/rendering-util/rendering-elements/shapes/iconSquare.ts

正方形背景付きのアイコンシェイプ。コーナー半径0.1の角丸矩形（実質正方形）を背景に使用する。アイコン埋め込みとラベル上下配置の基本実装。

### packages/mermaid/src/rendering-util/rendering-elements/shapes/imageSquare.ts

画像付きのシェイプ。外部画像 URL をデコードして `<image>` タグで埋め込む。アスペクト比の保持・`constraint` オプションによるサイズ固定をサポートし、ラベルは上下選択可能。

### packages/mermaid/src/rendering-util/rendering-elements/shapes/insertPolygonShape.ts

多角形 SVG 要素を挿入するシンプルなヘルパー関数。点の配列を `polygon` の `points` 属性に変換し、指定幅・高さで中心揃えの `translate` を付与する。多数のシェイプから呼び出される共通関数。

### packages/mermaid/src/rendering-util/rendering-elements/shapes/invertedTrapezoid.ts

逆台形（inv_trapezoid / Manual Operation）シェイプ。底辺が上、上辺が下の台形形状を4点ポリゴンで生成する。`handDrawn` では `roughjs` パス、通常は `insertPolygonShape` を使用する。

### packages/mermaid/src/rendering-util/rendering-elements/shapes/kanbanItem.ts

カンバンアイテムシェイプ。タイトル・チケット番号・担当者の3行テキストを持つ角丸矩形を生成する。優先度に応じた左側縦線の色付け・チケット URL へのリンク付けなどカンバン固有の機能を実装する。

### packages/mermaid/src/rendering-util/rendering-elements/shapes/labelImageUtils.ts

ラベル内の `<img>` タグが読み込まれるのを待つ非同期ユーティリティ。画像のみのラベルと混合ラベルで異なるスタイルを設定し、正確なバウンディングボックス取得を可能にする。

### packages/mermaid/src/rendering-util/rendering-elements/shapes/labelRect.ts

`roundedRect` と `labelRect` の2関数を含む。`roundedRect` は `drawRect` に角丸オプションを渡すラッパーで、`labelRect` はエッジラベル専用の不可視矩形（0.1×0.1px）を生成する。

### packages/mermaid/src/rendering-util/rendering-elements/shapes/leanLeft.ts

左傾きの平行四辺形（Lean Left / out-in）シェイプ。4点ポリゴンで右上から左下へ傾いた形を生成する。`handDrawn` では `roughjs` パスを使用する。

### packages/mermaid/src/rendering-util/rendering-elements/shapes/leanRight.ts

右傾きの平行四辺形（Lean Right / in-out）シェイプ。`leanLeft.ts` の鏡像版で、左上から右下へ傾く形を生成する。実装パターンは `leanLeft` と同一。

### packages/mermaid/src/rendering-util/rendering-elements/shapes/lightningBolt.ts

稲妻（Lightning Bolt / Communication Link）シェイプ。ラベルなしの6点ポリゴンで稲妻の形を生成する。`handDrawn` モードでは `roughjs` のパスを使用する。

### packages/mermaid/src/rendering-util/rendering-elements/shapes/linedCylinder.ts

横線付きシリンダー（Lined Cylinder / Disk Storage）シェイプ。標準シリンダーに加え、10%高さ位置に追加の楕円弧（横線）を描く。`handDrawn` モードでは外枠・内線を別々に描画する。

### packages/mermaid/src/rendering-util/rendering-elements/shapes/linedWaveEdgedRect.ts

横線付き波形矩形（Lined Document）シェイプ。波形下辺と左辺の縦線を組み合わせた多角形を生成する。文書スタックを模したデザイン。

### packages/mermaid/src/rendering-util/rendering-elements/shapes/mindmapCircle.ts

マインドマップ用の円形ノードシェイプ。`circle.ts` の `circle` 関数に `MindmapOptions`（padding）を渡す薄いラッパー関数。

### packages/mermaid/src/rendering-util/rendering-elements/shapes/multiRect.ts

複数の積み重なった矩形（Multi-Process / Stacked Rectangle）シェイプ。内側矩形と左上にオフセットした外側矩形の2つのパスを組み合わせて生成する。

### packages/mermaid/src/rendering-util/rendering-elements/shapes/multiWaveEdgedRectangle.ts

複数の積み重なった波形矩形（Multi-Document / Stacked Document）シェイプ。`multiRect` と同様の二層構造に、下辺を正弦波状にした形を生成する。

### packages/mermaid/src/rendering-util/rendering-elements/shapes/note.ts

ノート（Note）シェイプ。シーケンス図などで使用する注釈ボックス。`themeVariables.noteBkgColor`/`noteBorderColor` で色付けし、`handDrawn` では `roughjs` の矩形を使用する。

### packages/mermaid/src/rendering-util/rendering-elements/shapes/question.ts

決定菱形（Question / Decision）シェイプ。テキストサイズを基に菱形のサイズを計算し、4点ポリゴンで生成する。`calcIntersect` で汎用バウンドからの交差計算もサポートする。

### packages/mermaid/src/rendering-util/rendering-elements/shapes/rectLeftInvArrow.ts

左側に逆矢印切り込みのある矩形（Odd / rect_left_inv_arrow）シェイプ。左辺中央が内側に凹んだ5点ポリゴンを生成する。旧来の互換用シェイプ。

### packages/mermaid/src/rendering-util/rendering-elements/shapes/rectWithTitle.ts

タイトルと説明の2行テキストを持つ枠付き矩形（rectWithTitle）シェイプ。タイトル行と説明行の間に区切り線を挿入する。サブグラフや複合状態ノードに使用される。

### packages/mermaid/src/rendering-util/rendering-elements/shapes/requirementBox.ts

要求仕様図のボックスシェイプ。Requirement ノードには type/name/ID/text/risk/verifyMethod を、Element ノードには type/docRef を段組みで表示する。分割線とカラーインデックス付きのボックスを生成する。

### packages/mermaid/src/rendering-util/rendering-elements/shapes/roundedRect.ts

角丸矩形シェイプ。`drawRect` に `rx:5, ry:5` を渡すシンプルなラッパー。`themeVariables.radius` を使って半径を設定する `ShapeRenderOptions` 対応版と、固定値5の2バリアントがある。

### packages/mermaid/src/rendering-util/rendering-elements/shapes/roundedRectPath.ts

角丸矩形の SVG パスデータ文字列を生成するユーティリティ関数 `createRoundedRectPathD`。x/y/幅/高さ/半径を受け取り、M/H/A/V/Z コマンドの文字列を返す。複数のシェイプから参照される共通関数。

### packages/mermaid/src/rendering-util/rendering-elements/shapes/shadedProcess.ts

線引きプロセス（Shaded/Lined Process）シェイプ。左端に固定幅8pxのフレームを持つ矩形を多角形で生成する。ラベルはフレーム分だけ右にオフセットして中央揃えにする。

### packages/mermaid/src/rendering-util/rendering-elements/shapes/slopedRect.ts

傾いた矩形（Sloped Rect / Manual Input）シェイプ。上辺が右側に傾いた4点ポリゴンを生成する。高さは1.5倍スケールで計算して傾きを表現する。

### packages/mermaid/src/rendering-util/rendering-elements/shapes/squareRect.ts

標準矩形（Square Rect / Process）シェイプ。`drawRect` に `rx:0, ry:0` を渡す角丸なし矩形。`neo` ルックでは別のパディング値を使用する。

### packages/mermaid/src/rendering-util/rendering-elements/shapes/stadium.ts

スタジアム（Stadium / Terminal / Pill）シェイプ。`generateCirclePoints` で両端に半円を付けた丸角矩形を生成する。`createStadiumPathD` で標準 SVG パスも生成可能。

### packages/mermaid/src/rendering-util/rendering-elements/shapes/state.ts

状態図のステートノードシェイプ。`drawRect` に `rx:5` を渡す薄いラッパー。`neo` ルックでは半径3を使用する。

### packages/mermaid/src/rendering-util/rendering-elements/shapes/stateEnd.ts

状態図の終了点（Framed Circle）シェイプ。外側の大きい円と内側の塗りつぶし円の二重円を生成する。小サイズ時は `drop-shadow-small` フィルタで影を付ける。

### packages/mermaid/src/rendering-util/rendering-elements/shapes/stateStart.ts

状態図の開始点（Small Circle / Start）シェイプ。`solidStateFill` で塗りつぶした小さな円を生成する。`handDrawn` では `roughjs`、通常では SVG `<circle>` を使用する。

### packages/mermaid/src/rendering-util/rendering-elements/shapes/subroutine.ts

サブルーチン（Framed Rectangle）シェイプ。左右に8pxのフレームラインを持つ二重矩形を生成する。`handDrawn` では roughjs の矩形+2本の線、通常では `insertPolygonShape` を使用する。

### packages/mermaid/src/rendering-util/rendering-elements/shapes/taggedRect.ts

タグ付き矩形（Tagged Rectangle / Tagged Process）シェイプ。右下コーナーに小さな三角タグを持つ矩形を2つのパス（本体＋タグ）で生成する。タグの塗りつぶしは常に solid。

### packages/mermaid/src/rendering-util/rendering-elements/shapes/taggedWaveEdgedRectangle.ts

タグ付き波形矩形（Tagged Document）シェイプ。波形下辺の矩形に右上コーナーの波形タグを組み合わせた複合シェイプを生成する。`generateFullSineWavePoints` で両者の波形を生成する。

### packages/mermaid/src/rendering-util/rendering-elements/shapes/text.ts

テキストブロックシェイプ。ラベルをそのまま表示する透明な矩形（`class: text`）を生成する。枠線なし・塗りなしのシンプルなテキスト専用シェイプ。

### packages/mermaid/src/rendering-util/rendering-elements/shapes/tiltedCylinder.ts

傾いた横向きシリンダー（Horizontal Cylinder / Direct Access Storage）シェイプ。左右に楕円弧を持つ横長の筒形を生成する。垂直シリンダーとは rx/ry の使い方が異なる。

### packages/mermaid/src/rendering-util/rendering-elements/shapes/trapezoid.ts

台形（Trapezoid / Priority Action）シェイプ。上辺が下辺より狭い正台形を4点ポリゴンで生成する。`insertPolygonShape` または `roughjs` を使用する。

### packages/mermaid/src/rendering-util/rendering-elements/shapes/trapezoidalPentagon.ts

台形状五角形（Trapezoidal Pentagon / Loop Limit）シェイプ。上辺中央が内側に入り込む独特の6点形状を生成する。フローチャートのループ上限記号に使用。

### packages/mermaid/src/rendering-util/rendering-elements/shapes/triangle.ts

三角形（Triangle / Extract）シェイプ。上向きの三角形を3点ポリゴンで生成する。ラベルは三角形の上部に配置し、`useHtmlLabels` によってオフセット量を調整する。

### packages/mermaid/src/rendering-util/rendering-elements/shapes/util.ts

シェイプ描画の共通ユーティリティ関数集。`labelHelper`（ラベル付き `<g>` 生成）・`insertLabel`・`updateNodeBounds`・`getNodeClasses`・`createPathFromPoints`・`generateCirclePoints`・`generateFullSineWavePoints`・`mergePaths` など、すべてのシェイプが使う基盤関数を定義する。

### packages/mermaid/src/rendering-util/rendering-elements/shapes/waveEdgedRectangle.ts

波形下辺の矩形（Wave Edged Rectangle / Document）シェイプ。`generateFullSineWavePoints` で正弦波を生成して下辺に付加した矩形を描く。波の振幅はノード高さの1/8（neo では1/4）。

### packages/mermaid/src/rendering-util/rendering-elements/shapes/waveRectangle.ts

上下両辺が波形の矩形（Wave Rectangle / Flag / Paper Tape）シェイプ。上辺と下辺の両方に正弦波を使い、互いに逆位相で描く閉じたパスを生成する。

### packages/mermaid/src/rendering-util/rendering-elements/shapes/windowPane.ts

ウィンドウペイン（Internal Storage）シェイプ。外枠矩形に左辺と上辺の仕切り線を内包した十字格子状の形を単一 SVG パスで生成する。`rectOffset = 10` だけオフセットした二重格子構造。

### packages/mermaid/src/rendering-util/selectSvgElement.ts

ダイアグラム ID から SVG 要素を選択するユーティリティ。`securityLevel: 'sandbox'` の場合は iframe の内部 document を参照し、通常はページ本体の SVG 要素を `d3.select` で取得する。

### packages/mermaid/src/rendering-util/setupViewPortForSVG.ts

SVG のビューポートを設定するユーティリティ。`getBBox` でコンテンツ範囲を取得し、パディングを加えた `viewBox` を設定する。`configureSvgSize` で幅・高さと `useMaxWidth` を反映させる。

### packages/mermaid/src/rendering-util/splitText.ts

テキストを指定幅に収まるよう分割するユーティリティ。`Intl.Segmenter` でグラフェム/単語単位に分割し、`splitLineToFitWidth` で幅チェック関数に基づいて複数行に分割する。単語が長すぎる場合は `splitWordToFitWidth` で文字単位に分割する再帰的アルゴリズムを使用する。

### packages/mermaid/src/rendering-util/types.ts

rendering-util 全体で使用される型定義ファイル。`MarkdownWord`/`MarkdownLine`/`CheckFitFunction`・`Node`（`ClusterNode` | `NonClusterNode`）・`Edge`・`LayoutData`・`ShapeRenderOptions`・`KanbanNode` などの主要インターフェースを定義する。

### packages/mermaid/src/rendering-util/uid.ts

ユニーク ID を生成する `Uid` クラス。静的カウンターで連番を管理し、`Uid.next(name)` で `name123` 形式の ID を生成する。`href` プロパティと `toString()` メソッドで SVG の `url(#id)` 参照に直接使用できる。

---

## packages/mermaid — docs/.vitepress

### packages/mermaid/src/docs/.vitepress/canonical-config.ts

ドキュメントサイト用の canonical URL 設定を定義する。ベース URL・自動生成無効・除外パターン・変換ルールを定義した `canonicalConfig` オブジェクトと、相対パスから canonical URL 文字列を生成する `getCanonicalUrl` 関数を提供する。

### packages/mermaid/src/docs/.vitepress/canonical-urls.ts

VitePress の `transformPageData` フックから呼ばれる canonical URL 付与ロジック。パスの変換（`.md` 拡張子除去・`index` 除去・カスタム変換）、`<link rel="canonical">` の `<head>` への挿入を行う。

### packages/mermaid/src/docs/.vitepress/config.ts

mermaid ドキュメントサイトの VitePress 設定ファイル。ナビゲーション・サイドバー（syntax/config/ecosystem/community/news の各セクション）・OGP メタタグ・Shiki コードハイライト・canonical URL 付与・ホームページヒーローコピー変換を設定する。`DOCS_HOSTNAME` 環境変数でデプロイ先に応じてロゴやナビを切り替える。

### packages/mermaid/src/docs/.vitepress/contributors.ts

GitHub のコントリビューター一覧（`contributor-names.json`）とチームメンバーリストを統合し、アバターパスを付与してソートされた `teamMembers` 配列を生成する。コントリビューター出現順にチームメンバーを並び替え、クリエイターの Knut を先頭に置く。

### packages/mermaid/src/docs/.vitepress/headerDomainRules.ts

ホスト名（`mermaid.js.org` かどうか）に応じてヘッダーロゴ・ロゴリンク・ナビゲーションを切り替えるユーティリティ。`getHeaderLogo`・`getHeaderLogoLink`・`withConditionalHomeNav` を提供し、`mermaid.ai` 系デプロイでは「Home」ナビアイテムを追加する。

### packages/mermaid/src/docs/.vitepress/homepageHeroCopy.ts

`mermaid.js.org` 以外のドメインでビルドする場合に、ホームページのヒーローセクション（`index.md` のフロントマター）を書き換える `applyHomePageHeroCopy` 関数を提供する。VitePress の `transformPageData` フックから呼ばれ、ビルド時に静的な frontmatter を動的に上書きする。

### packages/mermaid/src/docs/.vitepress/mermaid-markdown-all.ts

VitePress の markdown-it プラグインとして、コードフェンス内の `mermaid`・`mermaid-example`・`warning`・`note`・`regexp`・`jison` ブロックを専用レンダリングに変換する。mermaid ブロックは `<Mermaid>` Vue コンポーネント（`<Suspense>` でラップ）に変換される。

### packages/mermaid/src/docs/.vitepress/ossHeroClass.ts

ホームページのヒーローコンポーネントに特定のCSSクラス (`oss-home-name-clip`) を付与するユーティリティ。`mermaid.ai` とそのサブドメインでは適用をスキップし、`/` のパスのときのみ VitePress のヒーロー `.name.clip` 要素にクラスを追加する。

### packages/mermaid/src/docs/.vitepress/scripts/fetch-avatars.ts

`contributor-names.json` に記載された GitHub ユーザーのアバター画像を GitHub から一括ダウンロードするスクリプト。バッチサイズ10で並列ダウンロードし、既存ファイルはスキップする。CI 環境ではエラー時にプロセスを終了させる。

### packages/mermaid/src/docs/.vitepress/scripts/fetch-contributors.ts

GitHub API からコントリビューター一覧を全ページ取得し `contributor-names.json` に保存するスクリプト。ローカル環境では既存ファイルがあればスキップし、CI 環境では毎回フェッチする。ボットアカウントはフィルタリングして除外する。

### packages/mermaid/src/docs/.vitepress/teamMembers.ts

Mermaid プロジェクトのコアチームメンバー情報（GitHub ID・氏名・Twitter・Mastodon・LinkedIn・ウェブサイト等）を定義する。クリエイターの `knut` と `plainTeamMembers` 配列をエクスポートし、`contributors.ts` 側でソーシャルリンクを付与して使用される。

### packages/mermaid/src/docs/.vitepress/theme/OssHomeHeroNameClipApplier.ts

Vue 3 の `defineComponent` で定義されたホームページ専用コンポーネント。`onMounted` フック内で `applyOssHomeHeroNameClipClass` を呼び出し、ヒーローの `.name.clip` 要素に CSS クラスを付与する。DOM 操作のみでテンプレートは持たない（`null` を返す）。

### packages/mermaid/src/docs/.vitepress/theme/index.ts

VitePress カスタムテーマのエントリポイント。DefaultTheme をベースに `Mermaid`・`Contributors` コンポーネントを登録し、`TopBar`・`HomePage`・`Tooltip`・`EditorSelectionModal`・`OssHomeHeroNameClipApplier` を各レイアウトスロットに挿入する。Plausible アナリティクスの初期化と旧 URL リダイレクト処理も行う。

### packages/mermaid/src/docs/.vitepress/theme/mermaid.ts

ドキュメントサイトで mermaid をインスタンス化・設定し SVG を返す `render` 関数を提供する。zenuml・elk・tidy-tree の外部ダイアグラム/レイアウトと logos アイコンパックを登録し、`mermaid.render` をラップした形でエクスポートする。

### packages/mermaid/src/docs/.vitepress/theme/plausible.ts

Plausible Analytics のトラッキングを初期化・実行するユーティリティ。`initPlausible` でトラッカーをロード・初期化し、`trackPlausibleEvent` でカスタムイベントを送信する。SSR（server-side）では動作しないよう `typeof window` チェックを行う。

### packages/mermaid/src/docs/.vitepress/theme/redirect.ts

旧ドキュメント URL から新 VitePress URL へのリダイレクトマッピングを管理する。`idRedirectMap`（旧ドキュメント ID → 新パス）と `urlRedirectMap`（旧 URL → 新 URL）の2種類のマッピングテーブルを持ち、`getRedirect` 関数でリダイレクト先パスを返す。

### packages/mermaid/src/docs/vite.config.ts

ドキュメントサイトのビルド設定。VitePress の最適化除外、unplugin-vue-components・UnoCSS（Uno/Attributify/Icons プリセット）・Vitepress-plugin-search の設定、mermaid 本体のエイリアス解決、ファイルインクルード用カスタムプラグインなどを定義する。`DOCS_HOSTNAME` 環境変数を `define` で注入する。

---

## packages/mermaid — その他ユーティリティ

### packages/mermaid/src/utils/base64.ts

文字列を UTF-8 エンコードしてから Base64 に変換する `toBase64` 関数のみを持つ小さなユーティリティ。`TextEncoder` と `btoa` を組み合わせて Unicode 文字列を正しく Base64 化する（MDN の「Unicode 問題」に対応）。sandbox iframe の src 生成などに使用される。

### packages/mermaid/src/utils/imperativeState.ts

リセット可能な状態コンテナ `ImperativeState<S>` クラスを提供する。コンストラクターに初期状態を返す関数を渡し、`reset()` で初期状態に戻せる。ダイアグラム DB などパース間で状態をリセットする必要がある用途に使用される。

### packages/mermaid/src/utils/lineWithOffset.ts

エッジの両端にあるマーカー（矢印頭）のサイズ分だけ線の始点・終点を短縮するオフセット計算ユーティリティ。`markerOffsets` に各マーカー種別のピクセルオフセット値を定義し、`getLineFunctionsWithOffset` で d3 line の x・y アクセサ関数を返す。in-source テストも含む。

### packages/mermaid/src/utils/sanitizeDirective.ts

mermaid のディレクティブ（`%%init%%` 等で渡される設定オブジェクト）をサニタイズする `sanitizeDirective` 関数を提供する。`configKeys` に存在しないキーや `__proto__` 系キーを削除し、CSS 値のバランスチェックを行う `sanitizeCss` も含む。プロトタイプ汚染や XSS を防ぐ。

### packages/mermaid/src/utils/subGraphTitleMargins.ts

フローチャートのサブグラフタイトルの上下マージンを `FlowchartDiagramConfig` から計算して返す `getSubGraphTitleMargins` 関数のみを持つ小さなユーティリティ。上下の値と合計値の3つを返す。

### packages/mermaid/src/themes/erDiagram-oldHardcodedValues.ts

ER ダイアグラムの旧スタイルで使われていたハードコードされた背景色定数2つ（奇数行 `#ffffff`・偶数行 `#f2f2f2`）をエクスポートするだけの小さなファイル。テーマファイルが参照して後方互換性を維持するために残されている。

### packages/mermaid/src/tests/util.ts

vitest 向けテストユーティリティを提供する。Jest のタグテンプレートリテラル形式を vitest の配列形式に変換する `convert` 関数、JSDOM を使って D3 を動作させるための `jsdomIt` ヘルパー、重複 ID 検出の `assertNoDuplicateIds`、セレクタで DOM 要素を取得する `ensureNodeFromSelector` などを含む。
