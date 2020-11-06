---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/get-azurermenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmEnvironment.md
ms.openlocfilehash: ef42490d18702682413fd2c0a19e301614ce4d94
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590097"
---
# <span data-ttu-id="baaec-101">Get-AzureRmEnvironment</span><span class="sxs-lookup"><span data-stu-id="baaec-101">Get-AzureRmEnvironment</span></span>

## <span data-ttu-id="baaec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="baaec-102">SYNOPSIS</span></span>
<span data-ttu-id="baaec-103">Bir Azure hizmetleri örneğinin uç noktalarını ve meta verilerini alın.</span><span class="sxs-lookup"><span data-stu-id="baaec-103">Get endpoints and metadata for an instance of Azure services.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="baaec-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="baaec-104">SYNTAX</span></span>

```
Get-AzureRmEnvironment [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="baaec-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="baaec-105">DESCRIPTION</span></span>
<span data-ttu-id="baaec-106">Get-AzureRmEnvironment cmdlet 'i bir Azure hizmetleri örneğinin uç noktalarını ve meta verilerini alır.</span><span class="sxs-lookup"><span data-stu-id="baaec-106">The Get-AzureRmEnvironment cmdlet gets endpoints and metadata for an instance of Azure services.</span></span>

## <span data-ttu-id="baaec-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="baaec-107">EXAMPLES</span></span>

### <span data-ttu-id="baaec-108">Örnek 1: Azurecyüksek ortamını alma</span><span class="sxs-lookup"><span data-stu-id="baaec-108">Example 1: Getting the AzureCloud environment</span></span>
```
PS C:\> Get-AzureRmEnvironment AzureCloud

Name       Resource Manager Url          ActiveDirectory Authority
----       --------------------          -------------------------
AzureCloud https://management.azure.com/ https://login.microsoftonline.com/
```

<span data-ttu-id="baaec-109">Bu örnekte, Azurecyüksek (varsayılan) ortamın uç noktalarının ve meta verilerinin nasıl alınacağı gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="baaec-109">This example shows how to get the endpoints and metadata for the AzureCloud (default) environment.</span></span>

### <span data-ttu-id="baaec-110">Örnek 2: AzureChinaCloud ortamını alma</span><span class="sxs-lookup"><span data-stu-id="baaec-110">Example 2: Getting the AzureChinaCloud environment</span></span>
```
PS C:\> Get-AzureRmEnvironment AzureChinaCloud | Format-List

Name                                              : AzureChinaCloud
EnableAdfsAuthentication                          : False
ActiveDirectoryServiceEndpointResourceId          : https://management.core.chinacloudapi.cn/
AdTenant                                          :
GalleryUrl                                        : https://gallery.chinacloudapi.cn/
ManagementPortalUrl                               : https://go.microsoft.com/fwlink/?LinkId=301902
ServiceManagementUrl                              : https://management.core.chinacloudapi.cn/
PublishSettingsFileUrl                            : https://go.microsoft.com/fwlink/?LinkID=301776
ResourceManagerUrl                                : https://management.chinacloudapi.cn/
SqlDatabaseDnsSuffix                              : .database.chinacloudapi.cn
StorageEndpointSuffix                             : core.chinacloudapi.cn
ActiveDirectoryAuthority                          : https://login.chinacloudapi.cn/
GraphUrl                                          : https://graph.chinacloudapi.cn/
GraphEndpointResourceId                           : https://graph.chinacloudapi.cn/
TrafficManagerDnsSuffix                           : trafficmanager.cn
AzureKeyVaultDnsSuffix                            : vault.azure.cn
AzureDataLakeStoreFileSystemEndpointSuffix        :
AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix :
AzureKeyVaultServiceEndpointResourceId            : https://vault.azure.cn
```

<span data-ttu-id="baaec-111">Bu örnekte, AzureChinaCloud ortamında uç noktaları ve meta verilerin nasıl alınacağı gösterilir.</span><span class="sxs-lookup"><span data-stu-id="baaec-111">This example shows how to get the endpoints and metadata for the AzureChinaCloud environment.</span></span>

### <span data-ttu-id="baaec-112">Örnek 3: AzureUSGovernment ortamını alma</span><span class="sxs-lookup"><span data-stu-id="baaec-112">Example 3: Getting the AzureUSGovernment environment</span></span>
```
PS C:\> Get-AzureRmEnvironment AzureUSGovernment

Name              Resource Manager Url                  ActiveDirectory Authority
----              --------------------                  -------------------------
AzureUSGovernment https://management.usgovcloudapi.net/ https://login.microsoftonline.us/
```

<span data-ttu-id="baaec-113">Bu örnekte, AzureUSGovernment ortamında uç noktaları ve meta verilerin nasıl alınacağı gösterilir.</span><span class="sxs-lookup"><span data-stu-id="baaec-113">This example shows how to get the endpoints and metadata for the AzureUSGovernment environment.</span></span>

## <span data-ttu-id="baaec-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="baaec-114">PARAMETERS</span></span>

### <span data-ttu-id="baaec-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="baaec-115">-DefaultProfile</span></span>
<span data-ttu-id="baaec-116">Azure ile iletişimde kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="baaec-116">The credentials, account, tenant and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="baaec-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="baaec-117">-Name</span></span>
<span data-ttu-id="baaec-118">Alınacak Azure örneğinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="baaec-118">Specifies the name of the Azure instance to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="baaec-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="baaec-119">CommonParameters</span></span>
<span data-ttu-id="baaec-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="baaec-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="baaec-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="baaec-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="baaec-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="baaec-122">INPUTS</span></span>

### <span data-ttu-id="baaec-123">System. String</span><span class="sxs-lookup"><span data-stu-id="baaec-123">System.String</span></span>

## <span data-ttu-id="baaec-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="baaec-124">OUTPUTS</span></span>

### <span data-ttu-id="baaec-125">Microsoft. Azure. Commands. Profile. modeller. PSAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="baaec-125">Microsoft.Azure.Commands.Profile.Models.PSAzureEnvironment</span></span>

## <span data-ttu-id="baaec-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="baaec-126">NOTES</span></span>

## <span data-ttu-id="baaec-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="baaec-127">RELATED LINKS</span></span>

[<span data-ttu-id="baaec-128">Add-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="baaec-128">Add-AzureRMEnvironment</span></span>](./Add-AzureRMEnvironment.md)

[<span data-ttu-id="baaec-129">Remove-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="baaec-129">Remove-AzureRMEnvironment</span></span>](./Remove-AzureRMEnvironment.md)

[<span data-ttu-id="baaec-130">Set-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="baaec-130">Set-AzureRMEnvironment</span></span>](./Set-AzureRMEnvironment.md)

