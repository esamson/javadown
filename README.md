# javadown

*javadown* is a fork of the Javadoc Standard Doclet that allows for javadoc to
be written in [Markdown syntax](http://daringfireball.net/projects/markdown/syntax).
All the standard javadocs tags are supported.

## Dependencies

[pegdown](https://github.com/sirthias/pegdown) is used for Markdown processing.
If you use Maven, this should not concern you.

## Usage

To use, simply specify `ph.samson.javadown.Javadown` as the doclet to be used
by the javadoc tool. For example, in Maven one would say:


```
    <plugin>
        <groupId>org.apache.maven.plugins</groupId>
        <artifactId>maven-javadoc-plugin</artifactId>
        <version>2.9</version>
        <configuration>
            <doclet>ph.samson.javadown.Javadown</doclet>
            <docletArtifact>
                <groupId>ph.samson</groupId>
                <artifactId>javadown</artifactId>
                <version>0.1</version>
            </docletArtifact>
        </configuration>
    </plugin>
```

