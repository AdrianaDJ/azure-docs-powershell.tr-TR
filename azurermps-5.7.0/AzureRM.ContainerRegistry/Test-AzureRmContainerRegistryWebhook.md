---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/test-azurermcontainerregistrynameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Test-AzureRmContainerRegistryWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Test-AzureRmContainerRegistryWebhook.md
ms.openlocfilehash: 02d16be7c41a95c32d4aa7b6f3231b68c0ba7244
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591027"
---
# <span data-ttu-id="9e4dc-101">Test-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="9e4dc-101">Test-AzureRmContainerRegistryWebhook</span></span>

## <span data-ttu-id="9e4dc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9e4dc-102">SYNOPSIS</span></span>
<span data-ttu-id="9e4dc-103">Web kancası ping olayını tetikler.</span><span class="sxs-lookup"><span data-stu-id="9e4dc-103">Triggers a webhook ping event.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9e4dc-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9e4dc-104">SYNTAX</span></span>

### <span data-ttu-id="9e4dc-105">Resourceıdparameterset (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="9e4dc-105">ResourceIdParameterSet (Default)</span></span>
```
Test-AzureRmContainerRegistryWebhook -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9e4dc-106">NameResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="9e4dc-106">NameResourceGroupParameterSet</span></span>
```
Test-AzureRmContainerRegistryWebhook [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9e4dc-107">WebhookObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9e4dc-107">WebhookObjectParameterSet</span></span>
```
Test-AzureRmContainerRegistryWebhook -Webhook <PSContainerRegistryWebhook>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9e4dc-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="9e4dc-108">DESCRIPTION</span></span>
<span data-ttu-id="9e4dc-109">Test-AzureRmContainerRegistryWebhook cmdlet kancası ping olayını tetikler.</span><span class="sxs-lookup"><span data-stu-id="9e4dc-109">The Test-AzureRmContainerRegistryWebhook cmdlet triggers a webhook ping event.</span></span>

## <span data-ttu-id="9e4dc-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9e4dc-110">EXAMPLES</span></span>

### <span data-ttu-id="9e4dc-111">Örnek 1: Web kancası ping olayını tetikler.</span><span class="sxs-lookup"><span data-stu-id="9e4dc-111">Example 1: Triggers a webhook ping event.</span></span>
```powershell
PS C:\> Test-AzureRmContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001"

Id
--
c5950af0-c8d0-4924-9873-1ba7da5cbf83
```

<span data-ttu-id="9e4dc-112">Web kancası ping olayını tetikler.</span><span class="sxs-lookup"><span data-stu-id="9e4dc-112">Triggers a webhook ping event.</span></span>

## <span data-ttu-id="9e4dc-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9e4dc-113">PARAMETERS</span></span>

### <span data-ttu-id="9e4dc-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e4dc-114">-DefaultProfile</span></span>
<span data-ttu-id="9e4dc-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9e4dc-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9e4dc-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="9e4dc-116">-Name</span></span>
<span data-ttu-id="9e4dc-117">Web kancası adı.</span><span class="sxs-lookup"><span data-stu-id="9e4dc-117">Webhook Name.</span></span>

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

### <span data-ttu-id="9e4dc-118">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="9e4dc-118">-RegistryName</span></span>
<span data-ttu-id="9e4dc-119">Kapsayıcı kayıt defteri adı.</span><span class="sxs-lookup"><span data-stu-id="9e4dc-119">Container Registry Name.</span></span>

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

### <span data-ttu-id="9e4dc-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e4dc-120">-ResourceGroupName</span></span>
<span data-ttu-id="9e4dc-121">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="9e4dc-121">Resource Group Name.</span></span>

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

### <span data-ttu-id="9e4dc-122">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="9e4dc-122">-ResourceId</span></span>
<span data-ttu-id="9e4dc-123">Kapsayıcı kayıt defteri Web kancası kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="9e4dc-123">The container registry Webhook resource id</span></span>

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

### <span data-ttu-id="9e4dc-124">-Web kancası</span><span class="sxs-lookup"><span data-stu-id="9e4dc-124">-Webhook</span></span>
<span data-ttu-id="9e4dc-125">Kapsayıcısı.</span><span class="sxs-lookup"><span data-stu-id="9e4dc-125">Container Registry Object.</span></span>

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

### <span data-ttu-id="9e4dc-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e4dc-126">CommonParameters</span></span>
<span data-ttu-id="9e4dc-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9e4dc-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e4dc-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9e4dc-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e4dc-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9e4dc-129">INPUTS</span></span>

### <span data-ttu-id="9e4dc-130">Microsoft. Azure. Commands. ContainerRegistry. Pscontainerregistryweb kancası</span><span class="sxs-lookup"><span data-stu-id="9e4dc-130">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>
<span data-ttu-id="9e4dc-131">System. String</span><span class="sxs-lookup"><span data-stu-id="9e4dc-131">System.String</span></span>

## <span data-ttu-id="9e4dc-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9e4dc-132">OUTPUTS</span></span>

### <span data-ttu-id="9e4dc-133">Microsoft. Azure. Management. ContainerRegistry. modeller. EventInfo</span><span class="sxs-lookup"><span data-stu-id="9e4dc-133">Microsoft.Azure.Management.ContainerRegistry.Models.EventInfo</span></span>

## <span data-ttu-id="9e4dc-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9e4dc-134">NOTES</span></span>

## <span data-ttu-id="9e4dc-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9e4dc-135">RELATED LINKS</span></span>

[<span data-ttu-id="9e4dc-136">Yeni-Azurermcontainerregistryweb kancası</span><span class="sxs-lookup"><span data-stu-id="9e4dc-136">New-AzureRmContainerRegistryWebhook</span></span>](New-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="9e4dc-137">Get-Azurermcontainerregistryweb kancası</span><span class="sxs-lookup"><span data-stu-id="9e4dc-137">Get-AzureRmContainerRegistryWebhook</span></span>](Get-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="9e4dc-138">Update-Azurermcontainerregistryweb kancası</span><span class="sxs-lookup"><span data-stu-id="9e4dc-138">Update-AzureRmContainerRegistryWebhook</span></span>](Update-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="9e4dc-139">Remove-Azurermcontainerregistryweb kancası</span><span class="sxs-lookup"><span data-stu-id="9e4dc-139">Remove-AzureRmContainerRegistryWebhook</span></span>](Remove-AzureRmContainerRegistryWebhook.md)
