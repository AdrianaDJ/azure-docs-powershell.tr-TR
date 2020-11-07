---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/remove-azurermautomationdscnodeconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationHybridWorkerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationHybridWorkerGroup.md
ms.openlocfilehash: b6f15bc55c2e9f9a05e60e7e6f2c139ddbb70454
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762324"
---
# <span data-ttu-id="7786c-101">Remove-AzureRmAutomationHybridWorkerGroup</span><span class="sxs-lookup"><span data-stu-id="7786c-101">Remove-AzureRmAutomationHybridWorkerGroup</span></span>

## <span data-ttu-id="7786c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7786c-102">SYNOPSIS</span></span>
<span data-ttu-id="7786c-103">Karma çalışanı grubunu otomasyondan kaldırır.</span><span class="sxs-lookup"><span data-stu-id="7786c-103">Removes hybrid worker group from Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7786c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7786c-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationHybridWorkerGroup [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7786c-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="7786c-105">DESCRIPTION</span></span>
<span data-ttu-id="7786c-106">Remove-AzureRmAutomationHybridWorkerGroup cmdlet 'i otomasyondan bir karma çalışanı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="7786c-106">The Remove-AzureRmAutomationHybridWorkerGroup cmdlet removes a hybrid worker group from Automation.</span></span>

## <span data-ttu-id="7786c-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7786c-107">EXAMPLES</span></span>

### <span data-ttu-id="7786c-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="7786c-108">Example 1</span></span>
<span data-ttu-id="7786c-109">Bu komut karma çalışanı adıyla kaldırır.</span><span class="sxs-lookup"><span data-stu-id="7786c-109">This command removes a hybrid worker by name.</span></span>

```powershell
PS C:\> Remove-AzureRmAutomationHybridWorkerGroup -ResourceGroupName "rg1" `
                                                  -AutomationAccountName "devAccount" `
                                                  -Name "GroupName" `
                                                  -Force
```

## <span data-ttu-id="7786c-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7786c-110">PARAMETERS</span></span>

### <span data-ttu-id="7786c-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="7786c-111">-AutomationAccountName</span></span>
<span data-ttu-id="7786c-112">Otomasyon hesap adı.</span><span class="sxs-lookup"><span data-stu-id="7786c-112">The automation account name.</span></span>

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

### <span data-ttu-id="7786c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7786c-113">-DefaultProfile</span></span>
<span data-ttu-id="7786c-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7786c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7786c-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="7786c-115">-Name</span></span>
<span data-ttu-id="7786c-116">Karma çalışanı grup adı.</span><span class="sxs-lookup"><span data-stu-id="7786c-116">The hybrid worker group name.</span></span>

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

### <span data-ttu-id="7786c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7786c-117">-ResourceGroupName</span></span>
<span data-ttu-id="7786c-118">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="7786c-118">The resource group name.</span></span>

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

### <span data-ttu-id="7786c-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="7786c-119">-Confirm</span></span>
<span data-ttu-id="7786c-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="7786c-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7786c-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7786c-121">-WhatIf</span></span>
<span data-ttu-id="7786c-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7786c-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7786c-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="7786c-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7786c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7786c-124">CommonParameters</span></span>
<span data-ttu-id="7786c-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7786c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7786c-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7786c-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7786c-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7786c-127">INPUTS</span></span>

### <span data-ttu-id="7786c-128">System. String</span><span class="sxs-lookup"><span data-stu-id="7786c-128">System.String</span></span>

## <span data-ttu-id="7786c-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7786c-129">OUTPUTS</span></span>

### <span data-ttu-id="7786c-130">System. void</span><span class="sxs-lookup"><span data-stu-id="7786c-130">System.Void</span></span>

## <span data-ttu-id="7786c-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7786c-131">NOTES</span></span>

## <span data-ttu-id="7786c-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7786c-132">RELATED LINKS</span></span>
