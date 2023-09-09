# expo-music-library

React Native Expo Native music library to retrieve song's albums, genres, artists, folders.
(Only for working for android at the time being, Need a macbook to implements IOS part)

## Table Of contents

- [Installation](#installation)
- [Usage](#usage)
- [API Reference](#api-reference)
- [Buy me a coffee](#buy-me-a-coffee)

## Installation

```
 npm install expo-music-library
```

## Usage

- Import

```
import * as MedialLibrary from "expo-music-library";
```

- Request permission to access storage

  ```
        let permissions = await MusicLibrary.requestPermissionsAsync();
        while (!permissions.granted) {
            permissions = await MusicLibrary.requestPermissionsAsync();
        }
  ```

## API Reference

- Retrieve Audio files

  ```
        const results = await MusicLibrary.getAssetsAsync({
            after: lastMediaAsset,
            mediaType: MusicLibrary.MediaType.audio,
            sortBy: sortBy,
        });
  ```

- Retrieve Albums

  ```
      const folders = await MusicLibrary.getAlbumsAsync()
  ```

- Retrieve Album's Songs

  ```
      const albumAssets = await MusicLibrary.getAlbumAssetsAsync(albumName)
  ```

- Retrieve Artists

  ```
      const artists = await MusicLibrary.getArtistsAsync()
  ```

- Retrieve Artist's Songs

  ```
      const artistAssets = await MusicLibrary.getArtistAssetsAsync(artistId)
  ```

- Retrieve Folders

  ```
      const folders = await MusicLibrary.getFoldersAsync()
  ```

- Retrieve Folder's Songs

  ```
      const folderAssets = await MusicLibrary.getFolderAssetsAsync(folderId)
  ```

- Retrieve Genres

  ```
      const genres = await MusicLibrary.getGenresAsync()
  ```

- Retrieve Genre's Songs

  ```
      const genreAssets = await MusicLibrary.getGenreAssetsAsync(genreId)
  ```

## Buy me a coffee

If my you find my work usefull and want to support me, kindly buy me a coffee here
<a href="https://www.buymeacoffee.com/fullstapp" target="_blank"><img src="https://www.buymeacoffee.com/assets/img/custom_images/orange_img.png" alt="Buy Me A Coffee" style="height: 41px !important;width: 174px !important;box-shadow: 0px 3px 2px 0px rgba(190, 190, 190, 0.5) !important;-webkit-box-shadow: 0px 3px 2px 0px rgba(190, 190, 190, 0.5) !important;" ></a>
