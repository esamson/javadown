# javadown

*javadown* is a fork of the Javadoc Standard Doclet that allows for javadoc to
be written in [Markdown syntax](http://daringfireball.net/projects/markdown/syntax).
All the standard javadocs tags are supported.

## Installation

*javadown* is released to Maven Central. You may use it directly in your maven
projects.

If you're not using maven, you may still download the jar manually from
[Maven Central](http://search.maven.org/#search%7Cga%7C1%7Cg%3A%22ph.samson%22%20AND%20a%3A%22javadown%22).
Note that [pegdown](https://github.com/sirthias/pegdown) is used for Markdown
processing. You'll need that and all its dependencies, too.

## Usage

To use, simply specify `ph.samson.javadown.Javadown` as the doclet to be used
by the javadoc tool. For example, in Maven one would say:


```
    <plugin>
        <groupId>org.apache.maven.plugins</groupId>
        <artifactId>maven-javadoc-plugin</artifactId>
        <version>2.9.1</version>
        <configuration>
            <doclet>ph.samson.javadown.Javadown</doclet>
            <docletArtifact>
                <groupId>ph.samson</groupId>
                <artifactId>javadown</artifactId>
                <version>1.0.1</version>
            </docletArtifact>
        </configuration>
    </plugin>
```

