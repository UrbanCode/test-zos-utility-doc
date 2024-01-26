# Steps

## Download Artifacts

Download a z/OS package from an external artifact repository. The repository can be either a Nexus or Artifactory repository.


| Name                | Type    | Description                                                                                      | Required |
|---------------------|---------|--------------------------------------------------------------------------------------------------|----------|
| Repository URL      | String  | The URL of the repository.                                                                       | Yes      |
| User Name           | String  | The user name used to authenticate with the repository.                                          | Yes      |
| Repository Password | String  | The password used to authenticate with the repository.                                           | Yes      |
| Artifactory api key | Boolean | Check this box to use API key authentication with artifact repository. Does not work with Nexus. | No       |
| Artifactory api key | String  | The api key used to authenticate with the artifactory repository.                                | No       |

!!! Warning
    Review with your security admins before allowing insecure connection. On default, it is disabled.

!!! Note
    * Select Proxy checkbox to enable proxy connection to artifactory using passed Proxy Host and Port. Proxy does not work for Nexus.
    * When USE_ATTLS property is set to TRUE, plugin will not handle encryption and will rely on server AT_TLS to encrypt the network communication with external repository. Default is FALSE.