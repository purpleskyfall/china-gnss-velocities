An open source GNSS velocity field in China
===========================================

Velocities are extracted from the crustal deformation data of CMONOC:

    Zhao B, et al., Crustal deformation on the Chinese mainland during
    1998-2004 based on GPS data, Geodesy and Geodynamics (2015)
    http://dx.doi.org/10.1016/j.geog.2014.12.006

The original horizontal velocities are respect to the Eurasia plate,
calculte the absolute values by:

    V = ΔV + ω × X

Where V is the absolute velocities vector of one GPS station, ΔV is
velocities vector respected to Eurasia plate, ω is the Euler vector of
Eurasia plate in ITRF2008, X is the coordinate vector of the station.
----------------------------------------------------------------------
However, the reference frame of the calculted absolute velocities V is
ITRF2008, transform them to ITRF2014 by:

             .   .     .
    V' = V + T + D·X + R·X

      .  .  .
Where T, D, R are transform parameters from ITRF2008 to ITRF2014, see:

    http://itrf.ensg.ign.fr/doc_ITRF/Transfo-ITRF2014_ITRFs.txt

----------------------------------------------------------------------
Units for the records:

    Lat: Latitude in angle degree
    Lon: Longitude in angle degree
    Vx: Velocity(mm/yr) in X component
    Vy: Velocity(mm/yr) in Y component
    Vz: Velocity(mm/yr) in Z component

See the image file for the station distribution.
