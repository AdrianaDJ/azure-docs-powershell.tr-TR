---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/remove-azurermeventhubnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubNamespace.md
ms.openlocfilehash: cec41bda56da33f22def6c44752effb3d705b935
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762646"
---
# <span data-ttu-id="fb5ce-101">Remove-AzureRmEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="fb5ce-101">Remove-AzureRmEventHubNamespace</span></span>

## <span data-ttu-id="fb5ce-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fb5ce-102">SYNOPSIS</span></span>
<span data-ttu-id="fb5ce-103">Belirtilen olay hub ad alanını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="fb5ce-103">Removes the specified Event Hubs namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fb5ce-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fb5ce-104">SYNTAX</span></span>

```
Remove-AzureRmEventHubNamespace [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fb5ce-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="fb5ce-105">DESCRIPTION</span></span>
<span data-ttu-id="fb5ce-106">Remove-AzureRmEventHubNamespace cmdlet 'i, belirtilen olay hub ad alanını kaldırır ve siler.</span><span class="sxs-lookup"><span data-stu-id="fb5ce-106">The Remove-AzureRmEventHubNamespace cmdlet removes and deletes the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="fb5ce-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fb5ce-107">EXAMPLES</span></span>

### <span data-ttu-id="fb5ce-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="fb5ce-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmEventHubNamespace -ResourceGroupName MyResourceGroupName -Name MyNamespaceName
```

<span data-ttu-id="fb5ce-109">\` \` Myresourcegroupname kaynak grubundaki Olay Hub ad alanı mynamespacadını kaldırır \` \` .</span><span class="sxs-lookup"><span data-stu-id="fb5ce-109">Removes the Event Hubs namespace \`MyNamespaceName\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="fb5ce-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fb5ce-110">PARAMETERS</span></span>

### <span data-ttu-id="fb5ce-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb5ce-111">-DefaultProfile</span></span>
<span data-ttu-id="fb5ce-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="fb5ce-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fb5ce-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="fb5ce-113">-Name</span></span>
<span data-ttu-id="fb5ce-114">EventHub ad alanı adı</span><span class="sxs-lookup"><span data-stu-id="fb5ce-114">EventHub Namespace Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb5ce-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb5ce-115">-ResourceGroupName</span></span>
<span data-ttu-id="fb5ce-116">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="fb5ce-116">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb5ce-117">-Onay</span><span class="sxs-lookup"><span data-stu-id="fb5ce-117">-Confirm</span></span>
<span data-ttu-id="fb5ce-118">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="fb5ce-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fb5ce-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb5ce-119">-WhatIf</span></span>
<span data-ttu-id="fb5ce-120">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="fb5ce-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fb5ce-121">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="fb5ce-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fb5ce-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb5ce-122">CommonParameters</span></span>
<span data-ttu-id="fb5ce-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fb5ce-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="fb5ce-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb5ce-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb5ce-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fb5ce-125">INPUTS</span></span>

### <span data-ttu-id="fb5ce-126">System. String</span><span class="sxs-lookup"><span data-stu-id="fb5ce-126">System.String</span></span>


## <span data-ttu-id="fb5ce-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fb5ce-127">OUTPUTS</span></span>

### <span data-ttu-id="fb5ce-128">System. Object</span><span class="sxs-lookup"><span data-stu-id="fb5ce-128">System.Object</span></span>

## <span data-ttu-id="fb5ce-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fb5ce-129">NOTES</span></span>

## <span data-ttu-id="fb5ce-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fb5ce-130">RELATED LINKS</span></span>
