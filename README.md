Of course all of this information is available elsewhere, but I felt like it would be somewhat useful to centralize a set of comparisons here. At a minimum, researching this and typing it all of out for myself will help me remember these details by virtue of muscle memory. This exercise certainly helped solidify my current understanding as well as revealed big holes in it.
I have no idea whether this will be actually useful to anyone else... and it's still a work in progress and most certainly not comprehensive. I also thought it was kind of interesting to see the similarities and differences of tools there are for them.

| PL | Home page | How to start a REPL | Project management tool |  How to create a new project | How to manage dependencies | How to build a project | Library repository |  
| --- | --- | --- | --- | --- | --- | --- | --- |
| Clojure | http://clojure.org | `java -cp clojure-1.8.0.jar clojure.main` <br/> or `lein repl` | [Leiningen](https://leiningen.org/) | `lein new new-project` | Listed in `project.clj` by their Maven coordinates | `lein compile` | https://clojars.org |
| Elixir | http://http://elixir-lang.org/ | `iex` | Mix | `mix new new_project` | Listed in `mix.exs` by name and semver if using Hex, or by git repo if using just Mix  | `mix compile` | https://hex.pm/ |
| Elm | http://elm-lang.org/ | `elm repl` | `elm-package` | There is no scaffolding tool. | Add new ones via `elm-package install` to `elm-package.json` | `elm make` | http://package.elm-lang.org/ |
| Erlang | https://www.erlang.org/ | `erl` | [Rebar3](http://www.rebar3.org/) | `rebar3 new release new_project` | Listed in `rebar.config` by name and semver if using Hex, or by git repo if using just Mix | `rebar3 compile` | https://hex.pm/ |
| F# | http://fsharp.org/ | `fsharpi`[¹](#fsharp-compiler) | Within an IDE, use [Xamarin](https://www.xamarin.com/) or [Visual Studio](https://www.visualstudio.com/); for a CLI tool use [Forge](forge.run) or [Yeoman](https://github.com/fsprojects/generator-fsharp) | See the documentation for the tools mentioned in the previous cell. | Use [Paket](https://fsprojects.github.io/Paket/) to manage them in `paket.dependencies` | See the documentation for the tools mentioned in the Project management tool cell. | https://www.nuget.org/ |
| Go | https://golang.org/ | [`gore`](https://github.com/motemen/gore) | There is no official one. | Read [this](https://golang.org/doc/code.html#Organization) for how set up a new project. | Read [this](https://github.com/golang/go/wiki/PackageManagementTools) for various different methods. | `go build` | N/A |
| Haskell | https://www.haskell.org/ | `ghci`[²](#haskell-compiler) | [Cabal](https://www.haskell.org/cabal/), [Stack](https://www.haskellstack.org/) | `cabal init`, or `stack new new_project simple` | Listed in `new_project.cabal` or `stack.yaml` | `cabal build` or `stack build` | https://hackage.haskell.org/ or https://www.stackage.org/ |
| Java | https://www.java.com | [`java-repl`](https://github.com/albertlatacz/java-repl) | [Maven](https://maven.apache.org/), [Ant](https://http://ant.apache.org/) | `mvn -B archetype:generate...` | Listed in `pom.xml` by their Maven coordinates | `mvn compile` | https://mvnrepository.com/ |
| OCaml | https://ocaml.org/ | `ocaml` or [`utop`](https://github.com/diml/utop)[³](#utop) | The closest analogue to other PLs is [OASIS](http://oasis.forge.ocamlcore.org/) | There is no scaffolding tool. | If using OASIS, list them by name in the `_oasis` file [⁴](#ocamlfind) | `make`[⁵](#ocamlbuild) | https://opam.ocaml.org/packages |
| PHP | https://php.net/ | `php -a` or [Boris](https://github.com/borisrepl/boris) | [Yeoman](http://yeoman.io/) with [Generator-BarePHP](https://github.com/juliangut/generator-barephp) | `yo barephp` | Listed in `composer.json` by package name or git repo URL if using [Composer](https://getcomposer.org/) | N/A | https://packagist.org/ |
| Ruby | https://www.ruby-lang.org/ | `irb` | [Bundler](http://bundler.io/) | `bundle gem new_project` | Added to `Gemfile` via `gem install` | `bundle install` |  https://rubygems.org/ |
| Rust | https://www.rust-lang.org/ | [`rusti`](https://github.com/murarth/rusti)[⁶](#rusti) | [Cargo](https://crates.io/) | `cargo new new_project` | Listed in `Cargo.toml` by name and semver | `cargo build` | https://crates.io/ |
| Swift | https://swift.org/ | `swift` | Swift Package Manager | `swift package init --type executable` or use XCode | Listed in `Package.swift` by their git repo URL | `swift build` or build within XCode | N/A |


<a name="fsharp-compiler">¹</a> This assumes the Mono platform; for the .NET platform, the REPL is started by running `fsi.exe`.  
<a name="haskell-compiler">²</a> This assumes, of course, that you are using GHC; there are other compilers.  
<a name="utop">³</a> UTop offers a _much_ better user experience than the bultin REPL.  
<a name="ocamlfind">⁴</a> OASIS relies on `ocamlfind` for name resolution of dependencies.  
<a name="ocamlbuild">⁵</a> OASIS generates various files for configuring the build and relies on `ocamlbuild` for building the project. See the [documentation](http://ocaml.org/learn/tutorials/setting_up_with_oasis.html#Goingfurther) for details.  
<a name="rusti">⁶</a> As of this writing, the latest version of `rusti` only works with the nightly build of Rust from 2016/08/01.  
