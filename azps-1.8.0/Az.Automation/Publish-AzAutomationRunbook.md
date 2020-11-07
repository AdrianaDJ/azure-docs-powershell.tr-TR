---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: E7F31B71-983A-4DB3-BB30-BDC5C0247E74
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/publish-azautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Publish-AzAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Publish-AzAutomationRunbook.md
ms.openlocfilehash: 1d3ea7321efaae0f9d1107e3d1e87fd3c432656f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93761550"
---
# <span data-ttu-id="e7aae-101">Publish-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="e7aae-101">Publish-AzAutomationRunbook</span></span>

## <span data-ttu-id="e7aae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e7aae-102">SYNOPSIS</span></span>
<span data-ttu-id="e7aae-103">Runbook yayımlar.</span><span class="sxs-lookup"><span data-stu-id="e7aae-103">Publishes a runbook.</span></span>

## <span data-ttu-id="e7aae-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e7aae-104">SYNTAX</span></span>

```
Publish-AzAutomationRunbook [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e7aae-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e7aae-105">DESCRIPTION</span></span>
<span data-ttu-id="e7aae-106">**Publish-AzAutomationRunbook** cmdlet 'ı, Azure Otomasyonu 'nun üretim ortamında kullanılmak üzere bir runbook yayımlar.</span><span class="sxs-lookup"><span data-stu-id="e7aae-106">The **Publish-AzAutomationRunbook** cmdlet publishes a runbook for use in the production environment of Azure Automation.</span></span>

## <span data-ttu-id="e7aae-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e7aae-107">EXAMPLES</span></span>

### <span data-ttu-id="e7aae-108">Örnek 1: runbook yayımlama</span><span class="sxs-lookup"><span data-stu-id="e7aae-108">Example 1: Publish a runbook</span></span>
```
PS C:\>Publish-AzAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="e7aae-109">Bu komut, Contoso17 adlı Azure Otomasyonu hesabında Runbk01 adındaki runbook 'u yayımlar.</span><span class="sxs-lookup"><span data-stu-id="e7aae-109">This command publishes the runbook named Runbk01 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="e7aae-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e7aae-110">PARAMETERS</span></span>

### <span data-ttu-id="e7aae-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="e7aae-111">-AutomationAccountName</span></span>
<span data-ttu-id="e7aae-112">Bu cmdlet 'in runbook yayımladığı Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e7aae-112">Specifies the name of the Automation account in which this cmdlet publishes a runbook.</span></span>

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

### <span data-ttu-id="e7aae-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7aae-113">-DefaultProfile</span></span>
<span data-ttu-id="e7aae-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="e7aae-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e7aae-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="e7aae-115">-Name</span></span>
<span data-ttu-id="e7aae-116">Bu cmdlet 'in yayımladığı runbook adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e7aae-116">Specifies the name of the runbook that this cmdlet publishes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: RunbookName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7aae-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e7aae-117">-ResourceGroupName</span></span>
<span data-ttu-id="e7aae-118">Bu cmdlet 'in runbook yayımladığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e7aae-118">Specifies the name of the resource group for which this cmdlet publishes a runbook.</span></span>

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

### <span data-ttu-id="e7aae-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7aae-119">CommonParameters</span></span>
<span data-ttu-id="e7aae-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e7aae-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7aae-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e7aae-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7aae-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e7aae-122">INPUTS</span></span>

### <span data-ttu-id="e7aae-123">System. String</span><span class="sxs-lookup"><span data-stu-id="e7aae-123">System.String</span></span>

## <span data-ttu-id="e7aae-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e7aae-124">OUTPUTS</span></span>

### <span data-ttu-id="e7aae-125">Microsoft. Azure. Commands. Automation. model. runbook</span><span class="sxs-lookup"><span data-stu-id="e7aae-125">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="e7aae-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e7aae-126">NOTES</span></span>

## <span data-ttu-id="e7aae-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e7aae-127">RELATED LINKS</span></span>

[<span data-ttu-id="e7aae-128">Dışarı aktarma-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="e7aae-128">Export-AzAutomationRunbook</span></span>](./Export-AzAutomationRunbook.md)

[<span data-ttu-id="e7aae-129">Get-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="e7aae-129">Get-AzAutomationRunbook</span></span>](./Get-AzAutomationRunbook.md)

[<span data-ttu-id="e7aae-130">Import-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="e7aae-130">Import-AzAutomationRunbook</span></span>](./Import-AzAutomationRunbook.md)

[<span data-ttu-id="e7aae-131">Yeni-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="e7aae-131">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="e7aae-132">Yeni-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="e7aae-132">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="e7aae-133">Remove-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="e7aae-133">Remove-AzAutomationRunbook</span></span>](./Remove-AzAutomationRunbook.md)

[<span data-ttu-id="e7aae-134">Set-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="e7aae-134">Set-AzAutomationRunbook</span></span>](./Set-AzAutomationRunbook.md)

[<span data-ttu-id="e7aae-135">Start-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="e7aae-135">Start-AzAutomationRunbook</span></span>](./Start-AzAutomationRunbook.md)


