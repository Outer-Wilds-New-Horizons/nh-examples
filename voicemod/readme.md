## Voice Mod

New Horizons includes support for the [Voice Acting Mod](https://outerwildsmods.com/mods/voiceactingmod/)! Simply add a folder to your mod with this name, and start adding recorded dialogue to it.

To match up the audio with a character's dialogue, you must name the file in the form "[DialogueTree->NameField] [DialogueTree->DialogueNode->Name] [DialogueTree->DialogueNode->Page number]"

For example, here is a snippet taken from Ernesto.xml:

```
<DialogueTree ...>
    <NameField>Ernesto</NameField>
    ...
    <DialogueNode>
        <Name>1</Name>
        <Dialogue>
            <Page>No I can't. You must be mistaken.</Page>
            <Page>Haha that's a joke. I took speaking as an elective in college.</Page>
        </Dialogue>
        ...
    </DialogueNode>
    ...
</DialogueTree>
```

So for the line "No I can't. You must be mistaken." the audio file must be named "Ernesto 1 0". We get "Ernesto" from the `<NameField>` tag, we get "1" from the `<Name>` tag, and then since this is the first page of dialogue we put 0 (we start counting from 0 instead of from 1).

Then for the line "Haha that's a joke. I took speaking as an elective in college." the audio file must be named "Ernesto 1 1". The NameField and Name are the same, but now we have moved to the next page so we write 1 instead of 0.

The file extension can be .wav or .ogg (and maybe .mp3? but don't do that).