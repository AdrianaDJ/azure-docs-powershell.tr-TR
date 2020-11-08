---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationhybridworkergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationHybridWorkerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationHybridWorkerGroup.md
ms.openlocfilehash: 78674e3245da1b8a58e099948bff23df9159efec
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94268115"
---
# <span data-ttu-id="df1f5-101">Remove-AzAutomationHybridWorkerGroup</span><span class="sxs-lookup"><span data-stu-id="df1f5-101">Remove-AzAutomationHybridWorkerGroup</span></span>

## <span data-ttu-id="df1f5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="df1f5-102">SYNOPSIS</span></span>
<span data-ttu-id="df1f5-103">Karma çalışanı grubunu otomasyondan kaldırır.</span><span class="sxs-lookup"><span data-stu-id="df1f5-103">Removes hybrid worker group from Automation.</span></span>

## <span data-ttu-id="df1f5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="df1f5-104">SYNTAX</span></span>

```
Remove-AzAutomationHybridWorkerGroup [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="df1f5-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="df1f5-105">DESCRIPTION</span></span>
<span data-ttu-id="df1f5-106">Remove-AzAutomationHybridWorkerGroup cmdlet 'i otomasyondan bir karma çalışanı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="df1f5-106">The Remove-AzAutomationHybridWorkerGroup cmdlet removes a hybrid worker group from Automation.</span></span>

## <span data-ttu-id="df1f5-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="df1f5-107">EXAMPLES</span></span>

### <span data-ttu-id="df1f5-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="df1f5-108">Example 1</span></span>
<span data-ttu-id="df1f5-109">Bu komut karma çalışanı adıyla kaldırır.</span><span class="sxs-lookup"><span data-stu-id="df1f5-109">This command removes a hybrid worker by name.</span></span>

```powershell
PS C:\> Remove-AzAutomationHybridWorkerGroup -ResourceGroupName "rg1" `
                                                  -AutomationAccountName "devAccount" `
                                                  -Name "GroupName" `
                                                  -Force
```

## <span data-ttu-id="df1f5-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="df1f5-110">PARAMETERS</span></span>

### <span data-ttu-id="df1f5-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="df1f5-111">-AutomationAccountName</span></span>
<span data-ttu-id="df1f5-112">Otomasyon hesap adı.</span><span class="sxs-lookup"><span data-stu-id="df1f5-112">The automation account name.</span></span>

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

### <span data-ttu-id="df1f5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df1f5-113">-DefaultProfile</span></span>
<span data-ttu-id="df1f5-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="df1f5-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="df1f5-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="df1f5-115">-Name</span></span>
<span data-ttu-id="df1f5-116">Karma çalışanı grup adı.</span><span class="sxs-lookup"><span data-stu-id="df1f5-116">The hybrid worker group name.</span></span>

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

### <span data-ttu-id="df1f5-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df1f5-117">-ResourceGroupName</span></span>
<span data-ttu-id="df1f5-118">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="df1f5-118">The resource group name.</span></span>

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

### <span data-ttu-id="df1f5-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="df1f5-119">-Confirm</span></span>
<span data-ttu-id="df1f5-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="df1f5-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="df1f5-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="df1f5-121">-WhatIf</span></span>
<span data-ttu-id="df1f5-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="df1f5-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="df1f5-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="df1f5-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="df1f5-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df1f5-124">CommonParameters</span></span>
<span data-ttu-id="df1f5-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="df1f5-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df1f5-126">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="df1f5-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df1f5-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="df1f5-127">INPUTS</span></span>

### <span data-ttu-id="df1f5-128">System. String</span><span class="sxs-lookup"><span data-stu-id="df1f5-128">System.String</span></span>

## <span data-ttu-id="df1f5-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="df1f5-129">OUTPUTS</span></span>

### <span data-ttu-id="df1f5-130">System. void</span><span class="sxs-lookup"><span data-stu-id="df1f5-130">System.Void</span></span>

## <span data-ttu-id="df1f5-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="df1f5-131">NOTES</span></span>

## <span data-ttu-id="df1f5-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="df1f5-132">RELATED LINKS</span></span>
