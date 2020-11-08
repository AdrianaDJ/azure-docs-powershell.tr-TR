---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 760C03A0-12DB-43C4-A180-B013FA77A513
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationvariable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationVariable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationVariable.md
ms.openlocfilehash: edb55424b16c0cdb6636f715ce6755a317e6f396
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94109203"
---
# <span data-ttu-id="e4a01-101">Remove-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="e4a01-101">Remove-AzAutomationVariable</span></span>

## <span data-ttu-id="e4a01-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e4a01-102">SYNOPSIS</span></span>
<span data-ttu-id="e4a01-103">Otomasyon değişkenini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="e4a01-103">Removes an Automation variable.</span></span>

## <span data-ttu-id="e4a01-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e4a01-104">SYNTAX</span></span>

```
Remove-AzAutomationVariable [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e4a01-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e4a01-105">DESCRIPTION</span></span>
<span data-ttu-id="e4a01-106">**Remove-AzAutomationVariable** cmdlet 'ı Azure Otomasyonu 'ndan bir değişkeni kaldırır.</span><span class="sxs-lookup"><span data-stu-id="e4a01-106">The **Remove-AzAutomationVariable** cmdlet removes a variable from Azure Automation.</span></span>

## <span data-ttu-id="e4a01-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e4a01-107">EXAMPLES</span></span>

### <span data-ttu-id="e4a01-108">Örnek 1: bir değişkeni kaldırma</span><span class="sxs-lookup"><span data-stu-id="e4a01-108">Example 1: Remove a variable</span></span>
```
PS C:\>Remove-AzAutomationVariable -AutomationAccountName "Contoso17" -Name "StringVariable22" -Force -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="e4a01-109">Bu komut, Contoso17 adındaki Otomasyon hesabındaki StringVariable22 adlı bir değişkeni kaldırır.</span><span class="sxs-lookup"><span data-stu-id="e4a01-109">This command removes a variable named StringVariable22 in the Automation account named Contoso17.</span></span>
<span data-ttu-id="e4a01-110">Bu komut *Force* parametresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e4a01-110">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="e4a01-111">Bu nedenle sizden onay istemez.</span><span class="sxs-lookup"><span data-stu-id="e4a01-111">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="e4a01-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e4a01-112">PARAMETERS</span></span>

### <span data-ttu-id="e4a01-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="e4a01-113">-AutomationAccountName</span></span>
<span data-ttu-id="e4a01-114">Bu cmdlet 'in sildiği değişkeni içeren Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e4a01-114">Specifies the name of the Automation account that contains the variable that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="e4a01-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4a01-115">-DefaultProfile</span></span>
<span data-ttu-id="e4a01-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="e4a01-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e4a01-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="e4a01-117">-Name</span></span>
<span data-ttu-id="e4a01-118">Bu cmdlet 'in sildiği değişkenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e4a01-118">Specifies the name of the variable that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="e4a01-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4a01-119">-ResourceGroupName</span></span>
<span data-ttu-id="e4a01-120">Bu cmdlet 'in bir değişkeni sildiği kaynak grubunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="e4a01-120">Specifies the resource group for which this cmdlet deletes a variable.</span></span>

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

### <span data-ttu-id="e4a01-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="e4a01-121">-Confirm</span></span>
<span data-ttu-id="e4a01-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e4a01-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e4a01-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e4a01-123">-WhatIf</span></span>
<span data-ttu-id="e4a01-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e4a01-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e4a01-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e4a01-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e4a01-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4a01-126">CommonParameters</span></span>
<span data-ttu-id="e4a01-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e4a01-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4a01-128">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e4a01-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4a01-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e4a01-129">INPUTS</span></span>

### <span data-ttu-id="e4a01-130">System. String</span><span class="sxs-lookup"><span data-stu-id="e4a01-130">System.String</span></span>

## <span data-ttu-id="e4a01-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e4a01-131">OUTPUTS</span></span>

### <span data-ttu-id="e4a01-132">System. void</span><span class="sxs-lookup"><span data-stu-id="e4a01-132">System.Void</span></span>

## <span data-ttu-id="e4a01-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e4a01-133">NOTES</span></span>

## <span data-ttu-id="e4a01-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e4a01-134">RELATED LINKS</span></span>

[<span data-ttu-id="e4a01-135">Get-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="e4a01-135">Get-AzAutomationVariable</span></span>](./Get-AzAutomationVariable.md)

[<span data-ttu-id="e4a01-136">Yeni-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="e4a01-136">New-AzAutomationVariable</span></span>](./New-AzAutomationVariable.md)

[<span data-ttu-id="e4a01-137">Set-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="e4a01-137">Set-AzAutomationVariable</span></span>](./Set-AzAutomationVariable.md)


