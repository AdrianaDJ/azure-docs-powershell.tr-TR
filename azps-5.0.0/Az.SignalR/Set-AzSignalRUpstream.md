---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/set-azsignalrupstream
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Set-AzSignalRUpstream.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Set-AzSignalRUpstream.md
ms.openlocfilehash: e04e87067f86f529117512e7443118f308b20547
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94324250"
---
# <span data-ttu-id="b191c-101">Set-AzSignalRUpstream</span><span class="sxs-lookup"><span data-stu-id="b191c-101">Set-AzSignalRUpstream</span></span>

## <span data-ttu-id="b191c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b191c-102">SYNOPSIS</span></span>
<span data-ttu-id="b191c-103">Bir SignalR hizmetinin akış yukarı ayarlarını ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="b191c-103">Set the upstream settings of a SignalR service.</span></span>

## <span data-ttu-id="b191c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b191c-104">SYNTAX</span></span>

### <span data-ttu-id="b191c-105">ResourceGroupParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="b191c-105">ResourceGroupParameterSet (Default)</span></span>
```
Set-AzSignalRUpstream [-ResourceGroupName <String>] [-Name] <String> [-AsJob]
 [-Template <PSUpstreamTemplate[]>] [-Clear] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b191c-106">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="b191c-106">ResourceIdParameterSet</span></span>
```
Set-AzSignalRUpstream -ResourceId <String> [-AsJob] [-Template <PSUpstreamTemplate[]>] [-Clear]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b191c-107">Inputobjectparameterset</span><span class="sxs-lookup"><span data-stu-id="b191c-107">InputObjectParameterSet</span></span>
```
Set-AzSignalRUpstream -InputObject <PSSignalRResource> [-AsJob] [-Template <PSUpstreamTemplate[]>] [-Clear]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b191c-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="b191c-108">DESCRIPTION</span></span>
<span data-ttu-id="b191c-109">Bir SignalR hizmetinin akış yukarı ayarlarını ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="b191c-109">Set the upstream settings of a SignalR service.</span></span>

## <span data-ttu-id="b191c-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b191c-110">EXAMPLES</span></span>

### <span data-ttu-id="b191c-111">Sıralı iki ters yöndeki şablon ayarlama</span><span class="sxs-lookup"><span data-stu-id="b191c-111">Set two ordered upstream templates</span></span>
```powershell
PS C:\>  Set-AzSignalRUpstream -name pssignalr -ResourceGroupName test_resource_group -Template @{UrlTemplate='http://host-connections1.com'; HubPattern='chat';EventPattern='broadcast' }, @{UrlTemplate='http://host-connections2.com'}

Templates
---------
{Microsoft.Azure.Commands.SignalR.Models.PSUpstreamTemplate, Microsoft.Azure.Commands.SignalR.Models.PSUpstreamTemplat…
```

<span data-ttu-id="b191c-112">Aşağıdaki JSON, ayarlanan gerçek şablonları temsil eder.</span><span class="sxs-lookup"><span data-stu-id="b191c-112">The following JSON represents the actual templates set.</span></span> 

 `
{
    "hubPattern": "chat",
    "eventPattern": "broadcast",
    "categoryPattern": "*",
    "urlTemplate": "http://host-connections1.com"
},
{
    "hubPattern": "*",
    "eventPattern": "*",
    "categoryPattern": "*",
    "urlTemplate": "http://host-connections2.com"
}
`

### <span data-ttu-id="b191c-113">Tüm yukarı akış ayarlarını Temizleme</span><span class="sxs-lookup"><span data-stu-id="b191c-113">Clear all the upstream settings</span></span>
```powershell
PS C:\>  Set-AzSignalRUpstream -name pssignalr -ResourceGroupName test_resource_group -Clear

Templates
---------
{}
```

## <span data-ttu-id="b191c-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b191c-114">PARAMETERS</span></span>

### <span data-ttu-id="b191c-115">-Iş</span><span class="sxs-lookup"><span data-stu-id="b191c-115">-AsJob</span></span>
<span data-ttu-id="b191c-116">Cmdlet 'i arka plan işinde çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="b191c-116">Run the cmdlet in background job.</span></span>

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

### <span data-ttu-id="b191c-117">-Clear</span><span class="sxs-lookup"><span data-stu-id="b191c-117">-Clear</span></span>
<span data-ttu-id="b191c-118">Tüm yukarı akış ayarlarını temizleyin.</span><span class="sxs-lookup"><span data-stu-id="b191c-118">Clear all the upstream settings.</span></span>

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

### <span data-ttu-id="b191c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b191c-119">-DefaultProfile</span></span>
<span data-ttu-id="b191c-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b191c-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b191c-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b191c-121">-InputObject</span></span>
<span data-ttu-id="b191c-122">SignalR kaynak nesnesi.</span><span class="sxs-lookup"><span data-stu-id="b191c-122">The SignalR resource object.</span></span>

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

### <span data-ttu-id="b191c-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="b191c-123">-Name</span></span>
<span data-ttu-id="b191c-124">SignalR hizmet adı.</span><span class="sxs-lookup"><span data-stu-id="b191c-124">The SignalR service name.</span></span>

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

### <span data-ttu-id="b191c-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b191c-125">-ResourceGroupName</span></span>
<span data-ttu-id="b191c-126">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="b191c-126">The resource group name.</span></span>
<span data-ttu-id="b191c-127">Belirtilmemişse, varsayılan değer kullanılacaktır.</span><span class="sxs-lookup"><span data-stu-id="b191c-127">The default one will be used if not specified.</span></span>

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

### <span data-ttu-id="b191c-128">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="b191c-128">-ResourceId</span></span>
<span data-ttu-id="b191c-129">SignalR hizmeti kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="b191c-129">The SignalR service resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b191c-130">-Şablon</span><span class="sxs-lookup"><span data-stu-id="b191c-130">-Template</span></span>
<span data-ttu-id="b191c-131">Yukarı akış ayarları için şablon öğeleri.</span><span class="sxs-lookup"><span data-stu-id="b191c-131">Template item(s) for upstream settings.</span></span>
<span data-ttu-id="b191c-132">Gerekli anahtar: UrlTemplate.</span><span class="sxs-lookup"><span data-stu-id="b191c-132">Required key: UrlTemplate.</span></span>
<span data-ttu-id="b191c-133">İsteğe bağlı tuşlar: HubPattern, EventPattern, CategoryPattern.</span><span class="sxs-lookup"><span data-stu-id="b191c-133">Optional keys: HubPattern, EventPattern, CategoryPattern.</span></span>
<span data-ttu-id="b191c-134">Şablon parametresini geçirmek için splatın sözdizimini kullanan örnek: @ {Urlşablonu = ' http://host-connections1.com ', hubpattern = ' sohbet '; EventPattern = ' Broadcast '}, @ {UrlTemplate = ' http://host-connections2.com '}</span><span class="sxs-lookup"><span data-stu-id="b191c-134">Example using splatting syntax to pass templates parameter: @{UrlTemplate='http://host-connections1.com', HubPattern= 'chat';EventPattern='broadcast' },@{UrlTemplate='http://host-connections2.com'}</span></span>

```yaml
Type: Microsoft.Azure.Commands.SignalR.Models.PSUpstreamTemplate[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b191c-135">-Onay</span><span class="sxs-lookup"><span data-stu-id="b191c-135">-Confirm</span></span>
<span data-ttu-id="b191c-136">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b191c-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b191c-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b191c-137">-WhatIf</span></span>
<span data-ttu-id="b191c-138">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b191c-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b191c-139">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b191c-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b191c-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b191c-140">CommonParameters</span></span>
<span data-ttu-id="b191c-141">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b191c-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b191c-142">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="b191c-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b191c-143">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b191c-143">INPUTS</span></span>

### <span data-ttu-id="b191c-144">System. String</span><span class="sxs-lookup"><span data-stu-id="b191c-144">System.String</span></span>

## <span data-ttu-id="b191c-145">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b191c-145">OUTPUTS</span></span>

### <span data-ttu-id="b191c-146">Microsoft. Azure. Commands. SignalR. modeller. PSServerlessUpstreamSettings</span><span class="sxs-lookup"><span data-stu-id="b191c-146">Microsoft.Azure.Commands.SignalR.Models.PSServerlessUpstreamSettings</span></span>

## <span data-ttu-id="b191c-147">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b191c-147">NOTES</span></span>

## <span data-ttu-id="b191c-148">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b191c-148">RELATED LINKS</span></span>

[<span data-ttu-id="b191c-149">PowerShell 'deki komutlara parametreleri geçirmek için splatın kullanma</span><span class="sxs-lookup"><span data-stu-id="b191c-149">How to use splatting to pass parameters to commands in PowerShell</span></span>](https://docs.microsoft.com/en-us/powershell/module/microsoft.powershell.core/about/about_splatting?view=powershell-7)
