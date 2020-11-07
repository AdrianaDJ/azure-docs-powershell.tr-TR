---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/new-azurermcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/New-AzureRmContainerRegistryReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/New-AzureRmContainerRegistryReplication.md
ms.openlocfilehash: 31170e24e88f6ce25c9fd344d254189eeeae64f0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762744"
---
# <span data-ttu-id="b16ff-101">New-AzureRmContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="b16ff-101">New-AzureRmContainerRegistryReplication</span></span>

## <span data-ttu-id="b16ff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b16ff-102">SYNOPSIS</span></span>
<span data-ttu-id="b16ff-103">Kapsayıcı kayıt defteri çoğaltması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b16ff-103">Creates a container registry replication.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b16ff-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b16ff-104">SYNTAX</span></span>

### <span data-ttu-id="b16ff-105">NameResourceGroupParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="b16ff-105">NameResourceGroupParameterSet (Default)</span></span>
```
New-AzureRmContainerRegistryReplication [-ResourceGroupName] <String> [-RegistryName] <String>
 -Location <String> [-Name <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b16ff-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b16ff-106">RegistryObjectParameterSet</span></span>
```
New-AzureRmContainerRegistryReplication -Registry <PSContainerRegistry> -Location <String> [-Name <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b16ff-107">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="b16ff-107">ResourceIdParameterSet</span></span>
```
New-AzureRmContainerRegistryReplication -Location <String> [-Name <String>] [-Tag <Hashtable>]
 -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b16ff-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="b16ff-108">DESCRIPTION</span></span>
<span data-ttu-id="b16ff-109">New-AzureRmContainerRegistryReplication cmdlet 'i yeni bir kapsayıcı kayıt defteri çoğaltması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b16ff-109">The New-AzureRmContainerRegistryReplication cmdlet creates a new container registry replication.</span></span>

## <span data-ttu-id="b16ff-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b16ff-110">EXAMPLES</span></span>

### <span data-ttu-id="b16ff-111">Örnek 1: yeni bir kapsayıcı kayıt defteri çoğaltması oluşturun.</span><span class="sxs-lookup"><span data-stu-id="b16ff-111">Example 1: Create a new container registry replication.</span></span>
```powershell
PS C:\>New-AzureRmContainerRegistryReplication -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name replication001 -Location 'west us' -Tag @{tagName='MyTag'}

Name                 Location   Provisioni Status               StatusTimestamp                Tags
                                ngState
----                 --------   ---------- ------               ---------------                ----
replication001       westus     Succeeded  Ready                11/17/2017 10:19:45 PM         {[tagName, MyTag]}
```

<span data-ttu-id="b16ff-112">Yeni kapsayıcı kayıt defteri çoğaltması oluşturun.</span><span class="sxs-lookup"><span data-stu-id="b16ff-112">Create a new container registry replication.</span></span>

## <span data-ttu-id="b16ff-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b16ff-113">PARAMETERS</span></span>

### <span data-ttu-id="b16ff-114">-Onay</span><span class="sxs-lookup"><span data-stu-id="b16ff-114">-Confirm</span></span>
<span data-ttu-id="b16ff-115">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b16ff-115">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b16ff-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b16ff-116">-DefaultProfile</span></span>
<span data-ttu-id="b16ff-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b16ff-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b16ff-118">-Konum</span><span class="sxs-lookup"><span data-stu-id="b16ff-118">-Location</span></span>
<span data-ttu-id="b16ff-119">Kapsayıcı kayıt defteri konumu.</span><span class="sxs-lookup"><span data-stu-id="b16ff-119">Container Registry Location.</span></span>
<span data-ttu-id="b16ff-120">Kaynak grubunun konumu.</span><span class="sxs-lookup"><span data-stu-id="b16ff-120">Default to the location of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ReplicationLocation

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b16ff-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="b16ff-121">-Name</span></span>
<span data-ttu-id="b16ff-122">Kapsayıcı kayıt defteri çoğaltma adı.</span><span class="sxs-lookup"><span data-stu-id="b16ff-122">Container Registry Replication Name.</span></span>
<span data-ttu-id="b16ff-123">Varsayılan konum adı.</span><span class="sxs-lookup"><span data-stu-id="b16ff-123">Default to the location name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ReplicationName, ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b16ff-124">-Registry</span><span class="sxs-lookup"><span data-stu-id="b16ff-124">-Registry</span></span>
<span data-ttu-id="b16ff-125">Kapsayıcısı.</span><span class="sxs-lookup"><span data-stu-id="b16ff-125">Container Registry Object.</span></span>

```yaml
Type: PSContainerRegistry
Parameter Sets: RegistryObjectParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b16ff-126">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="b16ff-126">-RegistryName</span></span>
<span data-ttu-id="b16ff-127">Kapsayıcı kayıt defteri adı.</span><span class="sxs-lookup"><span data-stu-id="b16ff-127">Container Registry Name.</span></span>

```yaml
Type: String
Parameter Sets: NameResourceGroupParameterSet
Aliases: ContainerRegistryName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b16ff-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b16ff-128">-ResourceGroupName</span></span>
<span data-ttu-id="b16ff-129">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="b16ff-129">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: NameResourceGroupParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b16ff-130">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="b16ff-130">-ResourceId</span></span>
<span data-ttu-id="b16ff-131">Kapsayıcı kayıt defteri kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="b16ff-131">The container registry resource id</span></span>

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

### <span data-ttu-id="b16ff-132">Etiketli</span><span class="sxs-lookup"><span data-stu-id="b16ff-132">-Tag</span></span>
<span data-ttu-id="b16ff-133">Kapsayıcı kayıt defteri etiketleri.</span><span class="sxs-lookup"><span data-stu-id="b16ff-133">Container Registry Tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b16ff-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b16ff-134">-WhatIf</span></span>
<span data-ttu-id="b16ff-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b16ff-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b16ff-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b16ff-136">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b16ff-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b16ff-137">CommonParameters</span></span>
<span data-ttu-id="b16ff-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b16ff-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b16ff-139">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b16ff-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b16ff-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b16ff-140">INPUTS</span></span>

### <span data-ttu-id="b16ff-141">System. String</span><span class="sxs-lookup"><span data-stu-id="b16ff-141">System.String</span></span>

## <span data-ttu-id="b16ff-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b16ff-142">OUTPUTS</span></span>

### <span data-ttu-id="b16ff-143">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="b16ff-143">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication</span></span>

## <span data-ttu-id="b16ff-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b16ff-144">NOTES</span></span>

## <span data-ttu-id="b16ff-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b16ff-145">RELATED LINKS</span></span>

[<span data-ttu-id="b16ff-146">Get-AzureRmContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="b16ff-146">Get-AzureRmContainerRegistryReplication</span></span>](New-AzureRmContainerRegistryReplication.md)

[<span data-ttu-id="b16ff-147">Remove-AzureRmContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="b16ff-147">Remove-AzureRmContainerRegistryReplication</span></span>](Remove-AzureRmContainerRegistryReplication.md)
