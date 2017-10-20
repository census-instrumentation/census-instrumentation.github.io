+++
Description = ""
Tags = ["Development", "golang"]
Categories = ["Development", "GoLang"]
menu = "main"
+++

<table>
<tr>
<td><img src="/images/census-logo-simple.svg" width="400"></td>
<td>
<h1> What is OpenCensus?</h1>

<p>A single distribution of libraries that automatically collects traces and
metrics from your app, displays them locally, and sends them to any analysis
tool.</p>
</td>
</tr>
</table>

The key features of OpenCensus include:

+   Standard wire protocols
    ([TraceContext](https://github.com/TraceContext/tracecontext-spec)) and
    consistent APIs for handling trace and metric data.
+   A single set of libraries for many languages, including Java, C++, Go,
    .Net, Python, PHP, Node.js, Erlang, and Ruby.
+   Included integrations with web and RPC frameworks, making traces and
    metrics available out of the box.
+   Included exporters for storage and analysis tools. Right now the list
    includes Zipkin, Prometheus, Datadog, Stackdriver, and Azure App Insights.
+   Full open source availability for additional integrations and export options.
+   No additional server or daemon is required to support OpenCensus.
+   In process debugging: an optional agent for displaying request and
    metrics data on instrumented hosts.

OpenCensus is being developed by a group of cloud providers, Application
Performance Management vendors, and open source contributors. The project is
[hosted on GitHub](https://github.com/census-instrumentation) and all work
occurs there.

## Concepts

### Distributed Tracing

A distributed trace tracks the progression of a single user request as it is
handled by the services and processes that make up an application. Each step is
called a _span_ in the trace. Spans include metadata about the step, including
especially the time spent in the step, called the span's _latency_. You can use
this information to tune the performance of your application.

Example: A customer completes an order on the checkout page of an e-commerce
application. The distributed trace for this request typically shows how the
request passes through the front end web service, the user authentication
service, the product database, and so on.

 Examples of distributed tracing systems include Zipkin, Jaeger, Datadog APM,
and Stackdriver Trace.

### Metrics

An application metric records information about some part of your application
system: the number of orders received, the number of failed authentications, the
number of RPC connections received, and so on. You use this information to track
usage trends and to detect anomalies that might indicate a problem.

OpenCensus automatically collects a set of predefined metrics from certain
runtime libraries, and you can easily send your own application and runtime
metrics. Because OpenCensus is linked with your application, it does not send
system-level metrics such as CPU or memory utilization.

 Examples of metrics analysis systems are Prometheus, Nagios, Datadog, and
Stackdriver Monitoring.

# FAQ

## Who is behind OpenCensus?

OpenCensus is being developed by a group of cloud providers, Application
Performance Management vendors, and open source contributors. The project is
hosted on GitHub and all work occurs there.

OpenCensus was initiated by Google, and is based on instrumentation systems used
inside of Google. OpenCensus is a complete rewrite of the Google system, and has
no Google intellectual property.

## What languages and integrations does OpenCensus support?

Languages supported:
Java (JVM and OpenJDK): versions 7 and above;
Java (Android): runtime version 14 and above;
C++;
Go.

Integrations supported:
Spring, gRPC, JDBC, net/http

Integrations under development: Dropwizard

Would you like to support a language or framework? Contact us!


## What APM tools does OpenCensus support?

The list is not yet available.


## How do I use OpenCensus in my application?

If you are using a supported application framework, follow its instructions
for configuring OpenCensus.

Choose a supported APM tool and follow its configuration instructions for
using OpenCensus.

You can also use the OpenCensus z-Pages to view your
tracing data, with our without an APM tool.

A user's guide will be released as soon as possible.

## What are the z-Pages?

OpenCensus provides a stand-alone application that communicates with the
OpenCensus code linked into your application through a gRPC channel. The
application displays configuration parameters and trace information held in
OpenCensus.


## How can I contribute to OpenCensus?

+   Help people on the discussion forums.
+   Tell us your success story using OpenCensus.
+   Tell us how we can improve OpenCensus, and help us do it.
+   Contribute to an existing library or create one for a new language.
+   Integrate OpenCensus with a new framework.
+   Integrate OpenCensus with a new APM tool.