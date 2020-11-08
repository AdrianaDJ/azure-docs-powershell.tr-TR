---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 5F45A12C-BB50-4732-BE80-188491DEF8B5
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationModule.md
ms.openlocfilehash: 8d7e63ed8bc24f772afa84106592ede5f9da9250
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94104924"
---
# <span data-ttu-id="c21bd-101">Remove-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="c21bd-101">Remove-AzAutomationModule</span></span>

## <span data-ttu-id="c21bd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c21bd-102">SYNOPSIS</span></span>
<span data-ttu-id="c21bd-103">Bir modülü Otomasyon 'dan kaldırır.</span><span class="sxs-lookup"><span data-stu-id="c21bd-103">Removes a module from Automation.</span></span>

## <span data-ttu-id="c21bd-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c21bd-104">SYNTAX</span></span>

```
Remove-AzAutomationModule [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c21bd-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c21bd-105">DESCRIPTION</span></span>
<span data-ttu-id="c21bd-106">**Remove-AzAutomationModule** cmdlet 'ı Azure Otomasyonu 'ndaki Otomasyon hesabından modülü kaldırır.</span><span class="sxs-lookup"><span data-stu-id="c21bd-106">The **Remove-AzAutomationModule** cmdlet removes a module from an Automation account in Azure Automation.</span></span>

## <span data-ttu-id="c21bd-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c21bd-107">EXAMPLES</span></span>

### <span data-ttu-id="c21bd-108">Örnek 1: modül kaldırma</span><span class="sxs-lookup"><span data-stu-id="c21bd-108">Example 1: Remove a module</span></span>
```
PS C:\>Remove-AzAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="c21bd-109">Bu komut, Contoso17 adlı Otomasyon hesabından ContosoModule adlı bir modülü kaldırır.</span><span class="sxs-lookup"><span data-stu-id="c21bd-109">This command removes a module named ContosoModule from the Automation account named Contoso17.</span></span>

## <span data-ttu-id="c21bd-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c21bd-110">PARAMETERS</span></span>

### <span data-ttu-id="c21bd-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="c21bd-111">-AutomationAccountName</span></span>
<span data-ttu-id="c21bd-112">Bu cmdlet 'in modülü kaldırdığı Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c21bd-112">Specifies the name of the Automation account from which this cmdlet removes a module.</span></span>

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

### <span data-ttu-id="c21bd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c21bd-113">-DefaultProfile</span></span>
<span data-ttu-id="c21bd-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="c21bd-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c21bd-115">-Force</span><span class="sxs-lookup"><span data-stu-id="c21bd-115">-Force</span></span>
<span data-ttu-id="c21bd-116">ps_force</span><span class="sxs-lookup"><span data-stu-id="c21bd-116">ps_force</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c21bd-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="c21bd-117">-Name</span></span>
<span data-ttu-id="c21bd-118">Bu cmdlet 'in kaldırdığı modülün adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c21bd-118">Specifies the name of the module that this cmdlet removes.</span></span>

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

### <span data-ttu-id="c21bd-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c21bd-119">-ResourceGroupName</span></span>
<span data-ttu-id="c21bd-120">Bu cmdlet 'in modülü kaldırırken kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c21bd-120">Specifies the name of a resource group in which this cmdlet removes a module.</span></span>

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

### <span data-ttu-id="c21bd-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="c21bd-121">-Confirm</span></span>
<span data-ttu-id="c21bd-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c21bd-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c21bd-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c21bd-123">-WhatIf</span></span>
<span data-ttu-id="c21bd-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c21bd-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c21bd-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c21bd-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c21bd-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c21bd-126">CommonParameters</span></span>
<span data-ttu-id="c21bd-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c21bd-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c21bd-128">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c21bd-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c21bd-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c21bd-129">INPUTS</span></span>

### <span data-ttu-id="c21bd-130">System. String</span><span class="sxs-lookup"><span data-stu-id="c21bd-130">System.String</span></span>

## <span data-ttu-id="c21bd-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c21bd-131">OUTPUTS</span></span>

### <span data-ttu-id="c21bd-132">System. void</span><span class="sxs-lookup"><span data-stu-id="c21bd-132">System.Void</span></span>

## <span data-ttu-id="c21bd-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c21bd-133">NOTES</span></span>

## <span data-ttu-id="c21bd-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c21bd-134">RELATED LINKS</span></span>

[<span data-ttu-id="c21bd-135">Get-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="c21bd-135">Get-AzAutomationModule</span></span>](./Get-AzAutomationModule.md)

[<span data-ttu-id="c21bd-136">Yeni-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="c21bd-136">New-AzAutomationModule</span></span>](./New-AzAutomationModule.md)

[<span data-ttu-id="c21bd-137">Set-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="c21bd-137">Set-AzAutomationModule</span></span>](./Set-AzAutomationModule.md)


