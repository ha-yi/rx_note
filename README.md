# rx_note

catatan mengenai RxJava



## Handle Exception.
```
Observable.error(Exception).onErrorResumeNext { exc ->
  // cek type `exc` apakah exception yg mau kita capture atau ga....
  // Misal kalo file not found kita finish, selain itu kita continue....
  // if (exc is FileNotFoundException) --> Observable.empty()
  // else --> Observable.just(NEXT VALUE)
}
```


## Mengulang Observable ketika terjadi error.
