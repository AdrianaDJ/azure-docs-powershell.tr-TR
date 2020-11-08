---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/get-azcontainerregistryreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryReplication.md
ms.openlocfilehash: 57b482368834d91e36a3f557c9657c82cea24f4e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94275583"
---
# <span data-ttu-id="e5a05-101">Get-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="e5a05-101">Get-AzContainerRegistryReplication</span></span>

## <span data-ttu-id="e5a05-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e5a05-102">SYNOPSIS</span></span>
<span data-ttu-id="e5a05-103">Kapsayıcı kayıt defterinin çoğaltmasını alır.</span><span class="sxs-lookup"><span data-stu-id="e5a05-103">Gets a replication of a container registry.</span></span>

## <span data-ttu-id="e5a05-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e5a05-104">SYNTAX</span></span>

### <span data-ttu-id="e5a05-105">ListReplicationByNameResourceGroupParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="e5a05-105">ListReplicationByNameResourceGroupParameterSet (Default)</span></span>
```
Get-AzContainerRegistryReplication [-ResourceGroupName] <String> [-RegistryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e5a05-106">ShowReplicationByNameResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="e5a05-106">ShowReplicationByNameResourceGroupParameterSet</span></span>
```
Get-AzContainerRegistryReplication [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e5a05-107">ShowReplicationByRegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e5a05-107">ShowReplicationByRegistryObjectParameterSet</span></span>
```
Get-AzContainerRegistryReplication [-Name] <String> -Registry <PSContainerRegistry>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e5a05-108">ListReplicationByRegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e5a05-108">ListReplicationByRegistryObjectParameterSet</span></span>
```
Get-AzContainerRegistryReplication -Registry <PSContainerRegistry> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e5a05-109">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="e5a05-109">ResourceIdParameterSet</span></span>
```
Get-AzContainerRegistryReplication -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e5a05-110">Tanım</span><span class="sxs-lookup"><span data-stu-id="e5a05-110">DESCRIPTION</span></span>
<span data-ttu-id="e5a05-111">Get-AzContainerRegistryReplication cmdlet 'i, kapsayıcı kayıt defterinin belirli bir çoğaltmasını veya kapsayıcı kayıt defterinin tüm çoğaltmaları alır.</span><span class="sxs-lookup"><span data-stu-id="e5a05-111">The Get-AzContainerRegistryReplication cmdlet gets a specified replication of a container registry or all the replications of a container registry.</span></span>

## <span data-ttu-id="e5a05-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e5a05-112">EXAMPLES</span></span>

### <span data-ttu-id="e5a05-113">Örnek 1: kapsayıcı kayıt defterinin belirtilen çoğaltmasını alma</span><span class="sxs-lookup"><span data-stu-id="e5a05-113">Example 1: Gets a specified replication of a container registry</span></span>
```powershell
PS C:\>Get-AzContainerRegistryReplication -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "myreplication"

Name                 Location   Provisioni Status               StatusTimestamp                Tags
                                ngState
----                 --------   ---------- ------               ---------------                ----
myreplication       westus     Succeeded  Ready                 11/17/2017 10:19:45 PM         {[tagName, MyTag]}
```

<span data-ttu-id="e5a05-114">Kapsayıcı kayıt defterinin belirtilen çoğaltmasını alma</span><span class="sxs-lookup"><span data-stu-id="e5a05-114">Gets a specified replication of a container registry</span></span>

### <span data-ttu-id="e5a05-115">Örnek 2: kapsayıcı kayıt defterinin tüm çoğaltmaları alınır</span><span class="sxs-lookup"><span data-stu-id="e5a05-115">Example 2: Gets all the replications of a container registry</span></span>
```powershell
PS C:\>Get-AzContainerRegistryReplication -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry"

Name                 Location   Provisioni Status               StatusTimestamp                Tags
                                ngState
----                 --------   ---------- ------               ---------------                ----
eastus               eastus     Succeeded  Ready                11/6/2017 6:14:47 PM           {}
myreplication        westus     Succeeded  Ready                11/17/2017 10:19:45 PM         {[tagName, MyTag]}
```

<span data-ttu-id="e5a05-116">Kapsayıcı kayıt defterinin tüm çoğaltmaları</span><span class="sxs-lookup"><span data-stu-id="e5a05-116">Gets all the replications of a container registry</span></span>

## <span data-ttu-id="e5a05-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e5a05-117">PARAMETERS</span></span>

### <span data-ttu-id="e5a05-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5a05-118">-DefaultProfile</span></span>
<span data-ttu-id="e5a05-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e5a05-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e5a05-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="e5a05-120">-Name</span></span>
<span data-ttu-id="e5a05-121">Kapsayıcı kayıt defteri çoğaltma adı.</span><span class="sxs-lookup"><span data-stu-id="e5a05-121">Container Registry Replication Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ShowReplicationByNameResourceGroupParameterSet, ShowReplicationByRegistryObjectParameterSet
Aliases: ReplicationName, ResourceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5a05-122">-Registry</span><span class="sxs-lookup"><span data-stu-id="e5a05-122">-Registry</span></span>
<span data-ttu-id="e5a05-123">Kapsayıcısı.</span><span class="sxs-lookup"><span data-stu-id="e5a05-123">Container Registry Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry
Parameter Sets: ShowReplicationByRegistryObjectParameterSet, ListReplicationByRegistryObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e5a05-124">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="e5a05-124">-RegistryName</span></span>
<span data-ttu-id="e5a05-125">Kapsayıcı kayıt defteri adı.</span><span class="sxs-lookup"><span data-stu-id="e5a05-125">Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListReplicationByNameResourceGroupParameterSet, ShowReplicationByNameResourceGroupParameterSet
Aliases: ContainerRegistryName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5a05-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5a05-126">-ResourceGroupName</span></span>
<span data-ttu-id="e5a05-127">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="e5a05-127">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListReplicationByNameResourceGroupParameterSet, ShowReplicationByNameResourceGroupParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5a05-128">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="e5a05-128">-ResourceId</span></span>
<span data-ttu-id="e5a05-129">Kapsayıcı kayıt defteri çoğaltma kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="e5a05-129">The container registry replication resource id</span></span>

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

### <span data-ttu-id="e5a05-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5a05-130">CommonParameters</span></span>
<span data-ttu-id="e5a05-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e5a05-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5a05-132">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="e5a05-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5a05-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e5a05-133">INPUTS</span></span>

### <span data-ttu-id="e5a05-134">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="e5a05-134">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

### <span data-ttu-id="e5a05-135">System. String</span><span class="sxs-lookup"><span data-stu-id="e5a05-135">System.String</span></span>

## <span data-ttu-id="e5a05-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e5a05-136">OUTPUTS</span></span>

### <span data-ttu-id="e5a05-137">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="e5a05-137">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication</span></span>

## <span data-ttu-id="e5a05-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e5a05-138">NOTES</span></span>

## <span data-ttu-id="e5a05-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e5a05-139">RELATED LINKS</span></span>

[<span data-ttu-id="e5a05-140">Yeni-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="e5a05-140">New-AzContainerRegistryReplication</span></span>](New-AzContainerRegistryReplication.md)

[<span data-ttu-id="e5a05-141">Remove-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="e5a05-141">Remove-AzContainerRegistryReplication</span></span>](Remove-AzContainerRegistryReplication.md)