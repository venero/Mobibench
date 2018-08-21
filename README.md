Mobile benchmark tool (mobibench)
================================

### Original repo: 
https://github.com/ESOS-Lab/Mobibench

### Sample usage: 

```
sudo ./Mobibench/shell/mobibench -p ./mount/mnt-nova/ -t 20 -d 0 -n 10000000 -j 3
```

### Build (shell version)
```
cd shell
make
```


### Usage (shell version)

	# mobibench [-p pathname] [-f file_size_Kb] [-r record_size_Kb] [-a access_mode] [-h]
                    [-y sync_mode] [-t thread_num] [-d db_mode] [-n db_transcations]
                    [-j SQLite_journalmode] [-s SQLite_syncmode] [-g replay_script] [-q]
                                     
                                     
* -p  set path name (default=./mobibench)
* -f  set file size in KBytes (default=1024)
* -r  set record size in KBytes (default=4)
* -a  set access mode (0=Write, 1=Random Write, 2=Read, 3=Random Read) (default=0)
* -y  set sync mode (0=Normal, 1=O_SYNC, 2=fsync, 3=O_DIRECT, 4=Sync+direct,
                     5=mmap, 6=mmap+MS_ASYNC, 7=mmap+MS_SYNC 8=fdatasync) (default=0)
* -t  set number of thread for test (default=1)
* -d  enable DB test mode (0=insert, 1=update, 2=delete)
* -n  set number of DB transaction (default=10)
* -j  set SQLite journal mode (0=DELETE, 1=TRUNCATE, 2=PERSIST, 3=WAL, 4=MEMORY, 
                               5=OFF) (default=1)
* -s  set SQLite synchronous mode (0=OFF, 1=NORMAL, 2=FULL) (default=2)
* -g  set replay script (output of MobiGen)
* -q  do not display progress(%) message                                                           			

