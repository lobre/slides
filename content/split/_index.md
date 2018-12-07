+++
title = "Split"
outputs = ["Reveal"]
[reveal_hugo]
theme = "simple"
+++

# docker-compose split

---

{{% section %}}

<img src="/slides/split/split-1-1.png" width="800" />

---

<img src="/slides/split/split-1-2.png" width="800" />

---

<img src="/slides/split/split-1-3.png" width="800" />

{{% /section %}}

---

{{% section %}}

<img src="/slides/split/split-2-1.png" width="800" />

---

<img src="/slides/split/split-2-2.png" width="800" />

---

<img src="/slides/split/split-2-3.png" width="800" />

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
