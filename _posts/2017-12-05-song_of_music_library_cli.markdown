---
layout: post
title:      "song of music library CLI"
date:       2017-12-05 11:59:21 -0500
permalink:  song_of_music_library_cli
---

Note for myself: 

    `class Song
        extend Concerns::Findable

     attr_accessor :name,:artist, :genre

     @@all = []

     def initialize(name, artist = nil, genre = nil, file_name = nil)
       @name = name
       self.artist=(artist) if artist
       self.genre=(genre) if genre
       self.file_name=(file_name) if file_name
     end
    end` 

So artist = nil means a optional second argument here, it can be = nil. 
self.artist=(artist) if artist, it means that if there is artist; then run class song artist=(artist).
same goes to genre and file_name arguments here, they are optional aruments.
Last I want to say I'm pround of myself, it had been a long road;lots of practices does pay off! you learned more and more everyday, keep fighting. 

     `def artist=(artist)
        @artist = artist
        artist.add_song(self)
     end`
		 
		 
Here since you have .add_song method at the other Class, you can put in (self) here as an argument as for song class for this artist= method at Song class.

     `def self.all
       @@all
     end

      def save
       @@all << self
    end

     def self.destroy_all
       self.all.clear
     end

     def self.new_from_filename(file_name)
       song = Song.new(file_name.split(" - ")[1])
       song.artist = Artist.find_or_create_by_name(file_name.split(" - ")[0]
	     song.genre = Genre.findorcreatebyname(filename.split(" - ")[2].delete".mp3")  
	     song.artist.add_song(song)
       song
     end
		 
		 
  <<--you can use .delete " " or .gsub(".mp3","')
	
       def self.create_from_filename(file_name)
         @@all << self.new_from_filename(file_name)
       end`

