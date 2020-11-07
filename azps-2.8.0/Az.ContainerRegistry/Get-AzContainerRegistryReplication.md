---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/get-azcontainerregistryreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryReplication.md
ms.openlocfilehash: 0a4844a3ed1bdc48f741215ae91ee075425cd68a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93752611"
---
# <span data-ttu-id="f1fe1-101">Get-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="f1fe1-101">Get-AzContainerRegistryReplication</span></span>

## <span data-ttu-id="f1fe1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f1fe1-102">SYNOPSIS</span></span>
<span data-ttu-id="f1fe1-103">Kapsayıcı kayıt defterinin çoğaltmasını alır.</span><span class="sxs-lookup"><span data-stu-id="f1fe1-103">Gets a replication of a container registry.</span></span>

## <span data-ttu-id="f1fe1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f1fe1-104">SYNTAX</span></span>

### <span data-ttu-id="f1fe1-105">ListReplicationByNameResourceGroupParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="f1fe1-105">ListReplicationByNameResourceGroupParameterSet (Default)</span></span>
```
Get-AzContainerRegistryReplication [-ResourceGroupName] <String> [-RegistryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f1fe1-106">ShowReplicationByNameResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="f1fe1-106">ShowReplicationByNameResourceGroupParameterSet</span></span>
```
Get-AzContainerRegistryReplication [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f1fe1-107">ShowReplicationByRegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f1fe1-107">ShowReplicationByRegistryObjectParameterSet</span></span>
```
Get-AzContainerRegistryReplication [-Name] <String> -Registry <PSContainerRegistry>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f1fe1-108">ListReplicationByRegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f1fe1-108">ListReplicationByRegistryObjectParameterSet</span></span>
```
Get-AzContainerRegistryReplication -Registry <PSContainerRegistry> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f1fe1-109">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="f1fe1-109">ResourceIdParameterSet</span></span>
```
Get-AzContainerRegistryReplication -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f1fe1-110">Tanım</span><span class="sxs-lookup"><span data-stu-id="f1fe1-110">DESCRIPTION</span></span>
<span data-ttu-id="f1fe1-111">Get-AzContainerRegistryReplication cmdlet 'i, kapsayıcı kayıt defterinin belirli bir çoğaltmasını veya kapsayıcı kayıt defterinin tüm çoğaltmaları alır.</span><span class="sxs-lookup"><span data-stu-id="f1fe1-111">The Get-AzContainerRegistryReplication cmdlet gets a specified replication of a container registry or all the replications of a container registry.</span></span>

## <span data-ttu-id="f1fe1-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f1fe1-112">EXAMPLES</span></span>

### <span data-ttu-id="f1fe1-113">Örnek 1: kapsayıcı kayıt defterinin belirtilen çoğaltmasını alma</span><span class="sxs-lookup"><span data-stu-id="f1fe1-113">Example 1: Gets a specified replication of a container registry</span></span>
```powershell
PS C:\>Get-AzContainerRegistryReplication -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "myreplication"

Name                 Location   Provisioni Status               StatusTimestamp                Tags
                                ngState
----                 --------   ---------- ------               ---------------                ----
myreplication       westus     Succeeded  Ready                 11/17/2017 10:19:45 PM         {[tagName, MyTag]}
```

<span data-ttu-id="f1fe1-114">Kapsayıcı kayıt defterinin belirtilen çoğaltmasını alma</span><span class="sxs-lookup"><span data-stu-id="f1fe1-114">Gets a specified replication of a container registry</span></span>

### <span data-ttu-id="f1fe1-115">Örnek 2: kapsayıcı kayıt defterinin tüm çoğaltmaları alınır</span><span class="sxs-lookup"><span data-stu-id="f1fe1-115">Example 2: Gets all the replications of a container registry</span></span>
```powershell
PS C:\>Get-AzContainerRegistryReplication -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry"

Name                 Location   Provisioni Status               StatusTimestamp                Tags
                                ngState
----                 --------   ---------- ------               ---------------                ----
eastus               eastus     Succeeded  Ready                11/6/2017 6:14:47 PM           {}
myreplication        westus     Succeeded  Ready                11/17/2017 10:19:45 PM         {[tagName, MyTag]}
```

<span data-ttu-id="f1fe1-116">Kapsayıcı kayıt defterinin tüm çoğaltmaları</span><span class="sxs-lookup"><span data-stu-id="f1fe1-116">Gets all the replications of a container registry</span></span>

## <span data-ttu-id="f1fe1-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f1fe1-117">PARAMETERS</span></span>

### <span data-ttu-id="f1fe1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1fe1-118">-DefaultProfile</span></span>
<span data-ttu-id="f1fe1-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f1fe1-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f1fe1-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="f1fe1-120">-Name</span></span>
<span data-ttu-id="f1fe1-121">Kapsayıcı kayıt defteri çoğaltma adı.</span><span class="sxs-lookup"><span data-stu-id="f1fe1-121">Container Registry Replication Name.</span></span>

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

### <span data-ttu-id="f1fe1-122">-Registry</span><span class="sxs-lookup"><span data-stu-id="f1fe1-122">-Registry</span></span>
<span data-ttu-id="f1fe1-123">Kapsayıcısı.</span><span class="sxs-lookup"><span data-stu-id="f1fe1-123">Container Registry Object.</span></span>

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

### <span data-ttu-id="f1fe1-124">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="f1fe1-124">-RegistryName</span></span>
<span data-ttu-id="f1fe1-125">Kapsayıcı kayıt defteri adı.</span><span class="sxs-lookup"><span data-stu-id="f1fe1-125">Container Registry Name.</span></span>

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

### <span data-ttu-id="f1fe1-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1fe1-126">-ResourceGroupName</span></span>
<span data-ttu-id="f1fe1-127">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="f1fe1-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="f1fe1-128">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="f1fe1-128">-ResourceId</span></span>
<span data-ttu-id="f1fe1-129">Kapsayıcı kayıt defteri çoğaltma kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="f1fe1-129">The container registry replication resource id</span></span>

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

### <span data-ttu-id="f1fe1-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1fe1-130">CommonParameters</span></span>
<span data-ttu-id="f1fe1-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f1fe1-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1fe1-132">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="f1fe1-132">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1fe1-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f1fe1-133">INPUTS</span></span>

### <span data-ttu-id="f1fe1-134">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="f1fe1-134">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

### <span data-ttu-id="f1fe1-135">System. String</span><span class="sxs-lookup"><span data-stu-id="f1fe1-135">System.String</span></span>

## <span data-ttu-id="f1fe1-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f1fe1-136">OUTPUTS</span></span>

### <span data-ttu-id="f1fe1-137">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="f1fe1-137">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication</span></span>

## <span data-ttu-id="f1fe1-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f1fe1-138">NOTES</span></span>

## <span data-ttu-id="f1fe1-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f1fe1-139">RELATED LINKS</span></span>

[<span data-ttu-id="f1fe1-140">Yeni-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="f1fe1-140">New-AzContainerRegistryReplication</span></span>](New-AzContainerRegistryReplication.md)

[<span data-ttu-id="f1fe1-141">Remove-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="f1fe1-141">Remove-AzContainerRegistryReplication</span></span>](Remove-AzContainerRegistryReplication.md)