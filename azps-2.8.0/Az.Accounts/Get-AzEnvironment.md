---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/get-azenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzEnvironment.md
ms.openlocfilehash: 3b8eb80f631743e9f8b12d8d422be40ee602e8e8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753732"
---
# <span data-ttu-id="ee47a-101">Get-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="ee47a-101">Get-AzEnvironment</span></span>

## <span data-ttu-id="ee47a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ee47a-102">SYNOPSIS</span></span>
<span data-ttu-id="ee47a-103">Bir Azure hizmetleri örneğinin uç noktalarını ve meta verilerini alın.</span><span class="sxs-lookup"><span data-stu-id="ee47a-103">Get endpoints and metadata for an instance of Azure services.</span></span>

## <span data-ttu-id="ee47a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ee47a-104">SYNTAX</span></span>

```
Get-AzEnvironment [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ee47a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ee47a-105">DESCRIPTION</span></span>
<span data-ttu-id="ee47a-106">Get-AzEnvironment cmdlet 'i bir Azure hizmetleri örneğinin uç noktalarını ve meta verilerini alır.</span><span class="sxs-lookup"><span data-stu-id="ee47a-106">The Get-AzEnvironment cmdlet gets endpoints and metadata for an instance of Azure services.</span></span>

## <span data-ttu-id="ee47a-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ee47a-107">EXAMPLES</span></span>

### <span data-ttu-id="ee47a-108">Örnek 1: Azurecyüksek ortamını alma</span><span class="sxs-lookup"><span data-stu-id="ee47a-108">Example 1: Getting the AzureCloud environment</span></span>
```
PS C:\> Get-AzEnvironment AzureCloud

Name       Resource Manager Url          ActiveDirectory Authority
----       --------------------          -------------------------
AzureCloud https://management.azure.com/ https://login.microsoftonline.com/
```

<span data-ttu-id="ee47a-109">Bu örnekte, Azurecyüksek (varsayılan) ortamın uç noktalarının ve meta verilerinin nasıl alınacağı gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="ee47a-109">This example shows how to get the endpoints and metadata for the AzureCloud (default) environment.</span></span>

### <span data-ttu-id="ee47a-110">Örnek 2: AzureChinaCloud ortamını alma</span><span class="sxs-lookup"><span data-stu-id="ee47a-110">Example 2: Getting the AzureChinaCloud environment</span></span>
```
PS C:\> Get-AzEnvironment AzureChinaCloud | Format-List

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

<span data-ttu-id="ee47a-111">Bu örnekte, AzureChinaCloud ortamında uç noktaları ve meta verilerin nasıl alınacağı gösterilir.</span><span class="sxs-lookup"><span data-stu-id="ee47a-111">This example shows how to get the endpoints and metadata for the AzureChinaCloud environment.</span></span>

### <span data-ttu-id="ee47a-112">Örnek 3: AzureUSGovernment ortamını alma</span><span class="sxs-lookup"><span data-stu-id="ee47a-112">Example 3: Getting the AzureUSGovernment environment</span></span>
```
PS C:\> Get-AzEnvironment AzureUSGovernment

Name              Resource Manager Url                  ActiveDirectory Authority
----              --------------------                  -------------------------
AzureUSGovernment https://management.usgovcloudapi.net/ https://login.microsoftonline.us/
```

<span data-ttu-id="ee47a-113">Bu örnekte, AzureUSGovernment ortamında uç noktaları ve meta verilerin nasıl alınacağı gösterilir.</span><span class="sxs-lookup"><span data-stu-id="ee47a-113">This example shows how to get the endpoints and metadata for the AzureUSGovernment environment.</span></span>

## <span data-ttu-id="ee47a-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ee47a-114">PARAMETERS</span></span>

### <span data-ttu-id="ee47a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee47a-115">-DefaultProfile</span></span>
<span data-ttu-id="ee47a-116">Azure ile iletişimde kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ee47a-116">The credentials, account, tenant and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee47a-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="ee47a-117">-Name</span></span>
<span data-ttu-id="ee47a-118">Alınacak Azure örneğinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ee47a-118">Specifies the name of the Azure instance to get.</span></span>

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

### <span data-ttu-id="ee47a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee47a-119">CommonParameters</span></span>
<span data-ttu-id="ee47a-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ee47a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee47a-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ee47a-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee47a-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ee47a-122">INPUTS</span></span>

### <span data-ttu-id="ee47a-123">System. String</span><span class="sxs-lookup"><span data-stu-id="ee47a-123">System.String</span></span>

## <span data-ttu-id="ee47a-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ee47a-124">OUTPUTS</span></span>

### <span data-ttu-id="ee47a-125">Microsoft. Azure. Commands. Profile. modeller. PSAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="ee47a-125">Microsoft.Azure.Commands.Profile.Models.PSAzureEnvironment</span></span>

## <span data-ttu-id="ee47a-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ee47a-126">NOTES</span></span>

## <span data-ttu-id="ee47a-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ee47a-127">RELATED LINKS</span></span>

[<span data-ttu-id="ee47a-128">Add-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="ee47a-128">Add-AzEnvironment</span></span>](./Add-AzEnvironment.md)

[<span data-ttu-id="ee47a-129">Remove-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="ee47a-129">Remove-AzEnvironment</span></span>](./Remove-AzEnvironment.md)

[<span data-ttu-id="ee47a-130">Set-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="ee47a-130">Set-AzEnvironment</span></span>](./Set-AzEnvironment.md)
