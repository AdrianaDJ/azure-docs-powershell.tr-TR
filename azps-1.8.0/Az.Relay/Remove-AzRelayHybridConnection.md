---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/remove-azrelayhybridconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Remove-AzRelayHybridConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Remove-AzRelayHybridConnection.md
ms.openlocfilehash: b0d7ef4a3fcaf681ea52719a5c7627784dac8d65
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93759502"
---
# <span data-ttu-id="ff6f9-101">Remove-AzRelayHybridConnection</span><span class="sxs-lookup"><span data-stu-id="ff6f9-101">Remove-AzRelayHybridConnection</span></span>

## <span data-ttu-id="ff6f9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ff6f9-102">SYNOPSIS</span></span>
<span data-ttu-id="ff6f9-103">Belirtilen HybridConnection ad alanından HybridConnection öğesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="ff6f9-103">Removes the HybridConnection from the specified HybridConnection namespace.</span></span>

## <span data-ttu-id="ff6f9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ff6f9-104">SYNTAX</span></span>

```
Remove-AzRelayHybridConnection [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ff6f9-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ff6f9-105">DESCRIPTION</span></span>
<span data-ttu-id="ff6f9-106">**Remove-AzRelayHybridConnection** cmdlet 'ı belirtilen geçiş ad alanındaki HybridConnection öğesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="ff6f9-106">The **Remove-AzRelayHybridConnection** cmdlet removes the HybridConnection from the specified Relay namespace.</span></span>

## <span data-ttu-id="ff6f9-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ff6f9-107">EXAMPLES</span></span>

### <span data-ttu-id="ff6f9-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="ff6f9-108">Example 1</span></span>
```
PS C:\> Remove-AzRelayHybridConnection -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestHybridConnection
```

<span data-ttu-id="ff6f9-109">Çalışma alanından HybridConnection öğesini kaldırır `TestHybridConnection` `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="ff6f9-109">Removes the HybridConnection `TestHybridConnection` from the namespace `TestNameSpace-Relay1`.</span></span>

## <span data-ttu-id="ff6f9-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ff6f9-110">PARAMETERS</span></span>

### <span data-ttu-id="ff6f9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff6f9-111">-DefaultProfile</span></span>
<span data-ttu-id="ff6f9-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ff6f9-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ff6f9-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="ff6f9-113">-Name</span></span>
<span data-ttu-id="ff6f9-114">HybridConnections adı.</span><span class="sxs-lookup"><span data-stu-id="ff6f9-114">HybridConnections Name.</span></span>

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

### <span data-ttu-id="ff6f9-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="ff6f9-115">-Namespace</span></span>
<span data-ttu-id="ff6f9-116">Ad alanı adı.</span><span class="sxs-lookup"><span data-stu-id="ff6f9-116">Namespace Name.</span></span>

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

### <span data-ttu-id="ff6f9-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff6f9-117">-ResourceGroupName</span></span>
<span data-ttu-id="ff6f9-118">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="ff6f9-118">Resource Group Name.</span></span>

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

### <span data-ttu-id="ff6f9-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="ff6f9-119">-Confirm</span></span>
<span data-ttu-id="ff6f9-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ff6f9-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ff6f9-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ff6f9-121">-WhatIf</span></span>
<span data-ttu-id="ff6f9-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ff6f9-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ff6f9-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ff6f9-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ff6f9-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff6f9-124">CommonParameters</span></span>
<span data-ttu-id="ff6f9-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ff6f9-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff6f9-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff6f9-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff6f9-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ff6f9-127">INPUTS</span></span>

### <span data-ttu-id="ff6f9-128">System. String</span><span class="sxs-lookup"><span data-stu-id="ff6f9-128">System.String</span></span>

## <span data-ttu-id="ff6f9-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ff6f9-129">OUTPUTS</span></span>

### <span data-ttu-id="ff6f9-130">System. void</span><span class="sxs-lookup"><span data-stu-id="ff6f9-130">System.Void</span></span>

## <span data-ttu-id="ff6f9-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ff6f9-131">NOTES</span></span>

## <span data-ttu-id="ff6f9-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ff6f9-132">RELATED LINKS</span></span>