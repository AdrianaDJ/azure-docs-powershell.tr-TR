---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azpeeringreceivedroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringReceivedRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringReceivedRoute.md
ms.openlocfilehash: 14557809041fc6f4268dbe28ad9d8f13a70e4054
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94277935"
---
# <span data-ttu-id="70135-101">Get-AzPeeringReceivedRoute</span><span class="sxs-lookup"><span data-stu-id="70135-101">Get-AzPeeringReceivedRoute</span></span>

## <span data-ttu-id="70135-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="70135-102">SYNOPSIS</span></span>
<span data-ttu-id="70135-103">Bir eşleme için alınan yolları listeler.</span><span class="sxs-lookup"><span data-stu-id="70135-103">Lists the received routes for a Peering.</span></span>

## <span data-ttu-id="70135-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="70135-104">SYNTAX</span></span>

### <span data-ttu-id="70135-105">ByResourceGroupAndName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="70135-105">ByResourceGroupAndName (Default)</span></span>
```
Get-AzPeeringReceivedRoute [-ResourceGroupName] <String> -Name <String> [-Prefix <String>] [-AsPath <String>]
 [-OriginAsValidationState <String>] [-RPKIValidationState <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="70135-106">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="70135-106">ByResourceId</span></span>
```
Get-AzPeeringReceivedRoute [-ResourceId] <String> [-Prefix <String>] [-AsPath <String>]
 [-OriginAsValidationState <String>] [-RPKIValidationState <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="70135-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="70135-107">DESCRIPTION</span></span>
<span data-ttu-id="70135-108">Bir eşten alınan yolların listesini listeler</span><span class="sxs-lookup"><span data-stu-id="70135-108">Lists recieved routes from a Peering</span></span>

## <span data-ttu-id="70135-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="70135-109">EXAMPLES</span></span>

### <span data-ttu-id="70135-110">Eşleme için ilk 100 alınan yollar</span><span class="sxs-lookup"><span data-stu-id="70135-110">List top 100 received routes for a peering</span></span>
```powershell
PS C:\> Get-AzPeeringReceivedRoute -ResourceGroupName $resourceGroupName -Name $peeringName
```

<span data-ttu-id="70135-111">Bir eşleme için tüm alınan yolları listeler</span><span class="sxs-lookup"><span data-stu-id="70135-111">Lists all of the received routes for a peering</span></span>

### <span data-ttu-id="70135-112">Yol olarak filtrele</span><span class="sxs-lookup"><span data-stu-id="70135-112">Filter by AS Path</span></span>
```powershell
PS C:\> Get-AzPeeringReceivedRoute -ResourceGroupName $resourceGroupName -Name $peeringName -AsPath "1234 5674 9834"
```

<span data-ttu-id="70135-113">Bir filtrenin tüm alınan yollarını listeler</span><span class="sxs-lookup"><span data-stu-id="70135-113">Lists all of the received routes for a peering with a filter on AS</span></span> 

### <span data-ttu-id="70135-114">RPKIValidationState 'e göre filtrele</span><span class="sxs-lookup"><span data-stu-id="70135-114">Filter by RPKIValidationState</span></span>
```powershell
PS C:\> Get-AzPeeringReceivedRoute -ResourceGroupName $resourceGroupName -Name $peeringName -RPKIValidationState "Valid"
```

<span data-ttu-id="70135-115">RPKIValidationState 'te bir filtreyle bir eşleme için alınan tüm yolları listeler</span><span class="sxs-lookup"><span data-stu-id="70135-115">Lists all of the received routes for a peering with a filter on RPKIValidationState</span></span>

### <span data-ttu-id="70135-116">Origin</span><span class="sxs-lookup"><span data-stu-id="70135-116">Filter by OriginAsValidationState</span></span>
```powershell
PS C:\> Get-AzPeeringReceivedRoute -ResourceGroupName $resourceGroupName -Name $peeringName -OriginAsValidationState "Valid"
```

<span data-ttu-id="70135-117">Originalıdoğrulama durumundaki filtreyle bir eşleme için alınan tüm yolları listeler</span><span class="sxs-lookup"><span data-stu-id="70135-117">Lists all of the received routes for a peering with a filter on OriginAsValidationState</span></span>

## <span data-ttu-id="70135-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="70135-118">PARAMETERS</span></span>

### <span data-ttu-id="70135-119">-AsPath</span><span class="sxs-lookup"><span data-stu-id="70135-119">-AsPath</span></span>
<span data-ttu-id="70135-120">Yol olarak filtreleyin.</span><span class="sxs-lookup"><span data-stu-id="70135-120">Filter by AS Path.</span></span>
<span data-ttu-id="70135-121">Örnek: ' 9342 1234 4567 '</span><span class="sxs-lookup"><span data-stu-id="70135-121">Example: '9342 1234 4567'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70135-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70135-122">-DefaultProfile</span></span>
<span data-ttu-id="70135-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="70135-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="70135-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="70135-124">-Name</span></span>
<span data-ttu-id="70135-125">Takdirin benzersiz adı.</span><span class="sxs-lookup"><span data-stu-id="70135-125">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70135-126">-OriginAsValidationState</span><span class="sxs-lookup"><span data-stu-id="70135-126">-OriginAsValidationState</span></span>
<span data-ttu-id="70135-127">Kaynağa geçerlilik durumu olarak filtre uygulama.</span><span class="sxs-lookup"><span data-stu-id="70135-127">Filter by origin AS validation state.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70135-128">-Önek</span><span class="sxs-lookup"><span data-stu-id="70135-128">-Prefix</span></span>
<span data-ttu-id="70135-129">Öneke göre filtreleyin.</span><span class="sxs-lookup"><span data-stu-id="70135-129">Filter by prefix.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70135-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70135-130">-ResourceGroupName</span></span>
<span data-ttu-id="70135-131">Var olan kaynak grubu adını oluştur veya kullan.</span><span class="sxs-lookup"><span data-stu-id="70135-131">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="70135-132">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="70135-132">-ResourceId</span></span>
<span data-ttu-id="70135-133">Kaynak kimliği dize adı.</span><span class="sxs-lookup"><span data-stu-id="70135-133">The resource id string name.</span></span>

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

### <span data-ttu-id="70135-134">-RPKIValidationState</span><span class="sxs-lookup"><span data-stu-id="70135-134">-RPKIValidationState</span></span>
<span data-ttu-id="70135-135">RPKı doğrulama durumuna göre filtreleyin.</span><span class="sxs-lookup"><span data-stu-id="70135-135">Filter by RPKI validation state.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70135-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70135-136">CommonParameters</span></span>
<span data-ttu-id="70135-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="70135-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70135-138">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="70135-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70135-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="70135-139">INPUTS</span></span>

### <span data-ttu-id="70135-140">System. String</span><span class="sxs-lookup"><span data-stu-id="70135-140">System.String</span></span>

## <span data-ttu-id="70135-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="70135-141">OUTPUTS</span></span>

### <span data-ttu-id="70135-142">Microsoft. Azure. PowerShell. cmdlet.</span><span class="sxs-lookup"><span data-stu-id="70135-142">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringReceivedRoute</span></span>

## <span data-ttu-id="70135-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="70135-143">NOTES</span></span>

## <span data-ttu-id="70135-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="70135-144">RELATED LINKS</span></span>
