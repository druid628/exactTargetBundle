# ExactTargetBundle

Symfony bundle for Exact Target library


## Installation

### Composer: 

Add exacttarget-bundle to composer.json

    {
        "require": {
            "druid628/exacttarget-bundle": "1.0.1"
        }
    }

    php composer.phar install

### AppKernel

Add ExactTargetBundle to the app/AppKernel.php file.

    class AppKernel extends Kernel
    {
        public function registerBundles()
        {
            $bundles = array(
                // ...
                new Druid628\ExactTarget\ExactTargetBundle\ExactTargetBundle(),
            )
        }
    }
                
 
## Configuration

In your app/config/config.yml add the following entries with your correct information:

    exact_target:
        credentials:
            username: 'yourUsername'
            password: 'yourPassword'
            server:   's4'


## Usage

From any where the ServiceContainer is available you can execute:

    $etClient = $container->get('exacttarget'); 

This will return you an instance of \druid628\exactTarget\EtClient [(more info)](https://github.com/druid628/exacttarget/wiki/EtClient)


## CHANGELOG
 
 * v1.0.0 - DO NOT USE - Initial Commit Contained Namespace issues
 * v1.1.0 - Added simple documentation (@druid628)  and Corrected Namespace issues (@rk3rn3r)

## Contributors

 * Micah Breedlove - <https://github.com/druid628> - [@druid628](http://twitter.com/druid628)
 * René Kerner     - <https://github.com/rk3rn3r>


