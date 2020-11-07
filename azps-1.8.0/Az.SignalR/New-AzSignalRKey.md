---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/new-azsignalrkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/New-AzSignalRKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/New-AzSignalRKey.md
ms.openlocfilehash: 3feb052875cdf9afa7a32d4e7fc8066517b16dd8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93759090"
---
# <span data-ttu-id="f343b-101">New-AzSignalRKey</span><span class="sxs-lookup"><span data-stu-id="f343b-101">New-AzSignalRKey</span></span>

## <span data-ttu-id="f343b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f343b-102">SYNOPSIS</span></span>
<span data-ttu-id="f343b-103">Bir SignalR hizmeti için erişim anahtarını yeniden oluşturun.</span><span class="sxs-lookup"><span data-stu-id="f343b-103">Regenerate an access key for a SignalR service.</span></span>

## <span data-ttu-id="f343b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f343b-104">SYNTAX</span></span>

### <span data-ttu-id="f343b-105">ResourceGroupParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="f343b-105">ResourceGroupParameterSet (Default)</span></span>
```
New-AzSignalRKey [-ResourceGroupName <String>] [-Name] <String> [-KeyType] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f343b-106">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="f343b-106">ResourceIdParameterSet</span></span>
```
New-AzSignalRKey -ResourceId <String> [-KeyType] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f343b-107">Inputobjectparameterset</span><span class="sxs-lookup"><span data-stu-id="f343b-107">InputObjectParameterSet</span></span>
```
New-AzSignalRKey -InputObject <PSSignalRResource> [-KeyType] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f343b-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="f343b-108">DESCRIPTION</span></span>
<span data-ttu-id="f343b-109">Bir SignalR hizmeti için erişim anahtarını yeniden oluşturun.</span><span class="sxs-lookup"><span data-stu-id="f343b-109">Regenerate an access key for a SignalR service.</span></span>

## <span data-ttu-id="f343b-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f343b-110">EXAMPLES</span></span>

### <span data-ttu-id="f343b-111">Birincil anahtarı yeniden üret</span><span class="sxs-lookup"><span data-stu-id="f343b-111">Regenerate the primary key</span></span>
```powershell
PS C:\> New-AzSignalRKey -ResourceGroupName myResourceGroup -Name mysignalr1 -KeyType Primary -PassThru

True
```

## <span data-ttu-id="f343b-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f343b-112">PARAMETERS</span></span>

### <span data-ttu-id="f343b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f343b-113">-DefaultProfile</span></span>
<span data-ttu-id="f343b-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f343b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f343b-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f343b-115">-InputObject</span></span>
<span data-ttu-id="f343b-116">SignalR kaynak nesnesi.</span><span class="sxs-lookup"><span data-stu-id="f343b-116">The SignalR resource object.</span></span>

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

### <span data-ttu-id="f343b-117">-KeyType</span><span class="sxs-lookup"><span data-stu-id="f343b-117">-KeyType</span></span>
<span data-ttu-id="f343b-118">Birincil veya Ikincil anahtar türü.</span><span class="sxs-lookup"><span data-stu-id="f343b-118">The key type, either Primary or Secondary.</span></span>

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

### <span data-ttu-id="f343b-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="f343b-119">-Name</span></span>
<span data-ttu-id="f343b-120">SignalR hizmet adı.</span><span class="sxs-lookup"><span data-stu-id="f343b-120">SignalR service name.</span></span>

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

### <span data-ttu-id="f343b-121">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="f343b-121">-PassThru</span></span>
<span data-ttu-id="f343b-122">Yeniden oluşturma başarıyla tamamlanırsa, doğru döndürür.</span><span class="sxs-lookup"><span data-stu-id="f343b-122">Returns true if the regeneration was completed successfully.</span></span>

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

### <span data-ttu-id="f343b-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f343b-123">-ResourceGroupName</span></span>
<span data-ttu-id="f343b-124">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="f343b-124">Resource group name.</span></span>

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

### <span data-ttu-id="f343b-125">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="f343b-125">-ResourceId</span></span>
<span data-ttu-id="f343b-126">SignalR hizmeti kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="f343b-126">The SignalR service resource ID.</span></span>

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

### <span data-ttu-id="f343b-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="f343b-127">-Confirm</span></span>
<span data-ttu-id="f343b-128">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f343b-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f343b-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f343b-129">-WhatIf</span></span>
<span data-ttu-id="f343b-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f343b-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f343b-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f343b-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f343b-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f343b-132">CommonParameters</span></span>
<span data-ttu-id="f343b-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f343b-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f343b-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f343b-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f343b-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f343b-135">INPUTS</span></span>

### <span data-ttu-id="f343b-136">System. String</span><span class="sxs-lookup"><span data-stu-id="f343b-136">System.String</span></span>

### <span data-ttu-id="f343b-137">Microsoft. Azure. Commands. SignalR. modeller. PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="f343b-137">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>

## <span data-ttu-id="f343b-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f343b-138">OUTPUTS</span></span>

### <span data-ttu-id="f343b-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f343b-139">System.Boolean</span></span>

## <span data-ttu-id="f343b-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f343b-140">NOTES</span></span>

## <span data-ttu-id="f343b-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f343b-141">RELATED LINKS</span></span>
