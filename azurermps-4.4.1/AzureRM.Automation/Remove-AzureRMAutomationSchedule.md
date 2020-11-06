---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: EAD39EE1-C66F-4092-8876-E7F9FA612481
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationSchedule.md
ms.openlocfilehash: 562b5b5986d544f5fa8d91e0f39cb34ef9dababd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591816"
---
# <span data-ttu-id="f3b1e-101">Remove-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="f3b1e-101">Remove-AzureRmAutomationSchedule</span></span>

## <span data-ttu-id="f3b1e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f3b1e-102">SYNOPSIS</span></span>
<span data-ttu-id="f3b1e-103">Otomasyon zamanlamasını siler.</span><span class="sxs-lookup"><span data-stu-id="f3b1e-103">Deletes an Automation schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f3b1e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f3b1e-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationSchedule [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f3b1e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f3b1e-105">DESCRIPTION</span></span>
<span data-ttu-id="f3b1e-106">**Remove-Azurermautomationzamanlama** cmdlet 'ı Azure Otomasyonu 'ndan bir zamanlama siler.</span><span class="sxs-lookup"><span data-stu-id="f3b1e-106">The **Remove-AzureRmAutomationSchedule** cmdlet deletes a schedule from Azure Automation.</span></span>

## <span data-ttu-id="f3b1e-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f3b1e-107">EXAMPLES</span></span>

### <span data-ttu-id="f3b1e-108">Örnek 1: zamanlamayı kaldırma</span><span class="sxs-lookup"><span data-stu-id="f3b1e-108">Example 1: Remove a schedule</span></span>
```
PS C:\>Remove-AzureRmAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="f3b1e-109">Bu komut, Schedule01 adlı zamanlamanın açıklamasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="f3b1e-109">This command modifies the description of the schedule named Schedule01.</span></span>

## <span data-ttu-id="f3b1e-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f3b1e-110">PARAMETERS</span></span>

### <span data-ttu-id="f3b1e-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="f3b1e-111">-AutomationAccountName</span></span>
<span data-ttu-id="f3b1e-112">Bu cmdlet 'in zamanlamayı değiştirdiği Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f3b1e-112">Specifies the name of an Automation account for which this cmdlet modifies a schedule.</span></span>

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

### <span data-ttu-id="f3b1e-113">-Force</span><span class="sxs-lookup"><span data-stu-id="f3b1e-113">-Force</span></span>
<span data-ttu-id="f3b1e-114">ps_force</span><span class="sxs-lookup"><span data-stu-id="f3b1e-114">ps_force</span></span>

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

### <span data-ttu-id="f3b1e-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="f3b1e-115">-Name</span></span>
<span data-ttu-id="f3b1e-116">Bu cmdlet 'in kaldırdığı zamanlamanın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f3b1e-116">Specifies the name for the schedule that this cmdlet removes.</span></span>

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

### <span data-ttu-id="f3b1e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3b1e-117">-ResourceGroupName</span></span>
<span data-ttu-id="f3b1e-118">Bu cmdlet 'in zamanlamayı kaldırdığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f3b1e-118">Specifies the name of a resource group for which this cmdlet removes a schedule.</span></span>

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

### <span data-ttu-id="f3b1e-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="f3b1e-119">-Confirm</span></span>
<span data-ttu-id="f3b1e-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f3b1e-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f3b1e-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f3b1e-121">-WhatIf</span></span>
<span data-ttu-id="f3b1e-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f3b1e-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f3b1e-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f3b1e-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f3b1e-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3b1e-124">-DefaultProfile</span></span>
<span data-ttu-id="f3b1e-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f3b1e-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f3b1e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3b1e-126">CommonParameters</span></span>
<span data-ttu-id="f3b1e-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f3b1e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3b1e-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3b1e-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3b1e-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f3b1e-129">INPUTS</span></span>

## <span data-ttu-id="f3b1e-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f3b1e-130">OUTPUTS</span></span>

## <span data-ttu-id="f3b1e-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f3b1e-131">NOTES</span></span>

## <span data-ttu-id="f3b1e-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f3b1e-132">RELATED LINKS</span></span>

[<span data-ttu-id="f3b1e-133">Get-Azurermautomationzamanlama</span><span class="sxs-lookup"><span data-stu-id="f3b1e-133">Get-AzureRmAutomationSchedule</span></span>](./Get-AzureRMAutomationSchedule.md)

[<span data-ttu-id="f3b1e-134">Yeni-Azurermautomationzamanlama</span><span class="sxs-lookup"><span data-stu-id="f3b1e-134">New-AzureRmAutomationSchedule</span></span>](./New-AzureRMAutomationSchedule.md)

[<span data-ttu-id="f3b1e-135">Set-Azurermautomationzamanlama</span><span class="sxs-lookup"><span data-stu-id="f3b1e-135">Set-AzureRmAutomationSchedule</span></span>](./Set-AzureRMAutomationSchedule.md)


