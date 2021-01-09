# WordPress

This is a WordPress repository configured to run on the [Kubernetes platform](https://kubernetes.io). It's a fork of Pantheon's WordPress fork modified to remove the Pantheon-specific source code. Use it as a base for a hardened WordPress installation created via Ansible using the [wordpress-helm](https://codeberg.org/vhs/wordpress-helm) Helm Chart from OAS.

Pantheon is a website platform optimized and configured to run high performance sites and then ransom those sites back to their customers when traffic rises due to popularity. This fork is intended to empower Pantheon customers stuck with a ransom note from Pantheon to self-host their sites on Kubernetes while saving money instead.

## Comparisons

Comparing Pantheon and Kubernetes.
### Monthly price

Pantheon is a good value when visitor count is under 25K per month. After that value quickly diminishes.

Monthly Visitors | Pantheon | Kubernetes
--- | --- | ---
25K–50K | $160† | $30‡
50K–150K | $275† | $30‡
150K–300K | $550† | Unknown
300K+ | $916† | Unknown

† Pantheon offers preferred pricing when paid annually. The charges are $114, $206, $412 and $687 respectively.

‡ Beware of monthly bandwidth limitations imposed by cloud-hosting providers such as [DigitalOcean](https://vhs.codeberg.page/go/digitalocean) and [Vultr](https://vhs.codeberg.page/go/vultr). Some providers offer unlimited bandwidth while others do not. Choosing the right one for you will depend on your specific requirements.

### Features

Pantheon offers some nice performance enhancements. All of them are possible in Kubernetes and can be added at any time.

Pantheon | Kubernetes
--- | ---
Varnish | —
Redis ($160/month)  | Redis (Included Free)
Apache Solr | —
New Relic ($160/month) | —
Nginx | Apache
PHP-FPM | PHP Redis
MySQL | MariaDB (Replicated)
PhantomJS | —
WP Cron | WP/MU Cron
WP Mail | —

As you can see you need to give up some things in order to migrate to Kubernetes. But because K8s is so flexible these items may be added back later on an as-needed basis with a little elbow grease.

## Getting Started

### 1. Spin-up a free site on Pantheon

If you do not yet have a Pantheon account, you can create one for free. Once you've verified your email address, you will be able to add sites from your dashboard. Choose "WordPress" to use the upstream distribution of this fork.

### 2. Load up the site

When the spin-up process is complete, you will be redirected to the site's dashboard. Click on the link under the site's name to access the Dev environment.

### 3. Run the WordPress installer

How about the WordPress database config screen? No need to worry about database connection information as that is taken care of in the background. The only step that you need to complete is the site information and the installation process will be complete.

### 4. Wait for ransom note

Pantheon has a tendency to change their pricing model every couple of years. When you eventually get a ransom note after getting backed into a corner begin your migration to Kubernetes.

### 5. Begin migration to Kubernetes

The entire migration process should take about a week or so for an experienced developer. Full migration instructions [are available](https://vhs.codeberg.page/post/move-pantheon-wordpress-site-kubernetes/) without fee.

### 6. Profit!

![profit](https://source.unsplash.com/rwfISioESQM)
