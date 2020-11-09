---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/new-azcontainerregistryreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistryReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistryReplication.md
ms.openlocfilehash: aadac0f7d408efd5f635d77d14f9afabfbd444d0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94319578"
---
# <span data-ttu-id="4b8ee-101">New-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="4b8ee-101">New-AzContainerRegistryReplication</span></span>

## <span data-ttu-id="4b8ee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4b8ee-102">SYNOPSIS</span></span>
<span data-ttu-id="4b8ee-103">Kapsayıcı kayıt defteri çoğaltması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4b8ee-103">Creates a container registry replication.</span></span>

## <span data-ttu-id="4b8ee-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4b8ee-104">SYNTAX</span></span>

### <span data-ttu-id="4b8ee-105">NameResourceGroupParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="4b8ee-105">NameResourceGroupParameterSet (Default)</span></span>
```
New-AzContainerRegistryReplication [-ResourceGroupName] <String> [-RegistryName] <String> -Location <String>
 [-Name <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4b8ee-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4b8ee-106">RegistryObjectParameterSet</span></span>
```
New-AzContainerRegistryReplication -Registry <PSContainerRegistry> -Location <String> [-Name <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4b8ee-107">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="4b8ee-107">ResourceIdParameterSet</span></span>
```
New-AzContainerRegistryReplication -Location <String> [-Name <String>] [-Tag <Hashtable>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4b8ee-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="4b8ee-108">DESCRIPTION</span></span>
<span data-ttu-id="4b8ee-109">New-AzContainerRegistryReplication cmdlet 'i yeni bir kapsayıcı kayıt defteri çoğaltması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4b8ee-109">The New-AzContainerRegistryReplication cmdlet creates a new container registry replication.</span></span>

## <span data-ttu-id="4b8ee-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4b8ee-110">EXAMPLES</span></span>

### <span data-ttu-id="4b8ee-111">Örnek 1: yeni bir kapsayıcı kayıt defteri çoğaltması oluşturun.</span><span class="sxs-lookup"><span data-stu-id="4b8ee-111">Example 1: Create a new container registry replication.</span></span>
```powershell
PS C:\>New-AzContainerRegistryReplication -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name replication001 -Location 'west us' -Tag @{tagName='MyTag'}

Name                 Location   Provisioni Status               StatusTimestamp                Tags
                                ngState
----                 --------   ---------- ------               ---------------                ----
replication001       westus     Succeeded  Ready                11/17/2017 10:19:45 PM         {[tagName, MyTag]}
```

<span data-ttu-id="4b8ee-112">Yeni kapsayıcı kayıt defteri çoğaltması oluşturun.</span><span class="sxs-lookup"><span data-stu-id="4b8ee-112">Create a new container registry replication.</span></span>

## <span data-ttu-id="4b8ee-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4b8ee-113">PARAMETERS</span></span>

### <span data-ttu-id="4b8ee-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b8ee-114">-DefaultProfile</span></span>
<span data-ttu-id="4b8ee-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4b8ee-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4b8ee-116">-Konum</span><span class="sxs-lookup"><span data-stu-id="4b8ee-116">-Location</span></span>
<span data-ttu-id="4b8ee-117">Kapsayıcı kayıt defteri konumu.</span><span class="sxs-lookup"><span data-stu-id="4b8ee-117">Container Registry Location.</span></span>
<span data-ttu-id="4b8ee-118">Kaynak grubunun konumu.</span><span class="sxs-lookup"><span data-stu-id="4b8ee-118">Default to the location of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ReplicationLocation

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b8ee-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="4b8ee-119">-Name</span></span>
<span data-ttu-id="4b8ee-120">Kapsayıcı kayıt defteri çoğaltma adı.</span><span class="sxs-lookup"><span data-stu-id="4b8ee-120">Container Registry Replication Name.</span></span>
<span data-ttu-id="4b8ee-121">Varsayılan konum adı.</span><span class="sxs-lookup"><span data-stu-id="4b8ee-121">Default to the location name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ReplicationName, ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b8ee-122">-Registry</span><span class="sxs-lookup"><span data-stu-id="4b8ee-122">-Registry</span></span>
<span data-ttu-id="4b8ee-123">Kapsayıcısı.</span><span class="sxs-lookup"><span data-stu-id="4b8ee-123">Container Registry Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry
Parameter Sets: RegistryObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b8ee-124">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="4b8ee-124">-RegistryName</span></span>
<span data-ttu-id="4b8ee-125">Kapsayıcı kayıt defteri adı.</span><span class="sxs-lookup"><span data-stu-id="4b8ee-125">Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases: ContainerRegistryName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b8ee-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4b8ee-126">-ResourceGroupName</span></span>
<span data-ttu-id="4b8ee-127">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="4b8ee-127">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b8ee-128">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="4b8ee-128">-ResourceId</span></span>
<span data-ttu-id="4b8ee-129">Kapsayıcı kayıt defteri kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="4b8ee-129">The container registry resource id</span></span>

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

### <span data-ttu-id="4b8ee-130">Etiketli</span><span class="sxs-lookup"><span data-stu-id="4b8ee-130">-Tag</span></span>
<span data-ttu-id="4b8ee-131">Kapsayıcı kayıt defteri etiketleri.</span><span class="sxs-lookup"><span data-stu-id="4b8ee-131">Container Registry Tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b8ee-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="4b8ee-132">-Confirm</span></span>
<span data-ttu-id="4b8ee-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="4b8ee-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4b8ee-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4b8ee-134">-WhatIf</span></span>
<span data-ttu-id="4b8ee-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="4b8ee-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4b8ee-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="4b8ee-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4b8ee-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b8ee-137">CommonParameters</span></span>
<span data-ttu-id="4b8ee-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4b8ee-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b8ee-139">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="4b8ee-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b8ee-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4b8ee-140">INPUTS</span></span>

### <span data-ttu-id="4b8ee-141">System. String</span><span class="sxs-lookup"><span data-stu-id="4b8ee-141">System.String</span></span>

## <span data-ttu-id="4b8ee-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4b8ee-142">OUTPUTS</span></span>

### <span data-ttu-id="4b8ee-143">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="4b8ee-143">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication</span></span>

## <span data-ttu-id="4b8ee-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4b8ee-144">NOTES</span></span>

## <span data-ttu-id="4b8ee-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4b8ee-145">RELATED LINKS</span></span>

[<span data-ttu-id="4b8ee-146">Get-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="4b8ee-146">Get-AzContainerRegistryReplication</span></span>](New-AzContainerRegistryReplication.md)

[<span data-ttu-id="4b8ee-147">Remove-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="4b8ee-147">Remove-AzContainerRegistryReplication</span></span>](Remove-AzContainerRegistryReplication.md)