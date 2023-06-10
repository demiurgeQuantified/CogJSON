# CogJSON
JSON schema and dataset for Toontown Online Cogs, primarily aiming to allow fan projects to easily utilise and customise Cogs.
## Aims:
- [x] Complete Cog dataset
- [ ] Attack data
- [ ] Panda3D library to parse the data and quickly create Cog actors
## Cog Format
Name | Type | Description | Default Value
--- | --- | --- | ---
department | String | The cog's department ("sellbot", "cashbot", "lawbot", "bossbot") | Required
body | String | The cog's body type ("a", "b", "c") | Required
size | Float | The scaling factor applied to the cog's body. | Required
head | String | The head mesh the cog uses. Must be a part of that body type's heads file. | Required
headTexture | String | The path to a texture to override the head mesh's with. | None
head2 | String | An additional head mesh to use (flunky glasses). | None
headColor | Color | The head's color tint. | None
gloveColor | Color/string | The tint of the cog's gloves. Can also be the string name of a cog department to get that department's default glove color. | Default color for the cog's department
minLevel | Integer | The lowest level this cog appears at. | 1
numLevels | Integer | How many levels this cog ranges between. The cog's max level will be minLevel plus this number, minus 1 | 5
## Body Format
Name | Type | Description | Default Value
--- | --- | --- | ---
model | String | The path of this body's main model. | Required
headsModel | String | The path of the model where the heads are stored. | Required
loseModel | String | The path of the model used when the cog is exploding | None
loseAnim | String | The name of the animation used when the cog is exploding | lose
animations | Dictionary | Pairs of animation names and model paths. | None
### Skelecog Format
Name | Type | Description | Default Value
--- | --- | --- | ---
model | String | The path of the model to use when a skelecog. | Required
loseModel | String | The path of the loseModel to use when a skelecog. | Required
## Department Format
Name | Type | Description | Default Value
--- | --- | --- | ---
blazer | String | The path of this department's torso texture. | Required
leg | String | The path of this department's leg texture. | Required
sleeve | String | The path of this department's sleeve texture. | Required
tie | String | The path of the tie texture, used for skelecogs. | Required
gloveColor | Color | Default glove color for this department. | None
### Medallion Format
Name | Type | Description | Default Value
--- | --- | --- | ---
model | String | The path to the model where the medallion is stored. | Required
part | String | If the medallion stores multiple models, the name of the part containing the wanted medallion. | Required
color | Color | The color to tint the medallion. | Required
## Attack Format
Attacks are planned but not included in the current version of the dataset, and the format outlined in the schema is WIP.
