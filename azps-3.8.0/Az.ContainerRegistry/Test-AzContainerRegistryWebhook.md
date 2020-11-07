---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/test-azcontainerregistrywebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Test-AzContainerRegistryWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Test-AzContainerRegistryWebhook.md
ms.openlocfilehash: 1245c92e13af691b0b439d6745a35a917bdf4d89
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93937550"
---
# <span data-ttu-id="0218d-101">Test-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="0218d-101">Test-AzContainerRegistryWebhook</span></span>

## <span data-ttu-id="0218d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0218d-102">SYNOPSIS</span></span>
<span data-ttu-id="0218d-103">Web kancası ping olayını tetikler.</span><span class="sxs-lookup"><span data-stu-id="0218d-103">Triggers a webhook ping event.</span></span>

## <span data-ttu-id="0218d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0218d-104">SYNTAX</span></span>

### <span data-ttu-id="0218d-105">Resourceıdparameterset (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="0218d-105">ResourceIdParameterSet (Default)</span></span>
```
Test-AzContainerRegistryWebhook -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0218d-106">NameResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="0218d-106">NameResourceGroupParameterSet</span></span>
```
Test-AzContainerRegistryWebhook [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0218d-107">WebhookObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0218d-107">WebhookObjectParameterSet</span></span>
```
Test-AzContainerRegistryWebhook -Webhook <PSContainerRegistryWebhook>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0218d-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="0218d-108">DESCRIPTION</span></span>
<span data-ttu-id="0218d-109">Test-AzContainerRegistryWebhook cmdlet kancası ping olayını tetikler.</span><span class="sxs-lookup"><span data-stu-id="0218d-109">The Test-AzContainerRegistryWebhook cmdlet triggers a webhook ping event.</span></span>

## <span data-ttu-id="0218d-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0218d-110">EXAMPLES</span></span>

### <span data-ttu-id="0218d-111">Örnek 1: Web kancası ping olayını tetikler.</span><span class="sxs-lookup"><span data-stu-id="0218d-111">Example 1: Triggers a webhook ping event.</span></span>
```powershell
PS C:\> Test-AzContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001"

Id
--
c5950af0-c8d0-4924-9873-1ba7da5cbf83
```

<span data-ttu-id="0218d-112">Web kancası ping olayını tetikler.</span><span class="sxs-lookup"><span data-stu-id="0218d-112">Triggers a webhook ping event.</span></span>

## <span data-ttu-id="0218d-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0218d-113">PARAMETERS</span></span>

### <span data-ttu-id="0218d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0218d-114">-DefaultProfile</span></span>
<span data-ttu-id="0218d-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0218d-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0218d-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="0218d-116">-Name</span></span>
<span data-ttu-id="0218d-117">Web kancası adı.</span><span class="sxs-lookup"><span data-stu-id="0218d-117">Webhook Name.</span></span>

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

### <span data-ttu-id="0218d-118">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="0218d-118">-RegistryName</span></span>
<span data-ttu-id="0218d-119">Kapsayıcı kayıt defteri adı.</span><span class="sxs-lookup"><span data-stu-id="0218d-119">Container Registry Name.</span></span>

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

### <span data-ttu-id="0218d-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0218d-120">-ResourceGroupName</span></span>
<span data-ttu-id="0218d-121">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="0218d-121">Resource Group Name.</span></span>

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

### <span data-ttu-id="0218d-122">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="0218d-122">-ResourceId</span></span>
<span data-ttu-id="0218d-123">Kapsayıcı kayıt defteri Web kancası kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="0218d-123">The container registry Webhook resource id</span></span>

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

### <span data-ttu-id="0218d-124">-Web kancası</span><span class="sxs-lookup"><span data-stu-id="0218d-124">-Webhook</span></span>
<span data-ttu-id="0218d-125">Kapsayıcısı.</span><span class="sxs-lookup"><span data-stu-id="0218d-125">Container Registry Object.</span></span>

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

### <span data-ttu-id="0218d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0218d-126">CommonParameters</span></span>
<span data-ttu-id="0218d-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0218d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0218d-128">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="0218d-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0218d-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0218d-129">INPUTS</span></span>

### <span data-ttu-id="0218d-130">Microsoft. Azure. Commands. ContainerRegistry. Pscontainerregistryweb kancası</span><span class="sxs-lookup"><span data-stu-id="0218d-130">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>

### <span data-ttu-id="0218d-131">System. String</span><span class="sxs-lookup"><span data-stu-id="0218d-131">System.String</span></span>

## <span data-ttu-id="0218d-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0218d-132">OUTPUTS</span></span>

### <span data-ttu-id="0218d-133">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryEventInfo</span><span class="sxs-lookup"><span data-stu-id="0218d-133">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryEventInfo</span></span>

## <span data-ttu-id="0218d-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0218d-134">NOTES</span></span>

## <span data-ttu-id="0218d-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0218d-135">RELATED LINKS</span></span>

[<span data-ttu-id="0218d-136">Yeni-Azcontainerregistryweb kancası</span><span class="sxs-lookup"><span data-stu-id="0218d-136">New-AzContainerRegistryWebhook</span></span>](New-AzContainerRegistryWebhook.md)

[<span data-ttu-id="0218d-137">Get-Azcontainerregistryweb kancası</span><span class="sxs-lookup"><span data-stu-id="0218d-137">Get-AzContainerRegistryWebhook</span></span>](Get-AzContainerRegistryWebhook.md)

[<span data-ttu-id="0218d-138">Update-Azcontainerregistryweb kancası</span><span class="sxs-lookup"><span data-stu-id="0218d-138">Update-AzContainerRegistryWebhook</span></span>](Update-AzContainerRegistryWebhook.md)

[<span data-ttu-id="0218d-139">Remove-Azcontainerregistryweb kancası</span><span class="sxs-lookup"><span data-stu-id="0218d-139">Remove-AzContainerRegistryWebhook</span></span>](Remove-AzContainerRegistryWebhook.md)