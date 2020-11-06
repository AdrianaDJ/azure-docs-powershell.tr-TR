---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/remove-azurermcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Remove-AzureRmContainerRegistryWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Remove-AzureRmContainerRegistryWebhook.md
ms.openlocfilehash: 058c923528227e05a4c8b8078f4495c56edfe20c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587592"
---
# <span data-ttu-id="b66ae-101">Remove-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="b66ae-101">Remove-AzureRmContainerRegistryWebhook</span></span>

## <span data-ttu-id="b66ae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b66ae-102">SYNOPSIS</span></span>
<span data-ttu-id="b66ae-103">Kapsayıcı kayıt defteri Web kancasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="b66ae-103">Removes a container registry webhook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b66ae-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b66ae-104">SYNTAX</span></span>

### <span data-ttu-id="b66ae-105">NameResourceGroupParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="b66ae-105">NameResourceGroupParameterSet (Default)</span></span>
```
Remove-AzureRmContainerRegistryWebhook [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b66ae-106">WebhookObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b66ae-106">WebhookObjectParameterSet</span></span>
```
Remove-AzureRmContainerRegistryWebhook -Webhook <PSContainerRegistryWebhook> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b66ae-107">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="b66ae-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmContainerRegistryWebhook -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b66ae-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="b66ae-108">DESCRIPTION</span></span>
<span data-ttu-id="b66ae-109">Remove-AzureRmContainerRegistryWebhook cmdlet 'i, kapsayıcı kayıt defteri Web kancasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="b66ae-109">The Remove-AzureRmContainerRegistryWebhook cmdlet removes a container registry webhook.</span></span>

## <span data-ttu-id="b66ae-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b66ae-110">EXAMPLES</span></span>

### <span data-ttu-id="b66ae-111">Örnek 1: kapsayıcı kayıt defteri Web kancasını kaldırın.</span><span class="sxs-lookup"><span data-stu-id="b66ae-111">Example 1: Remove a container registry webhook.</span></span>
```powershell
PS C:\> Remove-AzureRmContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001"
```

<span data-ttu-id="b66ae-112">Kapsayıcı kayıt defteri Web kancasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="b66ae-112">Removes a container registry webhook.</span></span>

## <span data-ttu-id="b66ae-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b66ae-113">PARAMETERS</span></span>

### <span data-ttu-id="b66ae-114">-Onay</span><span class="sxs-lookup"><span data-stu-id="b66ae-114">-Confirm</span></span>
<span data-ttu-id="b66ae-115">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b66ae-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b66ae-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b66ae-116">-DefaultProfile</span></span>
<span data-ttu-id="b66ae-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b66ae-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b66ae-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="b66ae-118">-Name</span></span>
<span data-ttu-id="b66ae-119">Web kancası adı.</span><span class="sxs-lookup"><span data-stu-id="b66ae-119">Webhook Name.</span></span>

```yaml
Type: String
Parameter Sets: NameResourceGroupParameterSet
Aliases: WebhookName, ResourceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b66ae-120">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="b66ae-120">-RegistryName</span></span>
<span data-ttu-id="b66ae-121">Kapsayıcı kayıt defteri adı.</span><span class="sxs-lookup"><span data-stu-id="b66ae-121">Container Registry Name.</span></span>

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

### <span data-ttu-id="b66ae-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b66ae-122">-ResourceGroupName</span></span>
<span data-ttu-id="b66ae-123">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="b66ae-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="b66ae-124">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="b66ae-124">-ResourceId</span></span>
<span data-ttu-id="b66ae-125">Kapsayıcı kayıt defteri Web kancası kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="b66ae-125">The container registry Webhook resource id</span></span>

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

### <span data-ttu-id="b66ae-126">-Web kancası</span><span class="sxs-lookup"><span data-stu-id="b66ae-126">-Webhook</span></span>
<span data-ttu-id="b66ae-127">Kapsayıcısı.</span><span class="sxs-lookup"><span data-stu-id="b66ae-127">Container Registry Object.</span></span>

```yaml
Type: PSContainerRegistryWebhook
Parameter Sets: WebhookObjectParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b66ae-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b66ae-128">-WhatIf</span></span>
<span data-ttu-id="b66ae-129">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b66ae-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b66ae-130">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b66ae-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b66ae-131">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="b66ae-131">-PassThru</span></span>
<span data-ttu-id="b66ae-132">Kaldırma işlemi başarılıysa bu cmdlet 'in doğru döndüğü anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="b66ae-132">Indicates that this cmdlet returns true if the removal was successful.</span></span>

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

### <span data-ttu-id="b66ae-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b66ae-133">CommonParameters</span></span>
<span data-ttu-id="b66ae-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b66ae-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b66ae-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b66ae-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b66ae-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b66ae-136">INPUTS</span></span>

### <span data-ttu-id="b66ae-137">Microsoft. Azure. Commands. ContainerRegistry. Pscontainerregistryweb kancası</span><span class="sxs-lookup"><span data-stu-id="b66ae-137">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>
<span data-ttu-id="b66ae-138">System. String</span><span class="sxs-lookup"><span data-stu-id="b66ae-138">System.String</span></span>

## <span data-ttu-id="b66ae-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b66ae-139">OUTPUTS</span></span>

### <span data-ttu-id="b66ae-140">System. Object</span><span class="sxs-lookup"><span data-stu-id="b66ae-140">System.Object</span></span>

## <span data-ttu-id="b66ae-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b66ae-141">NOTES</span></span>

## <span data-ttu-id="b66ae-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b66ae-142">RELATED LINKS</span></span>

[<span data-ttu-id="b66ae-143">Yeni-Azurermcontainerregistryweb kancası</span><span class="sxs-lookup"><span data-stu-id="b66ae-143">New-AzureRmContainerRegistryWebhook</span></span>](New-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="b66ae-144">Get-Azurermcontainerregistryweb kancası</span><span class="sxs-lookup"><span data-stu-id="b66ae-144">Get-AzureRmContainerRegistryWebhook</span></span>](Get-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="b66ae-145">Update-Azurermcontainerregistryweb kancası</span><span class="sxs-lookup"><span data-stu-id="b66ae-145">Update-AzureRmContainerRegistryWebhook</span></span>](Update-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="b66ae-146">Test-Azurermcontainerregistryweb kancası</span><span class="sxs-lookup"><span data-stu-id="b66ae-146">Test-AzureRmContainerRegistryWebhook</span></span>](Test-AzureRmContainerRegistryWebhook.md)
