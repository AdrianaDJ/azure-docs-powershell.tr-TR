---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsetriggersubscriptionstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseTriggerSubscriptionStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseTriggerSubscriptionStatus.md
ms.openlocfilehash: b18a308b94bdb486945186c67c3a905bcb0408d3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94323539"
---
# <span data-ttu-id="67218-101">Get-AzSynapseTriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="67218-101">Get-AzSynapseTriggerSubscriptionStatus</span></span>

## <span data-ttu-id="67218-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="67218-102">SYNOPSIS</span></span>
<span data-ttu-id="67218-103">Olay tetikleyicisi için aboneliğin durumunu belirtilen dış hizmet olaylarına alın.</span><span class="sxs-lookup"><span data-stu-id="67218-103">Get the status of the subscription for the event trigger to the specified external service events.</span></span>

## <span data-ttu-id="67218-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="67218-104">SYNTAX</span></span>

### <span data-ttu-id="67218-105">GetByName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="67218-105">GetByName (Default)</span></span>
```
Get-AzSynapseTriggerSubscriptionStatus -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="67218-106">GetByObject</span><span class="sxs-lookup"><span data-stu-id="67218-106">GetByObject</span></span>
```
Get-AzSynapseTriggerSubscriptionStatus -WorkspaceObject <PSSynapseWorkspace> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="67218-107">GetByInputObject</span><span class="sxs-lookup"><span data-stu-id="67218-107">GetByInputObject</span></span>
```
Get-AzSynapseTriggerSubscriptionStatus -InputObject <PSTriggerResource>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="67218-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="67218-108">DESCRIPTION</span></span>
<span data-ttu-id="67218-109">**Get-AzSynapseTriggerSubscriptionStatus** cmdlet 'i, olay tetikleyicisi için belirtilen dış hizmet olaylarına aboneliğin durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="67218-109">The **Get-AzSynapseTriggerSubscriptionStatus** cmdlet gets the status of the subscription for the event trigger to the specified external service events.</span></span> <span data-ttu-id="67218-110">Tetik, iade durumu "Enabled" olana kadar başlatılamıyor.</span><span class="sxs-lookup"><span data-stu-id="67218-110">The trigger can't be started until the returned status is "Enabled".</span></span>

## <span data-ttu-id="67218-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="67218-111">EXAMPLES</span></span>

### <span data-ttu-id="67218-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="67218-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseTriggerSubscriptionStatus -WorkspaceName ContosoWorkspace -Name ContosoTrigger
```

<span data-ttu-id="67218-113">Bu komut, ContosoTrigger adındaki subscribtion tetikleyicisi 'nin dış hizmet olaylarına durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="67218-113">This command will get the status of the subscribtion for trigger called ContosoTrigger to the external service events.</span></span>

### <span data-ttu-id="67218-114">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="67218-114">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseTriggerSubscriptionStatus -Name ContosoTrigger
```

<span data-ttu-id="67218-115">Bu komut, "subscribtion" tetikleyicisi için, Contosotetikleyicisi dış hizmet olaylarına ardışık düzen aracılığıyla.</span><span class="sxs-lookup"><span data-stu-id="67218-115">This command will get the status of the subscribtion for trigger called ContosoTrigger to the external service events through pipeline.</span></span>

### <span data-ttu-id="67218-116">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="67218-116">Example 3</span></span>
```powershell
PS C:\> $trigger = Get-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
PS C:\> $trigger | Get-AzSynapseTriggerSubscriptionStatus
```

<span data-ttu-id="67218-117">Bu komut, "subscribtion" tetikleyicisi için, Contosotetikleyicisi dış hizmet olaylarına ardışık düzen aracılığıyla.</span><span class="sxs-lookup"><span data-stu-id="67218-117">This command will get the status of the subscribtion for trigger called ContosoTrigger to the external service events through pipeline.</span></span>

## <span data-ttu-id="67218-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="67218-118">PARAMETERS</span></span>

### <span data-ttu-id="67218-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67218-119">-DefaultProfile</span></span>
<span data-ttu-id="67218-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="67218-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="67218-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="67218-121">-InputObject</span></span>
<span data-ttu-id="67218-122">Tetik nesnesi.</span><span class="sxs-lookup"><span data-stu-id="67218-122">The trigger object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource
Parameter Sets: GetByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="67218-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="67218-123">-Name</span></span>
<span data-ttu-id="67218-124">Tetik adı.</span><span class="sxs-lookup"><span data-stu-id="67218-124">The trigger name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByName, GetByObject
Aliases: TriggerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67218-125">-Çalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="67218-125">-WorkspaceName</span></span>
<span data-ttu-id="67218-126">SYNAPSE çalışma alanının adı.</span><span class="sxs-lookup"><span data-stu-id="67218-126">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67218-127">-</span><span class="sxs-lookup"><span data-stu-id="67218-127">-WorkspaceObject</span></span>
<span data-ttu-id="67218-128">genellikle ardışık düzen aracılığıyla geçen çalışma alanı giriş nesnesidir.</span><span class="sxs-lookup"><span data-stu-id="67218-128">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: GetByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="67218-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67218-129">CommonParameters</span></span>
<span data-ttu-id="67218-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="67218-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67218-131">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="67218-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67218-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="67218-132">INPUTS</span></span>

### <span data-ttu-id="67218-133">Microsoft. Azure. Commands. SYNAPSE. modeller. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="67218-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="67218-134">Microsoft. Azure. Commands. SYNAPSE. modeller. Pçarpıcı Ggerresource</span><span class="sxs-lookup"><span data-stu-id="67218-134">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span></span>

## <span data-ttu-id="67218-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="67218-135">OUTPUTS</span></span>

### <span data-ttu-id="67218-136">Microsoft. Azure. Commands. SYNAPSE. modeller. P, Ggersubscriptionoperationstatus</span><span class="sxs-lookup"><span data-stu-id="67218-136">Microsoft.Azure.Commands.Synapse.Models.PSTriggerSubscriptionOperationStatus</span></span>

## <span data-ttu-id="67218-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="67218-137">NOTES</span></span>

## <span data-ttu-id="67218-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="67218-138">RELATED LINKS</span></span>
