---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: EAD39EE1-C66F-4092-8876-E7F9FA612481
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationSchedule.md
ms.openlocfilehash: d56b631f106ef4984a81a8911af26288f720cac7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753234"
---
# <span data-ttu-id="784f4-101">Remove-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="784f4-101">Remove-AzAutomationSchedule</span></span>

## <span data-ttu-id="784f4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="784f4-102">SYNOPSIS</span></span>
<span data-ttu-id="784f4-103">Otomasyon zamanlamasını siler.</span><span class="sxs-lookup"><span data-stu-id="784f4-103">Deletes an Automation schedule.</span></span>

## <span data-ttu-id="784f4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="784f4-104">SYNTAX</span></span>

```
Remove-AzAutomationSchedule [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="784f4-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="784f4-105">DESCRIPTION</span></span>
<span data-ttu-id="784f4-106">**Remove-Azautomationzamanlama** cmdlet 'ı Azure Otomasyonu 'ndan bir zamanlama siler.</span><span class="sxs-lookup"><span data-stu-id="784f4-106">The **Remove-AzAutomationSchedule** cmdlet deletes a schedule from Azure Automation.</span></span>

## <span data-ttu-id="784f4-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="784f4-107">EXAMPLES</span></span>

### <span data-ttu-id="784f4-108">Örnek 1: zamanlamayı kaldırma</span><span class="sxs-lookup"><span data-stu-id="784f4-108">Example 1: Remove a schedule</span></span>
```
PS C:\>Remove-AzAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="784f4-109">Bu komut, Schedule01 adlı zamanlamayı kaynak grubu ResourceGroup01 Otomasyon hesabında Contoso17.</span><span class="sxs-lookup"><span data-stu-id="784f4-109">This command deletes the schedule named Schedule01 in automation account Contoso17 in resource group ResourceGroup01.</span></span>

## <span data-ttu-id="784f4-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="784f4-110">PARAMETERS</span></span>

### <span data-ttu-id="784f4-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="784f4-111">-AutomationAccountName</span></span>
<span data-ttu-id="784f4-112">Bu cmdlet 'in zamanlamayı kaldırdıkları Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="784f4-112">Specifies the name of an Automation account for which this cmdlet removes a schedule.</span></span>

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

### <span data-ttu-id="784f4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="784f4-113">-DefaultProfile</span></span>
<span data-ttu-id="784f4-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="784f4-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="784f4-115">-Force</span><span class="sxs-lookup"><span data-stu-id="784f4-115">-Force</span></span>
<span data-ttu-id="784f4-116">ps_force</span><span class="sxs-lookup"><span data-stu-id="784f4-116">ps_force</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="784f4-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="784f4-117">-Name</span></span>
<span data-ttu-id="784f4-118">Bu cmdlet 'in kaldırdığı zamanlamanın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="784f4-118">Specifies the name for the schedule that this cmdlet removes.</span></span>

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

### <span data-ttu-id="784f4-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="784f4-119">-ResourceGroupName</span></span>
<span data-ttu-id="784f4-120">Bu cmdlet 'in zamanlamayı kaldırdığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="784f4-120">Specifies the name of a resource group for which this cmdlet removes a schedule.</span></span>

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

### <span data-ttu-id="784f4-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="784f4-121">-Confirm</span></span>
<span data-ttu-id="784f4-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="784f4-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="784f4-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="784f4-123">-WhatIf</span></span>
<span data-ttu-id="784f4-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="784f4-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="784f4-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="784f4-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="784f4-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="784f4-126">CommonParameters</span></span>
<span data-ttu-id="784f4-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="784f4-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="784f4-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="784f4-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="784f4-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="784f4-129">INPUTS</span></span>

### <span data-ttu-id="784f4-130">System. String</span><span class="sxs-lookup"><span data-stu-id="784f4-130">System.String</span></span>

## <span data-ttu-id="784f4-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="784f4-131">OUTPUTS</span></span>

### <span data-ttu-id="784f4-132">System. void</span><span class="sxs-lookup"><span data-stu-id="784f4-132">System.Void</span></span>

## <span data-ttu-id="784f4-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="784f4-133">NOTES</span></span>

## <span data-ttu-id="784f4-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="784f4-134">RELATED LINKS</span></span>

[<span data-ttu-id="784f4-135">Get-Azautomationzamanlama</span><span class="sxs-lookup"><span data-stu-id="784f4-135">Get-AzAutomationSchedule</span></span>](./Get-AzAutomationSchedule.md)

[<span data-ttu-id="784f4-136">Yeni-Azautomationzamanlama</span><span class="sxs-lookup"><span data-stu-id="784f4-136">New-AzAutomationSchedule</span></span>](./New-AzAutomationSchedule.md)

[<span data-ttu-id="784f4-137">Set-Azautomationzamanlama</span><span class="sxs-lookup"><span data-stu-id="784f4-137">Set-AzAutomationSchedule</span></span>](./Set-AzAutomationSchedule.md)

