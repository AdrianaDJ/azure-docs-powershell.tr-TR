---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: EAD39EE1-C66F-4092-8876-E7F9FA612481
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/remove-azurermautomationschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationSchedule.md
ms.openlocfilehash: cce9b4eff96be34521af58ec85f7abb93d39b3cd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592348"
---
# <span data-ttu-id="775e2-101">Remove-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="775e2-101">Remove-AzureRmAutomationSchedule</span></span>

## <span data-ttu-id="775e2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="775e2-102">SYNOPSIS</span></span>
<span data-ttu-id="775e2-103">Otomasyon zamanlamasını siler.</span><span class="sxs-lookup"><span data-stu-id="775e2-103">Deletes an Automation schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="775e2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="775e2-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationSchedule [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="775e2-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="775e2-105">DESCRIPTION</span></span>
<span data-ttu-id="775e2-106">**Remove-Azurermautomationzamanlama** cmdlet 'ı Azure Otomasyonu 'ndan bir zamanlama siler.</span><span class="sxs-lookup"><span data-stu-id="775e2-106">The **Remove-AzureRmAutomationSchedule** cmdlet deletes a schedule from Azure Automation.</span></span>

## <span data-ttu-id="775e2-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="775e2-107">EXAMPLES</span></span>

### <span data-ttu-id="775e2-108">Örnek 1: zamanlamayı kaldırma</span><span class="sxs-lookup"><span data-stu-id="775e2-108">Example 1: Remove a schedule</span></span>
```
PS C:\>Remove-AzureRmAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="775e2-109">Bu komut, Schedule01 adlı zamanlamayı kaynak grubu ResourceGroup01 Otomasyon hesabında Contoso17.</span><span class="sxs-lookup"><span data-stu-id="775e2-109">This command deletes the schedule named Schedule01 in automation account Contoso17 in resource group ResourceGroup01.</span></span>

## <span data-ttu-id="775e2-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="775e2-110">PARAMETERS</span></span>

### <span data-ttu-id="775e2-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="775e2-111">-AutomationAccountName</span></span>
<span data-ttu-id="775e2-112">Bu cmdlet 'in zamanlamayı kaldırdıkları Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="775e2-112">Specifies the name of an Automation account for which this cmdlet removes a schedule.</span></span>

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

### <span data-ttu-id="775e2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="775e2-113">-DefaultProfile</span></span>
<span data-ttu-id="775e2-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="775e2-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="775e2-115">-Force</span><span class="sxs-lookup"><span data-stu-id="775e2-115">-Force</span></span>
<span data-ttu-id="775e2-116">ps_force</span><span class="sxs-lookup"><span data-stu-id="775e2-116">ps_force</span></span>

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

### <span data-ttu-id="775e2-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="775e2-117">-Name</span></span>
<span data-ttu-id="775e2-118">Bu cmdlet 'in kaldırdığı zamanlamanın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="775e2-118">Specifies the name for the schedule that this cmdlet removes.</span></span>

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

### <span data-ttu-id="775e2-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="775e2-119">-ResourceGroupName</span></span>
<span data-ttu-id="775e2-120">Bu cmdlet 'in zamanlamayı kaldırdığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="775e2-120">Specifies the name of a resource group for which this cmdlet removes a schedule.</span></span>

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

### <span data-ttu-id="775e2-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="775e2-121">-Confirm</span></span>
<span data-ttu-id="775e2-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="775e2-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="775e2-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="775e2-123">-WhatIf</span></span>
<span data-ttu-id="775e2-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="775e2-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="775e2-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="775e2-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="775e2-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="775e2-126">CommonParameters</span></span>
<span data-ttu-id="775e2-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="775e2-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="775e2-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="775e2-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="775e2-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="775e2-129">INPUTS</span></span>

### <span data-ttu-id="775e2-130">System. String</span><span class="sxs-lookup"><span data-stu-id="775e2-130">System.String</span></span>

## <span data-ttu-id="775e2-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="775e2-131">OUTPUTS</span></span>

### <span data-ttu-id="775e2-132">System. void</span><span class="sxs-lookup"><span data-stu-id="775e2-132">System.Void</span></span>

## <span data-ttu-id="775e2-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="775e2-133">NOTES</span></span>

## <span data-ttu-id="775e2-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="775e2-134">RELATED LINKS</span></span>

[<span data-ttu-id="775e2-135">Get-Azurermautomationzamanlama</span><span class="sxs-lookup"><span data-stu-id="775e2-135">Get-AzureRmAutomationSchedule</span></span>](./Get-AzureRMAutomationSchedule.md)

[<span data-ttu-id="775e2-136">Yeni-Azurermautomationzamanlama</span><span class="sxs-lookup"><span data-stu-id="775e2-136">New-AzureRmAutomationSchedule</span></span>](./New-AzureRMAutomationSchedule.md)

[<span data-ttu-id="775e2-137">Set-Azurermautomationzamanlama</span><span class="sxs-lookup"><span data-stu-id="775e2-137">Set-AzureRmAutomationSchedule</span></span>](./Set-AzureRMAutomationSchedule.md)


