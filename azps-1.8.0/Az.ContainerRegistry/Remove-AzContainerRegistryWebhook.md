---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/remove-azcontainerregistrywebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryWebhook.md
ms.openlocfilehash: 1c96b33fd93082c33dfb49abdf23fac8795b2b28
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93761177"
---
# <span data-ttu-id="b4bac-101">Remove-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="b4bac-101">Remove-AzContainerRegistryWebhook</span></span>

## <span data-ttu-id="b4bac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b4bac-102">SYNOPSIS</span></span>
<span data-ttu-id="b4bac-103">Kapsayıcı kayıt defteri Web kancasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="b4bac-103">Removes a container registry webhook.</span></span>

## <span data-ttu-id="b4bac-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b4bac-104">SYNTAX</span></span>

### <span data-ttu-id="b4bac-105">NameResourceGroupParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="b4bac-105">NameResourceGroupParameterSet (Default)</span></span>
```
Remove-AzContainerRegistryWebhook [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4bac-106">WebhookObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b4bac-106">WebhookObjectParameterSet</span></span>
```
Remove-AzContainerRegistryWebhook -Webhook <PSContainerRegistryWebhook> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4bac-107">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="b4bac-107">ResourceIdParameterSet</span></span>
```
Remove-AzContainerRegistryWebhook -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b4bac-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="b4bac-108">DESCRIPTION</span></span>
<span data-ttu-id="b4bac-109">Remove-AzContainerRegistryWebhook cmdlet 'i, kapsayıcı kayıt defteri Web kancasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="b4bac-109">The Remove-AzContainerRegistryWebhook cmdlet removes a container registry webhook.</span></span>

## <span data-ttu-id="b4bac-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b4bac-110">EXAMPLES</span></span>

### <span data-ttu-id="b4bac-111">Örnek 1: kapsayıcı kayıt defteri Web kancasını kaldırın.</span><span class="sxs-lookup"><span data-stu-id="b4bac-111">Example 1: Remove a container registry webhook.</span></span>
```powershell
PS C:\> Remove-AzContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001"
```

<span data-ttu-id="b4bac-112">Kapsayıcı kayıt defteri Web kancasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="b4bac-112">Removes a container registry webhook.</span></span>

## <span data-ttu-id="b4bac-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b4bac-113">PARAMETERS</span></span>

### <span data-ttu-id="b4bac-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4bac-114">-DefaultProfile</span></span>
<span data-ttu-id="b4bac-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b4bac-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b4bac-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="b4bac-116">-Name</span></span>
<span data-ttu-id="b4bac-117">Web kancası adı.</span><span class="sxs-lookup"><span data-stu-id="b4bac-117">Webhook Name.</span></span>

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

### <span data-ttu-id="b4bac-118">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="b4bac-118">-PassThru</span></span>
<span data-ttu-id="b4bac-119">Kaldırma işlemi başarılıysa bu cmdlet 'in doğru döndüğü anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="b4bac-119">Indicates that this cmdlet returns true if the removal was successful.</span></span>

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

### <span data-ttu-id="b4bac-120">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="b4bac-120">-RegistryName</span></span>
<span data-ttu-id="b4bac-121">Kapsayıcı kayıt defteri adı.</span><span class="sxs-lookup"><span data-stu-id="b4bac-121">Container Registry Name.</span></span>

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

### <span data-ttu-id="b4bac-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4bac-122">-ResourceGroupName</span></span>
<span data-ttu-id="b4bac-123">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="b4bac-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="b4bac-124">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="b4bac-124">-ResourceId</span></span>
<span data-ttu-id="b4bac-125">Kapsayıcı kayıt defteri Web kancası kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="b4bac-125">The container registry Webhook resource id</span></span>

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

### <span data-ttu-id="b4bac-126">-Web kancası</span><span class="sxs-lookup"><span data-stu-id="b4bac-126">-Webhook</span></span>
<span data-ttu-id="b4bac-127">Kapsayıcısı.</span><span class="sxs-lookup"><span data-stu-id="b4bac-127">Container Registry Object.</span></span>

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

### <span data-ttu-id="b4bac-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="b4bac-128">-Confirm</span></span>
<span data-ttu-id="b4bac-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b4bac-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b4bac-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4bac-130">-WhatIf</span></span>
<span data-ttu-id="b4bac-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b4bac-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b4bac-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b4bac-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b4bac-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4bac-133">CommonParameters</span></span>
<span data-ttu-id="b4bac-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b4bac-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4bac-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4bac-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4bac-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b4bac-136">INPUTS</span></span>

### <span data-ttu-id="b4bac-137">Microsoft. Azure. Commands. ContainerRegistry. Pscontainerregistryweb kancası</span><span class="sxs-lookup"><span data-stu-id="b4bac-137">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>

### <span data-ttu-id="b4bac-138">System. String</span><span class="sxs-lookup"><span data-stu-id="b4bac-138">System.String</span></span>

## <span data-ttu-id="b4bac-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b4bac-139">OUTPUTS</span></span>

### <span data-ttu-id="b4bac-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b4bac-140">System.Boolean</span></span>

## <span data-ttu-id="b4bac-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b4bac-141">NOTES</span></span>

## <span data-ttu-id="b4bac-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b4bac-142">RELATED LINKS</span></span>

[<span data-ttu-id="b4bac-143">Yeni-Azcontainerregistryweb kancası</span><span class="sxs-lookup"><span data-stu-id="b4bac-143">New-AzContainerRegistryWebhook</span></span>](New-AzContainerRegistryWebhook.md)

[<span data-ttu-id="b4bac-144">Get-Azcontainerregistryweb kancası</span><span class="sxs-lookup"><span data-stu-id="b4bac-144">Get-AzContainerRegistryWebhook</span></span>](Get-AzContainerRegistryWebhook.md)

[<span data-ttu-id="b4bac-145">Update-Azcontainerregistryweb kancası</span><span class="sxs-lookup"><span data-stu-id="b4bac-145">Update-AzContainerRegistryWebhook</span></span>](Update-AzContainerRegistryWebhook.md)

[<span data-ttu-id="b4bac-146">Test-Azcontainerregistryweb kancası</span><span class="sxs-lookup"><span data-stu-id="b4bac-146">Test-AzContainerRegistryWebhook</span></span>](Test-AzContainerRegistryWebhook.md)