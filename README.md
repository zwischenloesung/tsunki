# Tsunki

The idea behind 'tsunki' was to create an easy to use, yet very flexible
and extensible knowledge base system.

What would be the most easy way to organize meta information anywhere at any
time? What about simple files just laying around wherever they fit most,
loosely connected through internal associations directly defined in place?

As humans and machines shall access the data likewise, probably YAML pops
up in every mind. Tsunki proposes structures of YAML files by providing
JSON-/YAML-schemas.

For what kind of information is this meta document system created for?

The initial focus was to create a meta layer to abstract
config management environments - but it soon became clear, that it
was quite handy in various situations, from photo collections,
over bookmark management, a sensor device inventory, all the way to
a plant database.

Tsunki can be used in a meaningful way as a standalone solution, but it
becomes really powerful when external software solutions make use of the
above mentioned loose associations together with globally available anchors
connecting things in isolated contexts and presenting facets of the inherent
wisdom, just on request.


## Composition

Tsunki is composed of the following elements.


### Tsunki-Thing

Everything in Tsunki is first of all, a tsunki-thing. A tsunki thing is
a YAML-document containing information about the thing to be described.
It basically is a pointer to the actual thing, enriched with some meta data
about its target it is pointing at.


### Targets

Both abstract and concrete things can be managed by either using the
'target' parameter in the YAML-document, aka 'tsunki-thing', referencing
a list of URIs pointing to concrete things in spacetime or by leaving it
empty, thus "pointing to an idea in the void".


### Relations

Tsunki-things are related to each other. There are different forms of
relations and actions can be associated with them.


### Properties

Tsunki-things have properties. Those properties can be inherited by
other tsunki things. Tsunki-things can inherit from more than one
tsunki-thing and the priority of this relationship can be specified
to address potential conflicts.


### Tsunki-Context

A tsunki-thing exists in a tsunki-context. Usually this is a versioning
system repository.


### Tsunki-Facet

When editing or creating content, the focus mostly lies on a certain thing.
If information is about to be consumed though, the focus lies often on
certain aspects of things, so the data should be filtered and presented
in a view, corresponding to the question asked. This is called a
tsunki-facet here.


