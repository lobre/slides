+++
title = "Split"
outputs = ["Reveal"]
[reveal_hugo]
theme = "simple"

[[resources]]
  name = "split-1-:counter"
  src = "split-1*.png"

[[resources]]
  name = "split-2-:counter"
  src = "split-2*.png"
+++

# docker-compose split

---

{{% section %}}

{{< slide transition="none" >}}

{{< img "split-1-1" "schema 1-1" "Resize" "800x" >}}

---

{{< slide transition="none" >}}

{{< img "split-1-2" "schema 1-2" "Resize" "800x" >}}

---

{{< slide transition="none" >}}

{{< img "split-1-3" "schema 1-3" "Resize" "800x" >}}

{{% /section %}}

---

{{% section %}}

{{< slide transition="none" >}}

{{< img "split-2-1" "schema 2-1" "Resize" "800x" >}}

---

{{< slide transition="none" >}}

{{< img "split-2-2" "schema 2-2" "Resize" "800x" >}}

---

{{< slide transition="none" >}}

{{< img "split-2-3" "schema 2-3" "Resize" "800x" >}}

{{% /section %}}

---

## Benefits

 - Decrease resources usage
 - Speed up local machine setup
 - Avoid over publishing ports
 - Provide web interface

---

## Demo toolbox

{{% note %}}
docker inspect traefik | jq -r '.[0].NetworkSettings.Networks | keys'

docker run --rm --name nginx --label traefik.enable=true --label traefik.frontend.rule=Host:nginx.local --label ghosts.host=nginx.local nginx

 - category
 - description
{{% /note %}}

---

## Demo Amer

{{% note %}}
git co jira/ETECH-882_split-docker-compose
{{% /note %}}

---

## To setup machine

 - Install docker toolbox
 - Clone, setup and start toolkit
 - Clone Magento project
 - Start desired instance
 - Import dump

---

## Next steps

 - Finish splitting instances
 - Beta test with a few developers
 - Add profiling tools
 - Centralize mailcatcher
 - Support Docker for Windows?
