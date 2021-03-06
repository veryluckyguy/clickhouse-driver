# Changelog

## [Unreleased]

## [0.0.10] - 2018-03-14
### Added
- Server version specific tests.
- Nothing type.
- Travis CI build matrix.

### Fixed
- Possible IndexError in packet types string representation. Pull request [#28](https://github.com/mymarilyn/clickhouse-driver/pull/28) by [WouldYouKindly](https://github.com/WouldYouKindly).
- Do not use timezone in Date columns. Issue [#29](https://github.com/mymarilyn/clickhouse-driver/issues/29).
- Approximate rows to read calculation in `execute_with_progress`. Pull request [#30](https://github.com/mymarilyn/clickhouse-driver/pull/30) by [b1naryth1ef](https://github.com/b1naryth1ef).

### Changed
- List and Tuple types rendering in parameters substitution. Pull request [#27](https://github.com/mymarilyn/clickhouse-driver/pull/27) by [silentsokolov](https://github.com/silentsokolov).

## [0.0.9] - 2018-01-17
### Added
- Interval type. Pull request [#16](https://github.com/mymarilyn/clickhouse-driver/pull/16) by [kszucs](https://github.com/kszucs).

### Fixed
- Raise EOFError when no data is read in `_read_one` in Python 3.
- SSL file descriptors closing in Python 2.7.

### Changed
- Drop Python 3.2 support due to lz4 issues.
- Log level for normal operations raised to DEBUG. Pull request [#17](https://github.com/mymarilyn/clickhouse-driver/pull/17) by [kmatt](https://github.com/kmatt).

## [0.0.8] - 2017-10-23
### Added
- Parameters substitution for SELECT queries.
- SSL support.

### Fixed
- Columnar result returning from multiple blocks. Columns must be concatenated.
- Settings logger was root.
- Reading/writing Array(String) NotImplementedError raise.
- IPv6 support issue [#12](https://github.com/mymarilyn/clickhouse-driver/issues/12).

## [0.0.7] - 2017-10-12
### Added
- Configurable logging level in tests.
- Full error codes list.
- Force check clickhouse-cityhash is installed if compression is used.
- `Client` can be directly imported from package.
- `insert_block_size` parameter - maximum rows in block (default is 1048576).
- Columnar result returning (`columnar=True`). Pull request [#11](https://github.com/mymarilyn/clickhouse-driver/pull/11) by [kszucs](https://github.com/kszucs).
- Tunable types check (`types_check=True`). Off by default.

### Changed
- Handling only socket-related errors on ping. Errors are logged with `WARNING` level.
- Client is created per one test.
- Sending/receiving data speed significantly increased.

### Fixed
- Version detection in setup.py.
- Error handling on socket.shutdown.
- Install `enum34` only if required.
- `clickhouse-cityhash` import issue [#10](https://github.com/mymarilyn/clickhouse-driver/issues/10).

### Removed
- QuickLZ support
- six dependency

## [0.0.6] - 2017-09-19
### Added
- UUID type.
- Query limits settings.
- Code coverage.
- ClickHouse server and driver version upped to 54276.
- Changelog.
- Added column name to `TypeMismatchError`.
- Query progress information.
- Version of package.

### Fixed
- socket.timeout error handling on connect.

## [0.0.5] - 2017-07-16
### Added
- Nullable(T) type.
- Return data from TOTALS and EXTREMES packets.
- Query settings.
- query_id execution option.
- NULL type.
- Raise exception on SELECT queries.

### Changed
- Small columns refactoring.
- `clickhouse-client` in tests moved to docker.

## [0.0.4] - 2017-06-15
### Added
- FixedString(N) type.
- Enum8/16 types.
- Array(T) type.
- External data for query processing
- Raise UnknownTypeError for unsupported columns.

### Changed
- Socket connect timeout fix.

## [0.0.3] - 2017-05-24
### Added
- QuickLZ, LZ4/LZ4HC, ZSTD compressions.
- Support old servers without BlockInfo.
- Travis CI.
- flake8 syntax check.

## 0.0.2 - 2017-05-16
### Added
- [U]Int8/16/32/64 types.
- Date/DateTime types.
- String types.

[Unreleased]: https://github.com/mymarilyn/clickhouse-driver/compare/0.0.10...HEAD
[0.0.10]: https://github.com/mymarilyn/clickhouse-driver/compare/0.0.9...0.0.10
[0.0.9]: https://github.com/mymarilyn/clickhouse-driver/compare/0.0.8...0.0.9
[0.0.8]: https://github.com/mymarilyn/clickhouse-driver/compare/0.0.7...0.0.8
[0.0.7]: https://github.com/mymarilyn/clickhouse-driver/compare/0.0.6...0.0.7
[0.0.6]: https://github.com/mymarilyn/clickhouse-driver/compare/0.0.5...0.0.6
[0.0.5]: https://github.com/mymarilyn/clickhouse-driver/compare/0.0.4...0.0.5
[0.0.4]: https://github.com/mymarilyn/clickhouse-driver/compare/0.0.3...0.0.4
[0.0.3]: https://github.com/mymarilyn/clickhouse-driver/compare/0.0.2...0.0.3
