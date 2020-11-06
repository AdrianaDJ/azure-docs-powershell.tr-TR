---
external help file: Microsoft.Azure.Commands.SignalR.dll-Help.xml
Module Name: AzureRM.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.signalr/new-azurermsignalrkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SignalR/Commands.SignalR/help/New-AzureRmSignalRKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SignalR/Commands.SignalR/help/New-AzureRmSignalRKey.md
ms.openlocfilehash: 4b4f3a416ece999641570a33101a3e7ab201ca3b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590840"
---
# <span data-ttu-id="110fd-101">New-AzureRmSignalRKey</span><span class="sxs-lookup"><span data-stu-id="110fd-101">New-AzureRmSignalRKey</span></span>

## <span data-ttu-id="110fd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="110fd-102">SYNOPSIS</span></span>
<span data-ttu-id="110fd-103">Bir SignalR hizmeti için erişim anahtarını yeniden oluşturun.</span><span class="sxs-lookup"><span data-stu-id="110fd-103">Regenerate an access key for a SignalR service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="110fd-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="110fd-104">SYNTAX</span></span>

### <span data-ttu-id="110fd-105">ResourceGroupParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="110fd-105">ResourceGroupParameterSet (Default)</span></span>
```
New-AzureRmSignalRKey [-ResourceGroupName <String>] [-Name] <String> [-KeyType] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="110fd-106">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="110fd-106">ResourceIdParameterSet</span></span>
```
New-AzureRmSignalRKey -ResourceId <String> [-KeyType] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="110fd-107">Inputobjectparameterset</span><span class="sxs-lookup"><span data-stu-id="110fd-107">InputObjectParameterSet</span></span>
```
New-AzureRmSignalRKey -InputObject <PSSignalRResource> [-KeyType] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="110fd-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="110fd-108">DESCRIPTION</span></span>
<span data-ttu-id="110fd-109">Bir SignalR hizmeti için erişim anahtarını yeniden oluşturun.</span><span class="sxs-lookup"><span data-stu-id="110fd-109">Regenerate an access key for a SignalR service.</span></span>

## <span data-ttu-id="110fd-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="110fd-110">EXAMPLES</span></span>

### <span data-ttu-id="110fd-111">Birincil anahtarı yeniden üret</span><span class="sxs-lookup"><span data-stu-id="110fd-111">Regenerate the primary key</span></span>
```powershell
PS C:\> New-AzureRmSignalRKey -ResourceGroupName myResourceGroup -Name mysignalr1 -KeyType Primary -PassThru

True
```

## <span data-ttu-id="110fd-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="110fd-112">PARAMETERS</span></span>

### <span data-ttu-id="110fd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="110fd-113">-DefaultProfile</span></span>
<span data-ttu-id="110fd-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="110fd-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="110fd-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="110fd-115">-InputObject</span></span>
<span data-ttu-id="110fd-116">SignalR kaynak nesnesi.</span><span class="sxs-lookup"><span data-stu-id="110fd-116">The SignalR resource object.</span></span>

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

### <span data-ttu-id="110fd-117">-KeyType</span><span class="sxs-lookup"><span data-stu-id="110fd-117">-KeyType</span></span>
<span data-ttu-id="110fd-118">Birincil veya Ikincil anahtar türü.</span><span class="sxs-lookup"><span data-stu-id="110fd-118">The key type, either Primary or Secondary.</span></span>

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

### <span data-ttu-id="110fd-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="110fd-119">-Name</span></span>
<span data-ttu-id="110fd-120">SignalR hizmet adı.</span><span class="sxs-lookup"><span data-stu-id="110fd-120">SignalR service name.</span></span>

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

### <span data-ttu-id="110fd-121">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="110fd-121">-PassThru</span></span>
<span data-ttu-id="110fd-122">Yeniden oluşturma başarıyla tamamlanırsa, doğru döndürür.</span><span class="sxs-lookup"><span data-stu-id="110fd-122">Returns true if the regeneration was completed successfully.</span></span>

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

### <span data-ttu-id="110fd-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="110fd-123">-ResourceGroupName</span></span>
<span data-ttu-id="110fd-124">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="110fd-124">Resource group name.</span></span>

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

### <span data-ttu-id="110fd-125">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="110fd-125">-ResourceId</span></span>
<span data-ttu-id="110fd-126">SignalR hizmeti kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="110fd-126">The SignalR service resource ID.</span></span>

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

### <span data-ttu-id="110fd-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="110fd-127">-Confirm</span></span>
<span data-ttu-id="110fd-128">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="110fd-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="110fd-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="110fd-129">-WhatIf</span></span>
<span data-ttu-id="110fd-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="110fd-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="110fd-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="110fd-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="110fd-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="110fd-132">CommonParameters</span></span>
<span data-ttu-id="110fd-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="110fd-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="110fd-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="110fd-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="110fd-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="110fd-135">INPUTS</span></span>

### <span data-ttu-id="110fd-136">System. String</span><span class="sxs-lookup"><span data-stu-id="110fd-136">System.String</span></span>
<span data-ttu-id="110fd-137">Parametreler: RESOURCEID (ByValue)</span><span class="sxs-lookup"><span data-stu-id="110fd-137">Parameters: ResourceId (ByValue)</span></span>

### <span data-ttu-id="110fd-138">Microsoft. Azure. Commands. SignalR. modeller. PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="110fd-138">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>
<span data-ttu-id="110fd-139">Parametreler: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="110fd-139">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="110fd-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="110fd-140">OUTPUTS</span></span>

### <span data-ttu-id="110fd-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="110fd-141">System.Boolean</span></span>

## <span data-ttu-id="110fd-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="110fd-142">NOTES</span></span>

## <span data-ttu-id="110fd-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="110fd-143">RELATED LINKS</span></span>
