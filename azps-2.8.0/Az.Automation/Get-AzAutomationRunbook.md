---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: EDB918EA-4FF3-44EF-A4CA-5BFBD14340EA
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationRunbook.md
ms.openlocfilehash: 1b07ff07008c0af80a72c32ed64d6845d632db15
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753316"
---
# <span data-ttu-id="f8ab7-101">Get-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="f8ab7-101">Get-AzAutomationRunbook</span></span>

## <span data-ttu-id="f8ab7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f8ab7-102">SYNOPSIS</span></span>
<span data-ttu-id="f8ab7-103">Runbook alır.</span><span class="sxs-lookup"><span data-stu-id="f8ab7-103">Gets a runbook.</span></span>

## <span data-ttu-id="f8ab7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f8ab7-104">SYNTAX</span></span>

### <span data-ttu-id="f8ab7-105">Tümü (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="f8ab7-105">ByAll (Default)</span></span>
```
Get-AzAutomationRunbook [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f8ab7-106">ByRunbookName</span><span class="sxs-lookup"><span data-stu-id="f8ab7-106">ByRunbookName</span></span>
```
Get-AzAutomationRunbook [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f8ab7-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="f8ab7-107">DESCRIPTION</span></span>
<span data-ttu-id="f8ab7-108">**Get-AzAutomationRunbook** cmdlet 'ı Azure Otomasyonu runbook 'ları alır.</span><span class="sxs-lookup"><span data-stu-id="f8ab7-108">The **Get-AzAutomationRunbook** cmdlet gets Azure Automation runbooks.</span></span>
<span data-ttu-id="f8ab7-109">Belirli bir runbook almak için adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="f8ab7-109">To get a specific runbook, specify its name.</span></span>

## <span data-ttu-id="f8ab7-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f8ab7-110">EXAMPLES</span></span>

### <span data-ttu-id="f8ab7-111">Örnek 1: tüm runbook 'ları alma</span><span class="sxs-lookup"><span data-stu-id="f8ab7-111">Example 1: Get all runbooks</span></span>
```
PS C:\>Get-AzAutomationRunbook -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="f8ab7-112">Bu komut, Contoso17 adlı Azure Otomasyonu hesabındaki tüm runbook 'ları alır.</span><span class="sxs-lookup"><span data-stu-id="f8ab7-112">This command gets all runbooks in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="f8ab7-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f8ab7-113">PARAMETERS</span></span>

### <span data-ttu-id="f8ab7-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="f8ab7-114">-AutomationAccountName</span></span>
<span data-ttu-id="f8ab7-115">Bu cmdlet 'in runbook 'ları aldığı Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f8ab7-115">Specifies the name of an Automation account in which this cmdlet gets runbooks.</span></span>

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

### <span data-ttu-id="f8ab7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8ab7-116">-DefaultProfile</span></span>
<span data-ttu-id="f8ab7-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="f8ab7-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f8ab7-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="f8ab7-118">-Name</span></span>
<span data-ttu-id="f8ab7-119">Bu cmdlet 'in aldığı runbook 'un adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f8ab7-119">Specifies the name of a runbook that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRunbookName
Aliases: RunbookName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8ab7-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8ab7-120">-ResourceGroupName</span></span>
<span data-ttu-id="f8ab7-121">Bu cmdlet 'in runbook 'ları aldığı kaynak grubun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f8ab7-121">Specifies the name of the resource group for which this cmdlet gets runbooks.</span></span>

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

### <span data-ttu-id="f8ab7-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8ab7-122">CommonParameters</span></span>
<span data-ttu-id="f8ab7-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f8ab7-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8ab7-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f8ab7-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8ab7-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f8ab7-125">INPUTS</span></span>

### <span data-ttu-id="f8ab7-126">System. String</span><span class="sxs-lookup"><span data-stu-id="f8ab7-126">System.String</span></span>

## <span data-ttu-id="f8ab7-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f8ab7-127">OUTPUTS</span></span>

### <span data-ttu-id="f8ab7-128">Microsoft. Azure. Commands. Automation. model. runbook</span><span class="sxs-lookup"><span data-stu-id="f8ab7-128">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="f8ab7-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f8ab7-129">NOTES</span></span>

## <span data-ttu-id="f8ab7-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f8ab7-130">RELATED LINKS</span></span>

[<span data-ttu-id="f8ab7-131">Dışarı aktarma-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="f8ab7-131">Export-AzAutomationRunbook</span></span>](./Export-AzAutomationRunbook.md)

[<span data-ttu-id="f8ab7-132">Import-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="f8ab7-132">Import-AzAutomationRunbook</span></span>](./Import-AzAutomationRunbook.md)

[<span data-ttu-id="f8ab7-133">Yeni-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="f8ab7-133">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="f8ab7-134">Yeni-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="f8ab7-134">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="f8ab7-135">Yayımlama-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="f8ab7-135">Publish-AzAutomationRunbook</span></span>](./Publish-AzAutomationRunbook.md)

[<span data-ttu-id="f8ab7-136">Remove-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="f8ab7-136">Remove-AzAutomationRunbook</span></span>](./Remove-AzAutomationRunbook.md)

[<span data-ttu-id="f8ab7-137">Set-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="f8ab7-137">Set-AzAutomationRunbook</span></span>](./Set-AzAutomationRunbook.md)

[<span data-ttu-id="f8ab7-138">Start-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="f8ab7-138">Start-AzAutomationRunbook</span></span>](./Start-AzAutomationRunbook.md)


