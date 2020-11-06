---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/remove-azurermenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Remove-AzureRmEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Remove-AzureRmEnvironment.md
ms.openlocfilehash: 2916a4048987d703bc1cbb44653eae2cfb066a29
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593463"
---
# <span data-ttu-id="2ce4c-101">Remove-AzureRmEnvironment</span><span class="sxs-lookup"><span data-stu-id="2ce4c-101">Remove-AzureRmEnvironment</span></span>

## <span data-ttu-id="2ce4c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2ce4c-102">SYNOPSIS</span></span>
<span data-ttu-id="2ce4c-103">Belirli bir Azure örneğine bağlanmak için uç noktaları ve meta verileri kaldırır.</span><span class="sxs-lookup"><span data-stu-id="2ce4c-103">Removes endpoints and metadata for connecting to a given Azure instance.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2ce4c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2ce4c-104">SYNTAX</span></span>

```
Remove-AzureRmEnvironment [-Name] <String> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2ce4c-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="2ce4c-105">DESCRIPTION</span></span>
<span data-ttu-id="2ce4c-106">Remove-AzureRmEnvironment cmdlet, belirli bir Azure örneğine bağlanmak için uç noktaları ve meta veri bilgilerini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="2ce4c-106">The Remove-AzureRmEnvironment cmdlet removes endpoints and metadata information for connecting to a given Azure instance.</span></span>

## <span data-ttu-id="2ce4c-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2ce4c-107">EXAMPLES</span></span>

### <span data-ttu-id="2ce4c-108">Örnek 1: test ortamı oluşturma ve silme</span><span class="sxs-lookup"><span data-stu-id="2ce4c-108">Example 1: Creating and removing a test environment</span></span>
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

<span data-ttu-id="2ce4c-109">Bu örnekte Add-AzureRmEnvironment kullanarak nasıl ortam oluşturulacağı ve ardından Remove-AzureRmEnvironment kullanılarak nasıl kaldırılacağı gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="2ce4c-109">This example shows how to create an environment using Add-AzureRmEnvironment, and then how to delete the environment using Remove-AzureRmEnvironment.</span></span>

## <span data-ttu-id="2ce4c-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2ce4c-110">PARAMETERS</span></span>

### <span data-ttu-id="2ce4c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ce4c-111">-DefaultProfile</span></span>
<span data-ttu-id="2ce4c-112">Azure ile iletişimde kullanılan kimlik bilgileri, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2ce4c-112">The credentials, tenant and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ce4c-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="2ce4c-113">-Name</span></span>
<span data-ttu-id="2ce4c-114">Kaldırılacak ortamın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2ce4c-114">Specifies the name of the environment to remove.</span></span>

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

### <span data-ttu-id="2ce4c-115">-Kapsam</span><span class="sxs-lookup"><span data-stu-id="2ce4c-115">-Scope</span></span>
<span data-ttu-id="2ce4c-116">Değişikliklerin kapsamını, örneğin değişikliklerin yalnızca geçerli işleme veya bu kullanıcı tarafından başlatılan tüm oturumlara uygulanmasını belirler.</span><span class="sxs-lookup"><span data-stu-id="2ce4c-116">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

```yaml
Type: ContextModificationScope
Parameter Sets: (All)
Aliases: 
Accepted values: Process, CurrentUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ce4c-117">-Onay</span><span class="sxs-lookup"><span data-stu-id="2ce4c-117">-Confirm</span></span>
<span data-ttu-id="2ce4c-118">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="2ce4c-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2ce4c-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2ce4c-119">-WhatIf</span></span>
<span data-ttu-id="2ce4c-120">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="2ce4c-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2ce4c-121">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="2ce4c-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2ce4c-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ce4c-122">CommonParameters</span></span>
<span data-ttu-id="2ce4c-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2ce4c-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ce4c-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ce4c-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ce4c-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2ce4c-125">INPUTS</span></span>

### <span data-ttu-id="2ce4c-126">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="2ce4c-126">None</span></span>
<span data-ttu-id="2ce4c-127">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="2ce4c-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2ce4c-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2ce4c-128">OUTPUTS</span></span>

### <span data-ttu-id="2ce4c-129">PSAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="2ce4c-129">PSAzureEnvironment</span></span>

## <span data-ttu-id="2ce4c-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2ce4c-130">NOTES</span></span>

## <span data-ttu-id="2ce4c-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2ce4c-131">RELATED LINKS</span></span>

[<span data-ttu-id="2ce4c-132">Add-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="2ce4c-132">Add-AzureRMEnvironment</span></span>](./Add-AzureRMEnvironment.md)

[<span data-ttu-id="2ce4c-133">Get-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="2ce4c-133">Get-AzureRMEnvironment</span></span>](./Get-AzureRMEnvironment.md)

[<span data-ttu-id="2ce4c-134">Set-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="2ce4c-134">Set-AzureRMEnvironment</span></span>](./Set-AzureRMEnvironment.md)

