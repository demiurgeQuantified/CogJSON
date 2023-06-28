# ToontownJSON
ToontownJSON is a JSON schema and dataset for Toontown Online Cogs and Toons. It intends to separate the assets from their implementation details, so that custom assets can be added without strictly following undocumented and arbitrary model configuration. This means that common shortcuts such as phase maps are not utilised in order to keep the schema filesystem agnostic.

It is developed alongside [Toontown Utils](https://github.com/demiurgeQuantified/toontownutils), a Panda3D package that can create Cog/Toon actors from the data.