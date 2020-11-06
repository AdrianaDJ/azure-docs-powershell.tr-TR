---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/new-azurermcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/New-AzureRmContainerRegistryReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/New-AzureRmContainerRegistryReplication.md
ms.openlocfilehash: eaab02fe0e0adbd54bc80b15e6520442d9eb3c11
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93572853"
---
# <span data-ttu-id="ad7cf-101">New-AzureRmContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="ad7cf-101">New-AzureRmContainerRegistryReplication</span></span>

## <span data-ttu-id="ad7cf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ad7cf-102">SYNOPSIS</span></span>
<span data-ttu-id="ad7cf-103">Kapsayıcı kayıt defteri çoğaltması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ad7cf-103">Creates a container registry replication.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ad7cf-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ad7cf-104">SYNTAX</span></span>

### <span data-ttu-id="ad7cf-105">NameResourceGroupParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="ad7cf-105">NameResourceGroupParameterSet (Default)</span></span>
```
New-AzureRmContainerRegistryReplication [-ResourceGroupName] <String> [-RegistryName] <String>
 -Location <String> [-Name <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ad7cf-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ad7cf-106">RegistryObjectParameterSet</span></span>
```
New-AzureRmContainerRegistryReplication -Registry <PSContainerRegistry> -Location <String> [-Name <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ad7cf-107">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="ad7cf-107">ResourceIdParameterSet</span></span>
```
New-AzureRmContainerRegistryReplication -Location <String> [-Name <String>] [-Tag <Hashtable>]
 -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ad7cf-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="ad7cf-108">DESCRIPTION</span></span>
<span data-ttu-id="ad7cf-109">New-AzureRmContainerRegistryReplication cmdlet 'i yeni bir kapsayıcı kayıt defteri çoğaltması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ad7cf-109">The New-AzureRmContainerRegistryReplication cmdlet creates a new container registry replication.</span></span>

## <span data-ttu-id="ad7cf-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ad7cf-110">EXAMPLES</span></span>

### <span data-ttu-id="ad7cf-111">Örnek 1: yeni bir kapsayıcı kayıt defteri çoğaltması oluşturun.</span><span class="sxs-lookup"><span data-stu-id="ad7cf-111">Example 1: Create a new container registry replication.</span></span>
```powershell
PS C:\>New-AzureRmContainerRegistryReplication -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name replication001 -Location 'west us' -Tag @{tagName='MyTag'}

Name                 Location   Provisioni Status               StatusTimestamp                Tags
                                ngState
----                 --------   ---------- ------               ---------------                ----
replication001       westus     Succeeded  Ready                11/17/2017 10:19:45 PM         {[tagName, MyTag]}
```

<span data-ttu-id="ad7cf-112">Yeni kapsayıcı kayıt defteri çoğaltması oluşturun.</span><span class="sxs-lookup"><span data-stu-id="ad7cf-112">Create a new container registry replication.</span></span>

## <span data-ttu-id="ad7cf-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ad7cf-113">PARAMETERS</span></span>

### <span data-ttu-id="ad7cf-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad7cf-114">-DefaultProfile</span></span>
<span data-ttu-id="ad7cf-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ad7cf-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ad7cf-116">-Konum</span><span class="sxs-lookup"><span data-stu-id="ad7cf-116">-Location</span></span>
<span data-ttu-id="ad7cf-117">Kapsayıcı kayıt defteri konumu.</span><span class="sxs-lookup"><span data-stu-id="ad7cf-117">Container Registry Location.</span></span>
<span data-ttu-id="ad7cf-118">Kaynak grubunun konumu.</span><span class="sxs-lookup"><span data-stu-id="ad7cf-118">Default to the location of the resource group.</span></span>

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

### <span data-ttu-id="ad7cf-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="ad7cf-119">-Name</span></span>
<span data-ttu-id="ad7cf-120">Kapsayıcı kayıt defteri çoğaltma adı.</span><span class="sxs-lookup"><span data-stu-id="ad7cf-120">Container Registry Replication Name.</span></span>
<span data-ttu-id="ad7cf-121">Varsayılan konum adı.</span><span class="sxs-lookup"><span data-stu-id="ad7cf-121">Default to the location name.</span></span>

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

### <span data-ttu-id="ad7cf-122">-Registry</span><span class="sxs-lookup"><span data-stu-id="ad7cf-122">-Registry</span></span>
<span data-ttu-id="ad7cf-123">Kapsayıcısı.</span><span class="sxs-lookup"><span data-stu-id="ad7cf-123">Container Registry Object.</span></span>

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

### <span data-ttu-id="ad7cf-124">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="ad7cf-124">-RegistryName</span></span>
<span data-ttu-id="ad7cf-125">Kapsayıcı kayıt defteri adı.</span><span class="sxs-lookup"><span data-stu-id="ad7cf-125">Container Registry Name.</span></span>

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

### <span data-ttu-id="ad7cf-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad7cf-126">-ResourceGroupName</span></span>
<span data-ttu-id="ad7cf-127">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="ad7cf-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="ad7cf-128">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="ad7cf-128">-ResourceId</span></span>
<span data-ttu-id="ad7cf-129">Kapsayıcı kayıt defteri kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="ad7cf-129">The container registry resource id</span></span>

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

### <span data-ttu-id="ad7cf-130">Etiketli</span><span class="sxs-lookup"><span data-stu-id="ad7cf-130">-Tag</span></span>
<span data-ttu-id="ad7cf-131">Kapsayıcı kayıt defteri etiketleri.</span><span class="sxs-lookup"><span data-stu-id="ad7cf-131">Container Registry Tags.</span></span>

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

### <span data-ttu-id="ad7cf-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="ad7cf-132">-Confirm</span></span>
<span data-ttu-id="ad7cf-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ad7cf-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ad7cf-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad7cf-134">-WhatIf</span></span>
<span data-ttu-id="ad7cf-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ad7cf-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ad7cf-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ad7cf-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ad7cf-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad7cf-137">CommonParameters</span></span>
<span data-ttu-id="ad7cf-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ad7cf-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad7cf-139">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad7cf-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad7cf-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ad7cf-140">INPUTS</span></span>

### <span data-ttu-id="ad7cf-141">System. String</span><span class="sxs-lookup"><span data-stu-id="ad7cf-141">System.String</span></span>

## <span data-ttu-id="ad7cf-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ad7cf-142">OUTPUTS</span></span>

### <span data-ttu-id="ad7cf-143">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="ad7cf-143">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication</span></span>

## <span data-ttu-id="ad7cf-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ad7cf-144">NOTES</span></span>

## <span data-ttu-id="ad7cf-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ad7cf-145">RELATED LINKS</span></span>

[<span data-ttu-id="ad7cf-146">Get-AzureRmContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="ad7cf-146">Get-AzureRmContainerRegistryReplication</span></span>](New-AzureRmContainerRegistryReplication.md)

[<span data-ttu-id="ad7cf-147">Remove-AzureRmContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="ad7cf-147">Remove-AzureRmContainerRegistryReplication</span></span>](Remove-AzureRmContainerRegistryReplication.md)
