---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/remove-azcontainerregistryreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryReplication.md
ms.openlocfilehash: 41bdf9bbc33239590f9d3a6db4ffaa88ddf752a1
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93937562"
---
# <span data-ttu-id="5783a-101">Remove-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="5783a-101">Remove-AzContainerRegistryReplication</span></span>

## <span data-ttu-id="5783a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5783a-102">SYNOPSIS</span></span>
<span data-ttu-id="5783a-103">Kapsayıcı kayıt defteri çoğaltmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="5783a-103">Removes a container registry replication.</span></span>

## <span data-ttu-id="5783a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5783a-104">SYNTAX</span></span>

### <span data-ttu-id="5783a-105">NameResourceGroupParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="5783a-105">NameResourceGroupParameterSet (Default)</span></span>
```
Remove-AzContainerRegistryReplication [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5783a-106">ReplicationObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5783a-106">ReplicationObjectParameterSet</span></span>
```
Remove-AzContainerRegistryReplication -Replication <PSContainerRegistryReplication> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5783a-107">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="5783a-107">ResourceIdParameterSet</span></span>
```
Remove-AzContainerRegistryReplication -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5783a-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="5783a-108">DESCRIPTION</span></span>
<span data-ttu-id="5783a-109">Remove-AzContainerRegistryReplication cmdlet 'i kapsayıcı kayıt defteri çoğaltmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="5783a-109">The Remove-AzContainerRegistryReplication cmdlet removes a container registry replication.</span></span>

## <span data-ttu-id="5783a-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5783a-110">EXAMPLES</span></span>

### <span data-ttu-id="5783a-111">Örnek 1: kapsayıcı kayıt defteri çoğaltmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="5783a-111">Example 1: Removes a container registry replication.</span></span>
```powershell
PS C:\> Remove-AzContainerRegistryReplication -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "replication001"
```

<span data-ttu-id="5783a-112">Kapsayıcı kayıt defteri çoğaltmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="5783a-112">Removes a container registry replication.</span></span>

## <span data-ttu-id="5783a-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5783a-113">PARAMETERS</span></span>

### <span data-ttu-id="5783a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5783a-114">-DefaultProfile</span></span>
<span data-ttu-id="5783a-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5783a-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5783a-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="5783a-116">-Name</span></span>
<span data-ttu-id="5783a-117">Kapsayıcı kayıt defteri çoğaltma adı.</span><span class="sxs-lookup"><span data-stu-id="5783a-117">Container Registry Replication Name.</span></span>
<span data-ttu-id="5783a-118">Varsayılan konum adı.</span><span class="sxs-lookup"><span data-stu-id="5783a-118">Default to the location name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases: ReplicationName, ResourceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5783a-119">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="5783a-119">-PassThru</span></span>
<span data-ttu-id="5783a-120">Kaldırma işlemi başarılıysa bu cmdlet 'in doğru döndüğü anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="5783a-120">Indicates that this cmdlet returns true if the removal was successful.</span></span>

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

### <span data-ttu-id="5783a-121">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="5783a-121">-RegistryName</span></span>
<span data-ttu-id="5783a-122">Kapsayıcı kayıt defteri adı.</span><span class="sxs-lookup"><span data-stu-id="5783a-122">Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases: ContainerRegistryName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5783a-123">-Çoğaltma</span><span class="sxs-lookup"><span data-stu-id="5783a-123">-Replication</span></span>
<span data-ttu-id="5783a-124">Kapsayıcısı.</span><span class="sxs-lookup"><span data-stu-id="5783a-124">Container Registry Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication
Parameter Sets: ReplicationObjectParameterSet
Aliases: Replicatoin

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5783a-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5783a-125">-ResourceGroupName</span></span>
<span data-ttu-id="5783a-126">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="5783a-126">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5783a-127">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="5783a-127">-ResourceId</span></span>
<span data-ttu-id="5783a-128">Kapsayıcı kayıt defteri çoğaltma kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="5783a-128">The container registry replication resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5783a-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="5783a-129">-Confirm</span></span>
<span data-ttu-id="5783a-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="5783a-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5783a-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5783a-131">-WhatIf</span></span>
<span data-ttu-id="5783a-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="5783a-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5783a-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="5783a-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5783a-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5783a-134">CommonParameters</span></span>
<span data-ttu-id="5783a-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5783a-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5783a-136">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="5783a-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5783a-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5783a-137">INPUTS</span></span>

### <span data-ttu-id="5783a-138">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="5783a-138">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication</span></span>

### <span data-ttu-id="5783a-139">System. String</span><span class="sxs-lookup"><span data-stu-id="5783a-139">System.String</span></span>

## <span data-ttu-id="5783a-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5783a-140">OUTPUTS</span></span>

### <span data-ttu-id="5783a-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5783a-141">System.Boolean</span></span>

## <span data-ttu-id="5783a-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5783a-142">NOTES</span></span>

## <span data-ttu-id="5783a-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5783a-143">RELATED LINKS</span></span>

[<span data-ttu-id="5783a-144">Yeni-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="5783a-144">New-AzContainerRegistryReplication</span></span>](New-AzContainerRegistryReplication.md)

[<span data-ttu-id="5783a-145">Get-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="5783a-145">Get-AzContainerRegistryReplication</span></span>](Remove-AzContainerRegistryReplication.md)

