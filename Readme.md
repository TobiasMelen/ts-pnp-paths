## Disclaimer

This is not a package ready for use and is not available through npm. The current implementation has issues making it hard to recommend for use, in production or otherwise.

It's possible to copy the script file for testing purposes. Currently there are no external depencies besides Yarn and Node 8+.

# ts-pnp-paths

Script for generating tsconfig.json file with paths for Yarn pnp project. Running the command will create a new tsconfig file that can be used by extending to it from the main tsconfig file. The generated file should not be included in version control since it's tied to machine specific Yarn cache.

## Options
All are optional

### --rootPath/-r string
Path to folder containing the .pnp.js and yarn.lock file.
Default is **process.cwd()**.

### --configPath/-c string
Path for config file to generate. Relative from --rootPath. Default is **./tsconfig.pnp.json**

### --depth/-d number
Dependency depth of path generation. Leave undefined to generate paths for complete tree (all nested dependencies).

### --info/-i
Adds information output.

### --force/-f
Generate a new tsconfig.json even if yarn lock hasn't changed.

### 