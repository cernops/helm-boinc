# Helm Boinc

## Boinc Setup

The chart expects some configuration related to a valid Boinc account.

To use it with the LHC@home project (as an example), visit [its
homepage](http://lhcathome.cern.ch/lhcathome/) and create an account. Then
check the section *Account Keys* under *Account Information* - this is the
value to pass for *accountKey* in the chart values file.

If you wish to use another project such as SETI@home, make sure you also update
the *project* field.

## Deployment

You can rely on the CERN repository setup if you wish, or else install the
chart by fetching it locally first.
```bash
helm repo add cern https://s3-website.cern.ch/cern-charts
helm install cern/boinc
```

## LHC@home Setup

You can choose which applications you want to run directly on the [project
preferences](https://lhcathome.cern.ch/lhcathome/prefs.php?subset=project) web
page.

Note that if you choose to run *ATLAS Simulation* you need to uncomment the
repositories defined under *cvmfs* in the values file.

## Development

Feel free to open issues or submit merge requests.
