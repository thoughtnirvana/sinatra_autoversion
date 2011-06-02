### Sinatra autoversion

Auto-versions static assets so that long cache time can be set on them saving the bandwidth and decreasing
percieved latency.

The `auto_version` method appends the file hash to the file name. If the file changes, the hash changes. This naming
mechanism allows you to set large cache expiry times.

The only chane required is to use::

    link rel="stylesheet" type="text/css" href=auto_version("/css/base.css")

instead of this::

    link rel="stylesheet" type="text/css" href="/css/base.css"


The above example was for slim templates. But the basics are the same for any templating engine.

All static assets, images, css, js...can be and should be autoversioned.

This isn't required with Rails - it does its own form of auto versioning.
