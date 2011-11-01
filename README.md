##Installation

###1. update deps file
Add the following lines to your deps file

	[JirgnAssetsGoldenGridBundle]
		git=https://github.com/jirgn/JirgnAssetsGoldenGridBundle.git
		target=/bundles/Jirgn/Assets/GoldenGridBundle

###2. trigger vendor update
use bin/vendors update command to get the repository

###3. register namespaces
add following code to your app/autoload.php

	$loader->registerNamespaces(array(
		...
		'Jirgn'=> __DIR__.'/../vendor/bundles',
		...
	);
###4. add bundle to kernel
add following code to your app/AppKernel.php::

	public function registerBundles()
		{
		...
		new Jirgn\Assets\GoldenGrid\JirgnAssetsGoldenGridBundle(),
	}
