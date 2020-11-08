---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: A4226BFB-AB3B-4883-9D52-5EB7F29D8A71
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementRegion.md
ms.openlocfilehash: 2259990c568dbf6fd5b7bc6f8bff34c464a082ec
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94107992"
---
# <span data-ttu-id="f26ab-101">New-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="f26ab-101">New-AzApiManagementRegion</span></span>

## <span data-ttu-id="f26ab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f26ab-102">SYNOPSIS</span></span>
<span data-ttu-id="f26ab-103">Psapsananagementregion örneği oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f26ab-103">Creates an instance of PsApiManagementRegion.</span></span>

## <span data-ttu-id="f26ab-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f26ab-104">SYNTAX</span></span>

```
New-AzApiManagementRegion -Location <String> [-Capacity <Int32>]
 [-VirtualNetwork <PsApiManagementVirtualNetwork>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f26ab-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f26ab-105">DESCRIPTION</span></span>
<span data-ttu-id="f26ab-106">Bir Psapsananagementregion örneği oluşturmak için yardımcı komutu.</span><span class="sxs-lookup"><span data-stu-id="f26ab-106">Helper command to create an instance of PsApiManagementRegion.</span></span>
<span data-ttu-id="f26ab-107">Bu komut New-AzApiManagement komutuyla kullanılır.</span><span class="sxs-lookup"><span data-stu-id="f26ab-107">This command is to be used with New-AzApiManagement command.</span></span>

## <span data-ttu-id="f26ab-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f26ab-108">EXAMPLES</span></span>

### <span data-ttu-id="f26ab-109">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="f26ab-109">Example 1</span></span>
```
$apimRegion = New-AzApiManagementRegion -Location "Central US" 

$additionalRegions = @($apimRegion)

New-AzApiManagement -ResourceGroupName ContosoGroup -Location "West US" -Name ContosoApi -Organization Contoso -AdminEmail admin@contoso.com -AdditionalRegions $additionalRegions -Sku "Premium"
```

### <span data-ttu-id="f26ab-110">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="f26ab-110">Example 2</span></span>
```
$apimRegionVirtualNetwork = New-AzApiManagementVirtualNetwork -Location "Central US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-a1e8-3726ab15d0e2/resourceGroups/ContosoGroup/providers/Microsoft.Network/virtualNetworks/centralusvirtualNetwork/subnets/backendSubnet"

$apimRegion = New-AzApiManagementRegion -Location "Central US" -VirtualNetwork $apimRegionVirtualNetwork 

$additionalRegions = @($apimRegion)

$virtualNetwork = New-AzApiManagementVirtualNetwork -Location "West US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc2-4174-a1e8-3726ab15d0e2/resourceGroups/ContosoGroup/providers/Microsoft.Network/virtualNetworks/westUsVirtualNetwork/subnets/backendSubnet"

New-AzApiManagement -ResourceGroupName ContosoGroup -Location "West US" -Name ContosoApi -Organization Contoso -AdminEmail admin@contoso.com -AdditionalRegions $additionalRegions -VirtualNetwork $virtualNetwork -VpnType "External" -Sku "Premium"
```

<span data-ttu-id="f26ab-111">Orta ABD bölgesinde bir dış VpnType hizmeti Merkezi ABD 'de ek bir bölgeyle oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="f26ab-111">Creates an ApiManagement service of External VpnType in West US Region, with an Additional Region in Central US.</span></span>

## <span data-ttu-id="f26ab-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f26ab-112">PARAMETERS</span></span>

### <span data-ttu-id="f26ab-113">-Kapasite</span><span class="sxs-lookup"><span data-stu-id="f26ab-113">-Capacity</span></span>
<span data-ttu-id="f26ab-114">Azure API yönetim hizmeti ek bölgesinin SKU kapasitesi.</span><span class="sxs-lookup"><span data-stu-id="f26ab-114">Sku capacity of the Azure API Management service additional region.</span></span>
<span data-ttu-id="f26ab-115">Varsayılan değer 1 ' dir.</span><span class="sxs-lookup"><span data-stu-id="f26ab-115">Default value is 1.</span></span>

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

### <span data-ttu-id="f26ab-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f26ab-116">-DefaultProfile</span></span>
<span data-ttu-id="f26ab-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f26ab-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f26ab-118">-Konum</span><span class="sxs-lookup"><span data-stu-id="f26ab-118">-Location</span></span>
<span data-ttu-id="f26ab-119">API yönetim hizmeti için desteklenen bölge arasındaki yeni dağıtım bölgesinin konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="f26ab-119">Specifies the location of the new deployment region amongst the supported region for Api Management service.</span></span>
<span data-ttu-id="f26ab-120">Geçerli konumlar almak için, "Microsoft. Apsananae" Get-AzResourceProvider cmdlet 'ini kullanın. WHERE {$ _. ResourceTypes [0]. ResourceTypeName-EQ "hizmet"} | Select-Object konumları</span><span class="sxs-lookup"><span data-stu-id="f26ab-120">To obtain valid locations, use the cmdlet Get-AzResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

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

### <span data-ttu-id="f26ab-121">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="f26ab-121">-VirtualNetwork</span></span>
<span data-ttu-id="f26ab-122">Azure API Yönetimi dağıtım bölgesinin sanal ağ yapılandırması.</span><span class="sxs-lookup"><span data-stu-id="f26ab-122">Virtual Network Configuration of Azure API Management deployment region.</span></span>
<span data-ttu-id="f26ab-123">Varsayılan değer $null.</span><span class="sxs-lookup"><span data-stu-id="f26ab-123">Default value is $null.</span></span>

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

### <span data-ttu-id="f26ab-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f26ab-124">CommonParameters</span></span>
<span data-ttu-id="f26ab-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f26ab-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f26ab-126">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="f26ab-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f26ab-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f26ab-127">INPUTS</span></span>

### <span data-ttu-id="f26ab-128">Microsoft. Azure. Commands. apsanana</span><span class="sxs-lookup"><span data-stu-id="f26ab-128">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork</span></span>

## <span data-ttu-id="f26ab-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f26ab-129">OUTPUTS</span></span>

### <span data-ttu-id="f26ab-130">Microsoft. Azure. Commands. apsanana</span><span class="sxs-lookup"><span data-stu-id="f26ab-130">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion</span></span>

## <span data-ttu-id="f26ab-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f26ab-131">NOTES</span></span>

## <span data-ttu-id="f26ab-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f26ab-132">RELATED LINKS</span></span>
