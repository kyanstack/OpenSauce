# GitDaw 🎹 - Streamline Your Ableton Collaboration

GitDaw simplifies the process of collaborating on Ableton projects by utilizing the power of Git for version control. 
It enables team members to work on projects simultaneously while tracking changes in a structured manner. 
The workflow includes converting Ableton .als files to JSON format for better Git integration, while Git LFS handles large audio and MIDI files. 
This approach ensures an efficient and organized collaboration experience for your music production projects.

## Workflow Overview:
- Convert your Ableton Live Set (.als) file to JSON format using the provided script.
- Commit and push changes to the Git repository, including any new or modified audio and MIDI files.
- Collaborators can pull changes from the Git repository, download the necessary audio and MIDI files with Git LFS, and convert the JSON file back to an Ableton Live Set (.als) file.
- Collaborators can work on the project in Ableton, make their changes, and repeat the process by converting their updated Live Set to JSON, committing, and pushing changes to the Git repository.

By following this workflow, GitDaw helps maintain a clear history of changes and ensures a smooth, organized collaboration process for Ableton Live users.

## Installation

Install Git LFS by following the instructions on the [official website](https://git-lfs.github.com/).

Install the dependencies and build the project:
```
npm run init
```

## Usage

### Import Changes to Ableton

Convert ableton json file to `.als` file:
```
npm run jsonToAls -- yourFileName
```

Download large files (audio and MIDI files):
```
git lfs pull
```

You can now open the `.als` file in Ableton and make your changes.

### Commit Your Changes

After making changes in Ableton, convert the `.als` back to JSON:

```
npm run alsToJson -- yourFileName
```

This will create/update the [JSON file](https://github.com/raphaelDkhn/crs_live_set/tree/main/live_set/json).

Commit your changes and open a Pull Request.

### Prepare a Pull Request

Please write a descriptive title for the pull request that summarizes the changes you made.

In the description, provide more details about your changes. A good pull request description for this repository should include:
- A brief overview of the changes made to the Live Set, such as new tracks, effects, or instruments added.
- The specific sections of the Live Set that were affected, including track numbers or timecodes, if applicable.
- Any additional notes or context about your changes, such as the reason for making them or any feedback you're seeking from others.

Here's an example of a well-written pull request description:

```
This pull request adds a new bassline to the Ableton Live Set.

Changes made:

- Added a new track with a bass synth (Track 5).
- Created a bassline pattern in the session view (1:00 - 1:30).
- Adjusted the EQ and added compression to the bass track for better mixing.

I created this bassline to add more depth to the track and complement the existing melody. 
I'm looking for feedback on the sound design and any suggestions for improving the bassline pattern. 
Also, let me know if you think the bass sits well in the mix or if any further adjustments are needed.
```
