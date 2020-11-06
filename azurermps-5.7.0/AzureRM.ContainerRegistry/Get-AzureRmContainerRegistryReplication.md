---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/get-azurermcontainerregistrycredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Get-AzureRmContainerRegistryReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Get-AzureRmContainerRegistryReplication.md
ms.openlocfilehash: db03414e9cebe4c1593013a928b8a66d9b70bd91
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588967"
---
# <span data-ttu-id="6c71e-101">Get-AzureRmContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="6c71e-101">Get-AzureRmContainerRegistryReplication</span></span>

## <span data-ttu-id="6c71e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6c71e-102">SYNOPSIS</span></span>
<span data-ttu-id="6c71e-103">Kapsayıcı kayıt defterinin çoğaltmasını alır.</span><span class="sxs-lookup"><span data-stu-id="6c71e-103">Gets a replication of a container registry.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6c71e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6c71e-104">SYNTAX</span></span>

### <span data-ttu-id="6c71e-105">ListReplicationByNameResourceGroupParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="6c71e-105">ListReplicationByNameResourceGroupParameterSet (Default)</span></span>
```
Get-AzureRmContainerRegistryReplication [-ResourceGroupName] <String> [-RegistryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6c71e-106">ShowReplicationByNameResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="6c71e-106">ShowReplicationByNameResourceGroupParameterSet</span></span>
```
Get-AzureRmContainerRegistryReplication [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6c71e-107">ShowReplicationByRegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6c71e-107">ShowReplicationByRegistryObjectParameterSet</span></span>
```
Get-AzureRmContainerRegistryReplication [-Name] <String> -Registry <PSContainerRegistry>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6c71e-108">ListReplicationByRegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6c71e-108">ListReplicationByRegistryObjectParameterSet</span></span>
```
Get-AzureRmContainerRegistryReplication -Registry <PSContainerRegistry>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6c71e-109">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="6c71e-109">ResourceIdParameterSet</span></span>
```
Get-AzureRmContainerRegistryReplication -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6c71e-110">Tanım</span><span class="sxs-lookup"><span data-stu-id="6c71e-110">DESCRIPTION</span></span>
<span data-ttu-id="6c71e-111">Get-AzureRmContainerRegistryReplication cmdlet 'i, kapsayıcı kayıt defterinin belirli bir çoğaltmasını veya kapsayıcı kayıt defterinin tüm çoğaltmaları alır.</span><span class="sxs-lookup"><span data-stu-id="6c71e-111">The Get-AzureRmContainerRegistryReplication cmdlet gets a specified replication of a container registry or all the replications of a container registry.</span></span>

## <span data-ttu-id="6c71e-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6c71e-112">EXAMPLES</span></span>

### <span data-ttu-id="6c71e-113">Örnek 1: kapsayıcı kayıt defterinin belirtilen çoğaltmasını alma</span><span class="sxs-lookup"><span data-stu-id="6c71e-113">Example 1: Gets a specified replication of a container registry</span></span>
```powershell
PS C:\>Get-AzureRmContainerRegistryReplication -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "myreplication"

Name                 Location   Provisioni Status               StatusTimestamp                Tags
                                ngState
----                 --------   ---------- ------               ---------------                ----
myreplication       westus     Succeeded  Ready                 11/17/2017 10:19:45 PM         {[tagName, MyTag]}
```

<span data-ttu-id="6c71e-114">Kapsayıcı kayıt defterinin belirtilen çoğaltmasını alma</span><span class="sxs-lookup"><span data-stu-id="6c71e-114">Gets a specified replication of a container registry</span></span>

### <span data-ttu-id="6c71e-115">Örnek 2: kapsayıcı kayıt defterinin tüm çoğaltmaları alınır</span><span class="sxs-lookup"><span data-stu-id="6c71e-115">Example 2: Gets all the replications of a container registry</span></span>
```powershell
PS C:\>Get-AzureRmContainerRegistryReplication -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry"

Name                 Location   Provisioni Status               StatusTimestamp                Tags
                                ngState
----                 --------   ---------- ------               ---------------                ----
eastus               eastus     Succeeded  Ready                11/6/2017 6:14:47 PM           {}
myreplication        westus     Succeeded  Ready                11/17/2017 10:19:45 PM         {[tagName, MyTag]}
```

<span data-ttu-id="6c71e-116">Kapsayıcı kayıt defterinin tüm çoğaltmaları</span><span class="sxs-lookup"><span data-stu-id="6c71e-116">Gets all the replications of a container registry</span></span>

## <span data-ttu-id="6c71e-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6c71e-117">PARAMETERS</span></span>

### <span data-ttu-id="6c71e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c71e-118">-DefaultProfile</span></span>
<span data-ttu-id="6c71e-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6c71e-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c71e-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="6c71e-120">-Name</span></span>
<span data-ttu-id="6c71e-121">Kapsayıcı kayıt defteri çoğaltma adı.</span><span class="sxs-lookup"><span data-stu-id="6c71e-121">Container Registry Replication Name.</span></span>

```yaml
Type: String
Parameter Sets: ShowReplicationByNameResourceGroupParameterSet, ShowReplicationByRegistryObjectParameterSet
Aliases: ReplicationName, ResourceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c71e-122">-Registry</span><span class="sxs-lookup"><span data-stu-id="6c71e-122">-Registry</span></span>
<span data-ttu-id="6c71e-123">Kapsayıcısı.</span><span class="sxs-lookup"><span data-stu-id="6c71e-123">Container Registry Object.</span></span>

```yaml
Type: PSContainerRegistry
Parameter Sets: ShowReplicationByRegistryObjectParameterSet, ListReplicationByRegistryObjectParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6c71e-124">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="6c71e-124">-RegistryName</span></span>
<span data-ttu-id="6c71e-125">Kapsayıcı kayıt defteri adı.</span><span class="sxs-lookup"><span data-stu-id="6c71e-125">Container Registry Name.</span></span>

```yaml
Type: String
Parameter Sets: ListReplicationByNameResourceGroupParameterSet, ShowReplicationByNameResourceGroupParameterSet
Aliases: ContainerRegistryName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c71e-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6c71e-126">-ResourceGroupName</span></span>
<span data-ttu-id="6c71e-127">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="6c71e-127">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: ListReplicationByNameResourceGroupParameterSet, ShowReplicationByNameResourceGroupParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c71e-128">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="6c71e-128">-ResourceId</span></span>
<span data-ttu-id="6c71e-129">Kapsayıcı kayıt defteri çoğaltma kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="6c71e-129">The container registry replication resource id</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c71e-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c71e-130">CommonParameters</span></span>
<span data-ttu-id="6c71e-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6c71e-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c71e-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6c71e-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c71e-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6c71e-133">INPUTS</span></span>

### <span data-ttu-id="6c71e-134">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="6c71e-134">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>
<span data-ttu-id="6c71e-135">System. String</span><span class="sxs-lookup"><span data-stu-id="6c71e-135">System.String</span></span>

## <span data-ttu-id="6c71e-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6c71e-136">OUTPUTS</span></span>

### <span data-ttu-id="6c71e-137">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="6c71e-137">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication</span></span>
<span data-ttu-id="6c71e-138">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryReplication []</span><span class="sxs-lookup"><span data-stu-id="6c71e-138">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication[]</span></span>

## <span data-ttu-id="6c71e-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6c71e-139">NOTES</span></span>

## <span data-ttu-id="6c71e-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6c71e-140">RELATED LINKS</span></span>

[<span data-ttu-id="6c71e-141">Yeni-AzureRmContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="6c71e-141">New-AzureRmContainerRegistryReplication</span></span>](New-AzureRmContainerRegistryReplication.md)

[<span data-ttu-id="6c71e-142">Remove-AzureRmContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="6c71e-142">Remove-AzureRmContainerRegistryReplication</span></span>](Remove-AzureRmContainerRegistryReplication.md)
