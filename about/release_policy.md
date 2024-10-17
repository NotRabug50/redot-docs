allow\_comments  
False

# Godot release policy

Godot's release policy is in constant evolution. The description below
provides a general idea of what to expect, but what will actually happen
depends on the choices of core contributors and the needs of the
community at a given time.

## Godot versioning

Godot loosely follows [Semantic Versioning](https://semver.org/) with a
`major.minor.patch` versioning system, albeit with an interpretation of
each term adapted to the complexity of a game engine:

-   The `major` version is incremented when major compatibility
    breakages happen which imply significant porting work to move
    projects from one major version to another.

    For example, porting Godot projects from Godot 3.x to Godot 4.x
    requires running the project through a conversion tool, and then
    performing a number of further adjustments manually for what the
    tool could not do automatically.

-   The `minor` version is incremented for feature releases that do not
    break compatibility in a major way. Minor compatibility breakage in
    very specific areas *may* happen in minor versions, but the vast
    majority of projects should not be affected or require significant
    porting work.

    This is because Godot, as a game engine, covers many areas like
    rendering, physics, and scripting. Fixing bugs or implementing new
    features in one area might sometimes require changing a feature's
    behavior or modifying a class's interface, even if the rest of the
    engine API remains backwards compatible.

Tip

Upgrading to a new minor version is recommended for all users, but some
testing is necessary to ensure that your project still behaves as
expected.

-   The `patch` version is incremented for maintenance releases which
    focus on fixing bugs and security issues, implementing new
    requirements for platform support, and backporting safe usability
    enhancements. Patch releases are backwards compatible.

    Patch versions may include minor new features which do not impact
    the existing API, and thus have no risk of impacting existing
    projects.

Tip

Updating to new patch versions is therefore considered safe and strongly
recommended to all users of a given stable branch.

We call `major.minor` combinations *stable branches*. Each stable branch
starts with a `major.minor` release (without the `0` for `patch`) and is
further developed for maintenance releases in a Git branch of the same
name (for example patch updates for the 4.0 stable branch are developed
in the `4.0` Git branch).

## Release support timeline

Stable branches are supported *at least* until the next stable branch is
released and has received its first patch update. In practice, we
support stable branches on a *best effort* basis for as long as they
have active users who need maintenance updates.

Whenever a new major version is released, we make the previous stable
branch a long-term supported release, and do our best to provide fixes
for issues encountered by users of that branch who cannot port complex
projects to the new major version. This was the case for the 2.1 branch,
and is the case for the 3.x branch.

In a given minor release series, only the latest patch release receives
support. If you experience an issue using an older patch release, please
upgrade to the latest patch release of that series and test again before
reporting an issue on GitHub.

<table style="width:99%;">
<colgroup>
<col style="width: 13%" />
<col style="width: 20%" />
<col style="width: 65%" />
</colgroup>
<tbody>
<tr>
<td><strong>Version</strong></td>
<td><strong>Release date</strong></td>
<td><strong>Support level</strong></td>
</tr>
<tr>
<td>Godot 4.4 (<span class="title-ref">master</span>)</td>
<td>Q1 2025 (estimate)</td>
<td><img src="img/unstable.png" alt="unstable" /> <em>Development.</em>
Receives new features, usability and performance improvements, as well
as bug fixes, while under development.</td>
</tr>
<tr>
<td>Godot 4.3</td>
<td>August 2024</td>
<td><img src="img/supported.png" alt="supported" /> Receives fixes for
bugs and security issues, as well as patches that enable platform
support.</td>
</tr>
<tr>
<td>Godot 4.2</td>
<td>November 2023</td>
<td><img src="img/supported.png" alt="supported" /> Receives fixes for
bugs and security issues, as well as patches that enable platform
support.</td>
</tr>
<tr>
<td>Godot 4.1</td>
<td>July 2023</td>
<td><img src="img/supported.png" alt="supported" /> Receives fixes for
bugs and security issues, as well as patches that enable platform
support.</td>
</tr>
<tr>
<td>Godot 4.0</td>
<td>March 2023</td>
<td><img src="img/eol.png" alt="eol" /> No longer supported (last
update: 4.0.4).</td>
</tr>
<tr>
<td>Godot 3.7 (<span class="title-ref">3.x</span>)</td>
<td>No ETA for now</td>
<td><img src="img/supported.png" alt="supported" /> <em>Beta.</em>
Receives new features, usability and performance improvements, as well
as bug fixes, while under development.</td>
</tr>
<tr>
<td>Godot 3.6</td>
<td>September 2024</td>
<td><img src="img/supported.png" alt="supported" /> Receives fixes for
bugs and security issues, as well as patches that enable platform
support.</td>
</tr>
<tr>
<td>Godot 3.5</td>
<td>August 2022</td>
<td><img src="img/supported.png" alt="supported" /> Receives fixes for
bugs and security issues, as well as patches that enable platform
support.</td>
</tr>
<tr>
<td>Godot 3.4</td>
<td>November 2021</td>
<td><img src="img/eol.png" alt="eol" /> No longer supported (last
update: 3.4.5).</td>
</tr>
<tr>
<td>Godot 3.3</td>
<td>April 2021</td>
<td><img src="img/eol.png" alt="eol" /> No longer supported (last
update: 3.3.4).</td>
</tr>
<tr>
<td>Godot 3.2</td>
<td>January 2020</td>
<td><img src="img/eol.png" alt="eol" /> No longer supported (last
update: 3.2.3).</td>
</tr>
<tr>
<td>Godot 3.1</td>
<td>March 2019</td>
<td><img src="img/eol.png" alt="eol" /> No longer supported (last
update: 3.1.2).</td>
</tr>
<tr>
<td>Godot 3.0</td>
<td>January 2018</td>
<td><img src="img/eol.png" alt="eol" /> No longer supported (last
update: 3.0.6).</td>
</tr>
<tr>
<td>Godot 2.1</td>
<td>July 2016</td>
<td><img src="img/eol.png" alt="eol" /> No longer supported (last
update: 2.1.6).</td>
</tr>
<tr>
<td>Godot 2.0</td>
<td>February 2016</td>
<td><img src="img/eol.png" alt="eol" /> No longer supported (last
update: 2.0.4.1).</td>
</tr>
<tr>
<td>Godot 1.1</td>
<td>May 2015</td>
<td><img src="img/eol.png" alt="eol" /> No longer supported.</td>
</tr>
<tr>
<td>Godot 1.0</td>
<td>December 2014</td>
<td><img src="img/eol.png" alt="eol" /> No longer supported.</td>
</tr>
</tbody>
</table>

**Legend:** ![supported](img/supported.png) Full support –
![partial](img/partial.png) Partial support – ![eol](img/eol.png) No
support (end of life) – ![unstable](img/unstable.png) Development
version

Pre-release Godot versions aren't intended to be used in production and
are provided for testing purposes only.

See `doc_upgrading_to_godot_4` for instructions on migrating a project
from Godot 3.x to 4.x.

## Which version should I use for a new project?

We recommend using Godot 4.x for new projects, as the Godot 4.x series
will be supported long after 3.x stops receiving updates in the future.
One caveat is that a lot of third-party documentation hasn't been
updated for Godot 4.x yet. If you have to follow a tutorial designed for
Godot 3.x, we recommend keeping `doc_upgrading_to_godot_4` open in a
separate tab to check which methods have been renamed (if you get a
script error while trying to use a specific node or method that was
renamed in Godot 4.x).

If your project requires a feature that is missing in 4.x (such as
GLES2/WebGL 1.0), you should use Godot 3.x for a new project instead.

## Should I upgrade my project to use new engine versions?

Note

Upgrading software while working on a project is inherently risky, so
consider whether it's a good idea for your project before attempting an
upgrade. Also, make backups of your project or use version control to
prevent losing data in case the upgrade goes wrong.

That said, we do our best to keep minor and especially patch releases
compatible with existing projects.

The general recommendation is to upgrade your project to follow new
*patch* releases, such as upgrading from 4.0.2 to 4.0.3. This ensures
you get bug fixes, security updates and platform support updates (which
is especially important for mobile platforms). You also get continued
support, as only the last patch release receives support on official
community platforms.

For *minor* releases, you should determine whether it's a good idea to
upgrade on a case-by-case basis. We've made a lot of effort in making
the upgrade process as seamless as possible, but some breaking changes
may be present in minor releases, along with a greater risk of
regressions. Some fixes included in minor releases may also change a
class' expected behavior as required to fix some bugs. This is
especially the case in classes marked as *experimental* in the
documentation.

*Major* releases bring a lot of new functionality, but they also remove
previously existing functionality and may raise hardware requirements.
They also require much more work to upgrade to compared to minor
releases. As a result, we recommend sticking with the major release
you've started your project with if you are happy with how your project
currently works. For example, if your project was started with 3.5, we
recommend upgrading to 3.5.2 and possibly 3.6 in the future, but not to
4.0+, unless your project really needs the new features that come with
4.0+.

## When is the next release out?

While Godot contributors aren't working under any deadlines, we strive
to publish minor releases relatively frequently.

In particular, after the very length release cycle for 4.0, we are
pivoting to a faster paced development workflow, 4.1 released 4 months
after 4.0, and 4.2 released 4 months after 4.1

Frequent minor releases will enable us to ship new features faster
(possibly as experimental), get user feedback quickly, and iterate to
improve those features and their usability. Likewise, the general user
experience will be improved more steadily with a faster path to the end
users.

Maintenance (patch) releases are released as needed with potentially
very short development cycles, to provide users of the current stable
branch with the latest bug fixes for their production needs.

The 3.6 release is still planned and should be the last stable branch of
Godot 3.x. It will be a Long-Term Support (LTS) release, which we plan
to support for as long as users still need it (due to missing features
in Godot 4.x, or having published games which they need to keep updating
for platform requirements).

## What are the criteria for compatibility across engine versions?

Note

This section is intended to be used by contributors to determine which
changes are safe for a given release. The list is not exhaustive; it
only outlines the most common situations encountered during Godot's
development.

The following changes are acceptable in patch releases:

-   Fixing a bug in a way that has no major negative impact on most
    projects, such as a visual or physics bug. Godot's physics engine is
    not deterministic, so physics bug fixes are not considered to break
    compatibility. If fixing a bug has a negative impact that could
    impact a lot of projects, it should be made optional (e.g. using a
    project setting or separate method).
-   Adding a new optional parameter to a method.
-   Small-scale editor usability tweaks.

Note that we tend to be more conservative with the fixes we allow in
each subsequent patch release. For instance, 4.0.1 may receive more
impactful fixes than 4.0.4 would.

The following changes are acceptable in minor releases, but not patch
releases:

-   Significant new features.
-   Renaming a method parameter. In C#, method parameters can be passed
    by name (but not in GDScript). As a result, this can break some
    projects that use C#.
-   Deprecating a method, member variable, or class. This is done by
    adding a deprecated flag to its class reference, which will show up
    in the editor. When a method is marked as deprecated, it's slated to
    be removed in the next *major* release.
-   Changes that affect the default project theme's visuals.
-   Bug fixes which significantly change the behavior or the output,
    with the aim to meet user expectations better. In comparison, in
    patch releases, we may favor keeping a buggy behavior so we don't
    break existing projects which likely already rely on the bug or use
    a workaround.
-   Performance optimizations that result in visual changes.

The following changes are considered **compatibility-breaking** and can
only be performed in a new major release:

-   Renaming or removing a method, member variable, or class.
-   Modifying a node's inheritance tree by making it inherit from a
    different class.
-   Changing the default value of a project setting value in a way that
    affects existing projects. To only affect new projects, the project
    manager should write a modified `project.godot` instead.

Since Godot 5.0 hasn't been branched off yet, we currently discourage
making compatibility-breaking changes of this kind.

Note

When modifying a method's signature in any fashion (including adding an
optional parameter), a GDExtension compatibility method must be created.
This ensures that existing GDExtensions continue to work across patch
and minor releases, so that users don't have to recompile them. See
`doc_handling_compatibility_breakages` for more information.
