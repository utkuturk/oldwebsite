---
layout: post
---


First get the recordings from the server

```bash

remote_host="webexperiments@hjpatt-136.umd.edu"
remote_path="/Users/webexperiments/Sites/Web_Experiments/Phillips/Utku/corner_same_verb/uploads/*.zip"
local_path="~/Downloads/rec_feb23"
mkdir "$local_path"

scp "$remote_host:$remote_path" "$local_path"
```

Unzip and convert them to wav

```bash
cd "$local_path"
unzip \*.zip
for i in *.webm; do ffmpeg -i "$i" "${i%.*}.wav"; done
mkdir backup
mv \*.zip ,/backup
rm \*.webm
```


Group them according to the participant id. My random generated id is 8 characters long, thus `{file:0:8}` and `^.{8}_`.

```bash
for file in *; do
  if [[ -f "$file" ]]; then
    prefix="${file:0:8}"
    if [[ "$file" =~ ^.{8}_ ]]; then
      if [[ ! -d "$prefix" ]]; then
        mkdir "$prefix"
      fi
      mv "$file" "$prefix/"
    fi
  fi
done

```

For each participant group the files according to the type of the file. Habituation ones are put into a folder called `fam`, practice, intro and test files are put into a folder called `misc`. Using `nullglob` to prevent errors when there are no files of a certain type.

```bash
# Iterate through the newly created prefix directories
for prefix_dir in */; do
  prefix_dir="${prefix_dir%/}" # Remove trailing slash
  if [[ -d "$prefix_dir" ]]; then

    # Handle _fam_ files
    if [[ ! -d "$prefix_dir/fam" ]]; then
      mkdir "$prefix_dir/fam"
    fi
    setopt nullglob
    for fam_file in "$prefix_dir/"*_*fam_*; do
      if [[ -f "$fam_file" ]]; then
        if [[ "$fam_file" =~ .*_fam_.* ]]; then
          mv "$fam_file" "$prefix_dir/fam/"
        fi
      fi
    done
    unsetopt nullglob

    # Handle misc files (_practice_, _intro_, _test-)
    if [[ ! -d "$prefix_dir/misc" ]]; then
      mkdir "$prefix_dir/misc"
    fi
    setopt nullglob
    for misc_file in "$prefix_dir/"*_*practice_* "$prefix_dir/"*_*intro_* "$prefix_dir/"*_*test-*; do
      if [[ -f "$misc_file" ]]; then
        if [[ "$misc_file" =~ .*_practice_.* || "$misc_file" =~ .*_intro_.* || "$misc_file" =~ .*_test-.* ]]; then
          if [[ ! "$misc_file" =~ .*_fam_.* ]]; then # Ensure it's not a _fam_ file
              mv "$misc_file" "$prefix_dir/misc/"
          fi
        fi
      fi
    done
    unsetopt nullglob
  fi
done
```
