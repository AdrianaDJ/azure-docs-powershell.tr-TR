---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/remove-azcontainerregistrywebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryWebhook.md
ms.openlocfilehash: 4064728aeffb53fe9f6065d295455738b6a0f046
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94268866"
---
# <span data-ttu-id="83ace-101">Remove-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="83ace-101">Remove-AzContainerRegistryWebhook</span></span>

## <span data-ttu-id="83ace-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="83ace-102">SYNOPSIS</span></span>
<span data-ttu-id="83ace-103">Kapsayıcı kayıt defteri Web kancasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="83ace-103">Removes a container registry webhook.</span></span>

## <span data-ttu-id="83ace-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="83ace-104">SYNTAX</span></span>

### <span data-ttu-id="83ace-105">NameResourceGroupParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="83ace-105">NameResourceGroupParameterSet (Default)</span></span>
```
Remove-AzContainerRegistryWebhook [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="83ace-106">WebhookObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="83ace-106">WebhookObjectParameterSet</span></span>
```
Remove-AzContainerRegistryWebhook -Webhook <PSContainerRegistryWebhook> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="83ace-107">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="83ace-107">ResourceIdParameterSet</span></span>
```
Remove-AzContainerRegistryWebhook -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="83ace-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="83ace-108">DESCRIPTION</span></span>
<span data-ttu-id="83ace-109">Remove-AzContainerRegistryWebhook cmdlet 'i, kapsayıcı kayıt defteri Web kancasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="83ace-109">The Remove-AzContainerRegistryWebhook cmdlet removes a container registry webhook.</span></span>

## <span data-ttu-id="83ace-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="83ace-110">EXAMPLES</span></span>

### <span data-ttu-id="83ace-111">Örnek 1: kapsayıcı kayıt defteri Web kancasını kaldırın.</span><span class="sxs-lookup"><span data-stu-id="83ace-111">Example 1: Remove a container registry webhook.</span></span>
```powershell
PS C:\> Remove-AzContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001"
```

<span data-ttu-id="83ace-112">Kapsayıcı kayıt defteri Web kancasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="83ace-112">Removes a container registry webhook.</span></span>

## <span data-ttu-id="83ace-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="83ace-113">PARAMETERS</span></span>

### <span data-ttu-id="83ace-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83ace-114">-DefaultProfile</span></span>
<span data-ttu-id="83ace-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="83ace-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="83ace-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="83ace-116">-Name</span></span>
<span data-ttu-id="83ace-117">Web kancası adı.</span><span class="sxs-lookup"><span data-stu-id="83ace-117">Webhook Name.</span></span>

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

### <span data-ttu-id="83ace-118">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="83ace-118">-PassThru</span></span>
<span data-ttu-id="83ace-119">Kaldırma işlemi başarılıysa bu cmdlet 'in doğru döndüğü anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="83ace-119">Indicates that this cmdlet returns true if the removal was successful.</span></span>

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

### <span data-ttu-id="83ace-120">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="83ace-120">-RegistryName</span></span>
<span data-ttu-id="83ace-121">Kapsayıcı kayıt defteri adı.</span><span class="sxs-lookup"><span data-stu-id="83ace-121">Container Registry Name.</span></span>

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

### <span data-ttu-id="83ace-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="83ace-122">-ResourceGroupName</span></span>
<span data-ttu-id="83ace-123">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="83ace-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="83ace-124">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="83ace-124">-ResourceId</span></span>
<span data-ttu-id="83ace-125">Kapsayıcı kayıt defteri Web kancası kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="83ace-125">The container registry Webhook resource id</span></span>

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

### <span data-ttu-id="83ace-126">-Web kancası</span><span class="sxs-lookup"><span data-stu-id="83ace-126">-Webhook</span></span>
<span data-ttu-id="83ace-127">Kapsayıcısı.</span><span class="sxs-lookup"><span data-stu-id="83ace-127">Container Registry Object.</span></span>

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

### <span data-ttu-id="83ace-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="83ace-128">-Confirm</span></span>
<span data-ttu-id="83ace-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="83ace-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="83ace-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="83ace-130">-WhatIf</span></span>
<span data-ttu-id="83ace-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="83ace-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="83ace-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="83ace-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="83ace-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83ace-133">CommonParameters</span></span>
<span data-ttu-id="83ace-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="83ace-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83ace-135">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="83ace-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83ace-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="83ace-136">INPUTS</span></span>

### <span data-ttu-id="83ace-137">Microsoft. Azure. Commands. ContainerRegistry. Pscontainerregistryweb kancası</span><span class="sxs-lookup"><span data-stu-id="83ace-137">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>

### <span data-ttu-id="83ace-138">System. String</span><span class="sxs-lookup"><span data-stu-id="83ace-138">System.String</span></span>

## <span data-ttu-id="83ace-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="83ace-139">OUTPUTS</span></span>

### <span data-ttu-id="83ace-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="83ace-140">System.Boolean</span></span>

## <span data-ttu-id="83ace-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="83ace-141">NOTES</span></span>

## <span data-ttu-id="83ace-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="83ace-142">RELATED LINKS</span></span>

[<span data-ttu-id="83ace-143">Yeni-Azcontainerregistryweb kancası</span><span class="sxs-lookup"><span data-stu-id="83ace-143">New-AzContainerRegistryWebhook</span></span>](New-AzContainerRegistryWebhook.md)

[<span data-ttu-id="83ace-144">Get-Azcontainerregistryweb kancası</span><span class="sxs-lookup"><span data-stu-id="83ace-144">Get-AzContainerRegistryWebhook</span></span>](Get-AzContainerRegistryWebhook.md)

[<span data-ttu-id="83ace-145">Update-Azcontainerregistryweb kancası</span><span class="sxs-lookup"><span data-stu-id="83ace-145">Update-AzContainerRegistryWebhook</span></span>](Update-AzContainerRegistryWebhook.md)

[<span data-ttu-id="83ace-146">Test-Azcontainerregistryweb kancası</span><span class="sxs-lookup"><span data-stu-id="83ace-146">Test-AzContainerRegistryWebhook</span></span>](Test-AzContainerRegistryWebhook.md)