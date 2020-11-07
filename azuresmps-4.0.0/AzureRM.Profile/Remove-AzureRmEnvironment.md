---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8d9c783d6fe4047aa1d179cd661c88d13e9c716b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93761750"
---
# <span data-ttu-id="3b1f1-101">Remove-AzureRmEnvironment</span><span class="sxs-lookup"><span data-stu-id="3b1f1-101">Remove-AzureRmEnvironment</span></span>

## <span data-ttu-id="3b1f1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3b1f1-102">SYNOPSIS</span></span>
<span data-ttu-id="3b1f1-103">Belirli bir Azure örneğine bağlanmak için uç noktaları ve meta verileri kaldırır.</span><span class="sxs-lookup"><span data-stu-id="3b1f1-103">Removes endpoints and metadata for connecting to a given Azure instance.</span></span>

## <span data-ttu-id="3b1f1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3b1f1-104">SYNTAX</span></span>

```
Remove-AzureRmEnvironment [-Name] <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3b1f1-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="3b1f1-105">DESCRIPTION</span></span>
<span data-ttu-id="3b1f1-106">Remove-AzureRmEnvironment cmdlet, belirli bir Azure örneğine bağlanmak için uç noktaları ve meta veri bilgilerini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="3b1f1-106">The Remove-AzureRmEnvironment cmdlet removes endpoints and metadata information for connecting to a given Azure instance.</span></span>

## <span data-ttu-id="3b1f1-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3b1f1-107">EXAMPLES</span></span>

### <span data-ttu-id="3b1f1-108">Örnek 1: test ortamı oluşturma ve silme</span><span class="sxs-lookup"><span data-stu-id="3b1f1-108">Example 1: Creating and removing a test environment</span></span>
```
PS C:\> Add-AzureRmEnvironment -Name TestEnvironment `
        -ActiveDirectoryEndpoint TestADEndpoint `
        -ActiveDirectoryServiceEndpointResourceId TestADApplicationId `
        -ResourceManagerEndpoint TestRMEndpoint `
        -GalleryEndpoint TestGalleryEndpoint `
        -GraphEndpoint TestGraphEndpoint

Name                                              : TestEnvironment
EnableAdfsAuthentication                          : False
ActiveDirectoryServiceEndpointResourceId          : TestADApplicationId
AdTenant                                          :
GalleryUrl                                        : TestGalleryEndpoint
ManagementPortalUrl                               :
ServiceManagementUrl                              : 
PublishSettingsFileUrl                            :
ResourceManagerUrl                                : TestRMEndpoint
SqlDatabaseDnsSuffix                              :
StorageEndpointSuffix                             :
ActiveDirectoryAuthority                          : TestADEndpoint
GraphUrl                                          : TestGraphEndpoint
GraphEndpointResourceId                           :
TrafficManagerDnsSuffix                           :
AzureKeyVaultDnsSuffix                            :
AzureDataLakeStoreFileSystemEndpointSuffix        :
AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix :
AzureKeyVaultServiceEndpointResourceId            :

PS C:\> Remove-AzureRmEnvironment -Name TestEnvironment

Name                                              : TestEnvironment
EnableAdfsAuthentication                          : False
ActiveDirectoryServiceEndpointResourceId          : TestADApplicationId
AdTenant                                          :
GalleryUrl                                        : TestGalleryEndpoint
ManagementPortalUrl                               :
ServiceManagementUrl                              : 
PublishSettingsFileUrl                            :
ResourceManagerUrl                                : TestRMEndpoint
SqlDatabaseDnsSuffix                              :
StorageEndpointSuffix                             :
ActiveDirectoryAuthority                          : TestADEndpoint
GraphUrl                                          : TestGraphEndpoint
GraphEndpointResourceId                           :
TrafficManagerDnsSuffix                           :
AzureKeyVaultDnsSuffix                            :
AzureDataLakeStoreFileSystemEndpointSuffix        :
AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix :
AzureKeyVaultServiceEndpointResourceId            :
```

<span data-ttu-id="3b1f1-109">Bu örnekte Add-AzureRmEnvironment kullanarak nasıl ortam oluşturulacağı ve ardından Remove-AzureRmEnvironment kullanılarak nasıl kaldırılacağı gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="3b1f1-109">This example shows how to create an environment using Add-AzureRmEnvironment, and then how to delete the environment using Remove-AzureRmEnvironment.</span></span>

## <span data-ttu-id="3b1f1-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3b1f1-110">PARAMETERS</span></span>

### <span data-ttu-id="3b1f1-111">-Ad</span><span class="sxs-lookup"><span data-stu-id="3b1f1-111">-Name</span></span>
<span data-ttu-id="3b1f1-112">Kaldırılacak ortamın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3b1f1-112">Specifies the name of the environment to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b1f1-113">-Onay</span><span class="sxs-lookup"><span data-stu-id="3b1f1-113">-Confirm</span></span>
<span data-ttu-id="3b1f1-114">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="3b1f1-114">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b1f1-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3b1f1-115">-WhatIf</span></span>
<span data-ttu-id="3b1f1-116">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="3b1f1-116">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3b1f1-117">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="3b1f1-117">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b1f1-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b1f1-118">CommonParameters</span></span>
<span data-ttu-id="3b1f1-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3b1f1-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b1f1-120">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3b1f1-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b1f1-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3b1f1-121">INPUTS</span></span>

## <span data-ttu-id="3b1f1-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3b1f1-122">OUTPUTS</span></span>

### <span data-ttu-id="3b1f1-123">PSAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="3b1f1-123">PSAzureEnvironment</span></span>

## <span data-ttu-id="3b1f1-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3b1f1-124">NOTES</span></span>

## <span data-ttu-id="3b1f1-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3b1f1-125">RELATED LINKS</span></span>

[<span data-ttu-id="3b1f1-126">Add-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="3b1f1-126">Add-AzureRMEnvironment</span></span>]()

[<span data-ttu-id="3b1f1-127">Get-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="3b1f1-127">Get-AzureRMEnvironment</span></span>]()

[<span data-ttu-id="3b1f1-128">Set-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="3b1f1-128">Set-AzureRMEnvironment</span></span>]()

