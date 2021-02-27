# Observability Stack for Local Dev

This is a docker-compose setup for bringing up a local Grafana stack and examples of how to set up local development environments to write data to this stack, and even proxy it to SaaS solutions. This enables developers to continue using observability-driven development feedback loops even when working offline. Once things are set up here, going online/offline should be mostly transparent too.

# Status

This ain't ready yet. I just dumped these configs here to get it out on GitHub rather than just running my mouth on Twitter.

# Limitations

The UI tools available here don't seem to have the same kind of discovery tools the SaaS tools typically offer, so the Loki / promtail part becomes important for UX so that folks who log their trace / span ids can at least use log links to get to their traces in a couple clicks.

# Questions

Some stuff I'm not sure about maybe y'all know.

   * what's the best way to get promtail to slurp logs from a separate docker-compose instance running my service code?
   * how do I make the right URL for getting to Grafana obvious and accessible?

# PR Ideas

   * add prometheus and wire up the metrics path through the otel collector

