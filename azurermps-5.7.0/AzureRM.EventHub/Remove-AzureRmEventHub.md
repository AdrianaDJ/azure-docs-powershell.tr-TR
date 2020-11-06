---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/remove-azurermeventhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHub.md
ms.openlocfilehash: b546c4f610bb6bc8021547fa5f7f0516ffbc2371
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594962"
---
# <span data-ttu-id="218ed-101">Remove-AzureRmEventHub</span><span class="sxs-lookup"><span data-stu-id="218ed-101">Remove-AzureRmEventHub</span></span>

## <span data-ttu-id="218ed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="218ed-102">SYNOPSIS</span></span>
<span data-ttu-id="218ed-103">Belirtilen olay hub 'ını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="218ed-103">Removes the specified Event Hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="218ed-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="218ed-104">SYNTAX</span></span>

```
Remove-AzureRmEventHub [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="218ed-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="218ed-105">DESCRIPTION</span></span>
<span data-ttu-id="218ed-106">Remove-AzureRmEventHub cmdlet, verilen ad alanından belirtilen olay hub 'ını kaldırır ve siler.</span><span class="sxs-lookup"><span data-stu-id="218ed-106">The Remove-AzureRmEventHub cmdlet removes and deletes the specified Event Hub from the given namespace.</span></span>

## <span data-ttu-id="218ed-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="218ed-107">EXAMPLES</span></span>

### <span data-ttu-id="218ed-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="218ed-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmEventHub -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyEventHubName
```

<span data-ttu-id="218ed-109">Olay Hub \` myeventhubname 'i kaldırır \` .</span><span class="sxs-lookup"><span data-stu-id="218ed-109">Removes the Event Hub \`MyEventHubName\`.</span></span>

## <span data-ttu-id="218ed-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="218ed-110">PARAMETERS</span></span>

### <span data-ttu-id="218ed-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="218ed-111">-DefaultProfile</span></span>
<span data-ttu-id="218ed-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="218ed-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="218ed-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="218ed-113">-Name</span></span>
<span data-ttu-id="218ed-114">EventHub adı</span><span class="sxs-lookup"><span data-stu-id="218ed-114">EventHub Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: EventHubName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="218ed-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="218ed-115">-Namespace</span></span>
<span data-ttu-id="218ed-116">Ad alanı adı</span><span class="sxs-lookup"><span data-stu-id="218ed-116">Namespace Name</span></span>

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

### <span data-ttu-id="218ed-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="218ed-117">-ResourceGroupName</span></span>
<span data-ttu-id="218ed-118">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="218ed-118">Resource Group Name</span></span>

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

### <span data-ttu-id="218ed-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="218ed-119">-Confirm</span></span>
<span data-ttu-id="218ed-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="218ed-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="218ed-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="218ed-121">-WhatIf</span></span>
<span data-ttu-id="218ed-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="218ed-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="218ed-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="218ed-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="218ed-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="218ed-124">CommonParameters</span></span>
<span data-ttu-id="218ed-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="218ed-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="218ed-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="218ed-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="218ed-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="218ed-127">INPUTS</span></span>

### <span data-ttu-id="218ed-128">System. String</span><span class="sxs-lookup"><span data-stu-id="218ed-128">System.String</span></span>


## <span data-ttu-id="218ed-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="218ed-129">OUTPUTS</span></span>

### <span data-ttu-id="218ed-130">System. Object</span><span class="sxs-lookup"><span data-stu-id="218ed-130">System.Object</span></span>

## <span data-ttu-id="218ed-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="218ed-131">NOTES</span></span>

## <span data-ttu-id="218ed-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="218ed-132">RELATED LINKS</span></span>
