---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationhybridworkergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationHybridWorkerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationHybridWorkerGroup.md
ms.openlocfilehash: b9f23105b6fa84781ef1b0f0ba4be0e52e06ee08
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93761530"
---
# <span data-ttu-id="f5bb4-101">Remove-AzAutomationHybridWorkerGroup</span><span class="sxs-lookup"><span data-stu-id="f5bb4-101">Remove-AzAutomationHybridWorkerGroup</span></span>

## <span data-ttu-id="f5bb4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f5bb4-102">SYNOPSIS</span></span>
<span data-ttu-id="f5bb4-103">Karma çalışanı grubunu otomasyondan kaldırır.</span><span class="sxs-lookup"><span data-stu-id="f5bb4-103">Removes hybrid worker group from Automation.</span></span>

## <span data-ttu-id="f5bb4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f5bb4-104">SYNTAX</span></span>

```
Remove-AzAutomationHybridWorkerGroup [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f5bb4-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f5bb4-105">DESCRIPTION</span></span>
<span data-ttu-id="f5bb4-106">Remove-AzAutomationHybridWorkerGroup cmdlet 'i otomasyondan bir karma çalışanı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="f5bb4-106">The Remove-AzAutomationHybridWorkerGroup cmdlet removes a hybrid worker group from Automation.</span></span>

## <span data-ttu-id="f5bb4-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f5bb4-107">EXAMPLES</span></span>

### <span data-ttu-id="f5bb4-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="f5bb4-108">Example 1</span></span>
<span data-ttu-id="f5bb4-109">Bu komut karma çalışanı adıyla kaldırır.</span><span class="sxs-lookup"><span data-stu-id="f5bb4-109">This command removes a hybrid worker by name.</span></span>

```powershell
PS C:\> Remove-AzAutomationHybridWorkerGroup -ResourceGroupName "rg1" `
                                                  -AutomationAccountName "devAccount" `
                                                  -Name "GroupName" `
                                                  -Force
```

## <span data-ttu-id="f5bb4-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f5bb4-110">PARAMETERS</span></span>

### <span data-ttu-id="f5bb4-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="f5bb4-111">-AutomationAccountName</span></span>
<span data-ttu-id="f5bb4-112">Otomasyon hesap adı.</span><span class="sxs-lookup"><span data-stu-id="f5bb4-112">The automation account name.</span></span>

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

### <span data-ttu-id="f5bb4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5bb4-113">-DefaultProfile</span></span>
<span data-ttu-id="f5bb4-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f5bb4-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f5bb4-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="f5bb4-115">-Name</span></span>
<span data-ttu-id="f5bb4-116">Karma çalışanı grup adı.</span><span class="sxs-lookup"><span data-stu-id="f5bb4-116">The hybrid worker group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Group

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5bb4-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5bb4-117">-ResourceGroupName</span></span>
<span data-ttu-id="f5bb4-118">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="f5bb4-118">The resource group name.</span></span>

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

### <span data-ttu-id="f5bb4-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="f5bb4-119">-Confirm</span></span>
<span data-ttu-id="f5bb4-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f5bb4-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f5bb4-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f5bb4-121">-WhatIf</span></span>
<span data-ttu-id="f5bb4-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f5bb4-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f5bb4-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f5bb4-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f5bb4-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5bb4-124">CommonParameters</span></span>
<span data-ttu-id="f5bb4-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f5bb4-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5bb4-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f5bb4-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5bb4-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f5bb4-127">INPUTS</span></span>

### <span data-ttu-id="f5bb4-128">System. String</span><span class="sxs-lookup"><span data-stu-id="f5bb4-128">System.String</span></span>

## <span data-ttu-id="f5bb4-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f5bb4-129">OUTPUTS</span></span>

### <span data-ttu-id="f5bb4-130">System. void</span><span class="sxs-lookup"><span data-stu-id="f5bb4-130">System.Void</span></span>

## <span data-ttu-id="f5bb4-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f5bb4-131">NOTES</span></span>

## <span data-ttu-id="f5bb4-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f5bb4-132">RELATED LINKS</span></span>
