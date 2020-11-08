---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/remove-azwcfrelay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Remove-AzWcfRelay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Remove-AzWcfRelay.md
ms.openlocfilehash: f523f0d1166a40e04ac85344c0fc96640a140bb6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93933389"
---
# <span data-ttu-id="73e9e-101">Remove-AzWcfRelay</span><span class="sxs-lookup"><span data-stu-id="73e9e-101">Remove-AzWcfRelay</span></span>

## <span data-ttu-id="73e9e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="73e9e-102">SYNOPSIS</span></span>
<span data-ttu-id="73e9e-103">Belirtilen geçiş ad alanından WcfRelay 'i kaldırır.</span><span class="sxs-lookup"><span data-stu-id="73e9e-103">Removes the WcfRelay from the specified Relay namespace.</span></span>

## <span data-ttu-id="73e9e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="73e9e-104">SYNTAX</span></span>

```
Remove-AzWcfRelay [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="73e9e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="73e9e-105">DESCRIPTION</span></span>
<span data-ttu-id="73e9e-106">**Remove-AzWcfRelay** cmdlet 'ı, wcfrelay 'ı belirtilen geçiş ad alanından kaldırır.</span><span class="sxs-lookup"><span data-stu-id="73e9e-106">The **Remove-AzWcfRelay** cmdlet removes the WcfRelay from the specified Relay namespace.</span></span>

## <span data-ttu-id="73e9e-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="73e9e-107">EXAMPLES</span></span>

### <span data-ttu-id="73e9e-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="73e9e-108">Example 1</span></span>
```
PS C:\> Remove-AzWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -NamespaceName TestNameSpace-Relay1 -Name TestWCFRelay1
```

<span data-ttu-id="73e9e-109">WcfRelay `TestWCFRelay1` 'i ad alanından kaldırır `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="73e9e-109">Removes the WcfRelay `TestWCFRelay1` from the namespace `TestNameSpace-Relay1`.</span></span>

## <span data-ttu-id="73e9e-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="73e9e-110">PARAMETERS</span></span>

### <span data-ttu-id="73e9e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73e9e-111">-DefaultProfile</span></span>
<span data-ttu-id="73e9e-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="73e9e-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="73e9e-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="73e9e-113">-Name</span></span>
<span data-ttu-id="73e9e-114">WcfRelay adı.</span><span class="sxs-lookup"><span data-stu-id="73e9e-114">WcfRelay Name.</span></span>

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

### <span data-ttu-id="73e9e-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="73e9e-115">-Namespace</span></span>
<span data-ttu-id="73e9e-116">Ad alanı adı.</span><span class="sxs-lookup"><span data-stu-id="73e9e-116">Namespace Name.</span></span>

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

### <span data-ttu-id="73e9e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="73e9e-117">-ResourceGroupName</span></span>
<span data-ttu-id="73e9e-118">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="73e9e-118">Resource Group Name.</span></span>

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

### <span data-ttu-id="73e9e-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="73e9e-119">-Confirm</span></span>
<span data-ttu-id="73e9e-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="73e9e-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="73e9e-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="73e9e-121">-WhatIf</span></span>
<span data-ttu-id="73e9e-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="73e9e-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="73e9e-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="73e9e-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="73e9e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73e9e-124">CommonParameters</span></span>
<span data-ttu-id="73e9e-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="73e9e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73e9e-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="73e9e-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73e9e-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="73e9e-127">INPUTS</span></span>

### <span data-ttu-id="73e9e-128">System. String</span><span class="sxs-lookup"><span data-stu-id="73e9e-128">System.String</span></span>

## <span data-ttu-id="73e9e-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="73e9e-129">OUTPUTS</span></span>

### <span data-ttu-id="73e9e-130">System. void</span><span class="sxs-lookup"><span data-stu-id="73e9e-130">System.Void</span></span>

## <span data-ttu-id="73e9e-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="73e9e-131">NOTES</span></span>

## <span data-ttu-id="73e9e-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="73e9e-132">RELATED LINKS</span></span>