---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/remove-azurermwcfrelay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Remove-AzureRmWcfRelay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Remove-AzureRmWcfRelay.md
ms.openlocfilehash: 02949f3a16c9a259e645a035ce3e762db9582024
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588813"
---
# <span data-ttu-id="4257a-101">Remove-AzureRmWcfRelay</span><span class="sxs-lookup"><span data-stu-id="4257a-101">Remove-AzureRmWcfRelay</span></span>

## <span data-ttu-id="4257a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4257a-102">SYNOPSIS</span></span>
<span data-ttu-id="4257a-103">Belirtilen geçiş ad alanından WcfRelay 'i kaldırır.</span><span class="sxs-lookup"><span data-stu-id="4257a-103">Removes the WcfRelay from the specified Relay namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4257a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4257a-104">SYNTAX</span></span>

```
Remove-AzureRmWcfRelay [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4257a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="4257a-105">DESCRIPTION</span></span>
<span data-ttu-id="4257a-106">**Remove-AzureRmWcfRelay** cmdlet 'ı, wcfrelay 'ı belirtilen geçiş ad alanından kaldırır.</span><span class="sxs-lookup"><span data-stu-id="4257a-106">The **Remove-AzureRmWcfRelay** cmdlet removes the WcfRelay from the specified Relay namespace.</span></span>

## <span data-ttu-id="4257a-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4257a-107">EXAMPLES</span></span>

### <span data-ttu-id="4257a-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="4257a-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -NamespaceName TestNameSpace-Relay1 -Name TestWCFRelay1
```

<span data-ttu-id="4257a-109">WcfRelay `TestWCFRelay1` 'i ad alanından kaldırır `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="4257a-109">Removes the WcfRelay `TestWCFRelay1` from the namespace `TestNameSpace-Relay1`.</span></span>

## <span data-ttu-id="4257a-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4257a-110">PARAMETERS</span></span>

### <span data-ttu-id="4257a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4257a-111">-DefaultProfile</span></span>
<span data-ttu-id="4257a-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4257a-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4257a-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="4257a-113">-Name</span></span>
<span data-ttu-id="4257a-114">WcfRelay adı.</span><span class="sxs-lookup"><span data-stu-id="4257a-114">WcfRelay Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4257a-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="4257a-115">-Namespace</span></span>
<span data-ttu-id="4257a-116">Ad alanı adı.</span><span class="sxs-lookup"><span data-stu-id="4257a-116">Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4257a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4257a-117">-ResourceGroupName</span></span>
<span data-ttu-id="4257a-118">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="4257a-118">Resource Group Name.</span></span>

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

### <span data-ttu-id="4257a-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="4257a-119">-Confirm</span></span>
<span data-ttu-id="4257a-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="4257a-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4257a-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4257a-121">-WhatIf</span></span>
<span data-ttu-id="4257a-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="4257a-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4257a-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="4257a-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4257a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4257a-124">CommonParameters</span></span>
<span data-ttu-id="4257a-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4257a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4257a-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4257a-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4257a-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4257a-127">INPUTS</span></span>

### <span data-ttu-id="4257a-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4257a-128">-ResourceGroupName</span></span>
 <span data-ttu-id="4257a-129">System. String</span><span class="sxs-lookup"><span data-stu-id="4257a-129">System.String</span></span>
 

### <span data-ttu-id="4257a-130">-Namespace</span><span class="sxs-lookup"><span data-stu-id="4257a-130">-Namespace</span></span>
 <span data-ttu-id="4257a-131">System. String</span><span class="sxs-lookup"><span data-stu-id="4257a-131">System.String</span></span>
 

### <span data-ttu-id="4257a-132">-Ad</span><span class="sxs-lookup"><span data-stu-id="4257a-132">-Name</span></span>
 <span data-ttu-id="4257a-133">System. String</span><span class="sxs-lookup"><span data-stu-id="4257a-133">System.String</span></span>

## <span data-ttu-id="4257a-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4257a-134">OUTPUTS</span></span>

### <span data-ttu-id="4257a-135">System. Object</span><span class="sxs-lookup"><span data-stu-id="4257a-135">System.Object</span></span>

## <span data-ttu-id="4257a-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4257a-136">NOTES</span></span>

## <span data-ttu-id="4257a-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4257a-137">RELATED LINKS</span></span>

