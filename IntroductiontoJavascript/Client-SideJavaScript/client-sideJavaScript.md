most client-side JavaScript pro-
grammers choose to use a client-side library or framework to simplify their basic pro-
gramming tasks.

function debug(msg) {
var log = $("#debuglog"); // Find the element to display msg in.
if (log.length == 0) { // If it doesn't exist yet, create it...
log = $("<div id='debuglog'><h1>Debug Log</h1></div>");
log.appendTo(document.body); // and insert it at the end of the body.
}
log.append($("<pre/>").text(msg)); // Wrap msg in <pre> and append to log.
}