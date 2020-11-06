---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: A4226BFB-AB3B-4883-9D52-5EB7F29D8A71
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementRegion.md
ms.openlocfilehash: a5febccec0ed09cde866925ce03d7025408b27f2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593851"
---
# <span data-ttu-id="44620-101">New-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="44620-101">New-AzureRmApiManagementRegion</span></span>

## <span data-ttu-id="44620-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="44620-102">SYNOPSIS</span></span>
<span data-ttu-id="44620-103">Psapsananagementregion örneği oluşturur.</span><span class="sxs-lookup"><span data-stu-id="44620-103">Creates an instance of PsApiManagementRegion.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="44620-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="44620-104">SYNTAX</span></span>

```
New-AzureRmApiManagementRegion -Location <String> [-Capacity <Int32>]
 [-VirtualNetwork <PsApiManagementVirtualNetwork>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="44620-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="44620-105">DESCRIPTION</span></span>
<span data-ttu-id="44620-106">Bir Psapsananagementregion örneği oluşturmak için yardımcı komutu.</span><span class="sxs-lookup"><span data-stu-id="44620-106">Helper command to create an instance of PsApiManagementRegion.</span></span>
<span data-ttu-id="44620-107">Bu komut New-AzureRmApiManagement komutuyla kullanılır.</span><span class="sxs-lookup"><span data-stu-id="44620-107">This command is to be used with New-AzureRmApiManagement command.</span></span>

## <span data-ttu-id="44620-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="44620-108">EXAMPLES</span></span>

### <span data-ttu-id="44620-109">--------------------------Örnek 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="44620-109">--------------------------  Example 1  --------------------------</span></span>
```
$apimRegion = New-AzureRmApiManagementRegion -Location "Central US" 

$additionalRegions = @($apimRegion)

New-AzureRmApiManagement -ResourceGroupName ContosoGroup -Location "West US" -Name ContosoApi -Organization Contoso -AdminEmail admin@contoso.com -AdditionalRegions $additionalRegions -Sku "Premium"
```

### <span data-ttu-id="44620-110">--------------------------Örnek 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="44620-110">--------------------------  Example 2  --------------------------</span></span>
```
$apimRegionVirtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location "Central US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-a1e8-3726ab15d0e2/resourceGroups/ContosoGroup/providers/Microsoft.Network/virtualNetworks/centralusvirtualNetwork/subnets/backendSubnet"

$apimRegion = New-AzureRmApiManagementRegion -Location "Central US" -VirtualNetwork $apimRegionVirtualNetwork 

$additionalRegions = @($apimRegion)

$virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location "West US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc2-4174-a1e8-3726ab15d0e2/resourceGroups/ContosoGroup/providers/Microsoft.Network/virtualNetworks/westUsVirtualNetwork/subnets/backendSubnet"

New-AzureRmApiManagement -ResourceGroupName ContosoGroup -Location "West US" -Name ContosoApi -Organization Contoso -AdminEmail admin@contoso.com -AdditionalRegions $additionalRegions -VirtualNetwork $virtualNetwork -VpnType "External" -Sku "Premium"
```

<span data-ttu-id="44620-111">Orta ABD bölgesinde bir dış VpnType hizmeti Merkezi ABD 'de ek bir bölgeyle oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="44620-111">Creates an ApiManagement service of External VpnType in West US Region, with an Additional Region in Central US.</span></span>

## <span data-ttu-id="44620-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="44620-112">PARAMETERS</span></span>

### <span data-ttu-id="44620-113">-Kapasite</span><span class="sxs-lookup"><span data-stu-id="44620-113">-Capacity</span></span>
<span data-ttu-id="44620-114">Azure API yönetim hizmeti ek bölgesinin SKU kapasitesi.</span><span class="sxs-lookup"><span data-stu-id="44620-114">Sku capacity of the Azure API Management service additional region.</span></span>
<span data-ttu-id="44620-115">Varsayılan değer 1 ' dir.</span><span class="sxs-lookup"><span data-stu-id="44620-115">Default value is 1.</span></span>

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

### <span data-ttu-id="44620-116">-Konum</span><span class="sxs-lookup"><span data-stu-id="44620-116">-Location</span></span>
<span data-ttu-id="44620-117">Ek dağıtım bölgesinin konumu.</span><span class="sxs-lookup"><span data-stu-id="44620-117">Location of the additional deployment region.</span></span>

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

### <span data-ttu-id="44620-118">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="44620-118">-VirtualNetwork</span></span>
<span data-ttu-id="44620-119">Azure API Yönetimi dağıtım bölgesinin sanal ağ yapılandırması.</span><span class="sxs-lookup"><span data-stu-id="44620-119">Virtual Network Configuration of Azure API Management deployment region.</span></span>
<span data-ttu-id="44620-120">Varsayılan değer $null.</span><span class="sxs-lookup"><span data-stu-id="44620-120">Default value is $null.</span></span>

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

### <span data-ttu-id="44620-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44620-121">-DefaultProfile</span></span>
<span data-ttu-id="44620-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="44620-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="44620-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44620-123">CommonParameters</span></span>
<span data-ttu-id="44620-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="44620-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44620-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="44620-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44620-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="44620-126">INPUTS</span></span>

## <span data-ttu-id="44620-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="44620-127">OUTPUTS</span></span>

### <span data-ttu-id="44620-128">Microsoft. Azure. Commands. apsanana</span><span class="sxs-lookup"><span data-stu-id="44620-128">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion</span></span>

## <span data-ttu-id="44620-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="44620-129">NOTES</span></span>

## <span data-ttu-id="44620-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="44620-130">RELATED LINKS</span></span>

