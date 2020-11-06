---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Remove-AzureRmWcfRelay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Remove-AzureRmWcfRelay.md
ms.openlocfilehash: a774f388690ab2ee0528e94a2a96addecf1687fc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594585"
---
# <span data-ttu-id="bd484-101">Remove-AzureRmWcfRelay</span><span class="sxs-lookup"><span data-stu-id="bd484-101">Remove-AzureRmWcfRelay</span></span>

## <span data-ttu-id="bd484-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bd484-102">SYNOPSIS</span></span>
<span data-ttu-id="bd484-103">Belirtilen geçiş ad alanından WcfRelay 'i kaldırır.</span><span class="sxs-lookup"><span data-stu-id="bd484-103">Removes the WcfRelay from the specified Relay namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bd484-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="bd484-104">SYNTAX</span></span>

```
Remove-AzureRmWcfRelay [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bd484-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="bd484-105">DESCRIPTION</span></span>
<span data-ttu-id="bd484-106">**Remove-AzureRmWcfRelay** cmdlet 'ı, wcfrelay 'ı belirtilen geçiş ad alanından kaldırır.</span><span class="sxs-lookup"><span data-stu-id="bd484-106">The **Remove-AzureRmWcfRelay** cmdlet removes the WcfRelay from the specified Relay namespace.</span></span>

## <span data-ttu-id="bd484-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="bd484-107">EXAMPLES</span></span>

### <span data-ttu-id="bd484-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="bd484-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -NamespaceName TestNameSpace-Relay1 -Name TestWCFRelay1
```

<span data-ttu-id="bd484-109">WcfRelay `TestWCFRelay1` 'i ad alanından kaldırır `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="bd484-109">Removes the WcfRelay `TestWCFRelay1` from the namespace `TestNameSpace-Relay1`.</span></span>

## <span data-ttu-id="bd484-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="bd484-110">PARAMETERS</span></span>

### <span data-ttu-id="bd484-111">-Namespace</span><span class="sxs-lookup"><span data-stu-id="bd484-111">-Namespace</span></span>
<span data-ttu-id="bd484-112">Ad alanı adı.</span><span class="sxs-lookup"><span data-stu-id="bd484-112">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd484-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bd484-113">-ResourceGroupName</span></span>
<span data-ttu-id="bd484-114">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="bd484-114">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd484-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="bd484-115">-Name</span></span>
<span data-ttu-id="bd484-116">WcfRelay adı.</span><span class="sxs-lookup"><span data-stu-id="bd484-116">WcfRelay Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd484-117">-Onay</span><span class="sxs-lookup"><span data-stu-id="bd484-117">-Confirm</span></span>
<span data-ttu-id="bd484-118">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="bd484-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd484-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bd484-119">-WhatIf</span></span>
<span data-ttu-id="bd484-120">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="bd484-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bd484-121">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="bd484-121">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd484-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd484-122">-DefaultProfile</span></span>
<span data-ttu-id="bd484-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="bd484-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bd484-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd484-124">CommonParameters</span></span>
<span data-ttu-id="bd484-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="bd484-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd484-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bd484-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd484-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="bd484-127">INPUTS</span></span>

### <span data-ttu-id="bd484-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bd484-128">-ResourceGroupName</span></span>
 <span data-ttu-id="bd484-129">System. String</span><span class="sxs-lookup"><span data-stu-id="bd484-129">System.String</span></span>
 

### <span data-ttu-id="bd484-130">-Namespace</span><span class="sxs-lookup"><span data-stu-id="bd484-130">-Namespace</span></span>
 <span data-ttu-id="bd484-131">System. String</span><span class="sxs-lookup"><span data-stu-id="bd484-131">System.String</span></span>
 

### <span data-ttu-id="bd484-132">-Ad</span><span class="sxs-lookup"><span data-stu-id="bd484-132">-Name</span></span>
 <span data-ttu-id="bd484-133">System. String</span><span class="sxs-lookup"><span data-stu-id="bd484-133">System.String</span></span>

## <span data-ttu-id="bd484-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="bd484-134">OUTPUTS</span></span>

### <span data-ttu-id="bd484-135">System. Object</span><span class="sxs-lookup"><span data-stu-id="bd484-135">System.Object</span></span>

## <span data-ttu-id="bd484-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="bd484-136">NOTES</span></span>

## <span data-ttu-id="bd484-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="bd484-137">RELATED LINKS</span></span>

