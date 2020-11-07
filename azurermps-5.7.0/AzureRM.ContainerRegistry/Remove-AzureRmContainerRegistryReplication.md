---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/remove-azurermcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Remove-AzureRmContainerRegistryReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Remove-AzureRmContainerRegistryReplication.md
ms.openlocfilehash: 824b3226b29ba381b9ed963bf6a21f4691c17733
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762740"
---
# <span data-ttu-id="1623f-101">Remove-AzureRmContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="1623f-101">Remove-AzureRmContainerRegistryReplication</span></span>

## <span data-ttu-id="1623f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1623f-102">SYNOPSIS</span></span>
<span data-ttu-id="1623f-103">Kapsayıcı kayıt defteri çoğaltmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="1623f-103">Removes a container registry replication.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1623f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1623f-104">SYNTAX</span></span>

### <span data-ttu-id="1623f-105">NameResourceGroupParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="1623f-105">NameResourceGroupParameterSet (Default)</span></span>
```
Remove-AzureRmContainerRegistryReplication [-Name] <String> [-ResourceGroupName] <String>
 [-RegistryName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1623f-106">ReplicationObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1623f-106">ReplicationObjectParameterSet</span></span>
```
Remove-AzureRmContainerRegistryReplication -Replicatoin <PSContainerRegistryReplication> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1623f-107">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="1623f-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmContainerRegistryReplication -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1623f-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="1623f-108">DESCRIPTION</span></span>
<span data-ttu-id="1623f-109">Remove-AzureRmContainerRegistryReplication cmdlet 'i kapsayıcı kayıt defteri çoğaltmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="1623f-109">The Remove-AzureRmContainerRegistryReplication cmdlet removes a container registry replication.</span></span>

## <span data-ttu-id="1623f-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1623f-110">EXAMPLES</span></span>

### <span data-ttu-id="1623f-111">Örnek 1: kapsayıcı kayıt defteri çoğaltmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="1623f-111">Example 1: Removes a container registry replication.</span></span>
```powershell
PS C:\> Remove-AzureRmContainerRegistryReplication -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "replication001"
```

<span data-ttu-id="1623f-112">Kapsayıcı kayıt defteri çoğaltmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="1623f-112">Removes a container registry replication.</span></span>

## <span data-ttu-id="1623f-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1623f-113">PARAMETERS</span></span>

### <span data-ttu-id="1623f-114">-Onay</span><span class="sxs-lookup"><span data-stu-id="1623f-114">-Confirm</span></span>
<span data-ttu-id="1623f-115">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="1623f-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1623f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1623f-116">-DefaultProfile</span></span>
<span data-ttu-id="1623f-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1623f-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1623f-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="1623f-118">-Name</span></span>
<span data-ttu-id="1623f-119">Kapsayıcı kayıt defteri çoğaltma adı.</span><span class="sxs-lookup"><span data-stu-id="1623f-119">Container Registry Replication Name.</span></span>
<span data-ttu-id="1623f-120">Varsayılan konum adı.</span><span class="sxs-lookup"><span data-stu-id="1623f-120">Default to the location name.</span></span>

```yaml
Type: String
Parameter Sets: NameResourceGroupParameterSet
Aliases: ReplicationName, ResourceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1623f-121">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="1623f-121">-RegistryName</span></span>
<span data-ttu-id="1623f-122">Kapsayıcı kayıt defteri adı.</span><span class="sxs-lookup"><span data-stu-id="1623f-122">Container Registry Name.</span></span>

```yaml
Type: String
Parameter Sets: NameResourceGroupParameterSet
Aliases: ContainerRegistryName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1623f-123">-Replicatoın</span><span class="sxs-lookup"><span data-stu-id="1623f-123">-Replicatoin</span></span>
<span data-ttu-id="1623f-124">Kapsayıcısı.</span><span class="sxs-lookup"><span data-stu-id="1623f-124">Container Registry Object.</span></span>

```yaml
Type: PSContainerRegistryReplication
Parameter Sets: ReplicationObjectParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1623f-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1623f-125">-ResourceGroupName</span></span>
<span data-ttu-id="1623f-126">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="1623f-126">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: NameResourceGroupParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1623f-127">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="1623f-127">-ResourceId</span></span>
<span data-ttu-id="1623f-128">Kapsayıcı kayıt defteri çoğaltma kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="1623f-128">The container registry replication resource id</span></span>

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

### <span data-ttu-id="1623f-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1623f-129">-WhatIf</span></span>
<span data-ttu-id="1623f-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="1623f-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1623f-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="1623f-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1623f-132">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="1623f-132">-PassThru</span></span>
<span data-ttu-id="1623f-133">Kaldırma işlemi başarılıysa bu cmdlet 'in doğru döndüğü anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="1623f-133">Indicates that this cmdlet returns true if the removal was successful.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1623f-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1623f-134">CommonParameters</span></span>
<span data-ttu-id="1623f-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1623f-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1623f-136">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1623f-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1623f-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1623f-137">INPUTS</span></span>

### <span data-ttu-id="1623f-138">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="1623f-138">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication</span></span>
<span data-ttu-id="1623f-139">System. String</span><span class="sxs-lookup"><span data-stu-id="1623f-139">System.String</span></span>

## <span data-ttu-id="1623f-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1623f-140">OUTPUTS</span></span>

### <span data-ttu-id="1623f-141">System. Object</span><span class="sxs-lookup"><span data-stu-id="1623f-141">System.Object</span></span>

## <span data-ttu-id="1623f-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1623f-142">NOTES</span></span>

## <span data-ttu-id="1623f-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1623f-143">RELATED LINKS</span></span>

[<span data-ttu-id="1623f-144">Yeni-AzureRmContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="1623f-144">New-AzureRmContainerRegistryReplication</span></span>](New-AzureRmContainerRegistryReplication.md)

[<span data-ttu-id="1623f-145">Get-AzureRmContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="1623f-145">Get-AzureRmContainerRegistryReplication</span></span>](Remove-AzureRmContainerRegistryReplication.md)

