## Tuesday, February 9, 2021, 2:18:32PM EST <1612898312>

I need to be able to add the following to my resume: Jenkins, CI/CD,
Rundeck, Terraform, Vault, Ansible, puppet, chef, Grafana, Prometheus,
ElasticSearch, Zabbix.

## Tuesday, February 9, 2021, 12:00:51PM EST <1612890051>

I was reminded of the title "Staff Engineer" today while working on my
resume. Apparently, it is a Silicon Valley thing (which immediately
makes me want to puke). Here's a [Quora post (requires
JavaScript)](https://www.quora.com/What-is-Staff-Software-Engineer-title).
(By the way, Quora was probably created by dumb-asses who call
themselves "Principle Staff Engineers" but don't have a fucking clue why
creating a question and answer site that depends on JavaScript to see at
all is so fucking full of shit.)

So no, I'll still with titles that at least mean something in English:

* IT Infrastructure Engineer
* Senior Software Developer

If so fucking dumb-ass looks down on my for picking the wrong titles
that doesn't comply with some SV shit, well, sucks to be them. I'm fine.

I'm reminded again how Canada is a much better clue on this stuff. You
can't even call yourself an "engineer" if all you are is a software
developer.

## Tuesday, February 9, 2021, 3:13:45AM EST <1612858425>

Realized that dealing with Golang templates is so genericised now that
you don't really even need something like Hugo. In fact, the following
could be easily worked into a `kn` action that follows the KEG standard
for Knowledge Nodes:

```golang
package main

import (
	"fmt"
	"io/ioutil"
	"os"
	"html/template"

	"gopkg.in/yaml.v2"
)

func check(err error) {
	if err != nil {
		fmt.Println(err)
		os.Exit(1)
	}
}

func main() {

	out, err := os.Create("index.html")
	defer out.Close()
	check(err)

	data := map[string]interface{}{}

	buf, err := ioutil.ReadFile("data.yml")
	check(err)
	err = yaml.Unmarshal(buf, &data)
	check(err)

	t, err := template.ParseGlob("tmpl/*")
	check(err)
	err = t.Execute(out, data)
	check(err)
}
```


