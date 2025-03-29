# tobase
Really simple bash script to convert between number bases


A bc wrapper script to convert between number bases provided.

Usage:

    Using Here-String:
    tobase <oBase> <<< 0{x|b|o|[d]}...
    
    Using pipe:
    echo "0{x|b|o|[d]}..." | tobase <oBase>

Returns: The current number converted to <oBase>

Binary output is padded to multiple of 1byte(8bits)

Examples:

    $ echo "0xA3" | tobase 2
    10100011
    $ tobase 10 <<< 0b00101101
    45
    $ echo "356" | tobase 8
    544
