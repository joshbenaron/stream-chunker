# An example

    Chunker = require('stream-chunker');
    var chunker = Chunker(16) // split the stream of data into 16 byte chunks
    // make sure to add the event listeners/pipes before writing data
    chunker.on('data', function(data) {
        //do something with a 16 byte chunk of data
    });
    someStream.pipe(chunker); // pipe some data to chunker to get chunked
