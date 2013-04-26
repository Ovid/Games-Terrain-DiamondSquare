# NAME

Games::Terrain::DiamondSquare - Random terrain generation via the Diamond Square algorithm

# VERSION

version 0.02

# SYNOPSIS

    use Games::Terrain::DiamondSquare 'create_terrain';
    my $terrain = create_terrain( $height, $width, $roughness );

    foreach my $row (@$terrain) {
        foreach my $square (@$row) {
            # $square is a "height" value from 0.0 to 1.0. Do with it as you will
        }
    }

# DESCRIPTION

From Wikipedia: The diamond-square algorithm is a method for generating highly
realistic heightmaps for computer graphics. It's a fractal method of
generating random terrain "heights" which is reasonably fast (though this
being Perl, it's not fast enough for, say, real-time rendering).  A proper C
implementation would be nice here.

There is a `tohtml.pl` example in the `examples` directory of this
distribution.

# EXPORT

## `create_terrain`

    my $terrain = create_terrain( $height, $width );
    # or
    my $terrain = create_terrain( $height, $width, $roughness );

This function accepts integer `$height` and `$width` arguments and an
optional `$roughness` parameter. The latter is a float from 0.0 to 1.0
indicating how "rough" the map should be. Lower numbers generate smoother
maps. Defaults to `0.5`.

# EXAMPLE

Here's an example terrain generated from a test script:

    $$$$$$$$$$$$$$$$$$$$$$$####################*********************!**!!!!!!!!!!!!!
    $$$$$$$$$$$$$$$$$$$$$$#####################****************************!!!!!!!!!
    $$$$$$$$$$$$$$$$$$$$$$###########################*#*##*#*####************!!!!!!!
    ####$####$#$#$$$$$$$$$##########################################**********!!!!!!
    ################$$$$$$$$##########################################**********!!!!
    #################$$$$$$$$$##########################################**********!!
    *###############$$$$$$$$$$$#########################$##$#$$$$########**********!
    ****#*############$$#$##$##########################$$$$$$$$$$$########**********
    ********#############################################$$$$$$$$#########**********
    *************#########################################$#$##$########************
    !*!*************###################################################*************
    !!!!!!*!**********####*##*#*#######################################*************
    !!!!!!!!!!!*****************############$##########################*************
    =!!!!!!!!!!!!***************###########$$$##########################**#*#*******
    ====!!!!!!!!!!!!***********############$$$$$#############################*******
    ;=======!!=!!!!!!!**********##**#######$##############################**********
    ;;;;;;========!!!!!!!***************###############################*************
    ;;;;;;;;========!!!!!!!!*!*!**********############*##############************###
    ;;;;;;;;;;;=====!!!!!!!!!!!!!!!********#*#**************######*************#####
    :;;;;;;;;;;======!!!!!!!!!!!!!!!***************************#*#*********#########
    :::;;;;;;;;;======!!!!!!!!!!!!!!!*************************************##########
    ::::::;;;;;;=======!!!!!!!!!!!!!!!*!*******************************#############
    ~:::::;;;;;;;;=========!!=!!!!!!!!!!!!!*!***************************############
    ~~::::::;;;;;;;;=;===========!=!=!!!!!!!!!!!!!!!*********************#*#########
    ~~~~:::::::;;;;;;;;=;===============!!!!!!!!!!!!!!!*********************########
    ~~~~~~:::::::;;;;;;;;;;;;;=;==========!!!!!!!!!!!!!*!*******************########
    -~~~~~~~::::::::::;;;;;;;;;;;;;==========!=!!!!!!!!!!!!*****************########
    ----~~~~~~~::::::::::;;;;;;;;;;;;=============!!!!!!!!!***************##########
    ------~~~~~~~~:~:::::::;;;;;;;;;;;;;============!!!!!!!!**************#######$$$
    ,--------~-~~~~~~~:::::::::::;;;;;;;;;==========!!!!!!!!!***********#########$$$

# SEE ALSO

You can read about the algorithm at
[http://www.gameprogrammer.com/fractal.html#diamond](http://www.gameprogrammer.com/fractal.html#diamond)

This implementation is based off of
[http://www.smokycogs.com/blog/plasma-fractals/](http://www.smokycogs.com/blog/plasma-fractals/).

# AUTHOR

Curtis "Ovid" Poe <ovid@cpan.org>

# COPYRIGHT AND LICENSE

This software is copyright (c) 2013 by Curtis "Ovid" Poe.

This is free software; you can redistribute it and/or modify it under
the same terms as the Perl 5 programming language system itself.