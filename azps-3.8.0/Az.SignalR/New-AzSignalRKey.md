---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/new-azsignalrkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/New-AzSignalRKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/New-AzSignalRKey.md
ms.openlocfilehash: 9c27342a073f33a52881376037fc8d3a5d7e8bb1
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096765"
---
# <span data-ttu-id="631e0-101">New-AzSignalRKey</span><span class="sxs-lookup"><span data-stu-id="631e0-101">New-AzSignalRKey</span></span>

## <span data-ttu-id="631e0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="631e0-102">SYNOPSIS</span></span>
<span data-ttu-id="631e0-103">Bir SignalR hizmeti için erişim anahtarını yeniden oluşturun.</span><span class="sxs-lookup"><span data-stu-id="631e0-103">Regenerate an access key for a SignalR service.</span></span>

## <span data-ttu-id="631e0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="631e0-104">SYNTAX</span></span>

### <span data-ttu-id="631e0-105">ResourceGroupParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="631e0-105">ResourceGroupParameterSet (Default)</span></span>
```
New-AzSignalRKey [-ResourceGroupName <String>] [-Name] <String> [-KeyType] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="631e0-106">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="631e0-106">ResourceIdParameterSet</span></span>
```
New-AzSignalRKey -ResourceId <String> [-KeyType] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="631e0-107">Inputobjectparameterset</span><span class="sxs-lookup"><span data-stu-id="631e0-107">InputObjectParameterSet</span></span>
```
New-AzSignalRKey -InputObject <PSSignalRResource> [-KeyType] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="631e0-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="631e0-108">DESCRIPTION</span></span>
<span data-ttu-id="631e0-109">Bir SignalR hizmeti için erişim anahtarını yeniden oluşturun.</span><span class="sxs-lookup"><span data-stu-id="631e0-109">Regenerate an access key for a SignalR service.</span></span>

## <span data-ttu-id="631e0-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="631e0-110">EXAMPLES</span></span>

### <span data-ttu-id="631e0-111">Birincil anahtarı yeniden üret</span><span class="sxs-lookup"><span data-stu-id="631e0-111">Regenerate the primary key</span></span>
```powershell
PS C:\> New-AzSignalRKey -ResourceGroupName myResourceGroup -Name mysignalr1 -KeyType Primary -PassThru

True
```

## <span data-ttu-id="631e0-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="631e0-112">PARAMETERS</span></span>

### <span data-ttu-id="631e0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="631e0-113">-DefaultProfile</span></span>
<span data-ttu-id="631e0-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="631e0-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="631e0-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="631e0-115">-InputObject</span></span>
<span data-ttu-id="631e0-116">SignalR kaynak nesnesi.</span><span class="sxs-lookup"><span data-stu-id="631e0-116">The SignalR resource object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="631e0-117">-KeyType</span><span class="sxs-lookup"><span data-stu-id="631e0-117">-KeyType</span></span>
<span data-ttu-id="631e0-118">Birincil veya Ikincil anahtar türü.</span><span class="sxs-lookup"><span data-stu-id="631e0-118">The key type, either Primary or Secondary.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="631e0-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="631e0-119">-Name</span></span>
<span data-ttu-id="631e0-120">SignalR hizmet adı.</span><span class="sxs-lookup"><span data-stu-id="631e0-120">SignalR service name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="631e0-121">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="631e0-121">-PassThru</span></span>
<span data-ttu-id="631e0-122">Yeniden oluşturma başarıyla tamamlanırsa, doğru döndürür.</span><span class="sxs-lookup"><span data-stu-id="631e0-122">Returns true if the regeneration was completed successfully.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="631e0-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="631e0-123">-ResourceGroupName</span></span>
<span data-ttu-id="631e0-124">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="631e0-124">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="631e0-125">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="631e0-125">-ResourceId</span></span>
<span data-ttu-id="631e0-126">SignalR hizmeti kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="631e0-126">The SignalR service resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="631e0-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="631e0-127">-Confirm</span></span>
<span data-ttu-id="631e0-128">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="631e0-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="631e0-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="631e0-129">-WhatIf</span></span>
<span data-ttu-id="631e0-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="631e0-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="631e0-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="631e0-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="631e0-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="631e0-132">CommonParameters</span></span>
<span data-ttu-id="631e0-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="631e0-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="631e0-134">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="631e0-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="631e0-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="631e0-135">INPUTS</span></span>

### <span data-ttu-id="631e0-136">System. String</span><span class="sxs-lookup"><span data-stu-id="631e0-136">System.String</span></span>
### <span data-ttu-id="631e0-137">Microsoft. Azure. Commands. SignalR. modeller. PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="631e0-137">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>
## <span data-ttu-id="631e0-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="631e0-138">OUTPUTS</span></span>

### <span data-ttu-id="631e0-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="631e0-139">System.Boolean</span></span>
## <span data-ttu-id="631e0-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="631e0-140">NOTES</span></span>

## <span data-ttu-id="631e0-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="631e0-141">RELATED LINKS</span></span>
