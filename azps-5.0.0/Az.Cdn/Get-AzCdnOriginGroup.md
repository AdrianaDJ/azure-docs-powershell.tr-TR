---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnorigingroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnOriginGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnOriginGroup.md
ms.openlocfilehash: 98c41f8e9e1592cf0405f42701fc19f3badd9553
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94279534"
---
# <span data-ttu-id="8f1bb-101">Get-AzCdnOriginGroup</span><span class="sxs-lookup"><span data-stu-id="8f1bb-101">Get-AzCdnOriginGroup</span></span>

## <span data-ttu-id="8f1bb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8f1bb-102">SYNOPSIS</span></span>
<span data-ttu-id="8f1bb-103">CDN kaynak grubunu alır</span><span class="sxs-lookup"><span data-stu-id="8f1bb-103">Gets a CDN origin group</span></span>

## <span data-ttu-id="8f1bb-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8f1bb-104">SYNTAX</span></span>

### <span data-ttu-id="8f1bb-105">ByFieldsParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="8f1bb-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnOriginGroup -EndpointName <String> -OriginGroupName <String> -ProfileName <String>
 -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8f1bb-106">Byresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="8f1bb-106">ByResourceIdParameterSet</span></span>
```
Get-AzCdnOriginGroup -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8f1bb-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="8f1bb-107">DESCRIPTION</span></span>
<span data-ttu-id="8f1bb-108">Get-AzCdnOriginGroup cmdlet 'i CDN kaynak grubu alır.</span><span class="sxs-lookup"><span data-stu-id="8f1bb-108">The Get-AzCdnOriginGroup cmdlet retrieves a CDN origin group.</span></span>

## <span data-ttu-id="8f1bb-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8f1bb-109">EXAMPLES</span></span>

### <span data-ttu-id="8f1bb-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="8f1bb-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCdnOriginGroup -ResourceGroupName $resourceGroupName -ProfileName $profileName -EndpointName $endpointName -OriginGroupName $originGroupName
```

<span data-ttu-id="8f1bb-111">Bu komut belirtilen uç nokta içinde kaynak grubu alır.</span><span class="sxs-lookup"><span data-stu-id="8f1bb-111">This command will get the origin group within the specified endpoint.</span></span>

## <span data-ttu-id="8f1bb-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8f1bb-112">PARAMETERS</span></span>

### <span data-ttu-id="8f1bb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f1bb-113">-DefaultProfile</span></span>
<span data-ttu-id="8f1bb-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8f1bb-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8f1bb-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="8f1bb-115">-EndpointName</span></span>
<span data-ttu-id="8f1bb-116">Azure CDN uç noktası adı.</span><span class="sxs-lookup"><span data-stu-id="8f1bb-116">Azure CDN endpoint name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f1bb-117">-OriginGroupName</span><span class="sxs-lookup"><span data-stu-id="8f1bb-117">-OriginGroupName</span></span>
<span data-ttu-id="8f1bb-118">Azure CDN kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="8f1bb-118">Azure CDN origin group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f1bb-119">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="8f1bb-119">-ProfileName</span></span>
<span data-ttu-id="8f1bb-120">Azure CDN profil adı.</span><span class="sxs-lookup"><span data-stu-id="8f1bb-120">Azure CDN profile name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f1bb-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f1bb-121">-ResourceGroupName</span></span>
<span data-ttu-id="8f1bb-122">Azure CDN profilinin kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="8f1bb-122">The resource group of the Azure CDN profile.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f1bb-123">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="8f1bb-123">-ResourceId</span></span>
<span data-ttu-id="8f1bb-124">Kaynak grubu için kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="8f1bb-124">Resource Id for the the origin group</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f1bb-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f1bb-125">CommonParameters</span></span>
<span data-ttu-id="8f1bb-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8f1bb-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f1bb-127">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="8f1bb-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f1bb-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8f1bb-128">INPUTS</span></span>

### <span data-ttu-id="8f1bb-129">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="8f1bb-129">None</span></span>

## <span data-ttu-id="8f1bb-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8f1bb-130">OUTPUTS</span></span>

### <span data-ttu-id="8f1bb-131">System. Object</span><span class="sxs-lookup"><span data-stu-id="8f1bb-131">System.Object</span></span>

## <span data-ttu-id="8f1bb-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8f1bb-132">NOTES</span></span>

## <span data-ttu-id="8f1bb-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8f1bb-133">RELATED LINKS</span></span>
