---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: A4226BFB-AB3B-4883-9D52-5EB7F29D8A71
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementRegion.md
ms.openlocfilehash: 8d292f6e03661ae55a63686a0282ce65292087f5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587341"
---
# <span data-ttu-id="1cbf5-101">New-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="1cbf5-101">New-AzureRmApiManagementRegion</span></span>

## <span data-ttu-id="1cbf5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1cbf5-102">SYNOPSIS</span></span>
<span data-ttu-id="1cbf5-103">Psapsananagementregion örneği oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1cbf5-103">Creates an instance of PsApiManagementRegion.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1cbf5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1cbf5-104">SYNTAX</span></span>

```
New-AzureRmApiManagementRegion -Location <String> [-Capacity <Int32>]
 [-VirtualNetwork <PsApiManagementVirtualNetwork>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1cbf5-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="1cbf5-105">DESCRIPTION</span></span>
<span data-ttu-id="1cbf5-106">Bir Psapsananagementregion örneği oluşturmak için yardımcı komutu.</span><span class="sxs-lookup"><span data-stu-id="1cbf5-106">Helper command to create an instance of PsApiManagementRegion.</span></span>
<span data-ttu-id="1cbf5-107">Bu komut New-AzureRmApiManagement komutuyla kullanılır.</span><span class="sxs-lookup"><span data-stu-id="1cbf5-107">This command is to be used with New-AzureRmApiManagement command.</span></span>

## <span data-ttu-id="1cbf5-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1cbf5-108">EXAMPLES</span></span>

### <span data-ttu-id="1cbf5-109">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="1cbf5-109">Example 1</span></span>
```
$apimRegion = New-AzureRmApiManagementRegion -Location "Central US" 

$additionalRegions = @($apimRegion)

New-AzureRmApiManagement -ResourceGroupName ContosoGroup -Location "West US" -Name ContosoApi -Organization Contoso -AdminEmail admin@contoso.com -AdditionalRegions $additionalRegions -Sku "Premium"
```

### <span data-ttu-id="1cbf5-110">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="1cbf5-110">Example 2</span></span>
```
$apimRegionVirtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location "Central US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-a1e8-3726ab15d0e2/resourceGroups/ContosoGroup/providers/Microsoft.Network/virtualNetworks/centralusvirtualNetwork/subnets/backendSubnet"

$apimRegion = New-AzureRmApiManagementRegion -Location "Central US" -VirtualNetwork $apimRegionVirtualNetwork 

$additionalRegions = @($apimRegion)

$virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location "West US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc2-4174-a1e8-3726ab15d0e2/resourceGroups/ContosoGroup/providers/Microsoft.Network/virtualNetworks/westUsVirtualNetwork/subnets/backendSubnet"

New-AzureRmApiManagement -ResourceGroupName ContosoGroup -Location "West US" -Name ContosoApi -Organization Contoso -AdminEmail admin@contoso.com -AdditionalRegions $additionalRegions -VirtualNetwork $virtualNetwork -VpnType "External" -Sku "Premium"
```

<span data-ttu-id="1cbf5-111">Orta ABD bölgesinde bir dış VpnType hizmeti Merkezi ABD 'de ek bir bölgeyle oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="1cbf5-111">Creates an ApiManagement service of External VpnType in West US Region, with an Additional Region in Central US.</span></span>

## <span data-ttu-id="1cbf5-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1cbf5-112">PARAMETERS</span></span>

### <span data-ttu-id="1cbf5-113">-Kapasite</span><span class="sxs-lookup"><span data-stu-id="1cbf5-113">-Capacity</span></span>
<span data-ttu-id="1cbf5-114">Azure API yönetim hizmeti ek bölgesinin SKU kapasitesi.</span><span class="sxs-lookup"><span data-stu-id="1cbf5-114">Sku capacity of the Azure API Management service additional region.</span></span>
<span data-ttu-id="1cbf5-115">Varsayılan değer 1 ' dir.</span><span class="sxs-lookup"><span data-stu-id="1cbf5-115">Default value is 1.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1cbf5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1cbf5-116">-DefaultProfile</span></span>
<span data-ttu-id="1cbf5-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1cbf5-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1cbf5-118">-Konum</span><span class="sxs-lookup"><span data-stu-id="1cbf5-118">-Location</span></span>
<span data-ttu-id="1cbf5-119">API yönetim hizmeti için desteklenen bölge arasındaki yeni dağıtım bölgesinin konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="1cbf5-119">Specifies the location of the new deployment region amongst the supported region for Api Management service.</span></span>
<span data-ttu-id="1cbf5-120">Geçerli konumlar almak için, "Microsoft. Apsananae" Get-AzureRmResourceProvider cmdlet 'ini kullanın. WHERE {$ _. ResourceTypes [0]. ResourceTypeName-EQ "hizmet"} | Select-Object konumları</span><span class="sxs-lookup"><span data-stu-id="1cbf5-120">To obtain valid locations, use the cmdlet Get-AzureRmResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1cbf5-121">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="1cbf5-121">-VirtualNetwork</span></span>
<span data-ttu-id="1cbf5-122">Azure API Yönetimi dağıtım bölgesinin sanal ağ yapılandırması.</span><span class="sxs-lookup"><span data-stu-id="1cbf5-122">Virtual Network Configuration of Azure API Management deployment region.</span></span>
<span data-ttu-id="1cbf5-123">Varsayılan değer $null.</span><span class="sxs-lookup"><span data-stu-id="1cbf5-123">Default value is $null.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1cbf5-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1cbf5-124">CommonParameters</span></span>
<span data-ttu-id="1cbf5-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1cbf5-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1cbf5-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1cbf5-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1cbf5-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1cbf5-127">INPUTS</span></span>

### <span data-ttu-id="1cbf5-128">Microsoft. Azure. Commands. apsanana</span><span class="sxs-lookup"><span data-stu-id="1cbf5-128">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork</span></span>

## <span data-ttu-id="1cbf5-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1cbf5-129">OUTPUTS</span></span>

### <span data-ttu-id="1cbf5-130">Microsoft. Azure. Commands. apsanana</span><span class="sxs-lookup"><span data-stu-id="1cbf5-130">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion</span></span>

## <span data-ttu-id="1cbf5-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1cbf5-131">NOTES</span></span>

## <span data-ttu-id="1cbf5-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1cbf5-132">RELATED LINKS</span></span>
