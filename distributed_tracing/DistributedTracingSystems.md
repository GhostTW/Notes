# Distributed Tracing systems

* Tracing, aka distributed tracing, provides insight into the full lifecycles, aka traces, of requests to the system, allowing you to pinpoint failures and performance issues.
* Metrics provide quantitative information about processes running inside the system, including counters, gauges, and histograms.
* Logging provides insight into application-specific messages emitted by processes.

## Organizations / Standards

### W3C

#### Trace Context

A standard for tracing.

### Cloud Native Computing Foundation (CNCF)

云原生技术有利于各组织在公有云、私有云和混合云等新型动态环境中，构建和运行可弹性扩展的应用。云原生的代表技术包括容器、服务网格、微服务、不可变基础设施和声明式API。

这些技术能够构建容错性好、易于管理和便于观察的松耦合系统。结合可靠的自动化手段，云原生技术使工程师能够轻松地对系统作出频繁和可预测的重大变更。

云原生计算基金会（CNCF）致力于培育和维护一个厂商中立的开源生态系统，来推广云原生技术。我们通过将最前沿的模式民主化，让这些创新为大众所用。

* OpenCensus and OpenTracing joined forces under the CNCF.

## library and framework

### OpenTracing API (library?)

透過統一的流程及 API library 來做到跨工具共用追蹤系統

not a standard.

* SPAN
  * An operation name
  * A start timestamp and finish timestamp
  * A set of key:value span Tags
  * A set of key:value span Logs
  * A SpanContext
  * An implementation-dependent state to refer to the distinct span within a trace
  * Any Baggage Items
  * These are key:value pairs that cross process-boundaries.
  * These may be useful to have some data available for access throughout the trace.
* Spans and Relationships
  * Spans
  ![SpanTime](images\spans-time-view.png)

  * Relationships
  ![SpanRelationship](images\spans-relationship-view.png)

### OpenCensus

OpenCensus is a set of libraries for various languages that allow you to collect application metrics and distributed traces, then transfer the data to a backend of your choice in real time.

### OpenTelmely

To replace OpenTracing and OpenCensus projects

## References

[opentracing instrumenting-your-application](https://opentracing.io/docs/best-practices/instrumenting-your-application/)

[W3C trace context](https://www.w3.org/TR/trace-context/#conformance)

[opentelemetry-opentracing-opencensus](https://blog.newrelic.com/engineering/opentelemetry-opentracing-opencensus/)

[CNCF def](https://github.com/cncf/toc/blob/master/DEFINITION.md#%E4%B8%AD%E6%96%87%E7%89%88%E6%9C%AC)