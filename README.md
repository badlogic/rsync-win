# rsync-win (fork)

Fork of [rn7s2/rsync-win](https://github.com/rn7s2/rsync-win) with additional flags.

## Additional flags

- `--chmod=CHMOD` - Affect file and/or directory permissions
- `--no-perms` - Do not preserve permissions  
- `--omit-dir-times` - Omit directories from --times
- `-z, --compress` - Compress file data during transfer

## Usage

```
rsync-win.exe [OPTIONS] --src <SRC> --dest <DEST>

Options:
  -i, --identity <IDENTITY>  SSH identity file
  -v, --verbose              
  -q, --quiet                
  -c, --checksum             
  -a, --archive              
  -r, --recursive            
      --delete               
      --exclude <EXCLUDE>    
      --partial              
      --progress             
      --bwlimit <BWLIMIT>    
  -4, --ipv4                 
  -6, --ipv6                 
      --ssh-port <SSH_PORT>  
      --chmod <CHMOD>        Affect file and/or directory permissions
      --no-perms             Do not preserve permissions
      --omit-dir-times       Omit directories from --times
  -z, --compress             Compress file data during transfer
  -s, --src <SRC>            
  -d, --dest <DEST>          
  -h, --help                 Print help
  -V, --version              Print version
```

## Building

```bash
cargo build --release
```

Then copy `target/release/rsync-win.exe` alongside the `cygwin64` folder from the original rsync-win release.

## Release

Tag with `v*` to trigger GitHub Actions build.
