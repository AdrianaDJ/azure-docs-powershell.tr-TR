---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azpeeringregisteredasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringRegisteredAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringRegisteredAsn.md
ms.openlocfilehash: d23a034b2c51f37116c605d786393ba504da3f26
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94274297"
---
# <span data-ttu-id="63a3d-101">Get-AzPeeringRegisteredAsn</span><span class="sxs-lookup"><span data-stu-id="63a3d-101">Get-AzPeeringRegisteredAsn</span></span>

## <span data-ttu-id="63a3d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="63a3d-102">SYNOPSIS</span></span>
<span data-ttu-id="63a3d-103">İnternet Exchange Route Server türü için tescilli ASN 'yi alır.</span><span class="sxs-lookup"><span data-stu-id="63a3d-103">Gets the registered ASN for internet exchange route server type peerings.</span></span>

## <span data-ttu-id="63a3d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="63a3d-104">SYNTAX</span></span>

### <span data-ttu-id="63a3d-105">ByResourceGroupAndName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="63a3d-105">ByResourceGroupAndName (Default)</span></span>
```
Get-AzPeeringRegisteredAsn [-ResourceGroupName] <String> [-PeeringName] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="63a3d-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="63a3d-106">InputObject</span></span>
```
Get-AzPeeringRegisteredAsn [-InputObject] <PSPeering> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="63a3d-107">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="63a3d-107">ByResourceId</span></span>
```
Get-AzPeeringRegisteredAsn [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="63a3d-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="63a3d-108">DESCRIPTION</span></span>
<span data-ttu-id="63a3d-109">Kaydedilmiş bir ASN alın veya listeleyin.</span><span class="sxs-lookup"><span data-stu-id="63a3d-109">Get or list a registered ASN.</span></span>

## <span data-ttu-id="63a3d-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="63a3d-110">EXAMPLES</span></span>

### <span data-ttu-id="63a3d-111">Eşleme için kaydedilen kaynakları Listele</span><span class="sxs-lookup"><span data-stu-id="63a3d-111">List registered ASNs for peering</span></span>
```powershell
PS C:\> Get-AzPeeringRegisteredAsn -ResourceGroupName $resourceGroupName -PeeringName $peeringName
```

<span data-ttu-id="63a3d-112">Tescilli ASN 'yi listeler.</span><span class="sxs-lookup"><span data-stu-id="63a3d-112">Lists registered asn.</span></span>

### <span data-ttu-id="63a3d-113">Ada göre eşiçin tescil ASN 'yi alır</span><span class="sxs-lookup"><span data-stu-id="63a3d-113">Gets registered ASN for peering by name</span></span>
```powershell
PS C:\> Get-AzPeeringRegisteredAsn -ResourceGroupName $resourceGroupName -PeeringName $peeringName -Name $registeredAsnName
```

<span data-ttu-id="63a3d-114">Kaydettirilmiş eşleme ASN 'yi alır.</span><span class="sxs-lookup"><span data-stu-id="63a3d-114">Gets registered peering asn.</span></span>

## <span data-ttu-id="63a3d-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="63a3d-115">PARAMETERS</span></span>

### <span data-ttu-id="63a3d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63a3d-116">-DefaultProfile</span></span>
<span data-ttu-id="63a3d-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="63a3d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="63a3d-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="63a3d-118">-InputObject</span></span>
<span data-ttu-id="63a3d-119">Get-AzPeering kullanma</span><span class="sxs-lookup"><span data-stu-id="63a3d-119">Use a Get-AzPeering</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="63a3d-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="63a3d-120">-Name</span></span>
<span data-ttu-id="63a3d-121">Tescilli ASN 'nin adı</span><span class="sxs-lookup"><span data-stu-id="63a3d-121">The name of the registered ASN</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndName, InputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63a3d-122">-PeeringName</span><span class="sxs-lookup"><span data-stu-id="63a3d-122">-PeeringName</span></span>
<span data-ttu-id="63a3d-123">Takdirin benzersiz adı.</span><span class="sxs-lookup"><span data-stu-id="63a3d-123">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63a3d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="63a3d-124">-ResourceGroupName</span></span>
<span data-ttu-id="63a3d-125">Var olan kaynak grubu adını oluştur veya kullan.</span><span class="sxs-lookup"><span data-stu-id="63a3d-125">The create or use an existing resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63a3d-126">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="63a3d-126">-ResourceId</span></span>
<span data-ttu-id="63a3d-127">Kaynak kimliği dize adı.</span><span class="sxs-lookup"><span data-stu-id="63a3d-127">The resource id string name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63a3d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63a3d-128">CommonParameters</span></span>
<span data-ttu-id="63a3d-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="63a3d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63a3d-130">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="63a3d-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63a3d-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="63a3d-131">INPUTS</span></span>

### <span data-ttu-id="63a3d-132">Microsoft. Azure. PowerShell. cmdlet.</span><span class="sxs-lookup"><span data-stu-id="63a3d-132">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

### <span data-ttu-id="63a3d-133">System. String</span><span class="sxs-lookup"><span data-stu-id="63a3d-133">System.String</span></span>

## <span data-ttu-id="63a3d-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="63a3d-134">OUTPUTS</span></span>

### <span data-ttu-id="63a3d-135">Microsoft. Azure. PowerShell. cmdlet. eşleme. modeller. Pspeeringkayıt Teredasn</span><span class="sxs-lookup"><span data-stu-id="63a3d-135">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredAsn</span></span>

## <span data-ttu-id="63a3d-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="63a3d-136">NOTES</span></span>

## <span data-ttu-id="63a3d-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="63a3d-137">RELATED LINKS</span></span>
