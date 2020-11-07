---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/get-azurermcontainerregistrycredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Get-AzureRmContainerRegistryWebhookEvent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Get-AzureRmContainerRegistryWebhookEvent.md
ms.openlocfilehash: 68a0bd0c2e076cbd2e96fdbe06def979937ed714
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762382"
---
# <span data-ttu-id="6ab50-101">Get-AzureRmContainerRegistryWebhookEvent</span><span class="sxs-lookup"><span data-stu-id="6ab50-101">Get-AzureRmContainerRegistryWebhookEvent</span></span>

## <span data-ttu-id="6ab50-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6ab50-102">SYNOPSIS</span></span>
<span data-ttu-id="6ab50-103">Kapsayıcı kayıt defteri Web kancası olaylarını alır.</span><span class="sxs-lookup"><span data-stu-id="6ab50-103">Gets events of a container registry webhook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6ab50-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6ab50-104">SYNTAX</span></span>

### <span data-ttu-id="6ab50-105">ListWebhookEventsByNameResourceGroupParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="6ab50-105">ListWebhookEventsByNameResourceGroupParameterSet (Default)</span></span>
```
Get-AzureRmContainerRegistryWebhookEvent -WebhookName <String> [-ResourceGroupName] <String>
 [-RegistryName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6ab50-106">ListWebhookEventsByWebhookObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6ab50-106">ListWebhookEventsByWebhookObjectParameterSet</span></span>
```
Get-AzureRmContainerRegistryWebhookEvent -Webhook <PSContainerRegistryWebhook>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6ab50-107">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="6ab50-107">ResourceIdParameterSet</span></span>
```
Get-AzureRmContainerRegistryWebhookEvent -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6ab50-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="6ab50-108">DESCRIPTION</span></span>
<span data-ttu-id="6ab50-109">Get-AzureRmContainerRegistryWebhookEvent cmdlet, bir Web kancası 'nın tüm olaylarını listeler.</span><span class="sxs-lookup"><span data-stu-id="6ab50-109">The Get-AzureRmContainerRegistryWebhookEvent cmdlet lists all the events of a webhook.</span></span>

## <span data-ttu-id="6ab50-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6ab50-110">EXAMPLES</span></span>

### <span data-ttu-id="6ab50-111">Örnek 1: Web kancası 'nun tüm olaylarını alır.</span><span class="sxs-lookup"><span data-stu-id="6ab50-111">Example 1: Gets all the events of a webhook.</span></span>
```powershell
PS C:\>Get-AzureRmContainerRegistryWebhookEvent -ResourceGroupName mattacrtest001 -RegistryName premium001 -Name webhook001

   Webhook service Uri: http://www.bing.com/

ID                                       Action   Timestamp                      Response
                                                                                 StatusCode
--                                       ------   ---------                      ----------
3c6281b6-47cd-4129-948b-4036780236f0     ping     11/17/2017 5:10:09 PM          200
70f1d41d-15fe-4251-87b6-43c32a91eae7     ping     11/17/2017 6:56:23 AM          200
5d25556b-32d0-4377-8031-d8ba7a263d6a     ping     11/17/2017 6:27:41 AM          200
c1e7d8aa-9f1b-447c-9583-2a58b7f81026     ping     11/17/2017 12:09:41 AM         200
eb4aa503-0d14-4f25-8ae5-33cce9a8fd50     ping     11/16/2017 11:35:03 PM         200
85a93d7f-3923-4ec5-bb8e-9ded5b6549c1     ping     11/17/2017 5:10:09 PM          200
9e3c8b5f-e0ee-47cf-9727-df1c8d45a497     ping     11/17/2017 6:56:23 AM          200
2d0ce294-9b59-4f5c-953a-47f2b270526f     ping     11/17/2017 6:27:41 AM          200
```

<span data-ttu-id="6ab50-112">Bir Web kancası 'nun tüm olaylarını alır.</span><span class="sxs-lookup"><span data-stu-id="6ab50-112">Gets all the events of a webhook.</span></span>

## <span data-ttu-id="6ab50-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6ab50-113">PARAMETERS</span></span>

### <span data-ttu-id="6ab50-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ab50-114">-DefaultProfile</span></span>
<span data-ttu-id="6ab50-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6ab50-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6ab50-116">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="6ab50-116">-RegistryName</span></span>
<span data-ttu-id="6ab50-117">Kapsayıcı kayıt defteri adı.</span><span class="sxs-lookup"><span data-stu-id="6ab50-117">Container Registry Name.</span></span>

```yaml
Type: String
Parameter Sets: ListWebhookEventsByNameResourceGroupParameterSet
Aliases: ContainerRegistryName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ab50-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ab50-118">-ResourceGroupName</span></span>
<span data-ttu-id="6ab50-119">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="6ab50-119">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: ListWebhookEventsByNameResourceGroupParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ab50-120">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="6ab50-120">-ResourceId</span></span>
<span data-ttu-id="6ab50-121">Kapsayıcı kayıt defteri Web kancası kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="6ab50-121">The container registry Webhook resource id</span></span>

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

### <span data-ttu-id="6ab50-122">-Web kancası</span><span class="sxs-lookup"><span data-stu-id="6ab50-122">-Webhook</span></span>
<span data-ttu-id="6ab50-123">Kapsayıcısı.</span><span class="sxs-lookup"><span data-stu-id="6ab50-123">Container Registry Object.</span></span>

```yaml
Type: PSContainerRegistryWebhook
Parameter Sets: ListWebhookEventsByWebhookObjectParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ab50-124">-Webtakma adı</span><span class="sxs-lookup"><span data-stu-id="6ab50-124">-WebhookName</span></span>
<span data-ttu-id="6ab50-125">Web kancası adı.</span><span class="sxs-lookup"><span data-stu-id="6ab50-125">Webhook Name.</span></span>
```yaml
Type: String
Parameter Sets: ListWebhookEventsByNameResourceGroupParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ab50-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ab50-126">CommonParameters</span></span>
<span data-ttu-id="6ab50-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6ab50-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ab50-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6ab50-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ab50-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6ab50-129">INPUTS</span></span>

### <span data-ttu-id="6ab50-130">System. String</span><span class="sxs-lookup"><span data-stu-id="6ab50-130">System.String</span></span>

## <span data-ttu-id="6ab50-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6ab50-131">OUTPUTS</span></span>

### <span data-ttu-id="6ab50-132">System. Koleksiyonlar. Generic. IList ' 1 [[Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryWebhookEvent, Microsoft. Azure. Commands. ContainerRegistry, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="6ab50-132">System.Collections.Generic.IList\`1[[Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhookEvent, Microsoft.Azure.Commands.ContainerRegistry, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="6ab50-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6ab50-133">NOTES</span></span>

## <span data-ttu-id="6ab50-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6ab50-134">RELATED LINKS</span></span>

[<span data-ttu-id="6ab50-135">Yeni-Azurermcontainerregistryweb kancası</span><span class="sxs-lookup"><span data-stu-id="6ab50-135">New-AzureRmContainerRegistryWebhook</span></span>](New-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="6ab50-136">Get-Azurermcontainerregistryweb kancası</span><span class="sxs-lookup"><span data-stu-id="6ab50-136">Get-AzureRmContainerRegistryWebhook</span></span>](Get-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="6ab50-137">Update-Azurermcontainerregistryweb kancası</span><span class="sxs-lookup"><span data-stu-id="6ab50-137">Update-AzureRmContainerRegistryWebhook</span></span>](Update-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="6ab50-138">Remove-Azurermcontainerregistryweb kancası</span><span class="sxs-lookup"><span data-stu-id="6ab50-138">Remove-AzureRmContainerRegistryWebhook</span></span>](Remove-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="6ab50-139">Test-Azurermcontainerregistryweb kancası</span><span class="sxs-lookup"><span data-stu-id="6ab50-139">Test-AzureRmContainerRegistryWebhook</span></span>](Test-AzureRmContainerRegistryWebhook.md)

