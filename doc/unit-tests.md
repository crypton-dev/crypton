Compiling/running unit tests
------------------------------------

Unit tests will be automatically compiled if dependencies were met in configure
and tests weren't explicitly disabled.

After configuring, they can be run with 'make check'.

To run the cryptond tests manually, launch src/test/test_crypton .

To add more cryptond tests, add `BOOST_AUTO_TEST_CASE` functions to the existing
.cpp files in the test/ directory or add new .cpp files that
implement new BOOST_AUTO_TEST_SUITE sections.

To run the crypton-qt tests manually, launch src/qt/test/test_crypton-qt

To add more crypton-qt tests, add them to the `src/qt/test/` directory and
the `src/qt/test/test_main.cpp` file.
