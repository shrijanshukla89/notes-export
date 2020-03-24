# notes-export

### Export HTML copies of your notes from Apple Notes

I have made a change to handle the scenario where there are multiple notes with the same title. Content is appended to the exported file of the same name. 

Original script by Alex Chan <alex@alexwlchan.net>

    --
    -- notes-export.scpt
    -- Alex Chan <alex@alexwlchan.net>
    --
    -- Export all the notes from Notes.app into a folder as HTML text.
    -- A very basic backup script.
    --
    -- Usage:
    --  * Open this file in Script Editor
    --  * Run
    --  * Select a folder to export files to
    --
    -- Output:
    --  * A collection of (Latin-1 encoded) HTML files
    --  * A list of attachment names for each note.
    --
    -- Known issues:
    --  * Only the names of attachments are exported, not the files
    --    themselves.  (Look for the files in
    --    ~Library/Group Containers/group.com.apple.notes/Media).
    --  * Some attachment types (e.g. app links) show up as "Missing value"
    --  * Some formatting is lost.
    --  * It will exported notes in the "Recently Deleted" folder which
    --    haven't been purged from disk yet.
    --
