swagger: "2.0"
x-collection-name: Entertainment Express
x-complete: 1
info:
  title: Entertainment Express
  description: your-gateway-to-building-incredible-movie-tv-and-game-content-discovery-experiences-
  version: "2.0"
host: ee.iva-api.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /TvMedia/lineups/browse/{CountryID}/{RegionID}/{AreaID}:
    get:
      summary: ""
      description: Get lineups by AreaID.
      operationId: GetTvMediaLineupsByAreaID
      x-api-path-slug: tvmedialineupsbrowsecountryidregionidareaid-get
      parameters:
      - in: path
        name: AreaID
        description: Service area ID
      - in: path
        name: CountryID
        description: Country abbreviation
      - in: query
        name: Detail
        description: Set level of detail for response
      - in: query
        name: LineupType
        description: Filter by lineup type, valid types are OTA, SAT, CAB, IPTV
      - in: query
        name: ProviderId
        description: Filter by provider ID
      - in: path
        name: RegionID
        description: Region abbreviation
      - in: query
        name: TvMediaApiKey
        description: API Key supplied by TvMedia
      responses:
        200:
          description: OK
      tags:
      - TvMedia
      - Lineups
      - Browse
      - CountryID
      - RegionID
      - AreaID