---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/test-azurermcontainerregistrynameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Test-AzureRmContainerRegistryWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Test-AzureRmContainerRegistryWebhook.md
ms.openlocfilehash: 0a5894a411f4ffb5b3bde28db68961d321584e1d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762314"
---
# <span data-ttu-id="9f8df-101">Test-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="9f8df-101">Test-AzureRmContainerRegistryWebhook</span></span>

## <span data-ttu-id="9f8df-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9f8df-102">SYNOPSIS</span></span>
<span data-ttu-id="9f8df-103">Web kancası ping olayını tetikler.</span><span class="sxs-lookup"><span data-stu-id="9f8df-103">Triggers a webhook ping event.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9f8df-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9f8df-104">SYNTAX</span></span>

### <span data-ttu-id="9f8df-105">Resourceıdparameterset (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="9f8df-105">ResourceIdParameterSet (Default)</span></span>
```
Test-AzureRmContainerRegistryWebhook -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9f8df-106">NameResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="9f8df-106">NameResourceGroupParameterSet</span></span>
```
Test-AzureRmContainerRegistryWebhook [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9f8df-107">WebhookObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9f8df-107">WebhookObjectParameterSet</span></span>
```
Test-AzureRmContainerRegistryWebhook -Webhook <PSContainerRegistryWebhook>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9f8df-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="9f8df-108">DESCRIPTION</span></span>
<span data-ttu-id="9f8df-109">Test-AzureRmContainerRegistryWebhook cmdlet kancası ping olayını tetikler.</span><span class="sxs-lookup"><span data-stu-id="9f8df-109">The Test-AzureRmContainerRegistryWebhook cmdlet triggers a webhook ping event.</span></span>

## <span data-ttu-id="9f8df-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9f8df-110">EXAMPLES</span></span>

### <span data-ttu-id="9f8df-111">Örnek 1: Web kancası ping olayını tetikler.</span><span class="sxs-lookup"><span data-stu-id="9f8df-111">Example 1: Triggers a webhook ping event.</span></span>
```powershell
PS C:\> Test-AzureRmContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001"

Id
--
c5950af0-c8d0-4924-9873-1ba7da5cbf83
```

<span data-ttu-id="9f8df-112">Web kancası ping olayını tetikler.</span><span class="sxs-lookup"><span data-stu-id="9f8df-112">Triggers a webhook ping event.</span></span>

## <span data-ttu-id="9f8df-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9f8df-113">PARAMETERS</span></span>

### <span data-ttu-id="9f8df-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f8df-114">-DefaultProfile</span></span>
<span data-ttu-id="9f8df-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9f8df-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9f8df-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="9f8df-116">-Name</span></span>
<span data-ttu-id="9f8df-117">Web kancası adı.</span><span class="sxs-lookup"><span data-stu-id="9f8df-117">Webhook Name.</span></span>

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

### <span data-ttu-id="9f8df-118">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="9f8df-118">-RegistryName</span></span>
<span data-ttu-id="9f8df-119">Kapsayıcı kayıt defteri adı.</span><span class="sxs-lookup"><span data-stu-id="9f8df-119">Container Registry Name.</span></span>

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

### <span data-ttu-id="9f8df-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f8df-120">-ResourceGroupName</span></span>
<span data-ttu-id="9f8df-121">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="9f8df-121">Resource Group Name.</span></span>

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

### <span data-ttu-id="9f8df-122">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="9f8df-122">-ResourceId</span></span>
<span data-ttu-id="9f8df-123">Kapsayıcı kayıt defteri Web kancası kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="9f8df-123">The container registry Webhook resource id</span></span>

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

### <span data-ttu-id="9f8df-124">-Web kancası</span><span class="sxs-lookup"><span data-stu-id="9f8df-124">-Webhook</span></span>
<span data-ttu-id="9f8df-125">Kapsayıcısı.</span><span class="sxs-lookup"><span data-stu-id="9f8df-125">Container Registry Object.</span></span>

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

### <span data-ttu-id="9f8df-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f8df-126">CommonParameters</span></span>
<span data-ttu-id="9f8df-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9f8df-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f8df-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9f8df-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f8df-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9f8df-129">INPUTS</span></span>

### <span data-ttu-id="9f8df-130">Microsoft. Azure. Commands. ContainerRegistry. Pscontainerregistryweb kancası</span><span class="sxs-lookup"><span data-stu-id="9f8df-130">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>
<span data-ttu-id="9f8df-131">Parametreler: Web kancası (ByValue)</span><span class="sxs-lookup"><span data-stu-id="9f8df-131">Parameters: Webhook (ByValue)</span></span>

### <span data-ttu-id="9f8df-132">System. String</span><span class="sxs-lookup"><span data-stu-id="9f8df-132">System.String</span></span>

## <span data-ttu-id="9f8df-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9f8df-133">OUTPUTS</span></span>

### <span data-ttu-id="9f8df-134">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryEventInfo</span><span class="sxs-lookup"><span data-stu-id="9f8df-134">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryEventInfo</span></span>

## <span data-ttu-id="9f8df-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9f8df-135">NOTES</span></span>

## <span data-ttu-id="9f8df-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9f8df-136">RELATED LINKS</span></span>

[<span data-ttu-id="9f8df-137">Yeni-Azurermcontainerregistryweb kancası</span><span class="sxs-lookup"><span data-stu-id="9f8df-137">New-AzureRmContainerRegistryWebhook</span></span>](New-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="9f8df-138">Get-Azurermcontainerregistryweb kancası</span><span class="sxs-lookup"><span data-stu-id="9f8df-138">Get-AzureRmContainerRegistryWebhook</span></span>](Get-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="9f8df-139">Update-Azurermcontainerregistryweb kancası</span><span class="sxs-lookup"><span data-stu-id="9f8df-139">Update-AzureRmContainerRegistryWebhook</span></span>](Update-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="9f8df-140">Remove-Azurermcontainerregistryweb kancası</span><span class="sxs-lookup"><span data-stu-id="9f8df-140">Remove-AzureRmContainerRegistryWebhook</span></span>](Remove-AzureRmContainerRegistryWebhook.md)
