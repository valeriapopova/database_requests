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

insert into Singers
	values(1, 'Виктор Белан', 'Билан');
	
insert into Singers
	values(2, 'Елена Хрулева', 'Ваенга');
	
insert into Singers
	values(3, 'Марина Абросимова', 'Максим');
	
insert into Singers
	values(4, 'Алла Перфилова', 'Валерия');
	
insert into Singers
	values(5, 'Инесса Климчук', 'Ирина Аллегрова');
	
insert into Singers
	values(6, 'Лещев', 'Лещенко');
	
insert into Singers
	values(7, 'Стефани Джоанн Анджелина Джерманотта', 'Леди Гага');
	
insert into Singers
	values(8, 'Шакира Риполь', 'Шакира');
	
insert into Genres
	values(1, 'Рок');
	
insert into Genres
	values(2, 'Блюз');
	
insert into Genres
	values(3, 'Поп');
	
insert into Genres
	values(4, 'Инди');
	
insert into Genres
	values(5, 'Рэп');

insert into Albums 
	values(1, 'tusa', 2000 );

insert into Albums 
	values(2, 'juicy', 2005);

insert into Albums 
	values(3, 'baby baby', 1999);

insert into Albums 
	values(4, 'владимирский централ', 1980);

insert into Albums 
	values(5, '666', 2010 );

insert into Albums 
	values(6, 'Панамера', 2018 );

insert into Albums 
	values(7, 'bad romance', 1972);

insert into Albums 
	values(8, 'good boy', 2008 );
	
insert into Albums 
	values(9, 'my new life', 2017 );	

insert into tracks 
	values(1,'first', 8 , 3.5);

insert into tracks 
	values(2,'heroes', 7 , 3.5);

insert into tracks 
	values(3,'bad guy', 6 , 3.44);

insert into tracks 
	values(4,'sec sec', 5 , 3.56);

insert into tracks 
	values(5,'no kids', 4 , 3.23);

insert into tracks 
	values(6,'moneken', 3 , 4.55);

insert into tracks 
	values(7,'favorite day', 2, 3.22);

insert into tracks 
	values(8,'first thing', 1 , 3.55);

insert into tracks 
	values(9,'my love', 8 , 3.34);

insert into tracks 
	values(10,'мой день', 6 , 3.12);

insert into tracks 
	values(11,'не тот', 5 , 4.14);

insert into tracks 
	values(12,'романтика', 4 , 3.08);

insert into tracks 
	values(13,'великий', 1 , 3.5);

insert into tracks 
	values(14,'мистер ди', 2 , 7.55);

insert into tracks 
	values(15,'короче', 5 , 5.14);
	
insert into collection 
	values(1,'нулевые', 2010);
	
insert into collection 
	values(2,'лучшее из 00-х', 2011);
	
insert into collection 
	values(3,'хиты 90-х', 2001);
	
insert into collection 
	values(4,'хиты 80,90 и наших дней', 2020);
	
insert into collection 
	values(5,'best collection', 2008);
	
insert into collection 
	values(6,'lincoln', 2019);
	
insert into collection 
	values(7,'holiday', 2007);
	
insert into collection 
	values(8,'Christmas', 2021);
	
insert into GenresSinger 
	values(1, 1, 1);
	
insert into GenresSinger 
	values(2, 2, 2);
	
insert into GenresSinger 
	values(3, 3, 4);
	
insert into GenresSinger 
	values(4, 5, 3);
	
insert into GenresSinger 
	values(5, 4, 5);
	
insert into GenresSinger 
	values(6, 3, 6);
	
insert into GenresSinger 
	values(7, 1, 7);
	
insert into GenresSinger 
	values(8, 2, 8);
	
insert into SingerAlbum 
	values(1, 1, 8);
	
insert into SingerAlbum 
	values(2, 2, 7);
	
insert into SingerAlbum 
	values(3, 3, 6);
	
insert into SingerAlbum 
	values(4, 4, 5);
	
insert into SingerAlbum 
	values(5, 5, 4);
	
insert into SingerAlbum 
	values(6, 6, 3);
	
insert into SingerAlbum 
	values(7, 8, 2);
	
insert into SingerAlbum 
	values(8, 7, 1);
	

insert into SingerAlbum 
	values(9, 9, 5);


insert into collection_of_tracks
	values(1, 1);

insert into collection_of_tracks
	values(2, 2);

insert into collection_of_tracks
	values(3, 1);

insert into collection_of_tracks
	values(4, 3);

insert into collection_of_tracks
	values(5, 4);

insert into collection_of_tracks
	values(6, 5);

insert into collection_of_tracks
	values(7, 6);

insert into collection_of_tracks
	values(8, 8);

insert into collection_of_tracks
	values(9, 7);

insert into collection_of_tracks
	values(9, 6);

insert into collection_of_tracks
	values(11, 3);

insert into collection_of_tracks
	values(11, 1);

insert into collection_of_tracks
	values(2, 6);

insert into collection_of_tracks
	values(13, 8);

insert into collection_of_tracks
	values(13, 7);

insert into collection_of_tracks
	values(1, 2);

insert into collection_of_tracks
	values(14, 4);

insert into collection_of_tracks
	values(14, 5);
