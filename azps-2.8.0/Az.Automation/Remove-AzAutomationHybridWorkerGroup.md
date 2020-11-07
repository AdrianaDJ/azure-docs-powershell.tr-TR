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
ms.locfileid: "93753239"
---
# <span data-ttu-id="379c2-101">Remove-AzAutomationHybridWorkerGroup</span><span class="sxs-lookup"><span data-stu-id="379c2-101">Remove-AzAutomationHybridWorkerGroup</span></span>

## <span data-ttu-id="379c2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="379c2-102">SYNOPSIS</span></span>
<span data-ttu-id="379c2-103">Karma çalışanı grubunu otomasyondan kaldırır.</span><span class="sxs-lookup"><span data-stu-id="379c2-103">Removes hybrid worker group from Automation.</span></span>

## <span data-ttu-id="379c2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="379c2-104">SYNTAX</span></span>

```
Remove-AzAutomationHybridWorkerGroup [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="379c2-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="379c2-105">DESCRIPTION</span></span>
<span data-ttu-id="379c2-106">Remove-AzAutomationHybridWorkerGroup cmdlet 'i otomasyondan bir karma çalışanı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="379c2-106">The Remove-AzAutomationHybridWorkerGroup cmdlet removes a hybrid worker group from Automation.</span></span>

## <span data-ttu-id="379c2-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="379c2-107">EXAMPLES</span></span>

### <span data-ttu-id="379c2-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="379c2-108">Example 1</span></span>
<span data-ttu-id="379c2-109">Bu komut karma çalışanı adıyla kaldırır.</span><span class="sxs-lookup"><span data-stu-id="379c2-109">This command removes a hybrid worker by name.</span></span>

```powershell
PS C:\> Remove-AzAutomationHybridWorkerGroup -ResourceGroupName "rg1" `
                                                  -AutomationAccountName "devAccount" `
                                                  -Name "GroupName" `
                                                  -Force
```

## <span data-ttu-id="379c2-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="379c2-110">PARAMETERS</span></span>

### <span data-ttu-id="379c2-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="379c2-111">-AutomationAccountName</span></span>
<span data-ttu-id="379c2-112">Otomasyon hesap adı.</span><span class="sxs-lookup"><span data-stu-id="379c2-112">The automation account name.</span></span>

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

### <span data-ttu-id="379c2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="379c2-113">-DefaultProfile</span></span>
<span data-ttu-id="379c2-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="379c2-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="379c2-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="379c2-115">-Name</span></span>
<span data-ttu-id="379c2-116">Karma çalışanı grup adı.</span><span class="sxs-lookup"><span data-stu-id="379c2-116">The hybrid worker group name.</span></span>

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

### <span data-ttu-id="379c2-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="379c2-117">-ResourceGroupName</span></span>
<span data-ttu-id="379c2-118">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="379c2-118">The resource group name.</span></span>

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

### <span data-ttu-id="379c2-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="379c2-119">-Confirm</span></span>
<span data-ttu-id="379c2-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="379c2-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="379c2-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="379c2-121">-WhatIf</span></span>
<span data-ttu-id="379c2-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="379c2-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="379c2-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="379c2-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="379c2-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="379c2-124">CommonParameters</span></span>
<span data-ttu-id="379c2-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="379c2-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="379c2-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="379c2-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="379c2-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="379c2-127">INPUTS</span></span>

### <span data-ttu-id="379c2-128">System. String</span><span class="sxs-lookup"><span data-stu-id="379c2-128">System.String</span></span>

## <span data-ttu-id="379c2-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="379c2-129">OUTPUTS</span></span>

### <span data-ttu-id="379c2-130">System. void</span><span class="sxs-lookup"><span data-stu-id="379c2-130">System.Void</span></span>

## <span data-ttu-id="379c2-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="379c2-131">NOTES</span></span>

## <span data-ttu-id="379c2-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="379c2-132">RELATED LINKS</span></span>