# Linked Claims

Specification Status: Draft

<details>

<style>
dl {
  margin: 1em 0;
}
summary {
  font-weight: bold;
}
dt {
  font-weight: bold;
}
dd {
  margin-left: 2em;
}
</style>

  <summary>More details about this document</summary>
  <dt>Companion Paper:</dt>
  <dd><a href="#">Addressability is The Missing Link (in the Web of Trust)</a></dd>

  <dt>Editors:</dt>
  <dd>Golda Velez</dd>
  <dd>Andor Kesselman</dd>
  <dd>(add here as people contribute)</dd>
  
  <dt>Authors:</dt>
  <dd>Golda Velez</dd>
  <dd>Agnes Koinange</dd>
  <dd>Phil Long</dd>
  <dd>(add here as people contribute!)</dd>
  
  <dt>Feedback:</dt>
  <dd><a href="https://github.com/org/repo">GitHub Issues</a></dd>
  
  <dt>Related Documents:</dt>
  <dd><a href="#">tbd</a></dd>
</dl>

</details>

## Abstract

Evaluating the credibiity of digital information about the real world is a difficult problem, one which is not sufficiently addressed by cryptographic signing or blockchain validation.  An open, interoperable, cross-domain web of trust could enable robust credibility assessment; a number of projects pursue this goal.  LinkedClaims is a minimal standard to enable links between independent claims: each claim must be addressable (ie have a URI), must be about an addressable subject, and must be cryptographically signed.  Several desirable features are also identified, such as the ability to make a determinate hash of claim content.  The LinkedClaim pattern already exists in several independent projects and implementations; by defining profiles or mappings for these existing data structures to a LinkedClaim data model, we enable linking them together without requiring changes to their native formats.

