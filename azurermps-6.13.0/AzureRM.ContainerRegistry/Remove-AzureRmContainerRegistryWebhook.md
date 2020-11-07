---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/remove-azurermcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Remove-AzureRmContainerRegistryWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Remove-AzureRmContainerRegistryWebhook.md
ms.openlocfilehash: c1ba245f83db386e39f9fecf22f95d3681452d7a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764155"
---
# <span data-ttu-id="fb2d7-101">Remove-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="fb2d7-101">Remove-AzureRmContainerRegistryWebhook</span></span>

## <span data-ttu-id="fb2d7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fb2d7-102">SYNOPSIS</span></span>
<span data-ttu-id="fb2d7-103">Kapsayıcı kayıt defteri Web kancasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="fb2d7-103">Removes a container registry webhook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fb2d7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fb2d7-104">SYNTAX</span></span>

### <span data-ttu-id="fb2d7-105">NameResourceGroupParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="fb2d7-105">NameResourceGroupParameterSet (Default)</span></span>
```
Remove-AzureRmContainerRegistryWebhook [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fb2d7-106">WebhookObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fb2d7-106">WebhookObjectParameterSet</span></span>
```
Remove-AzureRmContainerRegistryWebhook -Webhook <PSContainerRegistryWebhook> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fb2d7-107">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="fb2d7-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmContainerRegistryWebhook -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fb2d7-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="fb2d7-108">DESCRIPTION</span></span>
<span data-ttu-id="fb2d7-109">Remove-AzureRmContainerRegistryWebhook cmdlet 'i, kapsayıcı kayıt defteri Web kancasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="fb2d7-109">The Remove-AzureRmContainerRegistryWebhook cmdlet removes a container registry webhook.</span></span>

## <span data-ttu-id="fb2d7-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fb2d7-110">EXAMPLES</span></span>

### <span data-ttu-id="fb2d7-111">Örnek 1: kapsayıcı kayıt defteri Web kancasını kaldırın.</span><span class="sxs-lookup"><span data-stu-id="fb2d7-111">Example 1: Remove a container registry webhook.</span></span>
```powershell
PS C:\> Remove-AzureRmContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001"
```

<span data-ttu-id="fb2d7-112">Kapsayıcı kayıt defteri Web kancasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="fb2d7-112">Removes a container registry webhook.</span></span>

## <span data-ttu-id="fb2d7-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fb2d7-113">PARAMETERS</span></span>

### <span data-ttu-id="fb2d7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb2d7-114">-DefaultProfile</span></span>
<span data-ttu-id="fb2d7-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="fb2d7-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fb2d7-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="fb2d7-116">-Name</span></span>
<span data-ttu-id="fb2d7-117">Web kancası adı.</span><span class="sxs-lookup"><span data-stu-id="fb2d7-117">Webhook Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases: WebhookName, ResourceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb2d7-118">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="fb2d7-118">-PassThru</span></span>
<span data-ttu-id="fb2d7-119">Kaldırma işlemi başarılıysa bu cmdlet 'in doğru döndüğü anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="fb2d7-119">Indicates that this cmdlet returns true if the removal was successful.</span></span>

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

### <span data-ttu-id="fb2d7-120">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="fb2d7-120">-RegistryName</span></span>
<span data-ttu-id="fb2d7-121">Kapsayıcı kayıt defteri adı.</span><span class="sxs-lookup"><span data-stu-id="fb2d7-121">Container Registry Name.</span></span>

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

### <span data-ttu-id="fb2d7-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb2d7-122">-ResourceGroupName</span></span>
<span data-ttu-id="fb2d7-123">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="fb2d7-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="fb2d7-124">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="fb2d7-124">-ResourceId</span></span>
<span data-ttu-id="fb2d7-125">Kapsayıcı kayıt defteri Web kancası kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="fb2d7-125">The container registry Webhook resource id</span></span>

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

### <span data-ttu-id="fb2d7-126">-Web kancası</span><span class="sxs-lookup"><span data-stu-id="fb2d7-126">-Webhook</span></span>
<span data-ttu-id="fb2d7-127">Kapsayıcısı.</span><span class="sxs-lookup"><span data-stu-id="fb2d7-127">Container Registry Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook
Parameter Sets: WebhookObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fb2d7-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="fb2d7-128">-Confirm</span></span>
<span data-ttu-id="fb2d7-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="fb2d7-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fb2d7-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb2d7-130">-WhatIf</span></span>
<span data-ttu-id="fb2d7-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="fb2d7-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fb2d7-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="fb2d7-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fb2d7-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb2d7-133">CommonParameters</span></span>
<span data-ttu-id="fb2d7-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fb2d7-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb2d7-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb2d7-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb2d7-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fb2d7-136">INPUTS</span></span>

### <span data-ttu-id="fb2d7-137">Microsoft. Azure. Commands. ContainerRegistry. Pscontainerregistryweb kancası</span><span class="sxs-lookup"><span data-stu-id="fb2d7-137">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>
<span data-ttu-id="fb2d7-138">Parametreler: Web kancası (ByValue)</span><span class="sxs-lookup"><span data-stu-id="fb2d7-138">Parameters: Webhook (ByValue)</span></span>

### <span data-ttu-id="fb2d7-139">System. String</span><span class="sxs-lookup"><span data-stu-id="fb2d7-139">System.String</span></span>

## <span data-ttu-id="fb2d7-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fb2d7-140">OUTPUTS</span></span>

### <span data-ttu-id="fb2d7-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="fb2d7-141">System.Boolean</span></span>

## <span data-ttu-id="fb2d7-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fb2d7-142">NOTES</span></span>

## <span data-ttu-id="fb2d7-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fb2d7-143">RELATED LINKS</span></span>

[<span data-ttu-id="fb2d7-144">Yeni-Azurermcontainerregistryweb kancası</span><span class="sxs-lookup"><span data-stu-id="fb2d7-144">New-AzureRmContainerRegistryWebhook</span></span>](New-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="fb2d7-145">Get-Azurermcontainerregistryweb kancası</span><span class="sxs-lookup"><span data-stu-id="fb2d7-145">Get-AzureRmContainerRegistryWebhook</span></span>](Get-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="fb2d7-146">Update-Azurermcontainerregistryweb kancası</span><span class="sxs-lookup"><span data-stu-id="fb2d7-146">Update-AzureRmContainerRegistryWebhook</span></span>](Update-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="fb2d7-147">Test-Azurermcontainerregistryweb kancası</span><span class="sxs-lookup"><span data-stu-id="fb2d7-147">Test-AzureRmContainerRegistryWebhook</span></span>](Test-AzureRmContainerRegistryWebhook.md)
