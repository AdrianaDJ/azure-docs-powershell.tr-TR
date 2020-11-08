---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: EDB918EA-4FF3-44EF-A4CA-5BFBD14340EA
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationRunbook.md
ms.openlocfilehash: edae476893de5a64e950902d2de7b31fe53b51ea
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94110088"
---
# <span data-ttu-id="c7453-101">Get-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="c7453-101">Get-AzAutomationRunbook</span></span>

## <span data-ttu-id="c7453-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c7453-102">SYNOPSIS</span></span>
<span data-ttu-id="c7453-103">Runbook alır.</span><span class="sxs-lookup"><span data-stu-id="c7453-103">Gets a runbook.</span></span>

## <span data-ttu-id="c7453-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c7453-104">SYNTAX</span></span>

### <span data-ttu-id="c7453-105">Tümü (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="c7453-105">ByAll (Default)</span></span>
```
Get-AzAutomationRunbook [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c7453-106">ByRunbookName</span><span class="sxs-lookup"><span data-stu-id="c7453-106">ByRunbookName</span></span>
```
Get-AzAutomationRunbook [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c7453-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="c7453-107">DESCRIPTION</span></span>
<span data-ttu-id="c7453-108">**Get-AzAutomationRunbook** cmdlet 'ı Azure Otomasyonu runbook 'ları alır.</span><span class="sxs-lookup"><span data-stu-id="c7453-108">The **Get-AzAutomationRunbook** cmdlet gets Azure Automation runbooks.</span></span>
<span data-ttu-id="c7453-109">Belirli bir runbook almak için adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="c7453-109">To get a specific runbook, specify its name.</span></span>

## <span data-ttu-id="c7453-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c7453-110">EXAMPLES</span></span>

### <span data-ttu-id="c7453-111">Örnek 1: tüm runbook 'ları alma</span><span class="sxs-lookup"><span data-stu-id="c7453-111">Example 1: Get all runbooks</span></span>
```
PS C:\>Get-AzAutomationRunbook -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="c7453-112">Bu komut, Contoso17 adlı Azure Otomasyonu hesabındaki tüm runbook 'ları alır.</span><span class="sxs-lookup"><span data-stu-id="c7453-112">This command gets all runbooks in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="c7453-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c7453-113">PARAMETERS</span></span>

### <span data-ttu-id="c7453-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="c7453-114">-AutomationAccountName</span></span>
<span data-ttu-id="c7453-115">Bu cmdlet 'in runbook 'ları aldığı Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c7453-115">Specifies the name of an Automation account in which this cmdlet gets runbooks.</span></span>

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

### <span data-ttu-id="c7453-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7453-116">-DefaultProfile</span></span>
<span data-ttu-id="c7453-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="c7453-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c7453-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="c7453-118">-Name</span></span>
<span data-ttu-id="c7453-119">Bu cmdlet 'in aldığı runbook 'un adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c7453-119">Specifies the name of a runbook that this cmdlet gets.</span></span>

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

### <span data-ttu-id="c7453-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c7453-120">-ResourceGroupName</span></span>
<span data-ttu-id="c7453-121">Bu cmdlet 'in runbook 'ları aldığı kaynak grubun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c7453-121">Specifies the name of the resource group for which this cmdlet gets runbooks.</span></span>

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

### <span data-ttu-id="c7453-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7453-122">CommonParameters</span></span>
<span data-ttu-id="c7453-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c7453-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7453-124">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c7453-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7453-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c7453-125">INPUTS</span></span>

### <span data-ttu-id="c7453-126">System. String</span><span class="sxs-lookup"><span data-stu-id="c7453-126">System.String</span></span>

## <span data-ttu-id="c7453-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c7453-127">OUTPUTS</span></span>

### <span data-ttu-id="c7453-128">Microsoft. Azure. Commands. Automation. model. runbook</span><span class="sxs-lookup"><span data-stu-id="c7453-128">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="c7453-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c7453-129">NOTES</span></span>

## <span data-ttu-id="c7453-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c7453-130">RELATED LINKS</span></span>

[<span data-ttu-id="c7453-131">Dışarı aktarma-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="c7453-131">Export-AzAutomationRunbook</span></span>](./Export-AzAutomationRunbook.md)

[<span data-ttu-id="c7453-132">Import-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="c7453-132">Import-AzAutomationRunbook</span></span>](./Import-AzAutomationRunbook.md)

[<span data-ttu-id="c7453-133">Yeni-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="c7453-133">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="c7453-134">Yeni-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="c7453-134">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="c7453-135">Yayımlama-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="c7453-135">Publish-AzAutomationRunbook</span></span>](./Publish-AzAutomationRunbook.md)

[<span data-ttu-id="c7453-136">Remove-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="c7453-136">Remove-AzAutomationRunbook</span></span>](./Remove-AzAutomationRunbook.md)

[<span data-ttu-id="c7453-137">Set-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="c7453-137">Set-AzAutomationRunbook</span></span>](./Set-AzAutomationRunbook.md)

[<span data-ttu-id="c7453-138">Start-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="c7453-138">Start-AzAutomationRunbook</span></span>](./Start-AzAutomationRunbook.md)


