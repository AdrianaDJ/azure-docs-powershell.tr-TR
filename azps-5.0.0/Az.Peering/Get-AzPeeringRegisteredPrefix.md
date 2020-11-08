---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azpeeringregisteredprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringRegisteredPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringRegisteredPrefix.md
ms.openlocfilehash: ca54d2a8969313742711306c701de3aefe54b30c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94276380"
---
# <span data-ttu-id="c01cd-101">Get-AzPeeringRegisteredPrefix</span><span class="sxs-lookup"><span data-stu-id="c01cd-101">Get-AzPeeringRegisteredPrefix</span></span>

## <span data-ttu-id="c01cd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c01cd-102">SYNOPSIS</span></span>
<span data-ttu-id="c01cd-103">Eş için kaydedilen öneki alır veya listeler.</span><span class="sxs-lookup"><span data-stu-id="c01cd-103">Gets or lists the registered prefix for peerings.</span></span>

## <span data-ttu-id="c01cd-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c01cd-104">SYNTAX</span></span>

### <span data-ttu-id="c01cd-105">ByResourceGroupAndName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="c01cd-105">ByResourceGroupAndName (Default)</span></span>
```
Get-AzPeeringRegisteredPrefix [-ResourceGroupName] <String> [-PeeringName] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c01cd-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="c01cd-106">InputObject</span></span>
```
Get-AzPeeringRegisteredPrefix [-InputObject] <PSPeering> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c01cd-107">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="c01cd-107">ByResourceId</span></span>
```
Get-AzPeeringRegisteredPrefix [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c01cd-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="c01cd-108">DESCRIPTION</span></span>
<span data-ttu-id="c01cd-109">Eş için kaydedilen öneki alır veya listeler.</span><span class="sxs-lookup"><span data-stu-id="c01cd-109">Gets or lists the registered prefix for peerings.</span></span>

## <span data-ttu-id="c01cd-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c01cd-110">EXAMPLES</span></span>

### <span data-ttu-id="c01cd-111">Eşleme için kaydedilen kaynakları Listele</span><span class="sxs-lookup"><span data-stu-id="c01cd-111">List registered ASNs for peering</span></span>
```powershell
PS C:\> Get-AzPeeringRegisteredPrefix -ResourceGroupName $resourceGroupName -PeeringName $peeringName
```

<span data-ttu-id="c01cd-112">Tescilli ASN 'yi listeler.</span><span class="sxs-lookup"><span data-stu-id="c01cd-112">Lists registered asn.</span></span>

### <span data-ttu-id="c01cd-113">Ada göre eşiçin tescil ASN 'yi alır</span><span class="sxs-lookup"><span data-stu-id="c01cd-113">Gets registered ASN for peering by name</span></span>
```powershell
PS C:\> Get-AzPeeringRegisteredPrefix -ResourceGroupName $resourceGroupName -PeeringName $peeringName -Name $registeredPrefixName
```

<span data-ttu-id="c01cd-114">Kaydettirilmiş eşleme ASN 'yi alır.</span><span class="sxs-lookup"><span data-stu-id="c01cd-114">Gets registered peering asn.</span></span>

<span data-ttu-id="c01cd-115">{{Buraya örnek açıklama ekleyin}}</span><span class="sxs-lookup"><span data-stu-id="c01cd-115">{{ Add example description here }}</span></span>

## <span data-ttu-id="c01cd-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c01cd-116">PARAMETERS</span></span>

### <span data-ttu-id="c01cd-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c01cd-117">-DefaultProfile</span></span>
<span data-ttu-id="c01cd-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c01cd-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c01cd-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c01cd-119">-InputObject</span></span>
<span data-ttu-id="c01cd-120">Get-AzPeering kullanma</span><span class="sxs-lookup"><span data-stu-id="c01cd-120">Use a Get-AzPeering</span></span>

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

### <span data-ttu-id="c01cd-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="c01cd-121">-Name</span></span>
<span data-ttu-id="c01cd-122">Önek adı.</span><span class="sxs-lookup"><span data-stu-id="c01cd-122">The name of prefix.</span></span>

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

### <span data-ttu-id="c01cd-123">-PeeringName</span><span class="sxs-lookup"><span data-stu-id="c01cd-123">-PeeringName</span></span>
<span data-ttu-id="c01cd-124">Takdirin benzersiz adı.</span><span class="sxs-lookup"><span data-stu-id="c01cd-124">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="c01cd-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c01cd-125">-ResourceGroupName</span></span>
<span data-ttu-id="c01cd-126">Var olan kaynak grubu adını oluştur veya kullan.</span><span class="sxs-lookup"><span data-stu-id="c01cd-126">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="c01cd-127">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="c01cd-127">-ResourceId</span></span>
<span data-ttu-id="c01cd-128">Kaynak kimliği dize adı.</span><span class="sxs-lookup"><span data-stu-id="c01cd-128">The resource id string name.</span></span>

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

### <span data-ttu-id="c01cd-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c01cd-129">CommonParameters</span></span>
<span data-ttu-id="c01cd-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c01cd-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c01cd-131">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="c01cd-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c01cd-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c01cd-132">INPUTS</span></span>

### <span data-ttu-id="c01cd-133">Microsoft. Azure. PowerShell. cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c01cd-133">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

### <span data-ttu-id="c01cd-134">System. String</span><span class="sxs-lookup"><span data-stu-id="c01cd-134">System.String</span></span>

## <span data-ttu-id="c01cd-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c01cd-135">OUTPUTS</span></span>

### <span data-ttu-id="c01cd-136">Microsoft. Azure. PowerShell. cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c01cd-136">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredPrefix</span></span>

## <span data-ttu-id="c01cd-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c01cd-137">NOTES</span></span>

## <span data-ttu-id="c01cd-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c01cd-138">RELATED LINKS</span></span>
