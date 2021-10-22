# hwww3
ЗАДАНИЕ 1

create table if not exists Genres (
    id serial primary key,
    name varchar(100)
);

create table if not exists Singers (
id serial primary key,
singer_name varchar(100),
alias varchar(100)
);

create table if not exists GenresSinger (
    id serial primary key,
    genre_id integer not null references Genres(id),
    singer_id integer not null references Singers(id)
);

create table if not exists collection (
    id serial primary key,
    name varchar(100),
    year_of_issue integer
);

create table if not exists Albums (
    id serial primary key,
    album_name varchar(30),
    year_of_issue integer
);

create table if not exists SingerAlbum (
    id serial primary key,
    album_id integer not null references Albums(id),
    singer_id integer not null references Singers(id)
);

create table if not exists tracks (
id serial primary key,
track_name varchar(30),
album_id integer not null references Albums(id),
duration integer not null
);

create table if not exists collection_of_tracks (
    tracks_id integer not null references tracks(id),
    collection_id integer not null references collection(id)
); 
