---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/remove-azrelaynamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Remove-AzRelayNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Remove-AzRelayNamespace.md
ms.openlocfilehash: 463ef6d1d23ffe809d8810a9cbf4dd0ebf1ff578
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94268178"
---
# <span data-ttu-id="9ff5d-101">Remove-AzRelayNamespace</span><span class="sxs-lookup"><span data-stu-id="9ff5d-101">Remove-AzRelayNamespace</span></span>

## <span data-ttu-id="9ff5d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9ff5d-102">SYNOPSIS</span></span>
<span data-ttu-id="9ff5d-103">Belirtilen kaynak grubundan ad alanını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="9ff5d-103">Removes the namespace from the specified resource group.</span></span> 

## <span data-ttu-id="9ff5d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9ff5d-104">SYNTAX</span></span>

```
Remove-AzRelayNamespace [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9ff5d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="9ff5d-105">DESCRIPTION</span></span>
<span data-ttu-id="9ff5d-106">**Remove-AzRelayNamespace** cmdlet 'i belirtilen kaynak grubundaki ad alanını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="9ff5d-106">The **Remove-AzRelayNamespace** cmdlet removes the namespace from the specified resource group.</span></span>

## <span data-ttu-id="9ff5d-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9ff5d-107">EXAMPLES</span></span>

### <span data-ttu-id="9ff5d-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="9ff5d-108">Example 1</span></span>
```
PS C:\> Remove-AzRelayNamespace -ResourceGroupName Default-ServiceBus-WestUS -Name TestNameSpace-Relay1
```

<span data-ttu-id="9ff5d-109">Belirtilen kaynak grubundan geçiş ad alanını kaldırır `TestNameSpace-Relay1` `Default-ServiceBus-WestUS` .</span><span class="sxs-lookup"><span data-stu-id="9ff5d-109">Removes the Relay namespace `TestNameSpace-Relay1` from the specified resource group `Default-ServiceBus-WestUS`.</span></span>

## <span data-ttu-id="9ff5d-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9ff5d-110">PARAMETERS</span></span>

### <span data-ttu-id="9ff5d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ff5d-111">-DefaultProfile</span></span>
<span data-ttu-id="9ff5d-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9ff5d-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9ff5d-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="9ff5d-113">-Name</span></span>
<span data-ttu-id="9ff5d-114">Geçiş ad alanı adı.</span><span class="sxs-lookup"><span data-stu-id="9ff5d-114">Relay Namespace Name.</span></span>

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

### <span data-ttu-id="9ff5d-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ff5d-115">-ResourceGroupName</span></span>
<span data-ttu-id="9ff5d-116">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="9ff5d-116">Resource Group Name.</span></span>

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

### <span data-ttu-id="9ff5d-117">-Onay</span><span class="sxs-lookup"><span data-stu-id="9ff5d-117">-Confirm</span></span>
<span data-ttu-id="9ff5d-118">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="9ff5d-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9ff5d-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9ff5d-119">-WhatIf</span></span>
<span data-ttu-id="9ff5d-120">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="9ff5d-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9ff5d-121">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="9ff5d-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9ff5d-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ff5d-122">CommonParameters</span></span>
<span data-ttu-id="9ff5d-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9ff5d-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ff5d-124">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9ff5d-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ff5d-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9ff5d-125">INPUTS</span></span>

### <span data-ttu-id="9ff5d-126">System. String</span><span class="sxs-lookup"><span data-stu-id="9ff5d-126">System.String</span></span>

## <span data-ttu-id="9ff5d-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9ff5d-127">OUTPUTS</span></span>

### <span data-ttu-id="9ff5d-128">System. void</span><span class="sxs-lookup"><span data-stu-id="9ff5d-128">System.Void</span></span>

## <span data-ttu-id="9ff5d-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9ff5d-129">NOTES</span></span>

## <span data-ttu-id="9ff5d-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9ff5d-130">RELATED LINKS</span></span>
