{% data variables.product.prodname_dependabot %} runners require access to the public internet, {% data variables.product.prodname_dotcom_the_website %}, and any internal registries that will be used in {% data variables.product.prodname_dependabot_updates %}. To minimize the risk to your internal network, you should limit access from the Virtual Machine (VM) to your internal network. This reduces the potential for damage to internal systems if a runner were to download a hijacked dependency.

{% ifversion fpt or ghec %}
You must also allow outbound traffic to `dependabot-actions.githubapp.com` to prevent the jobs for {% data variables.product.prodname_dependabot_security_updates %} from failing. For more information, see [AUTOTITLE](/actions/hosting-your-own-runners/managing-self-hosted-runners/communicating-with-self-hosted-runners).

{% endif %}
